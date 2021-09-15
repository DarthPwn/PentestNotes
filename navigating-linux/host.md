# host

## Find an IP of Host

```text
host example.com
```

## One Liner to Extract Sub Domain IPs that are Saved in a List

```text
for url in $(cat list.txt); do host $url; done | grep "has address" | cut -d " " -f 4 | sort -u
```



