## Information Gathering with NetZapper

## Overview

Url: https://github.com/NetZapper/NetZapper

## Clone and Install

```
git clone https://github.com/NetZapper/NetZapper.git
```

### Start NetZapper
Go to NetZapper folder and Run
``` 
>>> cd NetZapper
>>> chmod + x Net_Zapper_1.py
>>> python Net_Zapper_1.py
NetZapper$ python Net_Zapper_1.py 
 ####     ##		    ##########      					
 ## ##    ## ##### #######          ##     ##     #####  #####  ##### #####	
 ##  ##   ## #        #           ##      #  #    #    # #    # #     #    #	
 ##   ##  ## ####     #    ##   ##       ######   #####  #####  ###   #####	
 ##    ## ## #        #       ##        #      #  #      #      #     # #  	
 ##     #### #####    #      ######### #        # #      #      ##### #  ##	

1.Hosts Discovery
2.Ports Scanning
3.OS Detection
4.Brute Force SSH
Press ctrl+c to exit...

```
### Options
* Host Discovery
```
Enter network octects (net id) of ip e.g 192.168.10.*: 172.16.12.*

		Live Hosts are.....


 IP ADDRESS		  MAC ADDRESS

172.16.12.1		00:0c:29:84:a7:f9
172.16.12.2		00:0c:29:84:a7:f9
172.16.12.3		c8:be:19:51:0f:fc
```

1.Hosts Discovery
2.Ports Scanning
3.OS Detection
4.Brute Force SSH
Press ctrl+c to exit...
### Ports Scanning
```
Enter choice: 2

Enter Target IP: 172.16.12.236
Enter Ports(separated with spaces and '-' for range: 0-2000

Ports scanning started....

PORT	STATUS
135	OPEN
139	OPEN

```
### OS Detect
```
Hosts Discovery
2.Ports Scanning
3.OS Detection
4.Brute Force SSH
Press ctrl+c to exit...

Enter choice: 3

Enter Target IP: 172.16.12.236

172.16.12.236 belongs to Windows family...
```
