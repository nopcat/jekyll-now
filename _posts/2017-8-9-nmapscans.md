---
layout: post
title: useful nmap scans
---
enumerate and find as much information of the top 1000 ports (recommended first scan):<br>
``
$ nmap --top-ports 1000 -T4 -sC http://nop.cat
``
<br>
network sweeping:<br>
``
$ nmap -sn 192.168.11.200-250
``
<br>
scan for the top 20 TCP ports and save output in a file:<br>
``
$ nmap -sT -A --top-ports=20 192.168.11.200-250 -oG top-port-sweep.txt
``
<br>
banner grabbing, service ennumeration:<br>
``
$ nmap -sV -sT 192.168.1.100
``
<br>
OS identifying:<br>
``
$ nmap -O 10.0.0.10
``
<br>
attempt to connect to the SMB service:<br>
``
$ nmap 10.17.140.100 --script smb-os-discovery.nse
``
<br>
DNS zone transfer NSE script<br>
``
$ nmap --script=dns-zone-transfer -p 53	nop.cat 
``
