---
layout: post
title: useful nmap scans
---
network sweeping:

```
nmap -sn	192.168.11.200-250
```
scan for the top 20 TCP ports and save output in a file:

```
nmap -sT -A --top-ports=20 192.168.11.200-250 -oG top-port-sweep.txt
```


banner grabbing, service ennumeration:

```
nmap -sV -sT 192.168.1.100
```

OS identifying:

```
nmap -O 10.0.0.10
```

