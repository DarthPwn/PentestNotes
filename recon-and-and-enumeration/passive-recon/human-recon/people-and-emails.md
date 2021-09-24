# People and Emails Overview

## OSINT Framework

* an awesome list of tools for OSINT
* [https://osintframework.com/](https://osintframework.com/)

## Find People Using the Following Sources

* company website
* social media
* forums
* newsgroups
* metadata from documents
* company website
* blogs might have employees writing blogposts under their name
* spider it with burp and then search the result

## Tool that Searches Online Accounts

* [Profil3r](https://github.com/Rog3rSm1th/Profil3r)

## Social Media Dorks

```bash
site:twitter.com companyname
```

```bash
site:linkedin.com companyname
```

```bash
site:facebook.com companyname
```

## Email Harvesting

```bash
theHarvester -d [example.com](http://example.com/) -l 500 -b all
```

### [hunter.io](http://hunter.io/)

* great website for finding emails

## User Profiles Search

* [social-searcher.com](http://social-searcher.com/)

## Metadata From Documents

* find some documents and then run exiftool on them to see if there is any interesting metadata

```bash
site:example.com filetype:pdf
```

