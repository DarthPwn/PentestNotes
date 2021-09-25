# nmap

## Stealthy \(Default Nmap Scan\)

* SYN, SYN ACK, RST

```bash
nmap -sS [ip]
```

## Scan All Ports \(May Take Awhile\)

```bash
nmap [ip] -p-
```

## Scan for UDP \(Could take Hours\)

* DNS \(53\)
* SNMP \(161, 162\)
* DHCP \(67, 68

```bash
nmap [ip] -sU -T4
```

```bash
unicornscan -mU -v -I [ip]
```

## Scan for Version, with NSE-Scripts and Trying to Identify OS

```bash
nmap [ip] -sV -sC -O
```

## All Out Monster Scan

```bash
nmap -vvv -Pn -A -iL listOfIP.txt
```

## Fast Scan

```bash
nmap [ip] -F
```

## Only Scan the 100 Most Common Ports

```bash
nmap [ip] --top-ports 100
```

## Top 1000 Ports

```bash
-p
```

## All Ports

```bash
-p-
```

## Give Nmap File Input

```bash
 -iL file.txt
```

## "Stealthy" Scan

```bash
-sS
```

* by adding the -sS flag we are telling nmap to not finalize the three way handshake
* it will send a syn, receive syn-ack \(if the port is open\), and then terminate the connection
* not stealthy anymore

## Only Show Open Ports

```bash
nmap --open -p 80 10.10.10.10
```

## Output Scan

### To All Types

```bash
-oA nameOfFile
```

### To Text File

```bash
-oN nameOfFile
```

### To Grepable Format

```bash
-oG nameOfFile
```

### To XML

```bash
-oX nameOfFile
```

## Scan an Entire IP-range

### The -sn Flag Stops Nmap from Running port-scans and Speeds up the Process

* sn could be thought of as a network sweep

```bash
nmap -vvv -sn[ip/24]
```

### Specify a Specific Range

```bash
nmap -sP [ip.0-100]
```

## Sort the Machines that are Up

### So Let's Say 40 Machines Exist in the Range, Grep to Output Those IPs

* find the IPs that were online
* ip-range is the output from previous command \(network sweep\)
* you can of course combine them all

```bash
cat ip-range.txt | grep -B 1 "Host is up"
```

### Sort Out the IPs from the File

```bash
grep -o '[0-9]\{1,3\}\.[0-9]\{1,3\}\.[0-9]\{1,3\}\.[0-9]\{1,3\}' ip-range.txt > only-ip.txt
```

* Input all those IPs to Nmap and Scan Them

## Nmap One Liner Example

```bash
for ip in $(cat upIps); do nmap $ip & done
```

