<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# how to set a network conection. suppose that we want to make network comnnection to a NAS Device  to its directory. For eymple BAckups

To set up a network connection to a NAS device for accessing its directory (for example, for backups), the typical way on Windows is to **map a network drive** to the NAS shared folder. This makes the NAS folder appear as a drive letter (like D: or E:) on your PC, enabling easy access and file operations.

Here is a step-by-step guide on how to do this, including CMD commands and some notes:

***

## How to Map a Network Drive to a NAS Shared Folder in Windows

### 1. Prepare Your NAS

- Ensure your NAS has **SMB (Server Message Block)** file sharing enabled (the common Windows file sharing protocol).
- Assign a **static IP address** to your NAS or know its IP address on the network.
- Confirm the NAS shared folder you want to access has proper permissions (username/password if required).


### 2. Open Command Prompt (run as Administrator)

### 3. Use `net use` Command to Map the Network Drive

#### Syntax:

```cmd
net use <DriveLetter>: \\<NAS_IP_Address>\<SharedFolder> /user:<username> <password> /persistent:yes
```

- `<DriveLetter>`: The drive letter you want to assign (e.g., Z:)
- `<NAS_IP_Address>`: IP address of your NAS (e.g., 192.168.1.100)
- `<SharedFolder>`: The name of the shared folder on the NAS
- `/user`: The username with access to the NAS share (optional if no auth)
- `/persistent:yes`: Optional, reconnects the drive at each login


#### Example:

```cmd
net use Z: \\192.168.1.100\Backups /user:admin MyPassword /persistent:yes
```

This maps the NAS shared folder named "Backups" on NAS at 192.168.1.100 to drive letter Z: with username "admin" and password "MyPassword."

If no username or password is needed, simply omit `/user` and password:

```cmd
net use Z: \\192.168.1.100\Backups /persistent:yes
```


***

### 4. Access the Mapped Network Drive

- After running the command, open **File Explorer** and you will see the Z: drive containing the contents of the NAS "Backups" folder.
- You can now read/write files there as if it was a local disk.

***

## Additional Tips

- To **disconnect** the mapped drive, use:

```cmd
net use Z: /delete
```

- Use **UNC paths** (\\NAS_IP\Share) instead of mapped drives in scripts to avoid issues when running under different user contexts or services.
- If you want to **map a drive persistently but also want the password to be saved securely**, you need to connect once manually or use Windows Credential Manager.
- For automation in backup scripts or scheduled tasks, using UNC paths is often more reliable than mapped drives.
- If your NAS supports it, using a **hostname** instead of IP is more readable:

```cmd
net use Z: \\NAS-Device-Name\Backups /user:admin MyPassword /persistent:yes
```


***

## Summary Table of Key Commands

| Task | Command Example |
| :-- | :-- |
| Map NAS share to drive Z: | `net use Z: \\192.168.1.100\Backups /user:admin MyPassword /persistent:yes` |
| Map NAS share without auth | `net use Z: \\192.168.1.100\Backups /persistent:yes` |
| Delete mapped drive Z: | `net use Z: /delete` |
| Use UNC path in script | Access `\\192.168.1.100\Backups` directly without mapping |


***

Mapping a network drive to your NAS gives seamless access to backup directories or shared files as if it was a local drive, which simplifies administrative operations and automation.

If you want, I can also provide example batch scripts for mounting/removing the NAS mapped drive or scheduling backups using this setup.

Would you like that?

<div style="text-align: center">⁂</div>

[^1]: https://www.youtube.com/watch?v=ipZl_iRiYCc

[^2]: https://www.qnap.com/en/how-to/faq/article/two-alternative-methods-to-map-the-shared-folder-as-the-network-drive-in-windows

[^3]: https://www.youtube.com/watch?v=NhPquURIAoI

[^4]: https://support-en.wd.com/app/answers/detailweb/a_id/25436/~/how-to-access-and-map-a-wd-network-drive-on-windows-11-and-windows-10

[^5]: https://www.reddit.com/r/synology/comments/uc0v2x/how_to_access_nas_mapped_as_network_drive_in/

[^6]: https://unr.teamdynamix.com/TDClient/2684/Portal/KB/ArticleDet?ID=116969

[^7]: https://support.microsoft.com/en-us/windows/file-sharing-over-a-network-in-windows-b58704b2-f53a-4b82-7bc1-80f9994725bf

[^8]: https://answers.microsoft.com/en-us/windows/forum/all/map-nas-drive/e91e1b6b-3b5b-4f46-a15c-c4d3d5be5f75

[^9]: https://kb.synology.com/en-au/DSM/tutorial/How_to_map_network_drives_from_your_Synology_NAS

[^10]: https://kb.netgear.com/19864/How-do-I-map-a-network-drive-in-Windows

