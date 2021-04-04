# sudo

## Overview

* runs commands as super user

## List the Rights of the Sudo User

```bash
sudo -l
```

## Sudo Config File

```bash
/etc/sudoers
```

## Some Machines Cannot Edit sudoers File Due to a Non-Interactive Shell. Here is a Workaround

```bash
echo "username ALL=(ALL) ALL" >> /etc/sudoers
```

## Check Which Users are in Sudo Group

```bash
cat /etc/group/ | grep sudo
```

## Runs Commands as Specified User

```bash
sudo -u username /bin/bash
```

## Trick to Get Root Without Password \(Not Always\)

```bash
sudo su -
```

