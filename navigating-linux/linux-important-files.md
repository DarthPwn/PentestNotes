# Linux Important Files

## Useful User Information

```bash
user/passwd
```

## User Password Hashes

```bash
/etc/shadow (Unshadowing tool + JohntheRipper or Hashcat)
```

## Important Log Files

```bash
/var/logs (failed sudo goes here)
```

## Sudo Config File

* used to control the sudo permissions of every user on the system

```bash
/etc/sudoers
```

### **Certain Machines You Cannot Edit Sudoers File Without an Interactive Shell. Here is a Workaround**

```bash
echo "username ALL=(ALL) ALL" >> /etc/sudoers
```

## All Processes Stored in Proc

```bash
/proc/[pid]
```

## Place to Install Custom Tools from Github etc.

```bash
/opt
```

## Basic Programs

* ls, cd, cat, etc

```bash
/bin
```

## System Programs

* fdisk, mkfs, sysctl, etc

```bash
/sbin
```

## Configuration Files

```bash
/etc
```

## Temp Files

* usually deleted on reboot

```bash
/tmp
```

## Applications

* apt, ncat, nmap, etc

```bash
/usr/bin
```

## Application Support and Data Files

```bash
/usr/share
```

