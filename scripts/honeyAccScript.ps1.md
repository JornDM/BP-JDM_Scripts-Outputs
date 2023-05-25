# PowerShell script om een logfile en pop-up bericht te maken voor honey account}
```powershell
# vars
$warning_logs_DIR = "C:\Users\Administrator\Desktop\WARNING-LOGS"
$current_date = Get-Date -Format "dd-MM-yyyy"
$current_time = Get-Date -Format "HH.mm.ss"
$first_lines = "-----------------", 
"WARNING!!!!", "-----------------", 
"Er was net een poging om op het honeypot account 'admin' aan te melden!",
"Dit zijn de details van de aangemaakte log:"

# script

# - nakijken of map al bestaat
if (Test-Path "$warning_logs_DIR") {
    write-host "De map bestaat al..." -ForegroundColor Red
}
else {
    mkdir $warning_logs_DIR
    write-host "Map werd gemaakt op het bureaublad van Administrator" -ForegroundColor Green
}

# - maken van logbestand en eerste paar lijnen content toevoegen
New-Item -Path $warning_logs_DIR -Name "LOG_$current_date`_$current_time.txt" -ItemType File

Add-Content -Value $first_lines -Path "$warning_logs_DIR\LOG_$current_date`_$current_time.txt"

# - Laatste nieuwe log ophalen
$events = Get-WinEvent -FilterHashtable @{LogName='Security';ID=@(4634, 4624, 4648);ProviderName='Microsoft-Windows-Security-Auditing';} -MaxEvents 1000 | Where-Object {$_.Properties[5].Value -eq "admin"}
$latest_event = $events | Sort-Object TimeCreated -Descending | Select-Object -First 1

if ($latest_event) {
    # hulpbestand om belangrijke netwerk informatie op te halen 
    Add-Content -Path "C:\Users\Administrator\Desktop\temp.txt" -Value "Berichtgeving: $($latest_event.Message)"
    $network_info = findstr "Source" "C:\Users\Administrator\Desktop\temp.txt"

    Add-Content -Path "$warning_logs_DIR\LOG_$current_date`_$current_time.txt" -Value "De nieuwste gebeurtenis met ID 4634, 4624 of 4648 en met het account 'admin' is:"
    Add-Content -Path "$warning_logs_DIR\LOG_$current_date`_$current_time.txt" -Value "Gebeurtenis ID: $($latest_event.Id)"
    Add-Content -Path "$warning_logs_DIR\LOG_$current_date`_$current_time.txt" -Value "Gebeurtenis Type: $($latest_event.LogName)"
    Add-Content -Path "$warning_logs_DIR\LOG_$current_date`_$current_time.txt" -Value "Gebeurtenis tijd: $($latest_event.TimeCreated)"
    Add-Content -Path "$warning_logs_DIR\LOG_$current_date`_$current_time.txt" -Value "Accountnaam: $($latest_event.Properties[5].Value)"
    Add-Content -Path "$warning_logs_DIR\LOG_$current_date`_$current_time.txt" -Value "Status: $($latest_event.KeywordsDisplayNames)"
    Add-Content -Path "$warning_logs_DIR\LOG_$current_date`_$current_time.txt" -Value "IMPORTANT! Network info: `n$network_info"
    Add-Content -Path "$warning_logs_DIR\LOG_$current_date`_$current_time.txt" "------------------------------------------------------"
} else {
    Write-Host "Geen gebeurtenissen gevonden met de opgegeven criteria."
}

Remove-item -Path "C:\Users\Administrator\Desktop\temp.txt"

# Waarschuwing weergeven op het scherm 
Add-Type -AssemblyName System.Windows.Forms
[System.Windows.Forms.MessageBox]::Show("GEVAAR: Iemand probeerde net op het honey account 'admin' aan te melden!!`nRaadpleeg log bestand C:\Users\Administrator\Desktop\LOG_$current_date`_$current_time.txt voor meer info.", 'Waarschuwing', 'OK', 'Warning')
```
