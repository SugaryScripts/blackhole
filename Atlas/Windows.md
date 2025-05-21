[[+ Windows]]
[[balsamiq]]
[[Card/OS/Windows/Browser|Browser]]
[[Powershell]]
[[diskpart]]
Guide
[[download view only videos from sharepoint]]

```sh
# remove dir and its files
rm -r
```


##### Case
###### ZSH on Windows - [[Shell ZSH]]
[Make Windows Terminal Awesome with ZSH and Oh My ZSH! - DEV Community](https://dev.to/pavlosisaris/windows-command-line-revolution-unleash-zsh-and-oh-my-zsh-a-simple-guide-for-developers-271o)

uninstall wsl
[How to Completely Uninstall the Subsystem for Linux WSL on Windows | by bonguides.com | Medium](https://medium.com/@bonguides25/how-to-completely-uninstall-the-subsystem-for-linux-wsl-on-windows-24b0945050a0)

###### Freeze taskbar
[Redirecting](https://answers.microsoft.com/en-us/windows/forum/all/windows-taskbar-frozen/43f24ad0-ae0f-4342-a685-11248fa34435)
1. Make sure you've installed the latest updates for Windows, and then restart your machine. To find out more, read [Update Windows](https://support.microsoft.com/en-us/windows/update-windows-3c5ae7fc-9fb6-9af1-1984-b5e0412c556a).
2. In the search box on the taskbar, type **command prompt**, and right-click or press and hold **Command Prompt (Desktop app)** from the list of results. Select **Run as administrator**, and then select**Yes****.**
3. Type **DISM.exe /Online /Cleanup-image /Restorehealth** (note the space before each "/"), and then press **Enter**. (**Note:** This step may take a few minutes to start and complete.)
4. After you see a message that says "The operation completed successfully," type **sfc** **/scannow** (note the space between "sfc" and "/") and press **Enter**.
5. After you see a message that says, "Verification 100% complete," type **exit** and press **Enter**.