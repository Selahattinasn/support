



### 1. Betriebssysteminformationen abrufen

```powershell
Get-CimInstance -ClassName Win32_OperatingSystem | Select-Object Caption, Version, BuildNumber, Status
```


***

### 2. Installierte Software anzeigen

```powershell
Get-CimInstance -ClassName Win32_Product | Select-Object Name, Version
```

*Hinweis: `Win32_Product` kann langsam sein und Ruhezustände auf Anwendungen auslösen. Alternativ kannst du die Registry abfragen, wenn Performance wichtig ist.*

***

### 3. CPU Details

```powershell
Get-CimInstance -ClassName Win32_Processor | Select-Object Name, NumberOfCores, NumberOfLogicalProcessors
```


***

### 4. System-Betriebszeit (letzter Start)

```powershell
(Get-CimInstance -ClassName Win32_OperatingSystem).LastBootUpTime
```


***

### 5. Benutzerkonten auflisten

```powershell
Get-CimInstance -ClassName Win32_UserAccount | Select-Object Name, SID, Status
```


***

### 6. BIOS Informationen

```powershell
Get-CimInstance -ClassName Win32_BIOS | Select-Object Manufacturer, SerialNumber, Version
```


***

### 7. Informationen zu Festplattenlaufwerken

```powershell
Get-CimInstance -ClassName Win32_DiskDrive | Select-Object Model, SerialNumber, Size, MediaType
```


***

### 8. Arbeitsspeichermodule Info

```powershell
Get-CimInstance -ClassName Win32_PhysicalMemory | Select-Object Capacity, SerialNumber, Speed
```


***

### 9. Laufende Prozesse (Kurzinfo)

```powershell
Get-Process | Select-Object Id, ProcessName, CPU, WorkingSet
```


***

### 10. Prozess mit Prozess-ID beenden

```powershell
Stop-Process -Id 1234
```


***

### 11. Netzwerkadapter-Konfiguration

```powershell
Get-CimInstance -ClassName Win32_NetworkAdapterConfiguration | Select-Object Description, MACAddress, IPAddress
```


***

### 12. Windows Hotfixes (Updates) anzeigen

```powershell
Get-CimInstance -ClassName Win32_QuickFixEngineering | Select-Object HotFixID, Description, InstalledOn
```


***

### 13. Aktive Benutzersitzung anzeigen

```powershell
(Get-CimInstance -ClassName Win32_ComputerSystem).Username
```


***

### 14. Dienste-Status

```powershell
Get-Service | Select-Object Name, DisplayName, Status, StartType
```


***

### 15. Autostart-Programme auflisten

```powershell
Get-CimInstance -Namespace root\default -ClassName StdRegProv |
Invoke-CimMethod -MethodName EnumKey -Arguments @{hDefKey=0x80000002; sSubKeyName='Software\Microsoft\Windows\CurrentVersion\Run'} |
Select-Object -ExpandProperty sNames
```

*Alternativ:*

```powershell
Get-CimInstance -ClassName Win32_StartupCommand | Select-Object Name, Command, Location
```


***

### 16. Umgebungsvariablen anzeigen

```powershell
Get-ChildItem Env:
```


***

### 17. Remote-Prozess ausführen

```powershell
Invoke-Command -ComputerName RemotePC -Credential (Get-Credential) -ScriptBlock { Start-Process "notepad.exe" }
```


***

### 18. Software deinstallieren

```powershell
Get-CimInstance -ClassName Win32_Product | Where-Object { $_.Name -like '*SoftwareName*' } | ForEach-Object { $_.Uninstall() }
```

*Hinweis: Auch hier kann die Verwendung von `Win32_Product` Nebenwirkungen haben. Für komplexere Deinstallationsszenarien empfiehlt sich ggf. die Nutzung von MSI-Eigenschaften oder anderen Methoden.*

***

Wenn du weitere Unterstützung bei PowerShell-Skripten oder -Automatisierungen brauchst, helfe ich gerne!

