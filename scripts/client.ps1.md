# Client.ps1
```powershell
# --------------------------------- #
#            client.ps1             #
# --------------------------------- #
# Functions
function log([string] $msg) {
    write-host $msg
}

# -------> Start configuratie <--------
log "Ethernet-adapter hernoemen..."
Get-NetAdapter "Ethernet" | Rename-NetAdapter -newname 'LAN'

# Kleine timeout zodat IP-configuratie zeker kan inladen...
log 'Time-out inlassen voor het inladen van de IP-configuratie...'

Timeout /T 10 

# Enabling auto-login for WS-Client
log 'Auto-login inschakelen voor user bpAdmin...'

[string]$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon"

Set-ItemProperty $RegPath "AutoAdminLogon" -Value "1" -type String 
Set-ItemProperty $RegPath "DefaultUsername" -Value "bpAdmin@bp-2223-jorn.hogent" -type String 
Set-ItemProperty $RegPath "DefaultPassword" -Value "Test123456!" -type String

# Client laten joinen tot het domein 
log "Joinen van het domein..."

try {
    $joinCred = New-Object pscredential -ArgumentList ([pscustomobject]@{
        UserName = $null
        Password = (ConvertTo-SecureString -String 'Test123!' -AsPlainText -Force)[0]
    })
    Add-Computer -DomainName "bp-2223-jorn" -Options UnsecuredJoin,PasswordPass -Credential $joinCred -ErrorAction Stop     
} catch {
    Write-Error 'Het lukte helaas niet om het domein te joinen...'
}

Write-Host "Domein join succesvol! Computer opnieuw opstarten..." -ForegroundColor Green
Restart-Computer -Force 

# At the end of the installations => restart
log 'Toestel zal zich zodadelijk heropstarten...'
```