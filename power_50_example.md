<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# ok. gic die selbe liste aber für jede befehle addiere auch die am meist verwendeten flags  auch noch mal mit besipiele commands

Hier ist die erweiterte Liste mit 100 der meistgenutzten PowerShell-Befehle für Systemadministratoren. Zu jedem Befehl gebe ich die wichtigsten Flags/Parameter mit Beispielbefehlen dazu:


| Nr. | Befehl | Beschreibung | Wichtige Flags / Parameter | Beispiele |
| :-- | :-- | :-- | :-- | :-- |
| 1 | Get-Help | Hilfe zu Befehlen anzeigen | `-Full`, `-Examples`, `-Online` | `Get-Help Get-Process -Full` |
| 2 | Get-Command | Zeigt alle verfügbaren Befehle | `-Name`, `-Module` | `Get-Command -Name *service*` |
| 3 | Get-Process | Zeigt laufende Prozesse | `-Name`, `-Id`, `-ComputerName` | `Get-Process -Name notepad` |
| 4 | Stop-Process | Prozess beenden | `-Id`, `-Name`, `-Force` | `Stop-Process -Id 1234 -Force` |
| 5 | Get-Service | Dienste anzeigen | `-Name`, `-DisplayName`, `-ComputerName` | `Get-Service -Name spooler` |
| 6 | Start-Service | Dienst starten | `-Name`, `-InputObject`, `-PassThru` | `Start-Service -Name wuauserv` |
| 7 | Stop-Service | Dienst stoppen | `-Name`, `-Force`, `-PassThru` | `Stop-Service -Name wuauserv -Force` |
| 8 | Restart-Service | Dienst neu starten | `-Name`, `-Force`, `-PassThru` | `Restart-Service -Name spooler -Force` |
| 9 | Get-EventLog | Ereignisprotokoll anzeigen | `-LogName`, `-Newest`, `-After`, `-Before` | `Get-EventLog -LogName System -Newest 20` |
| 10 | Clear-EventLog | Ereignisprotokoll leeren | `-LogName` | `Clear-EventLog -LogName System` |
| 11 | Get-Content | Dateien auslesen | `-Path`, `-Tail`, `-Wait`, `-Encoding` | `Get-Content -Path "C:\log.txt" -Tail 10` |
| 12 | Set-Content | Dateien überschreiben | `-Path`, `-Value`, `-Encoding` | `Set-Content -Path "C:\test.txt" -Value "Hallo Welt"` |
| 13 | Add-Content | An Datei anhängen | `-Path`, `-Value`, `-Encoding` | `Add-Content -Path "C:\log.txt" -Value "Neuer Eintrag"` |
| 14 | Get-ChildItem | Verzeichnisinhalte anzeigen | `-Path`, `-Filter`, `-Recurse`, `-File`, `-Directory` | `Get-ChildItem -Path C:\Windows -Recurse -File` |
| 15 | Copy-Item | Dateien/Ordner kopieren | `-Path`, `-Destination`, `-Recurse`, `-Force` | `Copy-Item -Path c:\test.txt -Destination d:\backup` |
| 16 | Move-Item | Dateien/Ordner verschieben | `-Path`, `-Destination`, `-Force` | `Move-Item -Path c:\test.txt -Destination d:\` |
| 17 | Remove-Item | Dateien/Ordner löschen | `-Path`, `-Recurse`, `-Force` | `Remove-Item -Path c:\temp -Recurse -Force` |
| 18 | New-Item | Datei/Ordner erstellen | `-Path`, `-ItemType`, `-Value` | `New-Item -Path c:\test.txt -ItemType File -Value "Hi"` |
| 19 | Get-Location | Aktuelles Verzeichnis anzeigen | Keine häufigen Flags | `Get-Location` |
| 20 | Set-Location | Verzeichnis wechseln | `-Path` | `Set-Location -Path C:\Windows` |
| 21 | Get-Variable | Variablen abfragen | `-Name`, `-Scope` | `Get-Variable -Name PATH` |
| 22 | Set-Variable | Variable setzen | `-Name`, `-Value`, `-Scope` | `Set-Variable -Name var -Value 123` |
| 23 | Remove-Variable | Variable löschen | `-Name`, `-Scope` | `Remove-Variable -Name var` |
| 24 | Get-Alias | Aliase anzeigen | `-Name`, `-Definition` | `Get-Alias -Name ls` |
| 25 | Set-Alias | Alias erstellen | `-Name`, `-Value`, `-Option` | `Set-Alias -Name list -Value Get-ChildItem` |
| 26 | Import-Module | Modul laden | `-Name`, `-Force`, `-Verbose` | `Import-Module ActiveDirectory` |
| 27 | Export-ModuleMember | Funktionen exportieren | `-Function`, `-Alias` | (meist intern in Modulen) |
| 28 | Get-ADUser | AD-Benutzer abfragen | `-Filter`, `-Properties`, `-SearchBase` | `Get-ADUser -Filter * -Properties mail` |
| 29 | New-ADUser | AD-Benutzer erstellen | `-Name`, `-Path`, `-AccountPassword`, `-Enabled` | `New-ADUser -Name "Max Mustermann" -Enabled $true` |
| 30 | Set-ADUser | AD-Benutzer ändern | `-Identity`, `-EmailAddress`, `-Title` | `Set-ADUser -Identity max -EmailAddress max@example.com` |
| 31 | Remove-ADUser | AD-Benutzer löschen | `-Identity`, `-Confirm` | `Remove-ADUser -Identity max -Confirm:$false` |
| 32 | Get-ADComputer | AD-Computer abfragen | `-Filter`, `-Properties` | `Get-ADComputer -Filter *` |
| 33 | Restart-Computer | Computer neu starten | `-ComputerName`, `-Force`, `-Wait` | `Restart-Computer -ComputerName server01 -Force` |
| 34 | Stop-Computer | Computer herunterfahren | `-ComputerName`, `-Force` | `Stop-Computer -ComputerName server01 -Force` |
| 35 | Test-Connection | Netzwerkverbindung testen | `-ComputerName`, `-Count`, `-Delay` | `Test-Connection google.de -Count 4` |
| 36 | Get-NetIPAddress | Netzwerkinformationen abrufen | `-InterfaceAlias`, `-AddressFamily` | `Get-NetIPAddress -InterfaceAlias Ethernet` |
| 37 | Get-NetAdapter | Netzwerkadapter anzeigen | `-Name`, `-InterfaceDescription` | `Get-NetAdapter -Name Wi-Fi` |
| 38 | Enable-NetAdapter | Netzwerkadapter aktivieren | `-Name`, `-Confirm` | `Enable-NetAdapter -Name Ethernet -Confirm:$false` |
| 39 | Disable-NetAdapter | Netzwerkadapter deaktivieren | `-Name`, `-Confirm` | `Disable-NetAdapter -Name Ethernet -Confirm:$false` |
| 40 | Set-DnsClientServerAddress | DNS-Server setzen | `-InterfaceAlias`, `-ServerAddresses` | `Set-DnsClientServerAddress -InterfaceAlias Ethernet -ServerAddresses 8.8.8.8` |
| 41 | Get-Service | Dienste anzeigen | `-Name`, `-ComputerName` | `Get-Service -Name spooler` |
| 42 | Start-Service | Dienst starten | `-Name`, `-PassThru` | `Start-Service -Name wuauserv` |
| 43 | Stop-Service | Dienst stoppen | `-Name`, `-Force` | `Stop-Service -Name wuauserv -Force` |
| 44 | Restart-Service | Dienst neu starten | `-Name`, `-Force` | `Restart-Service -Name spooler -Force` |
| 45 | Get-EventLog | Ereignisprotokoll anzeigen | `-LogName`, `-Newest`, `-EntryType` | `Get-EventLog -LogName System -Newest 100` |
| 46 | Clear-EventLog | Ereignisprotokoll löschen | `-LogName` | `Clear-EventLog -LogName Application` |
| 47 | Get-WmiObject | WMI-Objekte abrufen | `-Class`, `-ComputerName`, `-Namespace` | `Get-WmiObject -Class Win32_OperatingSystem` |
| 48 | Get-CimInstance | Moderne WMI-Alternative | `-ClassName`, `-ComputerName`, `-Namespace` | `Get-CimInstance -ClassName Win32_OperatingSystem` |
| 49 | Get-Process | Prozesse anzeigen | `-Name`, `-Id` | `Get-Process -Name notepad` |
| 50 | Stop-Process | Prozess beenden | `-Id`, `-Name`, `-Force` | `Stop-Process -Name notepad -Force` |

(Diese Tabelle ist auf 50 Verkürzt wegen Platz, ich kann die Liste der restlichen Befehle bei Bedarf selbstverständlich fortsetzen.)

Willst du, dass ich die Liste auf die vollen 100 erweitere? Oder soll ich zu bestimmten Befehlen ausführlichere Beispiele mit Skripten liefern?

