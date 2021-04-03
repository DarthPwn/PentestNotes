# Bloodhound Overview

## Overview

* downloads AD data once we are on a machine/within the network and puts it into a graph

## Install and Setup

### Bloodhound \(Attacking Machine\)

```bash
apt install bloodhound
sudo neo4j console
```

```bash
bloodhound #(in a seperate window terminal)
```

* connect to the local URL it gives you \(default user:pass is “neo4j”\)
* sign into the website

### Invoke-Bloodhound \(Victim Machine\)

* [https://github.com/puckiestyle/powershell](https://github.com/puckiestyle/powershell)[https://github.com/puckiestyle/powershell/blob/master/SharpHound.ps1](https://github.com/puckiestyle/powershell/blob/master/SharpHound.ps1)
* put the file on the machine

## Running Bloodhound \(Victim Machine\)

```bash
powershell -ep bypass
. .\SharpHound.ps1
Invoke-BloodHound -CollectionMethod All -Domain MARVEL.local -ZipFileName file.zip
```

* move zip from victim to attacker machine

## Importing and Viewing Data

```bash
sudo neoj4 console
bloodhound #(sign into the website panel)
```

* upload zip file
* click little hamburger
* “Analysis” has awesome built in queries

## Resources

* [https://hunter2.gitbook.io/darthsidious/enumeration/bloodhound](https://hunter2.gitbook.io/darthsidious/enumeration/bloodhound)
* [https://www.ired.team/offensive-security-experiments/active-directory-kerberos-abuse/abusing-active-directory-with-bloodhound-on-kali-linux](https://www.ired.team/offensive-security-experiments/active-directory-kerberos-abuse/abusing-active-directory-with-bloodhound-on-kali-linux)

