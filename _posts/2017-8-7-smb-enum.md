---
layout: post
title: smb enumeration
---
Server Message Block (SMB) protocol’s security track record has been poor for more than 10 years, due to its complex implementation, and open nature.

SMB versions clarifications:
o SMB1 – Windows 2000, XP & Windows 2003
o SMB2 – Windows Vista SP1 & Windows 2008
o SMB2.1 – Windows 7 & Windows 2008  R2
o SMB3 – Windows 8 & Windows 2012

here find some ways to identify SMB netbios service:


using nmap
```
nmap -p 139,445	-oG	smb.txt	192.168.11.200‐254
```

using nbtscan (available in kali linux)

```
nbtscan	-r 192.168.11.0/24
```


null sessions allow unauthenticated servers (or hackers) to obtain browse list from other MS servers. this means it's possible to access large amounts of information about the machine, such as pwd policies, usernames, group names, machine names, users and host ids. this feature existed in SMB1 by default, later restricted though.
