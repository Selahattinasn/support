<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# how to see the network interfaces and their Ip settings with netsh command

To view your network interfaces and their IP settings using the netsh command in Windows, use the following steps and commands:

### 1. Open Command Prompt as Administrator

- Press **Windows + X** and select **Command Prompt (Admin)** or **Windows Terminal (Admin)**.


### 2. Show All Network Interfaces

```cmd
netsh interface show interface
```

This will display a list of all network interfaces (e.g., Ethernet, Wi-Fi, etc.) with their status.

### 3. Display IP Configuration for All Interfaces

```cmd
netsh interface ip show config
```

This command lists detailed IP information (including IP address, subnet mask, gateway, and DNS) for each interface.[^4]

### 4. Show IPv4 Interfaces Only

```cmd
netsh interface ipv4 show interfaces
```

To view just the IPv4 settings for each interface.[^3]

### 5. Show IPv6 Interfaces Only

```cmd
netsh interface ipv6 show interfaces
```

For IPv6 configuration details.[^3]

### 6. Display IP Address for Each Interface

```cmd
netsh interface ip show address
```

This displays the current IP address assigned to each interface.[^7]

***

**Tip:** For a comprehensive summary with all IPs, use `netsh interface ip show config`. For targeted info, use the `show interface` or `show address` commands.

These commands are useful for quick network diagnostics or when scripting administrative tasks.

<div style="text-align: center">⁂</div>

[^1]: https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/netsh

[^2]: https://stackoverflow.com/questions/61918509/using-netsh-to-find-an-interface-name-and-define-it-as-a-variable-in-a-batch-fil

[^3]: https://learn.microsoft.com/de-de/windows-server/networking/technologies/netsh/netsh-contexts

[^4]: https://lizardsystems.com/articles/configuring-network-settings-command-line-using-netsh/

[^5]: https://cyberraiden.wordpress.com/2025/04/20/configure-tcp-settings-for-network-interfaces-in-windows/

[^6]: https://www.serverwatch.com/guides/netsh-commands/

[^7]: https://www.ionos.com/digitalguide/server/tools/netsh/

