# Home Lab

This repository documents a private educational cybersecurity laboratory.
All security testing is performed only against systems owned by me or systems for which I have explicit authorization to conduct security testing.
The laboratory is designed for education, experimentation, defensive security research, and infrastructure development.

## High-Level Architecture

```text
┌──────────────────────────────────────────────────────────┐
│                     Physical Host                        │
│                                                          │
│  ┌────────────────────────────────────────────────────┐  │
│  │                     Proxmox                        │  │
│  │                                                    │  │
│  │  ┌──────────────┐       ┌──────────────┐           │  │
│  │  │ Windows      │       │ Windows 11   │           │  │
│  │  │ Server 2022  │       │ Client       │           │  │
│  │  └──────────────┘       └──────────────┘           │  │
│  │                                                    │  │
│  │  ┌──────────────┐       ┌──────────────┐           │  │
│  │  │ Kali Linux   │       │ Ubuntu       │           │  │
│  │  │ Security     │       │ Server       │           │  │
│  │  └──────────────┘       └──────────────┘           │  │
│  │                                                    │  │
│  └────────────────────────────────────────────────────┘  │
└──────────────────────────────────────────────────────────┘
```

---

## Virtualization

The laboratory uses Proxmox as the virtualization platform.

| Component           | Purpose                          |
| ------------------- | -------------------------------- |
| Physical Host       | Hardware platform                |
| Proxmox             | Virtualization and VM management |
| Windows Server 2022 | Windows infrastructure           |
| Windows 11          | Endpoint/client                  |
| Kali Linux          | Security testing workstation     |
| Ubuntu Server       | Linux server and services        |

I am currently use nested virtualization because Proxmox itself is running as a virtual machine on the physical host.

---

# Virtual Machines

## Windows Server 2022

* Active Directory Domain Services
* DNS
* User and group management
* Group Policy
* Windows authentication
* Security event collection
* Domain administration

```text
Hostname: DC01
Operating System: Windows Server 2022
Role: Domain Controller
Domain: lab.local
IP Address: 192.168.1.11/24
```

---

## Windows 11

* Domain-joined workstation
* Endpoint security experiments
* Windows event analysis
* Group Policy testing
* Authentication experiments
* Endpoint monitoring

```text
Hostname: WIN11PC1
Operating System: Windows 11
Role: Domain Client
Domain: lab.local
IP Address: 192.168.1.22/24
```

---

## Kali Linux

* Network reconnaissance
* Network traffic analysis
* Vulnerability assessment
* Web application security testing
* Security tool evaluation
* Controlled attack simulation

```text
Hostname: ATTK
Operating System: Kali Linux
Role: Attacker
IP Address: 192.168.1.21/24
```

---

## Ubuntu Server

* SSH
* Docker
* Nginx
* Databases
* Web applications
* Security monitoring agents
* Development services

```text
Hostname: UBS01
Operating System: Ubuntu Server
Role: Linux Server
IP Address: 192.168.1.13/24
```

---

#  Security Architecture

## Network Isolation

```text
Home Network
     │
     │
  Firewall
     │
     ▼
Cybersecurity Lab
     │
     ├── Management
     ├── Servers
     ├── Clients
     ├── Security Testing
     └── Monitoring
```
# Security Monitoring

```text
┌──────────────┐
│ Windows      │
└──────┬───────┘
       │
┌──────▼───────┐
│ Linux        │
└──────┬───────┘
       │
┌──────▼───────┐
│ Network      │
└──────┬───────┘
       │
       ▼
┌─────────────────────┐
│ Security Monitoring │
│                     │
│ Wazuh               │
│ Suricata            │
│ Zeek                │
└─────────────────────┘
```

---

# Repository Structure

```text
home-lab/
│
├── README.md
│
├── docs/
│   ├── architecture/
│   ├── networking/
│   ├── infrastructure/
│   └── security/
│
├── experiments/
│   ├── networking/
│   ├── windows/
│   ├── linux/
│   ├── web-security/
│   └── monitoring/
│
├── scripts/
│   ├── powershell/
│   ├── bash/
│   └── python/
│
├── configs/
│   ├── proxmox/
│   ├── networking/
│   ├── windows/
│   └── linux/
│
├── screenshots/
│
└── .gitignore
```
---

# Current Status

| Component            | Status      |
| -------------------- | ----------- |
| Proxmox              | Operational |
| Windows Server 2022  | Operational |
| Windows 11           | Operational |
| Kali Linux           | Operational |
| Ubuntu Server        | Operational |
| Active Directory     | Operational |
| Network Segmentation | Operational |
| Firewall             | Operational |
| SIEM                 | Operational |
| IDS/IPS              | Operational |
| Security Experiments | In Progress |

---