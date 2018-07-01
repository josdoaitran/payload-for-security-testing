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
* DNS Recon
```
  dnsrecon -t std -d  [url]
  dnsrecon -t axfr -d [url]
  dnsrecon -t tld -d [url]
```
_Example_
```
oaitran@kali:~$ dnsrecon -t std -d google.com
[*] Performing General Enumeration of Domain: google.com
[*] Checking for Zone Transfer for google.com name servers
[*] Resolving SOA Record
[+] 	 SOA ns1.google.com 216.239.32.10
[*] Resolving NS Records
[*] NS Servers found:
[*] 	NS ns1.google.com 216.239.32.10
[*] 	NS ns1.google.com 2001:4860:4802:32::a
[*] 	NS ns3.google.com 216.239.36.10
[*] 	NS ns3.google.com 2001:4860:4802:36::a
[*] 	NS ns4.google.com 216.239.38.10
[*] 	NS ns4.google.com 2001:4860:4802:38::a
[*] 	NS ns2.google.com 216.239.34.10
[*] 	NS ns2.google.com 2001:4860:4802:34::a
[*] Removing any duplicate NS server IP Addresses...
[*] ...  
```
* WhatWeb
```
  whatweb [url]
```
_Example_ 
```
oaitran@kali:~$ whatweb google.com
http://google.com [301 Moved Permanently] Country[UNITED STATES][US], HTTPServer[gws], IP[216.58.199.14], RedirectLocation[http://www.google.com/], Title[301 Moved], X-Frame-Options[SAMEORIGIN], X-XSS-Protection[1; mode=block]
http://www.google.com/ [200 OK] Cookies[1P_JAR,NID], Country[UNITED STATES][US], HTML5, HTTPServer[gws], HttpOnly[NID], IP[216.58.199.4], Script, Title[Google], X-Frame-Options[SAMEORIGIN], X-XSS-Protection[1; mode=block]

```
* dig
```
dig [url]
```
_Example_
```
oaitran@kali:~$ dig facebook.com

; <<>> DiG 9.10.6-Debian <<>> facebook.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 47981
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4000
;; QUESTION SECTION:
;facebook.com.			IN	A

;; ANSWER SECTION:
facebook.com.		266	IN	A	157.240.13.35

;; Query time: 42 msec
;; SERVER: 192.168.1.12#53(192.168.1.12)
;; WHEN: Sun Jul 01 11:15:43 +07 2018
;; MSG SIZE  rcvd: 57
```

* urlcrazy
``` 
urlcrazy [url]
```
_Example_
```
oaitran@kali:~$ urlcrazy google.com
/usr/share/urlcrazy/tld.rb:81: warning: key "2nd_level_registration" is duplicated and overwritten on line 81
/usr/share/urlcrazy/tld.rb:89: warning: key "2nd_level_registration" is duplicated and overwritten on line 89
/usr/share/urlcrazy/tld.rb:91: warning: key "2nd_level_registration" is duplicated and overwritten on line 91
URLCrazy Domain Report
Domain    : google.com
Keyboard  : qwerty
At        : 2018-07-01 12:18:40 +0700

# Please wait. 87 hostnames to process

Typo Type                     Typo           DNS-A            CC-A              DNS-MX                                Extn  
----------------------------------------------------------------------------------------------------------------------------
Character Omission            gogle.com      172.217.161.164  US,UNITED STATES                                        com   
Character Omission            googe.com      162.243.10.151                                                           com   
Character Omission            googl.com      172.217.161.164  US,UNITED STATES                                        com   
Character Omission            google.cm      172.217.161.163  US,UNITED STATES  aspmx.l.google.com                    cm    
Character Omission            goole.com      87.106.83.127    DE,GERMANY        mx01.1and1.co.uk                      com   
Character Repeat              ggoogle.com    172.217.161.164  ��,                                                     com   
Character Repeat              googgle.com                     ?                                                       com   
Character Repeat              googlee.com    172.217.161.164  US,UNITED STATES                                        com   
Character Repeat              googlle.com    54.221.207.100   US,UNITED STATES  mx94.mb1p.com                         c
```

* Matasploit
``` 
msfconsole
msf> whois bdtime.com
```
_Example_
```
msf > whois bdtime.com
[*] exec: whois bdtime.com

   Domain Name: BDTIME.COM
   Registry Domain ID: 1839746399_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.namebright.com
   Registrar URL: http://www.NameBright.com
   Updated Date: 2017-12-20T08:38:02Z
   Creation Date: 2013-12-19T19:01:54Z
   Registry Expiry Date: 2018-12-19T19:01:54Z
   Registrar: EchoDomain LLC

```
Try to exploit:
```
nslookup url
nmap -sS -Pn Public IP -vv
```
_Example_
```
msf > nslookup bdtimes.com
[*] exec: nslookup bdtimes.com

Server:		192.168.1.12
Address:	192.168.1.12#53

Non-authoritative answer:
Name:	bdtimes.com
Address: 66.198.240.42
msf > sudo nmap -sS -Pn 66.198.240.42 -vv
[*] exec: sudo nmap -sS -Pn 66.198.240.42 -vv

[sudo] password for doaitran: 

Starting Nmap 7.60 ( https://nmap.org ) at 2018-07-01 12:47 +07
Initiating Parallel DNS resolution of 1 host. at 12:47
Completed Parallel DNS resolution of 1 host. at 12:47, 0.04s elapsed
Initiating SYN Stealth Scan at 12:47
Scanning a2ss51.a2hosting.com (66.198.240.42) [1000 ports]
Discovered open port 110/tcp on 66.198.240.42
Discovered open port 993/tcp on 66.198.240.42
Discovered open port 587/tcp on 66.198.240.42
Discovered open port 443/tcp on 66.198.240.42
Discovered open port 995/tcp on 66.198.240.42
Discovered open port 3306/tcp on 66.198.240.42
Discovered open port 53/tcp on 66.198.240.42
Discovered open port 143/tcp on 66.198.240.42
Discovered open port 21/tcp on 66.198.240.42
Discovered open port 25/tcp on 66.198.240.42

```
### Network and port scanner
* nmap

* 
