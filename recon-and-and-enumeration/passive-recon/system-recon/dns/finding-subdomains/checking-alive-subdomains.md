# Checking Alive Subdomains

## Link and Download

* [https://github.com/tomnomnom/httprobe](https://github.com/tomnomnom/httprobe)
* go get -u github.com/tomnomnom/httprobe@master

## Use it with a Text File

```bash
cat subdomains.txt | httprobe
```

## Help Remove False Positives

```bash
cat subdomains.txt | httprobe -s
```

## Strip off the HTTPS at the End so it can be Scanned with Nmap

```bash
cat subdomains.txt | httprobe -s -p https:443 | sed 's/https?:\/\///' | tr -d ':443'
```

