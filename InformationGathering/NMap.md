# NMap

Check the valid IP on a IP range.

```
nmap -sS 192.168.1.*
```
To get started this is a simple command for scanning your local network (class C or /24):
```
nmap -sV -p 1-65535 192.168.1.1/24
```
## Nmap Target Selection
* Scan a single IP	
```nmap 192.168.1.1```
* Scan a host	
```nmap www.testhostname.com```
* Scan a range of IPs	
```nmap 192.168.1.1-20```
* Scan a subnet	
```nmap 192.168.1.0/24```
* Scan targets from a text file	
```nmap -iL list-of-ips.txt```
