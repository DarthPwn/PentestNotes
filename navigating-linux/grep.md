# grep

## Search Downloaded Page for Sub Domains

```text
grep -o '[^/]*\.example\.com' index.html | sort -u > list.txt
```

## Get IP from Sub Domains with host and grep Command

```text
for url in $(cat notepad.txt); do host $url; done | grep "has address" | cut -d " " -f 4 | sort -u
```





