# Hidden Files && Directories

## Dirb

### Example

```bash
dirb http://example.com
```

### Avoid WAFs

* it may show a 403 error instead of the expected 404
* this could indicate a WAF
* simple to avoid sometimes, just change the request header

```bash
dirb http://example.com -a "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/51.0.2704.106 Safari/537.36"
```

## OWASP ZAP

* insert your target
* add it to the context
* click the "+" sign
* click on forced browse

## WFuzz

```bash
wfuzz -c -z file,/root/.ZAP/fuzzers/dirbuster/directory-list-2.3-big.txt --sc 200 http://pegasus.dev:8080/FUZZ.php
```

## GoBuster

### Remove Irrelevant Response Codes

```bash
gobuster -u http://[ip] -w /usr/share/seclists/Discovery/Web_Content/common.txt -s '200,204,301,302,307,403,500' -e
```

## DirBuster

```bash
dirbuster&
```

### Built in Lists

```bash
/usr/share/wordlists/dirbuster
```

### Useful File Extensions

```bash
php, txt, zip, rar, pdf, docx
```

## DirDar

* [https://github.com/M4DM0e/DirDar](https://github.com/M4DM0e/DirDar)
* can brute-force forbidden directories \(403\)

