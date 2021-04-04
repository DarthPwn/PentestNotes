# Execution Cmd's

## Overview

* various commands to check/set execution policies

## Checks Current Execution Policy for cmdlets \(Powershell Scripts\)

```text
Get-ExecutionPolicy
```

## Set Execution Policy

```text
set-ExecutionPolicy "unrestricted"
```

## Types of Execution Policies

### **restricted**

* Powershell will not run scripts

### **assigned**

* only run scripts that are digitally signed
* if it has a publisher it has not seen before, it will ask if you trust the publisher

### remotesigned

* will not run scripts downloaded from the internet unless it has a digital signature
* Powershell will ask if you if you trust the publisher

### unrestricted

* ignores the digital signature but still asks if you trust the script before running from the internet

