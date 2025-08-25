<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# what was the shutdown kommands in windows

The primary command to shut down Windows from the command line is **shutdown.exe** with various parameters, such as **/s** for shutdown, **/r** for restart, **/l** for log off, and more.[^1][^2][^3]

## Common Windows Shutdown Commands

- **shutdown /s**
Shuts down the computer gracefully.[^2][^3][^4]
- **shutdown /r**
Restarts the computer instead of shutting down.[^3][^5]
- **shutdown /l**
Logs off the current user session without shutting down.[^5][^3]
- **shutdown /a**
Aborts a shutdown or restart that is already in progress.[^4][^3][^5]
- **shutdown /f**
Forces applications to close without warning the user (useful if system is stuck).[^3][^4][^5]
- **shutdown /t [seconds]**
Sets a delay (in seconds) before shutdown or restart; for example, "shutdown /s /t 60" shuts down in 60 seconds.[^4][^5][^3]
- **shutdown /p**
Turns off the computer without waiting for any timeout or warning (immediate power-off).[^6]


## Examples

- Immediate shutdown:
`shutdown /s /t 0`[^3][^4]
- Restart in 5 minutes:
`shutdown /r /t 300`[^3]
- Log off:
`shutdown /l`[^3]
- Abort a scheduled shutdown:
`shutdown /a`[^4]

These commands can be run from Command Prompt or PowerShell. They are useful for automating shutdown processes, scripting, and remote management of Windows computers.[^2][^5][^3]
<span style="display:none">[^10][^7][^8][^9]</span>

<div style="text-align: center">⁂</div>

[^1]: https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/shutdown

[^2]: https://woshub.com/shutdown-restart-windows-cmd/

[^3]: https://www.winfr.org/docs/winfr-cmd/windows-shutdown-command.html

[^4]: https://www.ionos.com/digitalguide/server/configuration/shutdown-commands-via-cmd/

[^5]: https://www.accuwebhosting.com/discussion/forum/peer-support/how-to-s/windows-vps/35800-shutdown-commands-for-windows

[^6]: https://www.windowscentral.com/how-use-shutdown-command-tool-windows-10

[^7]: https://learn.microsoft.com/de-de/windows-server/administration/windows-commands/shutdown

[^8]: https://www.reddit.com/r/windows/comments/yflhjq/is_there_a_difference_between_shutdown_s_and/

[^9]: https://praxistipps.chip.de/shutdown-per-cmd-die-wichtigsten-befehle_51207

[^10]: https://help.hawken.edu/portal/en/kb/articles/shut-down-or-restart-windows-10-devices

