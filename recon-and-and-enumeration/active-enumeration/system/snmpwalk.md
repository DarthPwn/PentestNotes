# snmpwalk

## Overview

* query SNMP values, if the SNMP read-only community string is known, which is usually "public"

## Enumerate the Whole MIB Tree

```bash
# -c : defines community string
# -v : defines snmp version
# -t : timeout period in seconds
# community_string is usually "public"
snmpwalk -c community_string -v1 -t 9 10.10.10.10
```

## Enumerate Users on Windows

```bash
# community_string is usually "public"
snmpwalk -c community_string -v1 10.10.10.10 1.3.6.1.4.1.77.1.2.25
```

## Enumerate Running Processes on Windows

```bash
# community_string is usually "public"
snmpwalk -c community_string -v1 10.10.10.10 1.3.6.1.2.1.25.4.2.1.2
```

## Enumerate Open TCP Ports

```bash
# community_string is usually "public"
snmpwalk -c community_string -v1 10.10.10.10 1.3.6.1.2.1.6.13.1.3
```

## Enumerate Installed Software

```bash
# community_string is usually "public"
snmpwalk -c community_string -v1 10.10.10.10 1.3.6.1.2.1.25.6.3.1.2
```

## SNMP Bruteforcing

* using hydra

```bash
hydra -P wordlist.txt -v 102.168.0.101 snmp
```

* using onesixtyone

```bash
onesixtyone -c community_strings_mib -i ip_list.txt
```

* [https://github.com/danielmiessler/SecLists/blob/master/Discovery/SNMP/common-snmp-community-strings.txt](https://github.com/danielmiessler/SecLists/blob/master/Discovery/SNMP/common-snmp-community-strings.txt)

