# Sublist3r
Sublist3r is a python tool designed to enumerate subdomains of websites using OSINT. It helps penetration testers and bug hunters collect and gather subdomains for the domain they are targeting. Sublist3r enumerates subdomains using many search engines such as Google, Yahoo, Bing, Baidu, and Ask. Sublist3r also enumerates subdomains using Netcraft, Virustotal, ThreatCrowd, DNSdumpster, and ReverseDNS.

URL: https://github.com/aboul3la/Sublist3r
## Install and Setup

Sublist3r depends on the `requests`, `dnspython`, and `argparse` python modules.
These dependencies can be installed using the requirements file:

* Installation on Windows:
``` c:\python27\python.exe -m pip install -r requirements.txt ```
* Installation on Linux
``` sudo pip install -r requirements.txt ```
Alternatively, each module can be installed independently as shown below.

### Requests Module (http://docs.python-requests.org/en/latest/)
* Install for Windows:
``` c:\python27\python.exe -m pip install requests ```
* Install for Ubuntu/Debian:
``` sudo apt-get install python-requests ```
* Install for Centos/Redhat:
``` sudo yum install python-requests ```
* Install using pip on Linux:
``` sudo pip install requests ```
### dnspython Module (http://www.dnspython.org/)
Install for Windows:
c:\python27\python.exe -m pip install dnspython
Install for Ubuntu/Debian:
sudo apt-get install python-dnspython
Install using pip:
sudo pip install dnspython
argparse Module
Install for Ubuntu/Debian:
sudo apt-get install python-argparse
Install for Centos/Redhat:
sudo yum install python-argparse
Install using pip:
sudo pip install argparse
for coloring in windows install the following libraries

c:\python27\python.exe -m pip install win_unicode_console colorama


