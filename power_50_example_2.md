<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# ja das will ich

Hier setze ich die Liste der wichtigsten PowerShell-Befehle für Systemadministratoren mit Flags und Beispielen fort, um die vollen 100 zu erreichen:


| Nr. | Befehl | Beschreibung | Wichtige Flags / Parameter | Beispiel |
| :-- | :-- | :-- | :-- | :-- |
| 51 | Get-History | Zeigt Befehlsverlauf an | `-Count` | `Get-History -Count 10` |
| 52 | Clear-History | Löscht Befehlsverlauf | Keine | `Clear-History` |
| 53 | Start-Job | Startet Hintergrundjob | `-ScriptBlock`, `-Name` | `Start-Job -ScriptBlock {Get-Process} -Name "ProzessJob"` |
| 54 | Get-Job | Zeigt laufende Hintergrundjobs | `-Name`, `-State` | `Get-Job -Name "ProzessJob"` |
| 55 | Receive-Job | Holt Ergebnisse von einem Job | `-Id`, `-Name`, `-Keep` | `Receive-Job -Name "ProzessJob"` |
| 56 | Remove-Job | Entfernt Job | `-Id`, `-Name` | `Remove-Job -Name "ProzessJob"` |
| 57 | Invoke-Command | Befehl remote ausführen | `-ComputerName`, `-Credential`, `-ScriptBlock` | `Invoke-Command -ComputerName Server01 -ScriptBlock {Get-Process}` |
| 58 | Enter-PSSession | Interaktives Remote-Shell | `-ComputerName`, `-Credential` | `Enter-PSSession -ComputerName Server01` |
| 59 | Exit-PSSession | Remote-Sitzung beenden | Keine | `Exit-PSSession` |
| 60 | Get-Date | Datum und Uhrzeit anzeigen | `-Format`, `-UFormat` | `Get-Date -Format "dd.MM.yyyy HH:mm"` |
| 61 | Set-Date | Datum und Uhrzeit setzen | `-Date` | `Set-Date -Date "2025-08-20 08:00"` |
| 62 | Get-EventSubscriber | Zeigt Ereignis-Abonnenten | Keine | `Get-EventSubscriber` |
| 63 | Register-ScheduledJob | Registriert geplanten Job | `-Name`, `-ScriptBlock`, `-Trigger` | `Register-ScheduledJob -Name "Backup" -ScriptBlock {Backup-Skript}` |
| 64 | Get-ScheduledJob | Zeigt geplante Jobs | Keine | `Get-ScheduledJob` |
| 65 | Unregister-ScheduledJob | Löscht geplanten Job | `-Name` | `Unregister-ScheduledJob -Name "Backup"` |
| 66 | New-ScheduledTaskTrigger | Erstellt Trigger für geplante Tasks | `-Daily`, `-At`, `-Weekly` | `New-ScheduledTaskTrigger -Daily -At 2am` |
| 67 | Register-ScheduledTask | Registriert geplante Aufgabe | `-TaskName`, `-Trigger`, `-Action` | `Register-ScheduledTask -TaskName "Backup" -Trigger $t -Action $a` |
| 68 | Get-ExecutionPolicy | Zeigt Execution Policy | Keine | `Get-ExecutionPolicy` |
| 69 | Set-ExecutionPolicy | Setzt Execution Policy | `-ExecutionPolicy`, `-Scope` | `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser` |
| 70 | Get-WindowsFeature | Installierte Windows Features anzeigen | `-Name`, `-ComputerName` | `Get-WindowsFeature -Name DNS` |
| 71 | Install-WindowsFeature | Feature installieren | `-Name`, `-IncludeManagementTools` | `Install-WindowsFeature -Name DNS -IncludeManagementTools` |
| 72 | Uninstall-WindowsFeature | Feature entfernen | `-Name` | `Uninstall-WindowsFeature -Name DNS` |
| 73 | Get-Volume | Volumeninformationen | Keine | `Get-Volume` |
| 74 | Format-Volume | Volumen formatieren | `-DriveLetter`, `-FileSystem`, `-Confirm` | `Format-Volume -DriveLetter D -FileSystem NTFS -Confirm:$false` |
| 75 | Mount-DiskImage | ISO-Datei mounten | `-ImagePath` | `Mount-DiskImage -ImagePath "C:\image.iso"` |
| 76 | Dismount-DiskImage | ISO-Datei unmounten | `-ImagePath` | `Dismount-DiskImage -ImagePath "C:\image.iso"` |
| 77 | Get-Disk | Festplatteninfo abrufen | `-Number`, `-FriendlyName` | `Get-Disk -Number 1` |
| 78 | Initialize-Disk | Festplatte initialisieren | `-Number`, `-PartitionStyle` | `Initialize-Disk -Number 1 -PartitionStyle GPT` |
| 79 | New-Partition | Neue Partition erstellen | `-DiskNumber`, `-UseMaximumSize`, `-DriveLetter` | `New-Partition -DiskNumber 1 -UseMaximumSize -DriveLetter E` |
| 80 | Set-Partition | Partition ändern | `-DriveLetter`, `-NewDriveLetter` | `Set-Partition -DriveLetter E -NewDriveLetter F` |
| 81 | Test-Path | Pfad testen | `-Path`, `-PathType` | `Test-Path -Path "C:\Windows"` |
| 82 | Get-Acl | Zugriffsrechte anzeigen | `-Path` | `Get-Acl -Path "C:\Windows\System32"` |
| 83 | Set-Acl | Zugriffsrechte setzen | `-Path`, `-AclObject` | `Set-Acl -Path "C:\Test.txt" -AclObject $acl` |
| 84 | Get-Module | Geladene Module anzeigen | `-Name` | `Get-Module -Name ActiveDirectory` |
| 85 | Import-Module | Modul laden | `-Name`, `-Force`, `-Verbose` | `Import-Module -Name ActiveDirectory -Force` |
| 86 | Remove-Module | Modul entladen | `-Name` | `Remove-Module -Name ActiveDirectory` |
| 87 | Get-EventLog | Ereignisprotokolle anzeigen | `-LogName`, `-Newest`, `-EntryType` | `Get-EventLog -LogName Application -Newest 50` |
| 88 | Clear-EventLog | Ereignisprotokoll löschen | `-LogName` | `Clear-EventLog -LogName Security` |
| 89 | Get-Random | Zufallszahlen erzeugen | `-Minimum`, `-Maximum` | `Get-Random -Minimum 1 -Maximum 100` |
| 90 | Get-NetFirewallRule | Firewallregeln anzeigen | `-DisplayName`, `-Enabled`, `-Direction` | `Get-NetFirewallRule -Enabled True` |
| 91 | New-NetFirewallRule | Neue Firewallregel erstellen | `-DisplayName`, `-Direction`, `-Protocol`, `-LocalPort`, `-Action` | `New-NetFirewallRule -DisplayName "Allow HTTP" -Direction Inbound -Protocol TCP -LocalPort 80 -Action Allow` |
| 92 | Remove-NetFirewallRule | Firewallregel löschen | `-DisplayName` | `Remove-NetFirewallRule -DisplayName "Allow HTTP"` |
| 93 | Enable-PSRemoting | PowerShell-Remoting aktivieren | `-Force`, `-SkipNetworkProfileCheck` | `Enable-PSRemoting -Force` |
| 94 | Disable-PSRemoting | PowerShell-Remoting deaktivieren | `-Force` | `Disable-PSRemoting -Force` |
| 95 | Get-EventViewer | Ereignisanzeige öffnen via Befehl | Keine | `Start-Process eventvwr` |
| 96 | Measure-Object | Objekte zählen oder Eigenschaften messen | `-Property`, `-Sum`, `-Average` | `Get-ChildItem | Measure-Object -Property Length -Sum` |
| 97 | Out-File | Ausgabe in Datei speichern | `-FilePath`, `-Encoding`, `-Append` | `Get-Process | Out-File -FilePath C:\process.txt -Encoding UTF8` |
| 98 | Export-Csv | Daten als CSV exportieren | `-Path`, `-NoTypeInformation`, `-Encoding` | `Get-Service | Export-Csv -Path C:\services.csv -NoTypeInformation` |
| 99 | Import-Csv | CSV-Datei importieren | `-Path` | `Import-Csv -Path C:\services.csv` |
| 100 | ConvertTo-Json | Daten in JSON umwandeln | `-Depth` | `Get-Process | ConvertTo-Json -Depth 3` |

Wenn du möchtest, kann ich zu bestimmten Befehlen ausführlichere Details, Skripte oder typische Anwendungsszenarien bereitstellen.

