# metasploit

## Run db\_nmap and all the Output will be Stored in the Metasploit Database and Available with

```bash
hosts
```

```bash
services
```

## Import Nmap Scans, but Must Output it in XML-Format First

```bash
nmap [ip] -oX result.xml
```

### Additionally, Output them to All Types

```bash
nmap [ip] -oA results
```

### Load it into the Metasploit Database

```bash
db_import /path/to/file.xml
```

## Metasploit Port Scan Modules

```bash
use auxiliary/scanner/portscan
```

## Search for Port Scan Modules

```bash
search portscan
```

```bash
search smb
```

## How to use a Module

```bash
use auxiliary/scanner/portscan/syn
```

