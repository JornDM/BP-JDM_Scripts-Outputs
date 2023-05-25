# Uitvoer 3: Gebruikers ophalen via Get-ADUser
```powershell
PS C:\> Get-ADUser -Filter * -SearchBase "OU=bachelorproef,DC=bp-2223-jorn,DC=hogent"


DistinguishedName : CN=bpAdmin,OU=bachelorproef,DC=bp-2223-jorn,DC=hogent
Enabled           : True
GivenName         : 
Name              : bpAdmin
ObjectClass       : user
ObjectGUID        : e1223a24-4f39-465b-b82e-e4a40995566c
SamAccountName    : bpAdmin
SID               : S-1-5-21-4194412052-2833681231-81850178-1104
Surname           : 
UserPrincipalName : bpAdmin@bp-2223-jorn.hogent

DistinguishedName : CN=Jorn,OU=bachelorproef,DC=bp-2223-jorn,DC=hogent
Enabled           : True
GivenName         : Jorn
Name              : Jorn
ObjectClass       : user
ObjectGUID        : b6d90391-602b-4a3c-b9bb-b4f57612e335
SamAccountName    : jorn
SID               : S-1-5-21-4194412052-2833681231-81850178-1108
Surname           : 
UserPrincipalName : jorn@bp-2223-jorn.hogent

DistinguishedName : CN=Bjorn Moeyerson,OU=bachelorproef,DC=bp-2223-jorn,DC=hogent
Enabled           : True
GivenName         : Bjorn
Name              : Bjorn Moeyerson
ObjectClass       : user
ObjectGUID        : d9f56264-7043-41fa-a9d2-75234ad622a8
SamAccountName    : bjorn
SID               : S-1-5-21-4194412052-2833681231-81850178-1126
Surname           : Moeyerson
UserPrincipalName : bjorn@bp-2223-jorn.hogent
```