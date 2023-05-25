# Uitvoer 9: Nieuwe Firewall regel maken als bpAdmin
```powershell
PS C:\Windows\system32> New-NetFirewallRule -DisplayName "FTP connection" -Direction Inbound -Protocol TCP -LocalPort 21 -Action Allow -RemoteAddress 192.168.50.101

Name                  : {1a15b0c9-454d-4db6-9727-bea7ee357675}
DisplayName           : FTP connection
Description           :
DisplayGroup          :
Group                 :
Enabled               : True
Profile               : Any
Platform              : {}
Direction             : Inbound
Action                : Allow
EdgeTraversalPolicy   : Block
LooseSourceMapping    : False
LocalOnlyMapping      : False
Owner                 :
PrimaryStatus         : OK
Status                : The rule was parsed successfully from the store. (65536)
EnforcementStatus     : NotApplicable
PolicyStoreSource     : PersistentStore
PolicyStoreSourceType : Local
```