# ReconDog
https://github.com/s0md3v/ReconDog
# Install and Update
```
git clone https://github.com/s0md3v/ReconDog.git

```

# Run
```
python dog.py 
                               ___       ___
                              |   \_____/   |
                             /  |\/     \/|  \    
                             \_/ | /\ /\ | \_/
 ____  ____ _____ _____  __   _  |_\/ \/_|  _____   ____   ____
|___/  |___ |     |    | | \  | /   \o/   \ |    \ |    | | ___
|   \_ |___ |____ |____| |  \_| \___/'\___/ |____/ |____| |____| v0.8
		     Made with <3 By Team Ultimate

1. Whois Lookup
2. DNS Lookup + Cloudflare Detector
3. Zone Transfer
4. Port Scan
5. HTTP Header Grabber
6. Honeypot Detector
7. Robots.txt Scanner
8. Link Grabber
9. IP Location Finder
10. Traceroute
11. Exit

```
* Whois Lookup
```
Enter your choice: 1
Enter Domain or IP Address: Google.com
   Domain Name: GOOGLE.COM
   Registry Domain ID: 2138514_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.markmonitor.com
   Registrar URL: http://www.markmonitor.com
   Updated Date: 2018-02-21T18:36:40Z
   Creation Date: 1997-09-15T04:00:00Z
   Registry Expiry Date: 2020-09-14T04:00:00Z
   Registrar: MarkMonitor Inc.
   Registrar IANA ID: 292
   Registrar Abuse Contact Email: abusecomplaints@markmonitor.com
   Registrar Abuse Contact Phone: +1.2083895740
   Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
   Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
   Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
   Domain Status: serverDeleteProhibited https://icann.org/epp#serverDeleteProhibited
   Domain Status: serverTransferProhibited https://icann.org/epp#serverTransferProhibited
   Domain Status: serverUpdateProhibited https://icann.org/epp#serverUpdateProhibited
   Name Server: NS1.GOOGLE.COM
   Name Server: NS2.GOOGLE.COM
   Name Server: NS3.GOOGLE.COM
   Name Server: NS4.GOOGLE.COM
   DNSSEC: unsigned
   URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
>>> Last update of whois database: 2018-07-02T09:23:05Z <<<
```
* DNS Lookup + Cloudflare Detector
```
Enter your choice: 2
Enter Domain: sstectutorials.com
;; Truncated, retrying in TCP mode.
sstectutorials.com.	3601	IN	SOA	pdns1.registrar-servers.com. hostmaster.registrar-servers.com. 2018030304 43200 3600 604800 3601
sstectutorials.com.	1800	IN	MX	10 eforward2.registrar-servers.com.
sstectutorials.com.	1800	IN	TXT	"v=spf1 include:spf.efwd.registrar-servers.com ~all"
sstectutorials.com.	1800	IN	A	198.54.114.169
sstectutorials.com.	1800	IN	NS	pdns2.registrar-servers.com.
sstectutorials.com.	1800	IN	MX	10 eforward1.registrar-servers.com.
sstectutorials.com.	1800	IN	MX	10 eforward3.registrar-servers.com.
sstectutorials.com.	1800	IN	MX	20 eforward5.registrar-servers.com.
sstectutorials.com.	1800	IN	NS	pdns1.registrar-servers.com.
sstectutorials.com.	1800	IN	MX	15 eforward4.registrar-servers.com.
```
* Port scan
```
Enter your choice: 4
Enter Domain or IP Address: sstectutorials.com

Starting Nmap 7.01 ( https://nmap.org ) at 2018-07-02 09:28 UTC
Nmap scan report for sstectutorials.com (198.54.114.169)
Host is up (0.072s latency).
rDNS record for 198.54.114.169: server254-1.web-hosting.com
PORT     STATE    SERVICE        VERSION
21/tcp   open     ftp            Pure-FTPd
22/tcp   filtered ssh
23/tcp   filtered telnet
80/tcp   open     http-proxy     HAProxy http proxy
110/tcp  open     pop3           Dovecot pop3d
143/tcp  open     imap           Dovecot imapd
443/tcp  open     ssl/http-proxy HAProxy http proxy
3389/tcp filtered ms-wbt-server
Service Info: Device: load balancer

```
* Link Grabber
```
ots.txt Scanner
8. Link Grabber
9. IP Location Finder
10. Traceroute
11. Exit
Enter your choice: 8
Enter URL: sstectutorials.com  
https://sstectutorials.com/

```
* Traceroute
```
10. Traceroute
11. Exit
Enter your choice: 10
Enter Domain or IP Address: sstectutorials.com 
Start: Mon Jul  2 09:38:19 2018
HOST: whatweb                                   Loss%   Snt   Last   Avg  Best  Wrst StDev
  1.|-- 45.55.64.254                               0.0%     3    1.3   0.7   0.2   1.3   0.0
  2.|-- 138.197.251.22                             0.0%     3    0.3   0.8   0.3   1.2   0.0
  3.|-- 138.197.244.34                             0.0%     3    0.9   0.9   0.9   1.0   0.0
  4.|-- ce-0-4-0-3.r08.nycmny01.us.bb.gin.ntt.net  0.0%     3    1.2   1.2   1.2   1.2   0.0
  5.|-- ae-3.r24.nycmny01.us.bb.gin.ntt.net        0.0%     3   14.3   6.2   2.1  14.3   7.0
  6.|-- ae-4.r22.sttlwa01.us.bb.gin.ntt.net        0.0%     3   66.0  68.7  66.0  71.4   2.5
  7.|-- ae-0.r23.sttlwa01.us.bb.gin.ntt.net        0.0%     3   64.3  62.1  60.8  64.3   1.9
  8.|-- ae-3.r23.snjsca04.us.bb.gin.ntt.net        0.0%     3   82.7  82.7  82.7  82.8   0.0
  9.|-- 192.80.16.179                              0.0%     3   80.6  80.7  80.6  80.7   0.0
 10.|-- 107.154.13.242.ip.incapdns.net             0.0%     3   84.6  84.6  84.5  84.6   0.0
 11.|-- ???                                       100.0     3    0.0   0.0   0.0   0.0   0.0
 12.|-- 199.193.7.158                              0.0%     3   93.6  93.7  93.5  94.0   0.0
 13.|-- server254-1.web-hosting.com                0.0%     3   95.4  95.3  94.8  95.7   0.0

```
