# LinkedIn

## linkedin2username

* [https://github.com/initstring/linkedin2username](https://github.com/initstring/linkedin2username)
* This is a pure web-scraper, no API key required. You use your valid LinkedIn username and password to login, it will create several lists of possible username formats for all employees of a company you point it at.

```bash
#Here's an example to pull all employees of Uber:
python linkedin2username.py myname@email.com uber-com

#Here's an example to pull a shorter list and 
#append the domain name @uber.com to them:
python linkedin2username.py myname@email.com uber-com -d 5 -n 'uber.com'
```

