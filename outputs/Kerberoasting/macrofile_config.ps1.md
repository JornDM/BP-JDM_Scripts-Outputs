# Uitvoer 6: Het maken en configureren van een macrofile
```powershell
PS C:\Windows\System32\myDIR> new-item -name macros

    Directory: C:\Windows\System32\myDIR

Mode                LastWriteTime         Length Name                                                                  
----                -------------         ------ ----                                                                  
-a----        4/28/2023  12:48 PM              0 macros

PS C:\Windows\System32\myDIR> Add-Content -Path .\macros -Value "hi=hostname"

C:\Windows\system32> reg add "HKCU\Software\Microsoft\Command Processor" /v Autorun /d "doskey /macrofile=\"C:\Windows\System32\myDIR\macros"" /f
The operation completed successfully.

C:\Windows\system32> reg query "HKCU\Software\Microsoft\Command Processor" /v Autorun

C:\Windows\System32\myDIR> doskey /macrofile=macros

PS C:\Windows\System32\myDIR> hi
hi : The term 'hi' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the 
spelling of the name, or if a path was included, verify that the path is correct and try again.
At line:1 char:1
+ hi
+ ~~
    + CategoryInfo          : ObjectNotFound: (hi:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```