# nbtscan

## Overview

* NBTscan is a program for scanning IP networks for NetBIOS name information. It sends NetBIOS status query to each address in supplied range and lists received information in human readable form. For each responded host it lists IP address, NetBIOS computer name, logged-in user name and MAC address \(such as Ethernet\).
* [https://github.com/scallywag/nbtscan](https://github.com/scallywag/nbtscan)
* [http://www.unixwiz.net/tools/nbtscan.html](http://www.unixwiz.net/tools/nbtscan.html)

## Examples

```bash
# Scans the whole C-class network
nbtscan -r 192.168.1.0/24

# Scans a range from 192.168.1.25 to 192.168.1.137                
nbtscan 192.168.1.25-137

# Scans C-class network. Prints results in script-friendly
# format using colon as field separator, like this:
                # 192.168.0.1:NT_SERVER:00U
                # 192.168.0.1:MY_DOMAIN:00G
                # 192.168.0.1:ADMINISTRATOR:03U
                # 192.168.0.2:OTHER_BOX:00U
                # ...
nbtscan -v -s : 192.168.1.0/24
 
# Scans IP addresses specified in file iplist   
nbtscan -f iplist
```



