# tr

## Overview

* translates and manipulates text

## Transform All Letters into CAPS

```bash
tr "[:lower:]" "[:upper:]" < fileinput > fileoutput
```

## Remove Characters, for Example the "."

```bash
cat file.txt | tr -d "."
```

## Remove All Dots and Replace Them With an Underscore

```bash
cat file.txt | tr "." "_"
```

