# Information Gathering

## Overview


## Tools

### DNS Analysis
* DNS Map
```
dnsmap [url]
dnsmap [url] -r [output directory]
```
_Example_
```
oaitran@kali:~$ dnsmap google.com
dnsmap 0.30 - DNS Network Mapper by pagvac (gnucitizen.org)

[+] searching (sub)domains for google.com using built-in wordlist
[+] using maximum random delay of 10 millisecond(s) between requests

accounts.google.com
IPv6 address #1: 2404:6800:4005:802::200d

accounts.google.com
IP address #1: 216.58.199.13

admin.google.com
IPv6 address #1: 2404:6800:4008:c07::66

admin.google.com
IP address #1: 216.58.199.14

ai.google.com
IPv6 address #1: 2404:6800:4005:802::200e

```
* DNS Enum
```
dnsenum [Url]
```
_Example_
```
oaitran@kali:~$ dnsenum google.com 
Smartmatch is experimental at /usr/bin/dnsenum line 698.
Smartmatch is experimental at /usr/bin/dnsenum line 698.
dnsenum VERSION:1.2.4

-----   google.com   -----


Host's addresses:
__________________

google.com.                              212      IN    A        216.58.199.14


Name Servers:
______________

ns2.google.com.                          10870    IN    A        216.239.34.10
ns1.google.com.                          17697    IN    A        216.239.32.10
ns3.google.com.                          17697    IN    A        216.239.36.10
ns4.google.com.                          21595    IN    A        216.239.38.10
```
### Network and port scanner
* nmap

* 
