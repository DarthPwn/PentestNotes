# recon-ng

## Overview

* full-featured web recon framework written in Python
* same basic structure as Metasploit

## Find Subdomains

```bash
recon-ng
use use recon/domains-host/
show options #shows vast amount of alternatives
set source website.com #all subdomains will be saved in "hosts"
show hosts #which you can use with
```

## Resolve IPs of Subdomains if Not Automatic

```bash
use recon/hosts-hosts/resolve
run #resolve all hosts in the host file
```

## Download Other Modules for recon-ng

```bash
###Search Modules
marketplace search example

###More Info about Modules
marketplace info example

###Install the module
marketplace install recon/path/to/the/module

###Use the downloaded module
module load recon/path/to/the/module

###Display details about the module and the required parameters
info #after module is loaded, different from "marketplace info"

###Set required parameters in module
options set VALUE example_parameter

###Run the module
run

###Exit the module and go back to the main menu
back

###Show different databases
show
show hosts

###For example, one module can save data into "HOSTS" db, like example.com
###Another module can then use it for its own purpose 
```

