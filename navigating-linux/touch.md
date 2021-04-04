# touch

## Overview

* changes timestamps or creates empty files

## Change Access Time Only

```bash
touch -a filename
```

## Change Modify Time Only

```bash
touch -m filename
```

## Change Access and Modify Time

```bash
touch -am filename
```

## Changes Date to Given Time

```bash
touch -d '1 May 2005 10:22' filename
```

### **automatically sets time to 0:00**

```bash
touch -d '14 May' filename
```

### **automatically sets date to current date**

```bash
touch -d '14:24' filename
```

## Creates an Empty File

```bash
touch filename
```

