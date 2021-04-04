# iptables

## Overview

* firewall tool for Linux
* scans incoming and outgoing traffic
* you can add rules or remove rules/filters

## View Active Rules

```bash
iptables -L
```

## View Active Rules with Line Numbers

```bash
iptables -L -v --line-numbers
```

## Return iptables to Default Settings \(Accepts all Connections\)

```bash
iptables --policy INPUT ACCEPT
iptables --policy OUTPUT ACCEPT
iptables --policy FORWARD ACCEPT

#or put "DROP" for "ACCEPT" to forbid all traffic
```

## Block Connection from a Single IP

```bash
#A is for Append
#S is for Source

iptables -A INPUT -s <ip> -j DROP
```

## Block Connections from an Entire Range

```bash
#A is for Append
#S is for Source

iptables -A INPUT -s <ip/24> -j DROP
```

## Block Outgoing Connections

```bash
#A is for Append
#S is for Source

iptables -A OUTPUT -d <ip> -j DROP
```

## Remove One Rule

```bash
iptables -D INPUT 2
```

## Remove All Rules

```bash
iptables -F
```

## Changes Reset After Reboot Unless Saved

```bash
sudo /sbin/iptables-save/
```

