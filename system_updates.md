<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# and a comprehensive guide to update system and/or  drivers with examplke commands

Here is a comprehensive guide for updating Windows systems and managing drivers via command line tools, focused on practical commands for daily system administration tasks using PowerShell and built-in Windows utilities.

***

## 1. Windows System Updates with PowerShell and PSWindowsUpdate Module

The preferred method for managing Windows updates via command line is the PowerShell module **PSWindowsUpdate**, which is not built into Windows by default but can be installed from the PowerShell Gallery.

### Installing PSWindowsUpdate Module

Run PowerShell **as Administrator** and enter:

```powershell
# Enable TLS 1.2 for secure connection if needed
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12

# Install the PSWindowsUpdate module (forces reinstallation if needed)
Install-Module -Name PSWindowsUpdate -Force
```


### Import the Module

```powershell
Import-Module PSWindowsUpdate
```


### Check Available Updates

To list all available updates for the local computer:

```powershell
Get-WindowsUpdate
```

To list updates on a remote computer:

```powershell
Get-WindowsUpdate -ComputerName RemoteComputerName
```


### Install All Available Updates

Automatically download, install updates, and reboot if needed:

```powershell
Install-WindowsUpdate -AcceptAll -AutoReboot
```

Or equivalently:

```powershell
Get-WindowsUpdate -AcceptAll -Install -AutoReboot
```


### Install Specific Updates by KB Article Number

To install a specific update:

```powershell
Install-WindowsUpdate -KBArticleID KB5017308 -AcceptAll -AutoReboot
```


### View Update History

To review installed update history:

```powershell
Get-WUHistory
```

With limiting to the last N updates, e.g., last 5 updates:

```powershell
Get-WUHistory -Last 5
```


### Uninstall Specific Updates

To uninstall a specific update:

```powershell
Remove-WindowsUpdate -KBArticleID KB5017308 -NoRestart
```


### Hide and Unhide Updates

To prevent a specific update from reinstalling:

```powershell
$HideList = "KB5017308"
Get-WindowsUpdate -KBArticleID $HideList -Hide
```

To unhide it later:

```powershell
Show-WindowsUpdate -KBArticleID $HideList
```


***

## 2. Update Drivers via Command Line

While Windows Update can install some drivers, driver management tools like **pnputil** and **DISM** can be used for more specific tasks.

### Using pnputil to Manage Drivers

- **List all installed third-party drivers:**

```cmd
pnputil /enum-drivers
```

- **Add a new driver package (from .inf driver file):**

```cmd
pnputil /add-driver "C:\Drivers\DriverName.inf" /install
```

- **Delete a driver package:**

```cmd
pnputil /delete-driver oem##.inf /uninstall /force
```

Replace `oem##.inf` with the driver name from the list.

### Using DISM (Deployment Image Servicing and Management)

The DISM tool can be used to add and remove driver packages during offline image servicing or on the running OS.

- **Add a driver package:**

```cmd
dism /online /add-driver /driver:"C:\Drivers\DriverName.inf" /forceunsigned
```

- **Remove a driver package:**

```cmd
dism /online /remove-driver /driver:oem##.inf
```


### Update Drivers via Device Manager CLI (devcon)

Microsoft provides `devcon` as a command line alternative to Device Manager to update drivers:

- **Update a driver for a device:**

```cmd
devcon update "C:\Drivers\DriverName.inf" <HardwareID>
```


***

## 3. Additional Useful Update \& Restart Commands

- Restart computer after updates or manually:

```powershell
Restart-Computer -Force
```

- Perform Windows Update and restart from a single PowerShell script:

```powershell
Install-WindowsUpdate -AcceptAll -AutoReboot
Restart-Computer -Force
```


***

## Summary Table

| Task | Command Example |
| :-- | :-- |
| Install PSWindowsUpdate module | `Install-Module -Name PSWindowsUpdate -Force` |
| List available updates | `Get-WindowsUpdate` |
| Install all updates | `Install-WindowsUpdate -AcceptAll -AutoReboot` |
| Install specific update | `Install-WindowsUpdate -KBArticleID KB5017308` |
| View update history | `Get-WUHistory` |
| Uninstall update | `Remove-WindowsUpdate -KBArticleID KB5017308 -NoRestart` |
| Hide update | `$HideList = "KB5017308"; Get-WindowsUpdate -KBArticleID $HideList -Hide` |
| List installed drivers | `pnputil /enum-drivers` |
| Add a driver package | `pnputil /add-driver "C:\Drivers\DriverName.inf" /install` |
| Delete a driver package | `pnputil /delete-driver oem##.inf /uninstall /force` |
| Restart computer | `Restart-Computer -Force` |


***

This guide offers powerful command-line methods to update Windows systems and drivers efficiently—useful for system administrators automating patch management and driver deployment.

If you want, I can provide scripts to automate bulk update or driver installation.

***

Sources:
MiniTool PSWindowsUpdate Ultimate Guide[^1]
Microsoft Q\&A PSWindowsUpdate examples[^2]
PowerShellIsFun blog on PSWindowsUpdate[^3]
WindowsPro.de Windows Update using PowerShell detailed guide[^4]

<div style="text-align: center">⁂</div>

[^1]: https://www.partitionwizard.com/partitionmagic/powershell-windows-update.html

[^2]: https://learn.microsoft.com/en-us/answers/questions/1613848/update-and-restart-from-powershell-or-command-line

[^3]: https://powershellisfun.com/2024/01/19/using-the-powershell-pswindowsupdate-module/

[^4]: https://www.windowspro.de/wolfgang-sommergut/windows-updates-powershell-pswindowsupdate-auflisten-herunterladen-installieren

[^5]: https://www.reddit.com/r/PowerShell/comments/1efu8e8/windows_update_and_powershell/

[^6]: https://www.thomas-krampe.com/2022/03/windows-updates-mit-powershell-durchfuehren/

[^7]: https://techcommunity.microsoft.com/discussions/windowsinsiderprogram/updating-windows-using-powershell/4088094

[^8]: https://www.computerweekly.com/de/ratgeber/So-verwalten-Sie-Windows-Updates-mit-PowerShell

