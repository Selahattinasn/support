<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# Please answer with CMD commands,

Got it — you want the **Task Scheduler creation** example for running an update script on a daily or weekly basis, **only using CMD commands** instead of PowerShell.

Here’s how to do it using **`SCHTASKS`** in Command Prompt:

***

## **1. Daily Task Example**

Run script `D:\Scripts\UpdateScript.bat` every day at **02:00 AM**:

```cmd
SCHTASKS /CREATE /SC DAILY /TN "Daily Update Script" /TR "cmd.exe /c D:\Scripts\UpdateScript.bat" /ST 02:00 /RU SYSTEM
```


***

## **2. Weekly Task Example**

Run script `E:\NAS\UpdateScript.bat` every Monday and Wednesday at **03:00 AM**:

```cmd
SCHTASKS /CREATE /SC WEEKLY /D MON,WED /TN "Weekly Update Script" /TR "cmd.exe /c E:\NAS\UpdateScript.bat" /ST 03:00 /RU SYSTEM
```


***

## **3. If Using UNC Path for NAS Script**

If the script is on a NAS share (to avoid mapped drive issues in scheduled tasks):

```cmd
SCHTASKS /CREATE /SC DAILY /TN "NAS Update Script" /TR "cmd.exe /c \\NAS-Server\Share\UpdateScript.bat" /ST 02:00 /RU domain\username /RP yourpassword
```

- `/RU domain\username` — run under a domain/user account with network access.
- `/RP yourpassword` — password for that account (required if not SYSTEM).

***

## Parameter Guide

| Parameter | Description |
| :-- | :-- |
| `/CREATE` | Creates a new task |
| `/SC` | Schedule type: DAILY, WEEKLY |
| `/D` | Days of the week for weekly tasks (MON,TUE,...) |
| `/ST` | Start time (HH:MM in 24hr format) |
| `/TN` | Task name |
| `/TR` | Path to the script or program to run |
| `/RU` | Run as user (SYSTEM or account) |
| `/RP` | Password for the account (omit for SYSTEM) |


***

💡 **Tips for admins**:

- Always use `"cmd.exe /c <yourscript>"` to ensure batch/PowerShell scripts run correctly.
- If your update script is a PowerShell `.ps1` file, replace `/TR` with:

```cmd
/TR "powershell.exe -NoProfile -ExecutionPolicy Bypass -File D:\Scripts\UpdateScript.ps1"
```

- For NAS locations, UNC paths + domain credentials are more reliable than mapped drives.

***

If you want, I can give you **a CMD one-liner** that will automatically detect the script on `D:` or `E:` (whichever exists) and create the scheduled task accordingly.
Do you want me to prepare that?

