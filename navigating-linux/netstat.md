# netstat

## Overview

* view open ports and what they can call out to
* you may not see every PID if you are not root

## Examples

```bash
netstat -ano
```

```bash
netstat -anpt
```

```bash
#all
-a
#show numeric addresses
-n
#show port
-p
#TCP
-t
```

## Provides Important Info with a Good Layout

```bash
netstat -tulpn
```

