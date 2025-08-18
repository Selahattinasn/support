<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# can you please provide the wmic commands for systemadminsitartion for daily task of a system administration. pleaese with example commands and as comprehensive guide

Here is a comprehensive guide to WMIC (Windows Management Instrumentation Command-line) commands for daily system administration tasks, with practical examples. WMIC is a powerful built-in Windows tool that simplifies system management by providing a command-line interface to WMI (Windows Management Instrumentation). It helps gather system information, manage processes, configure hardware, audit users, and much more.

***

## Overview of WMIC

- WMIC allows querying and managing both local and remote systems.
- You can get detailed hardware, software, network, user, process, and configuration info.
- WMIC supports executing commands synchronously on one or many computers.
- It can automate repetitive tasks via batch scripts.
- Run Command Prompt as Administrator to access most WMIC commands.

***

## Commonly Used WMIC Commands and Examples for System Administration

### 1. Get Operating System Information

```cmd
wmic os get caption,version,buildnumber,status
```

Gets OS name, version, build, and current status.

### 2. View Installed Software

```cmd
wmic product get name,version
```

Lists installed programs and their versions.

### 3. CPU Details

```cmd
wmic cpu get name,numberofcores,numberoflogicalprocessors
```

Shows CPU model and core/thread count.

### 4. System Uptime

```cmd
wmic os get lastbootuptime
```

Displays the last boot time for uptime calculation.

### 5. List User Accounts

```cmd
wmic useraccount get name,sid,status
```

Lists all user accounts with their security identifiers and status.

### 6. BIOS Information

```cmd
wmic bios get manufacturer,serialnumber,version
```

Gets BIOS manufacturer, serial number, and version info.

### 7. Disk Drive Information

```cmd
wmic diskdrive get model,serialnumber,size,mediaType
```

Provides info about physical drives, size, and type.

### 8. Memory Modules Info

```cmd
wmic memorychip get capacity,serialnumber,speed
```

Details each physical RAM module's capacity, speed, and serial.

### 9. Running Processes (Summary)

```cmd
wmic process list brief
```

Lists running processes with brief info.

### 10. Kill a Process by ID

```cmd
wmic process where processid="1234" delete
```

Terminates process with specified PID.

### 11. Network Adapter Configuration

```cmd
wmic nicconfig get description,macaddress,ipaddress
```

Displays network adapter description, MAC, and IP addresses.

### 12. List Windows Hotfixes (Patches)

```cmd
wmic qfe get hotfixid,description,installedon
```

Shows installed Windows updates with IDs and install dates.

### 13. Active User Session

```cmd
wmic computersystem get username
```

Shows the current logged-in user.

### 14. Services Status

```cmd
wmic service get name,displayname,state,startmode
```

Lists services with their name, status, and startup type.

### 15. Startup Programs

```cmd
wmic startup get caption,command,location
```

Lists programs set to start on boot.

### 16. Environment Variables

```cmd
wmic environment get name,username,variablevalue
```

Shows environment variables for the current user or system.

### 17. Remote Command Execution

Run a process remotely on another machine (requires appropriate permissions):

```cmd
wmic /node:"RemotePC" /user:"DOMAIN\AdminUser" process call create "notepad.exe"
```


### 18. Software Uninstallation

Uninstall software by name:

```cmd
wmic product where "name like '%SoftwareName%'" call uninstall
```


***

## Useful Global Switches for WMIC

- `/node:<computername>` — Run command on remote computer(s).
- `/user:<username>` and `/password:<password>` — Credentials for remote.
- `/namespace:<namespace>` — Specify WMI namespace (default root\cimv2).
- `/output:<filename>` — Save output to a file.
- `/interactive:on|off` — Enable or disable confirmation prompts.
- `/failfast:on|off` — Skip unreachable hosts faster in remote commands.

***

## Summary Table of Common WMIC Commands

| Task | Command Example |
| :-- | :-- |
| OS info | `wmic os get caption,version,buildnumber,status` |
| Installed software | `wmic product get name,version` |
| CPU info | `wmic cpu get name,numberofcores,numberoflogicalprocessors` |
| System uptime | `wmic os get lastbootuptime` |
| List user accounts | `wmic useraccount get name,sid,status` |
| BIOS details | `wmic bios get manufacturer,serialnumber,version` |
| Disk drives info | `wmic diskdrive get model,serialnumber,size,mediaType` |
| Memory modules | `wmic memorychip get capacity,serialnumber,speed` |
| List running processes | `wmic process list brief` |
| Kill a process | `wmic process where processid="1234" delete` |
| Network config | `wmic nicconfig get description,macaddress,ipaddress` |
| Installed Windows patches | `wmic qfe get hotfixid,description,installedon` |
| Logged-in user | `wmic computersystem get username` |
| Services status | `wmic service get name,displayname,state,startmode` |
| Startup programs | `wmic startup get caption,command,location` |
| Environment variables | `wmic environment get name,username,variablevalue` |
| Remote process execution | `wmic /node:"RemotePC" /user:"DOMAIN\AdminUser" process call create "notepad.exe"` |
| Uninstall software | `wmic product where "name like '%SoftwareName%'" call uninstall` |


***

This guide covers the most important WMIC commands that you can use daily to monitor, manage, troubleshoot, and configure Windows systems both locally and remotely. WMIC remains a highly useful tool, especially in environments where GUI access is limited or scripting is required.

If you want, I can also provide example batch scripts to automate common WMIC tasks or deeper examples for specific administrative needs.

Would you like me to provide that?

***

Sources from various WMIC guides and Windows official documentation.[^1][^2][^3][^4][^6]

<div style="text-align: center">⁂</div>

[^1]: https://it4home.dk/index.php/2024/01/16/maximizing-efficiency-with-wmic-a-guide-to-windows-system-management/

[^2]: https://learn.microsoft.com/en-us/windows/win32/wmisdk/wmic

[^3]: https://trustedsec.com/blog/command-line-underdog-wmic-in-action

[^4]: https://www.appliedincidentresponse.com/files/WMIC-Quick-Reference.pdf

[^5]: https://www.varonis.com/blog/wmi-windows-management-instrumentation

[^6]: https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/wmic

[^7]: https://kwcsec.gitbook.io/the-red-team-handbook/techniques/enumeration/recon-commands/wmic-commands

[^8]: https://www.scribd.com/document/114406758/Admin-Wmic

[^9]: https://www.xorrior.com/wmic-the-enterprise/

