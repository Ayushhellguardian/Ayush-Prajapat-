# Course 3 — Networks & Network Security

**Platform:** Google Cybersecurity Professional Certificate, Coursera  
**Duration:** ~14 hours

---

## What This Course Covers

How networks work, common protocols, and how to identify and harden network vulnerabilities.

---

## Key Topics

### OSI Model — 7 Layers

| Layer | Name | Protocols/Examples |
|-------|------|--------------------|
| 7 | Application | HTTP, HTTPS, DNS, FTP, SMTP |
| 6 | Presentation | SSL/TLS, JPEG, encryption |
| 5 | Session | Authentication sessions |
| 4 | Transport | TCP, UDP |
| 3 | Network | IP, ICMP, routers |
| 2 | Data Link | MAC addresses, switches |
| 1 | Physical | Cables, Wi-Fi signals |

### Common Network Protocols & Ports

| Protocol | Port | Purpose |
|----------|------|---------|
| HTTP | 80 | Web traffic (unencrypted) |
| HTTPS | 443 | Web traffic (encrypted) |
| SSH | 22 | Secure remote login |
| DNS | 53 | Domain name to IP resolution |
| DHCP | 67/68 | Automatic IP assignment |
| FTP | 21 | File transfer |
| SMTP | 25 | Email sending |

### Firewall Types

| Type | Description |
|------|-------------|
| **Stateless** | Filters based on fixed rules only |
| **Stateful** | Tracks state of active connections |
| **NGFW** | Deep packet inspection, application awareness |
| **WAF** | Specifically protects web applications |

### Network Hardening

Network hardening reduces the attack surface. Key techniques covered:

- **Port filtering** — Block unused ports at the firewall
- **Network segmentation** — Separate sensitive systems from general network
- **Patch management** — Keep all devices updated
- **Multi-factor authentication (MFA)** — Add second layer to all logins
- **Strong password policies** — Prevent brute force attacks
- **Principle of least privilege** — Users get only the access they need

### Traffic Analysis Tools

- **Wireshark** — GUI-based packet analyzer; captures and filters live traffic
- **tcpdump** — Command-line packet sniffer for Linux environments

---

## Skills Gained
`OSI model` `TCP/IP` `Network protocols` `Firewalls` `VPN` `Network hardening` `Wireshark` `tcpdump`
