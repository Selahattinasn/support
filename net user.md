<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# can sou also provide a comprehensive guide for "net user" command please with examle commands. thats is for daily system administration topics

Here is a comprehensive guide to the Windows **net user** command, designed for daily system administration tasks, including detailed explanations and example commands.

***

## Overview of net user Command

The **net user** command is a command-line utility built into Windows that allows administrators to manage local (and domain) user accounts. It can:

- List all user accounts on a system.
- Create new user accounts.
- Modify existing accounts (passwords, status, group memberships).
- Enable or disable user accounts.
- Set account properties such as passwords, expiration dates, logon hours, home directories.
- Delete user accounts.

You must run the command prompt or PowerShell as an **Administrator** to perform most user management tasks.

***

## Syntax

```
net user [<UserName> {<Password> | *} [<Options>]] [/domain]
net user [<UserName> [/delete] [/domain]]
net user [/help]
```

- **UserName**: The user account name.
- **Password**: Set or change the password. Use `*` to get a prompt to enter the password securely.
- **/add**: Add a new user account.
- **/delete**: Delete a user account.
- **/active:{yes|no}**: Enable or disable a user.
- **/expire:<date>**: Set account expiration (dates like `MM/DD/YYYY` or `never`).
- **/times:<times>**: Restrict logon hours.
- **/homedir:<path>**: Set user’s home directory.
- **/fullname:"<Full Name>"**: Set the user's full name.
- **/passwordchg:{yes|no}**: Allow or disallow the user to change their password.
- **/passwordreq:{yes|no}**: Require or not require a password.

***

## Common Use Cases and Example Commands

### 1. List All User Accounts on the Local Machine

```cmd
net user
```

Lists all local users on the computer.

***

### 2. View Detailed Information About a Specific User

```cmd
net user username
```

Example:

```cmd
net user JohnDoe
```

Shows detailed account info like last logon, groups, password settings.

***

### 3. Create a New User Account

```cmd
net user NewUserName NewPassword /add
```

Example:

```cmd
net user alice P@ssw0rd /add
```

Creates user "alice" with the password "P@ssw0rd".

***

### 4. Create a New User and Specify Additional Options

```cmd
net user jays Cyk4^g3B /add /fullname:"Jay Jamison" /passwordreq:yes /active:yes /times:M-F,08:00-17:00
```

- Full name: Jay Jamison
- Password required and set
- Active account
- Can log in Monday to Friday, 8 AM to 5 PM

***

### 5. Set or Change a User's Password (Prompt for Password)

```cmd
net user username *
```

Example:

```cmd
net user alice *
```

You will be prompted to enter and confirm a new password securely.

***

### 6. Disable a User Account

```cmd
net user username /active:no
```

Example:

```cmd
net user alice /active:no
```

This disables the "alice" user account.

***

### 7. Enable a User Account

```cmd
net user username /active:yes
```

Example:

```cmd
net user alice /active:yes
```


***

### 8. Delete a User Account

```cmd
net user username /delete
```

Example:

```cmd
net user alice /delete
```

Deletes the "alice" user.

***

### 9. Set Account Expiration Date

```cmd
net user username /expire:MM/DD/YYYY
```

Example:

```cmd
net user alice /expire:12/31/2025
```

Account "alice" expires December 31, 2025.

***

### 10. Restrict Logon Hours

```cmd
net user username /times:<days,hours>
```

Example (logon allowed Monday-Friday 8 AM to 5 PM):

```cmd
net user alice /times:M-F,08:00-17:00
```

Multiple time blocks can be separated by semicolons.

***

### 11. Set User’s Home Directory

```cmd
net user username /homedir:\\server\share\folder
```

Example:

```cmd
net user alice /homedir:\\fileserver\users\alice
```


***

### 12. Prevent User from Changing Password

```cmd
net user username /passwordchg:no
```

Example:

```cmd
net user alice /passwordchg:no
```


***

### 13. Require or Remove Password Requirement

```cmd
net user username /passwordreq:yes
```

or

```cmd
net user username /passwordreq:no
```


***

## Summary Table of Key net user Commands

| Task | Command Example |
| :-- | :-- |
| List all users | `net user` |
| View user details | `net user username` |
| Add new user | `net user alice P@ssw0rd /add` |
| Add user with options | `net user jays Cyk4^g3B /add /fullname:"Jay Jamison"` |
| Change user password | `net user alice *` (prompts for input) |
| Disable user | `net user alice /active:no` |
| Enable user | `net user alice /active:yes` |
| Delete user | `net user alice /delete` |
| Set account expiration | `net user alice /expire:12/31/2025` |
| Restrict logon hours | `net user alice /times:M-F,08:00-17:00` |
| Set home directory | `net user alice /homedir:\\fileserver\users\alice` |
| Prevent password change | `net user alice /passwordchg:no` |
| Set password requirement | `net user alice /passwordreq:yes` |


***

This command provides powerful control for user management directly from the command line and is essential for scripting and bulk administrative tasks.

If you want, I can also provide some sample batch scripts for common user management workflows.

***

Would you like example scripts or further advanced usage details?

<div style="text-align: center">⁂</div>

[^1]: https://www.minitool.com/news/net-user-command.html

[^2]: https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/net-user

[^3]: https://en.wikiversity.org/wiki/Net_(command)/User

[^4]: https://lazyadmin.nl/it/net-user-command/

[^5]: https://www.lifewire.com/net-user-command-2618097

[^6]: https://www.linkedin.com/pulse/20-net-user-commands-you-can-use-troubleshoot-users-active-decelles

[^7]: https://thedxt.ca/2024/11/net-user-and-net-group/

[^8]: https://infrasos.com/net-user-command-manage-local-windows-users-accounts/

[^9]: https://www.youtube.com/watch?v=XeY5reQ0wSw

