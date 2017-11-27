---
layout: post
title: useful nmap scans
---
enumerate and find as much information of the top 1000 ports (recommended first scan):

```
$ nmap --top-ports 1000 -T4 -sC http://nop.cat
```
network sweeping:

```
$ nmap -sn 192.168.11.200-250
```
scan for the top 20 TCP ports and save output in a file:

```
$ nmap -sT -A --top-ports=20 192.168.11.200-250 -oG top-port-sweep.txt
```


banner grabbing, service ennumeration:

```
$ nmap -sV -sT 192.168.1.100
```

OS identifying:

```
$ nmap -O 10.0.0.10
```

attempt to connect to the SMB service:

```
$ nmap 10.17.140.100 --script smb-os-discovery.nse
```

DNS zone transfer NSE script

```
$ nmap --script=dns-zone-transfer -p 53	nop.cat 
```
