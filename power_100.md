<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# auch list mir am mesit evrwendete 100 powershell befehle vom Systemadminisztratorem mit exampke commands bitte

Hier sind 100 der am häufigsten genutzten PowerShell-Befehle für Systemadministratoren mit kurzen Erklärungen und Beispielbefehlen. Diese Liste deckt viele typische Aufgaben in der Systemverwaltung, Fehlerbehebung, Nutzerverwaltung und Automatisierung ab:


| Nr. | Befehl | Beschreibung | Beispiel |
| :-- | :-- | :-- | :-- |
| 1 | Get-Help | Zeigt Hilfe zu PowerShell-Befehlen | `Get-Help Get-Process` |
| 2 | Get-Command | Listet alle verfügbaren PowerShell-Befehle | `Get-Command` |
| 3 | Get-Process | Listet laufende Prozesse | `Get-Process` |
| 4 | Stop-Process | Beendet einen Prozess nach Name oder ID | `Stop-Process -Id 1234` |
| 5 | Get-Service | Zeigt Dienste und deren Status | `Get-Service` |
| 6 | Start-Service | Startet einen Dienst | `Start-Service -Name "Spooler"` |
| 7 | Stop-Service | Stoppt einen Dienst | `Stop-Service -Name "Spooler"` |
| 8 | Restart-Service | Startet einen Dienst neu | `Restart-Service -Name "Spooler"` |
| 9 | Get-EventLog | Ruft Ereignisprotokolle ab | `Get-EventLog -LogName System -Newest 20` |
| 10 | Clear-EventLog | Leert ein Ereignisprotokoll | `Clear-EventLog -LogName System` |
| 11 | Get-Content | Liest Inhalte aus einer Datei | `Get-Content -Path "C:\log.txt" -Tail 10` |
| 12 | Set-Content | Schreibt Inhalt in eine Datei | `Set-Content -Path "C:\test.txt" -Value "Hallo"` |
| 13 | Add-Content | Hängt Inhalt an eine Datei an | `Add-Content -Path "C:\log.txt" -Value "Neuer Eintrag"` |
| 14 | Get-ChildItem | Listet Dateien und Ordner | `Get-ChildItem -Path C:\Windows` |
| 15 | Copy-Item | Kopiert Datei oder Ordner | `Copy-Item -Path c:\test.txt -Destination d:\backup` |
| 16 | Move-Item | Verschiebt Datei oder Ordner | `Move-Item -Path c:\test.txt -Destination d:\` |
| 17 | Remove-Item | Löscht Datei oder Ordner | `Remove-Item -Path c:\test.txt` |
| 18 | New-Item | Erstellt Datei oder Ordner | `New-Item -Path c:\test.txt -ItemType File` |
| 19 | Get-Location | Zeigt den aktuellen Pfad | `Get-Location` |
| 20 | Set-Location | Wechselt das Verzeichnis | `Set-Location -Path C:\Windows` |
| 21 | Get-Variable | Listet PowerShell-Variablen | `Get-Variable` |
| 22 | Set-Variable | Erstellt oder ändert Variablen | `Set-Variable -Name "var" -Value "Wert"` |
| 23 | Remove-Variable | Löscht Variablen | `Remove-Variable -Name "var"` |
| 24 | Get-Alias | Listet Aliase (Kurzbefehle) | `Get-Alias` |
| 25 | Set-Alias | Erstellt eigenen Alias | `Set-Alias -Name list -Value Get-ChildItem` |
| 26 | Import-Module | Importiert PowerShell-Module | `Import-Module ActiveDirectory` |
| 27 | Export-ModuleMember | Exportiert Funktionen aus Modulen | (in eigenen Modulen) |
| 28 | Get-ADUser | Listet Active Directory Users (Active Directory Modul) | `Get-ADUser -Filter *` |
| 29 | New-ADUser | Erstellt neuen AD-Benutzer | `New-ADUser -Name "Max"` |
| 30 | Set-ADUser | Ändert AD-Benutzer-Eigenschaften | `Set-ADUser -Identity max -EmailAddress max@beispiel.de` |
| 31 | Remove-ADUser | Löscht AD-Benutzer | `Remove-ADUser -Identity max` |
| 32 | Get-ADComputer | Listet Computerobjekte im AD | `Get-ADComputer -Filter *` |
| 33 | Restart-Computer | Startet Rechner neu | `Restart-Computer -ComputerName server01` |
| 34 | Shutdown-Computer | Fährt Rechner herunter | `Stop-Computer -ComputerName server01` |
| 35 | Test-Connection | Prüft Netzwerkverbindung (ping) | `Test-Connection google.de` |
| 36 | Get-NetIPAddress | Zeigt IP-Adressen der Netzwerkkarten | `Get-NetIPAddress` |
| 37 | Get-NetAdapter | Listet Netzwerkadapter | `Get-NetAdapter` |
| 38 | Enable-NetAdapter | Aktiviert Netzwerkadapter | `Enable-NetAdapter -Name "Ethernet"` |
| 39 | Disable-NetAdapter | Deaktiviert Netzwerkadapter | `Disable-NetAdapter -Name "Ethernet"` |
| 40 | Set-DnsClientServerAddress | Setzt DNS-Serveradresse | `Set-DnsClientServerAddress -InterfaceAlias Ethernet -ServerAddresses 8.8.8.8` |
| 41 | Get-Service | Zeigt Dienste | `Get-Service` |
| 42 | Start-Service | Startet Dienst | `Start-Service -Name spooler` |
| 43 | Stop-Service | Stoppt Dienst | `Stop-Service -Name spooler` |
| 44 | Restart-Service | Startet Dienst neu | `Restart-Service -Name spooler` |
| 45 | Get-EventLog | Listet Ereignisprotokolle | `Get-EventLog -LogName System -Newest 100` |
| 46 | Clear-EventLog | Löscht Ereignisprotokoll | `Clear-EventLog -LogName Application` |
| 47 | Get-WmiObject | Ruft WMI-Informationen ab | `Get-WmiObject -Class Win32_OperatingSystem` |
| 48 | Get-CimInstance | Moderne Alternative zu Get-WmiObject | `Get-CimInstance -ClassName Win32_OperatingSystem` |
| 49 | Get-Process | Zeigt Prozesse | `Get-Process` |
| 50 | Stop-Process | Beendet Prozess | `Stop-Process -Name notepad` |
| 51 | Get-History | Listet Befehlsverlauf | `Get-History` |
| 52 | Clear-History | Löscht Befehlsverlauf | `Clear-History` |
| 53 | Start-Job | Startet Hintergrundjob | `Start-Job -ScriptBlock { Get-Process }` |
| 54 | Get-Job | Zeigt Hintergrundjobs | `Get-Job` |
| 55 | Receive-Job | Holt Ergebnis eines Jobs | `Receive-Job -Id 1` |
| 56 | Remove-Job | Entfernt Job | `Remove-Job -Id 1` |
| 57 | Invoke-Command | Führe Befehle auf Remote-Computern aus | `Invoke-Command -ComputerName Server01 -ScriptBlock { Get-Process }` |
| 58 | Enter-PSSession | Interaktive Sitzung auf Remote-Computer | `Enter-PSSession -ComputerName Server01` |
| 59 | Exit-PSSession | Beendet Remote-Sitzung | `Exit-PSSession` |
| 60 | Get-Date | Zeigt Datum und Uhrzeit | `Get-Date` |
| 61 | Set-Date | Setzt Datum und Uhrzeit | `Set-Date -Date "2025-08-19 15:00"` |
| 62 | Get-EventLog | Ereignisprotokolle anzeigen | `Get-EventLog -LogName Security -Newest 50` |
| 63 | New-ADGroup | Erstellt neue AD-Gruppe | `New-ADGroup -Name "Admins" -GroupScope Global` |
| 64 | Add-ADGroupMember | Fügt Benutzer zu AD-Gruppe hinzu | `Add-ADGroupMember -Identity Admins -Members max` |
| 65 | Remove-ADGroupMember | Entfernt Benutzer aus AD-Gruppe | `Remove-ADGroupMember -Identity Admins -Members max` |
| 66 | Get-ServiceStatus | Zeigt Status von Diensten | `Get-Service -Name W32Time` |
| 67 | Set-ExecutionPolicy | Setzt Ausführungsrichtlinie | `Set-ExecutionPolicy RemoteSigned` |
| 68 | Get-EventSubscriber | Zeigt Event Subscriber | `Get-EventSubscriber` |
| 69 | Register-ScheduledJob | Registriert einen geplanten Job | `Register-ScheduledJob -Name "Backup" -ScriptBlock { Backup-Job }` |
| 70 | Get-ScheduledJob | Zeigt geplante Jobs | `Get-ScheduledJob` |
| 71 | Unregister-ScheduledJob | Entfernt geplanten Job | `Unregister-ScheduledJob -Name "Backup"` |
| 72 | New-ScheduledTaskTrigger | Erstellt Trigger für geplante Aufgaben | `New-ScheduledTaskTrigger -Daily -At 2am` |
| 73 | Register-ScheduledTask | Registriert geplante Aufgabe | `Register-ScheduledTask -TaskName "DailyBackup" -Trigger $trigger -Action $action` |
| 74 | Get-ExecutionPolicy | Zeigt aktuelle Ausführungsrichtlinie | `Get-ExecutionPolicy` |
| 75 | Get-WindowsFeature | Zeigt installierte Windows-Features | `Get-WindowsFeature` |
| 76 | Install-WindowsFeature | Installiert Windows-Feature | `Install-WindowsFeature -Name DNS` |
| 77 | Uninstall-WindowsFeature | Entfernt Windows-Feature | `Remove-WindowsFeature -Name DNS` |
| 78 | Get-Volume | Zeigt Volumen und Laufwerksinformationen | `Get-Volume` |
| 79 | Format-Volume | Formatiert ein Volumen | `Format-Volume -DriveLetter D -FileSystem NTFS` |
| 80 | Mount-DiskImage | Bindet ISO-Datei ein | `Mount-DiskImage -ImagePath "C:\image.iso"` |
| 81 | Dismount-DiskImage | Trennt ISO-Datei | `Dismount-DiskImage -ImagePath "C:\image.iso"` |
| 82 | Get-Disk | Zeigt Festplatteninformationen | `Get-Disk` |
| 83 | Initialize-Disk | Initialisiert Festplatte | `Initialize-Disk -Number 1` |
| 84 | New-Partition | Erstellt neue Partition | `New-Partition -DiskNumber 1 -UseMaximumSize` |
| 85 | Set-Partition | Ändert Eigenschaften einer Partition | `Set-Partition -DriveLetter E -NewDriveLetter F` |
| 86 | Get-ChildItem | Listet Dateien/Ordner | `Get-ChildItem -Path C:\Windows\System32` |
| 87 | Test-Path | Prüft ob ein Pfad existiert | `Test-Path -Path "C:\Windows"` |
| 88 | Get-Acl | Zeigt Zugriffsrechte an | `Get-Acl -Path C:\test.txt` |
| 89 | Set-Acl | Setzt Zugriffsrechte | `Set-Acl -Path C:\test.txt -AclObject $acl` |
| 90 | Get-Job | Zeigt Hintergrundjobs | `Get-Job` |
| 91 | Get-Location | Zeigt aktuellen Pfad | `Get-Location` |
| 92 | Get-Member | Zeigt Eigenschaften von Objekten | `Get-Process | Get-Member` |
| 93 | Get-Module | Listet importierte Module | `Get-Module` |
| 94 | Get-OSVersion | Zeigt Betriebssystemversion | `(Get-CimInstance Win32_OperatingSystem).Caption` |
| 95 | Get-Random | Erzeugt Zufallszahl | `Get-Random -Minimum 1 -Maximum 100` |
| 96 | Get-NetFirewallRule | Zeigt Firewallregeln | `Get-NetFirewallRule` |
| 97 | New-NetFirewallRule | Erstellt neue Firewallregel | `New-NetFirewallRule -DisplayName "Allow HTTP" -Direction Inbound -Protocol TCP -LocalPort 80 -Action Allow` |
| 98 | Remove-NetFirewallRule | Entfernt Firewallregel | `Remove-NetFirewallRule -DisplayName "Allow HTTP"` |
| 99 | Enable-PSRemoting | Aktiviert PowerShell-Remoting | `Enable-PSRemoting -Force` |
| 100 | Disable-PSRemoting | Deaktiviert PowerShell-Remoting | `Disable-PSRemoting -Force` |

Diese Liste ist ein guter Einstieg und deckt viele typische Aufgaben in der Systemadministration mit PowerShell ab. Möchtest du eine ausführlichere Erklärung oder Skript-Beispiele zu einzelnen Befehlen?
<span style="display:none">[^1][^2][^3][^4][^5][^6][^7]</span>

<div style="text-align: center">⁂</div>

[^1]: https://www.reddit.com/r/PowerShell/comments/s8rj49/for_those_that_work_in_it_admin_what_are_the_key/?tl=de

[^2]: https://www.ionos.de/digitalguide/server/konfiguration/powershell-befehle/

[^3]: https://www.scriptrunner.com/de/ressourcen/blog/top-10-powershell-befehle-zur-fehlerbehebung

[^4]: https://www.youtube.com/watch?v=jvKU7JoFl0c

[^5]: https://blog.tekspace.io/top-100-essential-powershell-commands-your-must-know-cheat-sheet/

[^6]: https://www.assets.dpunkt.de/leseproben/13153/2_Cmdlets%20-%20die%20PowerShell-Befehle.pdf

[^7]: https://download.microsoft.com/download/7/3/b/73ba405f-e693-461c-99fc-0920bc02c18c/Windows-Powershell.pdf

