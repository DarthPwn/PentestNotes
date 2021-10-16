# PowerView Overview

## GitHub Link

* [https://github.com/PowerShellMafia/PowerSploit](https://github.com/PowerShellMafia/PowerSploit) (deprecated)
* [https://github.com/PowerShellMafia/PowerSploit/blob/master/Recon/PowerView.ps1](https://github.com/PowerShellMafia/PowerSploit/blob/master/Recon/PowerView.ps1) (or download this)
* part of Empire

## How to Upload It

* it needs to be on target machine
* use the many methods to get the file on the victim machine

## Bypassing AV Tips

* Remove the Comments at the Top of the Script

## Usage

### Step 1: Navigate to Folder where PowerView is and Execute Command

```bash
powershell -ep bypass
```

### Step 2: Run the Script with These Two Options

```bash
powershell .\script.ps1
. .\script.ps1
```

### Step 3: Run Powerview Commands

```bash
Get-NetDomain (view forest)
Get-NetDomainController (get DC ip, etc)
Get-DomainPolicy OR (Get-DomainPolicy)."system access"
Get-NetUser OR Get-NetUser | select/description
Get-UserProperty OR Get-UserProperty -Properties pwdlastset/logoncount/badpwdcount
Get-NetComputer -FullData
Get-NetGroup -GroupName *admin*/"Domain Admin"
Invoke-ShareFinder
Get-NetGPO | select displayname, whenchanged
```

## PowerView Cheat Sheet

* [https://gist.github.com/HarmJ0y/184f9822b195c52dd50c379ed3117993](https://gist.github.com/HarmJ0y/184f9822b195c52dd50c379ed3117993)
