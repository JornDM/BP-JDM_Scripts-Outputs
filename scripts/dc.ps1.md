# dc.ps1
```powershell
# --------------------------------- #
#               dc.ps1              #
# --------------------------------- # 

# Functions
function log([string] $msg) {
    write-host $msg -ForegroundColor Yellow
}

# Dit script zal de dc VM gaan configureren. 
Set-ExecutionPolicy Unrestricted -confirm:$false -Force CurrentUser  

clear  

# ========================
#     IP-configuratie
# ========================
[ipaddress] $ipv4 = "192.168.50.2"
[string] $prefix = "24"
[ipaddress] $gateway = "192.168.50.1"
[string] $dns = "192.168.50.2" # Dc zal DNS service voorzien 

# Ophalen van de WAN-adapter
log 'Ophalen WAN-adapter'  
$WAN_adapter = (Get-NetIPAddress) | Where-Object {$_.IPAddress -match '10.0.2.15'}
[string] $interface_WAN = $WAN_adapter.InterfaceAlias 

# IP-adressen configureren op de adapters
log 'Configureren van de netwerk-adapters...'  
Get-NetAdapter -Name "$interface_WAN" | Rename-NetAdapter -NewName "WAN"

# Zoeken naar juiste naam van de intnet adapater en deze naam veranderen naar 'LAN'
try {
    if (Get-NetAdapter -Name 'Ethernet' -ErrorAction Ignore) {
        log 'De naam van de intnet-adapter was "Ethernet", nu aanpassen naar LAN...' 
        Get-NetAdapter -Name 'Ethernet' | Rename-NetAdapter -NewName 'LAN'
    }
} catch {
    log 'De adapater met de naam "Ethernet" bestaat niet.'
}

try {
    if (Get-NetAdapter -Name 'Ethernet 2' -ErrorAction Stop) {
        log 'De naam van de intnet-adapter was "Ethernet 2", nu aanpassen naar LAN...'
        Get-NetAdapter -Name 'Ethernet 2' | Rename-NetAdapter -NewName 'LAN'
    }
} catch {
    log 'De adapter met de naam "Ethernet 2" bestaat niet.'
}

$IP_Assigned_Flag = Get-NetIPAddress -IPAddress '192.168.50.2' -ErrorAction Ignore
$bp_intnet = (Get-NetAdapter -Name 'LAN').ifIndex 

if ($IP_Assigned_Flag -eq $null) {
    log "Het IP-adres is nog niet toegekend aan de adapter. Dit zal nu gebeuren..."
    New-NetIPAddress -AddressFamily IPv4 -IPAddress $ipv4 -PrefixLength $prefix -InterfaceIndex $bp_intnet -DefaultGateway $gateway
}
else {
    log "Het IP-adres werd reeds toegekend aan de adapter. Doorgaan naar de volgende stap..."
}

# Configureren van DNS adres
log 'Configureren van het DNS adres'
Set-DnsClientServerAddress -InterfaceIndex $bp_intnet -ServerAddresses $dns 

# ------------------------
#     ACTIVE DIRECTORY
# ------------------------

# Installatie Active Directory service en promotie tot DC 
[string] $domain = "bp-2223-jorn.hogent"
[string] $domain_netbios = "bp-2223-jorn"

log "Installeren van de Active Directory Service..."
Add-WindowsFeature AD-Domain-Services -includeManagementTools
Import-Module ADDSDeployment

log "Dit toestel promoveren tot domeincontroller (dc)..."
Install-ADDSForest -DomainName "$domain" -DomainNetbiosName $domain_netbios -installDNS:$true -SafeModeAdministratorPassword (ConvertTo-SecureString -String "Test123!" -AsPlainText -Force) -Force 

write-host 'Promotie is gelukt! Nu toestel heropstarten...' -ForegroundColor Green 

# Instellen dat de admin user de default user is om automatisch inloggen in te schakelen
Set-ItemProperty $RegPath "AutoAdminLogon" -Value "1" -type String 
Set-ItemProperty $RegPath "DefaultUsername" -Value "Administrator" -type String 
Set-ItemProperty $RegPath "DefaultPassword" -Value "admin123" -type String

# --------> Start configuratie AD <-----------
# Hier is er mogelijks een restart nodig!
Import-Module ADDSDeployment

log "Toestellen toevoegen om automatische join tot domein mogelijk te maken..."
New-ADComputer -Name "client" -AccountPassword (ConvertTo-SecureString -String 'admin123' -AsPlainText -Force)

log "Aanmaken custom OU genaamd 'bachelorproef'"
$ou_flag = Get-ADOrganizationalUnit -Filter {Name -eq 'bachelorproef'} -ErrorAction Ignore 

if ($ou_flag -eq $null) {
    log "De OU bestaat nog niet. Deze nu maken..."
    New-ADOrganizationalUnit -Name 'bachelorproef' -Path 'DC=bp-2223-jorn,DC=hogent' -ProtectedFromAccidentalDeletion:$false
}
else {
    log "De OU bestaat al, verder gaan..."
}

log "Aanmaken custom admin genaamd 'bpAdmin'"
$user_flag = get-aduser -Filter {Name -eq 'bpAdmin'} -ErrorAction Ignore 
[string] $name = 'bpAdmin'
$pass_admin = ConvertTo-SecureString "Qwerty1" -AsPlainText -Force 
[string] $domain = 'bp-2223-jorn'

if ($user_flag -eq $null) {
    log "De gebruiker bestaat nog niet. Deze zal nu worden aangemaakt..."
    New-ADuser -Name $name `
    -DisplayName $name `
    -path "OU=bachelorproef,DC=bp-2223-jorn,DC=hogent" `
    -AccountPassword $pass_admin `
    -PasswordNeverExpires $true `
    -Enabled $true `
    -ChangePasswordAtLogon $false `
    -UserPrincipalName "$name@$domain.hogent" `
    -Description "Main domain admin"
}
else {
    log "De gebruiker bestaat al. Nu verder doen..."
}


log "Admin bpAdmin de juiste rechten geven..."
$groepen = @("Administrators", "Domain Admins", "Enterprise Admins", "Group Policy Creator Owners","Schema Admins")
foreach($groep in $groepen) {
    Add-ADGroupmember -ErrorAction Ignore -Identity "$groep" -Members "bpAdmin"  
}

# -----------
#    NAT
# -----------
log "Installeren rollen nodig voor NAT routing..."

$features=@(
  'RemoteAccess',
  'DirectAccess-VPN',
  'Routing',
  'Web-Server',
  'Web-WebServer',
  'Web-Common-Http',
  'Web-Default-Doc',
  'Web-Dir-Browsing',
  'Web-Http-Errors',
  'Web-Static-Content',
  'Web-Health',
  'Web-Http-Logging',
  'Web-Performance',
  'Web-Stat-Compression',
  'Web-Security',
  'Web-Filtering',
  'Web-IP-Security',
  'Web-Mgmt-Tools',
  'Web-Scripting-Tools',
  'Windows-Internal-Database',
  'GPMC',
  'RSAT',
  'RSAT-Role-Tools',
  'RSAT-RemoteAccess',
  'RSAT-RemoteAccess-Powershell'
)
Install-WindowsFeature -Name $features

# Het heropstarten gebeurt automatisch
log "Installatie is gelukt! Nu heropstarten..."

# Install en configuratie Remote Access
log 'Installatie en configuratie Remote Access (RA)...'
Install-RemoteAccess -VpnType Vpn

# Interface namen aan vars toewijzen
$ExternalInterface="WAN"
$InternalInterface="LAN"

# Rules uitschrijven voor NAT routing
cmd.exe /c "netsh routing ip nat install"
cmd.exe /c "netsh routing ip nat add interface $ExternalInterface"
cmd.exe /c "netsh routing ip nat set interface $ExternalInterface mode=full"
cmd.exe /c "netsh routing ip nat add interface $InternalInterface"

# -------
#   DNS
# -------

# Aanmaken Forward Lookup Zone
log "Aanmaken forward lookup zone..."

$exists = get-dnsserverzone -name "bp-2223-jorn.hogent"
if($exists) {
log "De DNS forwarding zone die je wenst te maken bestaat al. Doorgaan..."
}
else {
Add-DnsServerPrimaryZone -Name "bp-2223-jorn.hogent" -ReplicationScope "Domain"
}

# Aanmaken Reverse Lookup Zone
log "Toeovegen DNS primary zone..."
Add-DnsServerPrimaryZone -networkID "192.168.50.0/24" -ReplicationScope "Domain" -DynamicUpdate "Secure"

# Toevoegen Forwarder
log 'Toevoegen DNS Forwarder (8.8.8.8)...' 
Add-DnsServerForwarder -IPAddress 8.8.8.8

# Omzetten A records naar PTR records
$computerName = 'dc'; 

# Ophalen van alle dns A records
log 'Alle DNS A-records omzetten naar PTR-records...' 

$records = Get-DnsServerResourceRecord -ZoneName 'bp-2223-jorn.hogent' -RRType A -ComputerName $computerName; 
foreach ($record in $records) 
{ 
# PTR Domain name var
$ptrDomain = $record.HostName + '.bp-2223-jorn.hogent'; 

# IP omdraaien voor dezelfde record
$name = ($record.RecordData.IPv4Address.ToString() -replace '^(\d+)\.(\d+)\.(\d+).(\d+)$','$4.$3.$2');

# Toevoegen van de nieuwe PTR record
Add-DnsServerResourceRecordPtr -Name $name -ZoneName '50.168.192.in-addr.arpa' -ComputerName $computerName -PtrDomainName $ptrDomain; 
}

# -------
#  DHCP
# -------

# Instalation DHCP Server + management tools
log "Installeren van de DHCP-role..."
Install-WindowsFeature DHCP -IncludeManagementTools

# Authorizing DHCP Server
log "Deze server authorizeren..."
Add-DhcpServerInDC -DnsName "dc.bp-2223-jorn.hogent" -IPAddress 192.168.50.2

# Creating a DHCP Scope
log 'Aanmaken DHCP scope (Range = [192.168.50.101 - 192.168.50.150])...' 

Add-DhcpServerv4Scope `
-startRange 192.168.50.101 `
-EndRange 192.168.50.150 `
-SubnetMask 255.255.255.0 `
-Name "bpClientScope" `
-Description "Scope that will give VM 'client' an IP in [192.168.50.101 - 192.168.50.105]" `
-LeaseDuration 8:00:00

# Further Configuration of the DHCP Scope
write-host 'Configuratie DHCP-scope' -ForegroundColor Yellow

# 1. Excluding other addresses
Add-DhcpServerv4ExclusionRange -ScopeID 192.168.50.0 -StartRange 192.168.50.2 -EndRange 192.168.50.100
Add-DhcpServerv4ExclusionRange -ScopeID 192.168.50.0 -StartRange 192.168.50.151 -EndRange 192.168.50.254

# 2. Default Gateway
Set-DhcpServerv4OptionValue -ScopeID 192.168.50.0 -Router 192.168.50.2  # = ip adres van DC!

# 3. DNS + Domain Name
Set-DhcpServerv4OptionValue -ScopeId 192.168.50.0 -DnsServer '192.168.50.2' -DnsDomain "bp-2223-jorn.hogent"

# Start installing MSSQL db 
write-host 'Mounten van de SQL Server installation ISO...' -ForegroundColor Yellow

Mount-DiskImage -ImagePath "C:\en_sql_server_2019_standard_x64_dvd_814b57aa.iso"
    
write-host 'Installeren SQL Server...' -ForegroundColor Yellow
F:\setup.exe /qs /ACTION=Install /FEATURES=SQLEngine /INSTANCENAME=MSSQLSERVER /SQLSVCACCOUNT="NT SERVICE\MSSQLSERVER" /SQLSVCPASSWORD="Test123456!" /SQLSYSADMINACCOUNTS="bp-2223-jorn.hogent\bpAdmin" /AGTSVCACCOUNT="NT AUTHORITY\Network Service" /TCPENABLED=1 /IACCEPTSQLSERVERLICENSETERMS /SUPPRESSPRIVACYSTATEMENTNOTICE

Write-Host 'Installatie voltooid! Nu wachten op restart...' -ForegroundColor Green
Restart-Computer -Force  
```