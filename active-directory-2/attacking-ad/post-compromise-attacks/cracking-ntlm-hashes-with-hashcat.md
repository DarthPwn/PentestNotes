# Cracking NTLM Hashes with Hashcat

## NTLM Hashes

* are local hashes within SAM database

## Hashcat

```bash
hashcat -m 1000 hashes.txt /usr/share/wordlists/rockyou.txt
```

* empty passwords is most likely a disabled account

