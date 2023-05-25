# Uitvoer 5: Firewall regels ophalen via NT Authority
```powershell
PS C:\Windows\system32> Get-NetFirewallRule


Name                  : vm-monitoring-dcom
DisplayName           : Virtual Machine Monitoring (DCOM-In)
Description           : Allow DCOM traffic for remote Windows Management Instrumentation.
DisplayGroup          : Virtual Machine Monitoring
Group                 : @icsvc.dll,-700
Enabled               : False
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

Name                  : vm-monitoring-icmpv4
DisplayName           : Virtual Machine Monitoring (Echo Request - ICMPv4-In)
Description           : Echo Request messages are sent as ping requests to other nodes.
DisplayGroup          : Virtual Machine Monitoring
Group                 : @icsvc.dll,-700
Enabled               : False
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

Name                  : vm-monitoring-icmpv6
DisplayName           : Virtual Machine Monitoring (Echo Request - ICMPv6-In)
Description           : Echo Request messages are sent as ping requests to other nodes.
DisplayGroup          : Virtual Machine Monitoring
Group                 : @icsvc.dll,-700
Enabled               : False
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

Name                  : vm-monitoring-nb-session
DisplayName           : Virtual Machine Monitoring (NB-Session-In)
Description           : Allow NetBIOS Session Service connections.
DisplayGroup          : Virtual Machine Monitoring
Group                 : @icsvc.dll,-700
Enabled               : False
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

Name                  : vm-monitoring-rpc
DisplayName           : Virtual Machine Monitoring (RPC)
Description           : Allow Task Scheduler service to be remotely managed via RPC/TCP.
DisplayGroup          : Virtual Machine Monitoring
Group                 : @icsvc.dll,-700
Enabled               : False
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

