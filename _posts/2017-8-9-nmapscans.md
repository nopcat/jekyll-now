---
layout: post
title: nmap scans
---
network sweeping:

```
root@kali:~# nmap -sn	192.168.11.200-250
```
scan for the top 20 TCP ports and save output in a file:

```
root@kali:~# nmap –sT –A --top-ports=20 192.168.11.200-250 –oG top-port-sweep.txt
```
