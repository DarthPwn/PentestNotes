# MySQL

## Attempt Connection to MySQL

```bash
mysql -h [ip] -u [username] -p [enter password after you click enter]
```

## Metasploit Module to Enumerate Further

```bash
auxiliary/admin/mysql/mysql_sql
```

### Show Version

* this is on by dault

### Show Database \#

```bash
set SQL show databases
```

## Metasploit Module to Dump Database

```bash
auxiliary/scanner/mysql/mysql_schemedump
```

### First: Start MySQL on Attacking Machine

```bash
systemctl mysql start
```

### Second: Run Module on Msfconsole

```bash
set parameters
set payload
run
```

## Metasploit Module to Dump Users and Hashes

```bash
auxiliary/scanner/mysql/mysql_hashdump
```

