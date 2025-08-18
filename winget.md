<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# How to update with winget program. What for to use.

The Windows Package Manager, known as **winget**, is a command-line tool in Windows designed to simplify **discovering, installing, upgrading, removing, and configuring software applications** on Windows computers. It is included by default in Windows 10 version 1709 and later, including Windows 11.

***

## What is winget used for?

- **Automate software installation and updates** from a curated repository of apps.
- Easily **search for software packages** in repositories.
- **Upgrade installed applications** to the latest available versions.
- **Uninstall programs** via command line.
- Manage software on multiple machines, facilitating scripting and automation.
- Export and import lists of installed applications to recreate or maintain environments.

It is especially useful for system administrators and developers wanting to automate or speed up software management without GUI interaction.

***

## Basic winget Commands and Usage Examples for System Administration

### 1. Search for a Package or Application

Find if a software package is available in the repositories:

```powershell
winget search <appname>
```

Example:

```powershell
winget search powershell
```


***

### 2. Install a Package

Install an application by its name or ID:

```powershell
winget install <appname_or_packageID>
```

Example:

```powershell
winget install Microsoft.PowerToys
```

- By default, installation is silent (no UI). Use `--interactive` if you want to show installer UI.

***

### 3. Upgrade Installed Applications

- List all upgradable packages:

```powershell
winget upgrade
```

- Upgrade a specific application:

```powershell
winget upgrade Microsoft.PowerToys
```

- Upgrade all upgradable applications at once:

```powershell
winget upgrade --all
```


***

### 4. Uninstall a Package

Remove an installed application:

```powershell
winget uninstall <appname_or_packageID>
```

Example:

```powershell
winget uninstall Microsoft.PowerToys
```


***

### 5. List Installed Packages

Show all installed applications (not limited to winget packages):

```powershell
winget list
```


***

### 6. Export and Import Package Lists

- Export current installed packages to a JSON file:

```powershell
winget export -o packages.json
```

- Import and install all packages from a JSON file:

```powershell
winget import packages.json
```

This is useful for setting up a consistent environment on multiple machines.

***

### 7. Show Package Details

View metadata such as version, publisher, description, homepage, and licenses:

```powershell
winget show <appname_or_packageID>
```

Example:

```powershell
winget show Microsoft.PowerToys
```


***

## Additional Notes

- WinGet uses official repositories and community manifests to find and install software.
- It requires running from PowerShell or Command Prompt with appropriate user privileges (sometimes Administrator for system-wide installs).
- Commands have flexible parameters for automation, silent installs, license acceptance, and specifying repositories.
- For a full list of commands and options, use:

```powershell
winget --help
```


***

## Summary Table of Core winget Commands

| Task | Command Example | Description |
| :-- | :-- | :-- |
| Search for packages | `winget search Firefox` | Search for software |
| Install a package | `winget install Mozilla.Firefox` | Install software |
| Upgrade all applications | `winget upgrade --all` | Upgrade all updatable apps |
| Upgrade single package | `winget upgrade Microsoft.PowerToys` | Upgrade specific app |
| Uninstall an app | `winget uninstall Microsoft.PowerToys` | Remove installed software |
| List installed apps | `winget list` | Show installed applications |
| Export installed packages | `winget export -o packages.json` | Export list to JSON |
| Import packages | `winget import packages.json` | Install packages from JSON file |
| Show package details | `winget show Microsoft.PowerToys` | Get metadata about a package |


***

This tool is highly valuable for system administrators automating software lifecycle management, simplifying deployment, updates, and ensuring consistency across many systems.

If you want, I can also provide advanced examples or scripting ideas using winget commands.

***

Sources:[^1][^2][^4][^5]

<div style="text-align: center">⁂</div>

[^1]: https://learn.microsoft.com/en-us/windows/package-manager/winget/

[^2]: https://www.petergirnus.com/blog/how-to-use-windows-package-manager-winget

[^3]: https://www.advancedinstaller.com/winget-windows-package-management.html

[^4]: https://talent500.com/blog/what-is-winget/

[^5]: https://learn.microsoft.com/en-us/windows/package-manager/

[^6]: https://www.youtube.com/watch?v=UoxmPalvz1g

[^7]: https://www.webhi.com/how-to/winget-windows-tutorial-guide/

[^8]: https://github.com/microsoft/winget-cli

[^9]: https://www.reddit.com/r/sysadmin/comments/1cwqjlb/winget_for_dummies/

