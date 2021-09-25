# masscan

## Overview

* this tool can scan the whole internet \(not recommended\)
* very fast and efficient
* requires sudo to run its best

## Examples

```bash
# Scan a class B subnet for port 443
masscan 10.11.0.0/16 -p443
 
# Scan a class B subnet for port 80 or 443
masscan 10.11.0.0/16 -p80,443

# Scan a class B subnet for the top 100 ports
masscan 10.11.0.0/16 ‐‐top-ports 100

# --rate is the rate of transmission, -e to specify a raw network interface, 
# and --router-ip for the gateway IP
sudo masscan -p443 10.10.10.0/24 --rate=1000 -e tap0 --router-ip 10.10.10.1
```

