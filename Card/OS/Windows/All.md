# Power Shell
## Enable execution
Run the command below with administrator. For running script like yarn and npm.
```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted
```
alt
```powershell
Get-ExecutionPolicy
Set-ExecutionPolicy RemoteSigned
```
### Execution policy
- **Restricted**: This is the default policy and prevents running any scripts. You can still use PowerShell for individual commands but cannot execute scripts.
- **AllSigned**: This policy allows you to run scripts that have been digitally signed by a trusted publisher. Any unsigned scripts will not be executed.
- **RemoteSigned**: This policy enables you to run locally-created scripts, while scripts downloaded from the internet must be signed by a trusted publisher to execute.
- **Unrestricted**: This policy permits the execution of all scripts, regardless of their origin or whether they are signed. This setting may pose security risks, so use it with caution.

## Power shell latest version
url:: [Installing PowerShell on Windows - PowerShell | Microsoft Learn](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.4#winget)
```powershell
winget search Microsoft.PowerShell
winget install --id Microsoft.Powershell --source
winget winget install --id Microsoft.Powershell.Preview --source winget
winget list --name PowerShell --upgrade-available
```
## Location Picture Default Windows Wallpaper
```
C:\Windows\Web\Screen
```

# Startup
To create an autorun script on Windows that opens Notepad (or any other program) when Windows starts, you can follow these steps:

### Method 1: Using the Startup Folder

1. **Open the Startup Folder**:
   - Press `Win + R` to open the Run dialog.
   - Type `shell:startup` and press Enter. This opens the Startup folder.

2. **Create a Shortcut**:
   - Right-click inside the Startup folder and select `New` > `Shortcut`.
   - In the "Type the location of the item" field, enter the path to Notepad. For Notepad, you can enter:
     ```
     C:\Windows\System32\notepad.exe
     ```
   - Click `Next`, then give the shortcut a name (e.g., `Open Notepad`), and click `Finish`.

3. **Verify**:
   - Restart your computer to test if Notepad opens automatically.

### Method 2: Using Task Scheduler

1. **Open Task Scheduler**:
   - Press `Win + R`, type `taskschd.msc`, and press Enter.

2. **Create a New Task**:
   - In the Task Scheduler window, click `Create Basic Task` in the Actions pane on the right.

3. **Configure the Task**:
   - **Name**: Give your task a name, like `Open Notepad`.
   - **Trigger**: Choose `When the computer starts`, then click `Next`.
   - **Action**: Choose `Start a program`, then click `Next`.
   - **Program/Script**: Enter the path to Notepad:
     ```
     C:\Windows\System32\notepad.exe
     ```
   - Click `Next`, review the settings, and click `Finish`.

4. **Verify**:
   - Restart your computer to check if Notepad opens automatically.

### Method 3: Using Windows Registry (Advanced)

**Warning**: Editing the registry can affect system stability. Be cautious and consider backing up the registry before making changes.

1. **Open Registry Editor**:
   - Press `Win + R`, type `regedit`, and press Enter.

2. **Navigate to the Startup Path**:
   - Go to `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run`.

3. **Add a New String Value**:
   - Right-click in the right pane, select `New` > `String Value`.
   - Name the new value (e.g., `Open Notepad`).

4. **Set the Value Data**:
   - Double-click the new string value.
   - In the "Value data" field, enter the path to Notepad:
     ```
     C:\Windows\System32\notepad.exe
     ```
   - Click `OK` and close the Registry Editor.

5. **Verify**:
   - Restart your computer to ensure Notepad opens automatically.

Using the Startup folder or Task Scheduler is generally safer and more user-friendly for most tasks, while editing the registry should be a last resort or for advanced users.