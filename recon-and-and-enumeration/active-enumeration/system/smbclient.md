# smbclient

## Overview

* often used to check anonymous login

## Get Share Names and Attempt Anonymous Login to the Main Share Folder

```bash
smbclient -L \\\\[ip]
```

## Attempt Connection with Anonymous Login with a Specific Share

```bash
smbclient \\\\[ip]\\SHARENAME
```

## Anonymous Login as a Specific User and Default Port

```bash
smbclient \\\\[ip]\\SHARENAME -u username -p 445
```

