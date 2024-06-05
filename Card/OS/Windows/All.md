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
