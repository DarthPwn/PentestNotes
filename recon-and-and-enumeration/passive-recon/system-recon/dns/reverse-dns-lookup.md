# Reverse DNS-Lookup

## If IP Range is Known, You Can See Which Machines are Online and Find the Domain Addresses. Put the IPs into a TXT File and Run a Script

```bash
#!/bin/bash/
while read p; do
    echo $p;
    host $p;
done < IPOnlyFile.txt
```

## More Tools that can do DNS Lookup

* [https://www.cyberciti.biz/faq/how-to-test-or-check-reverse-dns/](https://www.cyberciti.biz/faq/how-to-test-or-check-reverse-dns/)

