# systemctl && service

## Overview

* edits the services running on Linux

## systemctl

### **enable and disable various services on Linux \(turn off on reboot\)**

```bash
systemctl start ssh
```

```bash
system status ssh
```

```bash
systemctl stop ssh
```

### **make services start on boot**

```bash
systemctl enable ssh
```

```bash
systemctl enable apache2
```

## service

### **start services**

```bash
service apache2 start
```

```bash
service ssh start
```

```bash
service postgresql start
```

### **stop services**

```bash
service apache2 stop
```

```bash
service ssh stop
```

```bash
service postgresql stop
```

