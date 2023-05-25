# Uitvoer 4: Alle gebruikers proberen ophalen als bpAdmin
```powershell 
PS C:\> Get-ADuser -Filter *

DistinguishedName : CN=Administrator,CN=Users,DC=bp-2223-jorn,DC=hogent
Enabled           : True
GivenName         :
Name              : Administrator
ObjectClass       : user
ObjectGUID        : 71d347a1-43f2-465e-80b3-29591be4948a
SamAccountName    : Administrator
SID               : S-1-5-21-515683379-1161447010-2736559910-500
Surname           :
UserPrincipalName :

DistinguishedName : CN=Guest,CN=Users,DC=bp-2223-jorn,DC=hogent
Enabled           : True
GivenName         :
Name              : Guest
ObjectClass       : user
ObjectGUID        : 7841a85e-00a5-4068-91ed-7c9388f2326a
SamAccountName    : Guest
SID               : S-1-5-21-515683379-1161447010-2736559910-501
Surname           :
UserPrincipalName :

DistinguishedName : CN=krbtgt,CN=Users,DC=bp-2223-jorn,DC=hogent
Enabled           : False
GivenName         :
Name              : krbtgt
ObjectClass       : user
ObjectGUID        : fd8868ac-6f14-41b6-8d8f-3998f9a172cc
SamAccountName    : krbtgt
SID               : S-1-5-21-515683379-1161447010-2736559910-502
Surname           :
UserPrincipalName :

DistinguishedName : CN=bpAdmin,OU=bachelorproef,DC=bp-2223-jorn,DC=hogent
Enabled           : True
GivenName         :
Name              : bpAdmin
ObjectClass       : user
ObjectGUID        : 866e493c-ed16-4b9f-8a3f-797d444532fe
SamAccountName    : bpAdmin
SID               : S-1-5-21-515683379-1161447010-2736559910-1104
Surname           :
UserPrincipalName : bpAdmin@bp-2223-jorn.hogent

DistinguishedName : CN=sshd,CN=Users,DC=bp-2223-jorn,DC=hogent
Enabled           : True
GivenName         :
Name              : sshd
ObjectClass       : user
ObjectGUID        : 7d1cea1d-2b6a-40ce-a8f1-e7f3b96deeee
SamAccountName    : sshd
SID               : S-1-5-21-515683379-1161447010-2736559910-1106
Surname           :
UserPrincipalName :

DistinguishedName : CN=Jorn,OU=bachelorproef,DC=bp-2223-jorn,DC=hogent
Enabled           : True
GivenName         : Jorn
Name              : Jorn
ObjectClass       : user
ObjectGUID        : d4f8ee7c-13e3-46fd-820e-98a5e7306385
SamAccountName    : jorn
SID               : S-1-5-21-515683379-1161447010-2736559910-1107
Surname           :
UserPrincipalName : jorn@bp-2223-jorn.hogent

DistinguishedName : CN=Lisa,OU=bachelorproef,DC=bp-2223-jorn,DC=hogent
Enabled           : True
GivenName         : Lisa
Name              : Lisa
ObjectClass       : user
ObjectGUID        : 4c4e837f-84f6-4ce5-9851-4d91896fff9e
SamAccountName    : lisa
SID               : S-1-5-21-515683379-1161447010-2736559910-1108
Surname           :
UserPrincipalName : lisa@bp-2223-jorn.hogent    
```