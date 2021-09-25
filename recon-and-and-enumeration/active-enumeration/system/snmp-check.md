# snmp-check

## Overview

* Like to snmpwalk, snmp-check allows you to enumerate the SNMP devices and places the output in a very human readable friendly format. It could be useful for penetration testing or systems monitoring. Distributed under GPL license and based on “Athena-2k” script by jshaw.
* [https://tools.kali.org/information-gathering/snmp-check](https://tools.kali.org/information-gathering/snmp-check)

## Examples

```bash
# Help/Manual Page
snmp-check -h

 Usage: snmp-check [OPTIONS] <target IP address>

  -p --port        : SNMP port. Default port is 161;
  -c --community   : SNMP community. Default is public;
  -v --version     : SNMP version (1,2c). Default is 1;

  -w --write       : detect write access (separate action by enumeration);

  -d --disable_tcp : disable TCP connections enumeration!
  -t --timeout     : timeout in seconds. Default is 5;
  -r --retries     : request retries. Default is 1;
  -i --info        : show script version;
  -h --help        : show help menu;
  
 # Specific Example
 snmp-check 192.168.1.2 -c public # where public is the known community string
```

