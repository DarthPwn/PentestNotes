# AD DS Sensitive Files

## Ntds.dit

* contains everything that is stored in Active Directory Data

```bash
users
objects
groups
password hashes (cracking, pass the hash, golden ticket attacks)
```

* stored here by default

```bash
%SystemRoot%\NTDS folder on all domain controllers
```

* can only be accessed through domain process and protocols

