# cut && tr

## Overview

* cut && tr are useful commands to extract output
* translates or delete characters
* supports a range of transformations including uppercase to lowercase, remove repeating characters, deleted specific characters, and basic find and repacle

## Example from TheCyberMentor

```bash
ifconfig | grep "64 bytes" | cut -d " " -f 4 | tr -d ":"
```

