# Installing GoLang for Tools

## Overview

* GoLang is becoming extremely popular
* used for multiple tools

## How to Install

```bash
sudo apt-get install -y goland
#use this after the above command to add text into the .bashrc (LINUX USES NEW SHELL)
sudo gedit .bashrc
#this is the text to add into .bashrc
export.GOROOT=/usr/local/go
export.GOPATH=$HOME/go
export.PATH=$GOPATH/bin:$GOROOT/bin:$PATH
#finally run this command, remember Linux has different shell now
source .bashrc
```

