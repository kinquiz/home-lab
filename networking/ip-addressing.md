# IP Addressing

| Host | Interface | IP | Network | Purpose |
|---|---|---|---|---|
| DC01 | vmbr1 | 10.10.10.10 | 10.10.10.0/24 | Active Directory |
| WIN11PC1 | vmbr1 | 10.10.10.20 | 10.10.10.0/24 | Windows Client |
| ATTK | vmbr1 | 10.10.10.30 | 10.10.10.0/24 | Security Testing |
| UBS01 | vmbr1 | 10.10.10.40 | 10.10.10.0/24 | Linux Server |



.1       Gateway
.2-.9    Infrastructure
.10-.19  Windows infrastructure
.20-.29  Clients
.30-.39  Security
.40-.49  Linux servers
.50-.99  Other infrastructure
.100+    DHCP