# 🛡️ Cybersecurity & Ethical Hacking — 60 Day Mastery

<p align="center">
  <strong>60-Day Practical Cybersecurity Learning Roadmap</strong><br>
  Kali Linux • Networking • Reconnaissance • Web Security • Linux • Windows • Active Directory • Python • CTF
</p>

<p align="center">

![Kali Linux](https://img.shields.io/badge/Kali%20Linux-557C94?style=for-the-badge\&logo=kalilinux\&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge\&logo=linux\&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge\&logo=python\&logoColor=white)
![Networking](https://img.shields.io/badge/Networking-005571?style=for-the-badge)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-000000?style=for-the-badge\&logo=hackthebox\&logoColor=white)

</p>

---

## 🎯 About This Repository

This repository contains my **60-day practical journey to build strong Cybersecurity and Ethical Hacking skills**.

The roadmap is designed around a simple principle:

> **Learn → Practice → Document → Review → Build**

I already have a foundation in **Linux and Networking**, so this roadmap focuses on applying that knowledge to cybersecurity.

The goal is not to memorize Kali Linux commands.

The goal is to understand:

```text
How systems work
       ↓
How security controls work
       ↓
How vulnerabilities occur
       ↓
How vulnerabilities are identified
       ↓
How they can be safely validated
       ↓
How they should be fixed
```

---

# ⚠️ Ethical & Legal Notice

This repository is strictly for:

* Cybersecurity education
* Ethical hacking
* CTF competitions
* Security research
* Defensive security
* Authorized penetration testing
* Personal cybersecurity labs

Only test systems that you **own or have explicit permission to test**.

Never use these techniques against:

* Unauthorized websites
* Public infrastructure
* Other people's accounts
* Networks without permission
* Production systems without authorization

For practical exploitation, I use **isolated labs, CTF platforms, and intentionally vulnerable applications**.

---

# 🚀 60-Day Learning Path

```text
                    CYBERSECURITY
                          │
                          ▼
                 ┌─────────────────┐
                 │   Kali Linux    │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Security Basics │
                 └────────┬────────┘
                          │
             ┌────────────┴────────────┐
             ▼                         ▼
        Reconnaissance             Networking
             │                         │
             ▼                         ▼
           Nmap                   Wireshark
             │                         │
             └────────────┬────────────┘
                          ▼
                   Enumeration
                          │
                          ▼
                  Web Application
                     Security
                          │
                          ▼
                     Burp Suite
                          │
                          ▼
                     OWASP
                          │
              ┌───────────┴───────────┐
              ▼                       ▼
          Linux Security        Windows Security
              │                       │
              └───────────┬───────────┘
                          ▼
                  Active Directory
                          │
                          ▼
                 Python Automation
                          │
                          ▼
                       CTFs
                          │
                          ▼
                  Security Reporting
                          │
                          ▼
                Defensive Security
```

---

# 📚 What I Will Learn

| Area                | Main Skills                            |
| ------------------- | -------------------------------------- |
| 🐉 Kali Linux       | Environment, tools, package management |
| 🌐 Networking       | TCP/IP, DNS, HTTP, ports, protocols    |
| 🔎 Recon            | OSINT, DNS, attack surface             |
| 🔬 Scanning         | Nmap, service detection                |
| 🧩 Enumeration      | SSH, FTP, SMB, HTTP, DNS               |
| 🌍 Web Security     | HTTP, authentication, authorization    |
| 🕷️ Burp Suite      | Proxy, Repeater, request analysis      |
| 🔐 OWASP            | Common web vulnerabilities             |
| 🦈 Wireshark        | Packet and protocol analysis           |
| 🐧 Linux Security   | Permissions, sudo, SUID, services      |
| 🪟 Windows          | Users, services, PowerShell, security  |
| 🏢 Active Directory | AD, Kerberos, LDAP, GPO                |
| 🐍 Python           | Security automation                    |
| 🏆 CTF              | Practical methodology                  |
| 📝 Reporting        | Findings, evidence, remediation        |
| 🛡️ Defense         | Monitoring, hardening, detection       |

---

# 🗓️ 60-Day Roadmap

## 🟢 Week 01 — Kali Linux & Security Foundation

| Day | Topic                 | Practice                 | Output           |
| --: | --------------------- | ------------------------ | ---------------- |
|  01 | Kali Setup            | VM + isolated lab        | Lab environment  |
|  02 | APT & Packages        | Install/manage tools     | Tool inventory   |
|  03 | Linux Permissions     | `chmod`, `chown`, `sudo` | Permission notes |
|  04 | Processes & Services  | `ps`, `systemctl`        | Process report   |
|  05 | Linux Networking      | `ip`, `ss`, routing      | Network diagram  |
|  06 | Security Fundamentals | CIA, risk, threat        | Security notes   |
|  07 | Weekly Assessment     | Kali lab                 | Week 1 report    |

### Core Commands

```bash
whoami
id
hostname
uname -a
pwd
ls -la
ip addr
ip route
ip neigh
ss -tuln
ps aux
systemctl
journalctl
```

---

# 🔵 Week 02 — Reconnaissance & Nmap

| Day | Topic              | Main Tools            | Output              |
| --: | ------------------ | --------------------- | ------------------- |
|  08 | Recon Fundamentals | `whois`               | Recon notes         |
|  09 | DNS                | `dig`, `host`         | DNS map             |
|  10 | Subdomains         | Amass, Subfinder      | Enumeration results |
|  11 | OSINT              | theHarvester, WhatWeb | Recon report        |
|  12 | Nmap Basics        | Nmap                  | Port scan           |
|  13 | Nmap Advanced      | Nmap/NSE              | Scan report         |
|  14 | Recon Mini-CTF     | Multiple              | CTF report          |

### Authorized Lab Examples

```bash
whois example.com
dig example.com
host example.com
```

```bash
nmap <LAB-IP>
```

```bash
nmap -sV <LAB-IP>
```

```bash
nmap -sC -sV <LAB-IP>
```

```bash
nmap -p- <LAB-IP>
```

> Replace `<LAB-IP>` only with an IP belonging to your authorized lab.

---

# 🟠 Week 03 — Service Enumeration

| Day | Topic                   | Tools                | Practice               |
| --: | ----------------------- | -------------------- | ---------------------- |
|  15 | Service Enumeration     | Nmap                 | Identify services      |
|  16 | FTP                     | FTP/Nmap             | Lab enumeration        |
|  17 | SSH                     | SSH/Nmap             | Configuration analysis |
|  18 | SMB                     | SMBClient/NetExec    | Lab enumeration        |
|  19 | Web Enumeration         | Gobuster/Feroxbuster | Web lab                |
|  20 | Enumeration Methodology | Multiple             | Full checklist         |
|  21 | Assessment              | Multiple             | Enumeration report     |

### Useful Tools

```text
Nmap
Netcat
Nmap NSE
SMBClient
Enum4linux-ng
WhatWeb
Gobuster
Feroxbuster
Nikto
```

---

# 🔴 Week 04 — Web Application Security

| Day | Topic          | Main Focus                        |
| --: | -------------- | --------------------------------- |
|  22 | HTTP           | Requests, responses, headers      |
|  23 | Burp Suite     | Proxy + HTTP history              |
|  24 | Authentication | Sessions + login security         |
|  25 | Authorization  | Access control                    |
|  26 | Injection      | SQLi + command injection concepts |
|  27 | File Security  | Traversal + upload security       |
|  28 | OWASP          | Web security review               |

### Burp Suite Workflow

```text
Browser
   ↓
Burp Proxy
   ↓
Capture Request
   ↓
Understand Request
   ↓
Modify in Lab
   ↓
Repeater
   ↓
Analyze Response
   ↓
Document Finding
```

---

# 🟣 Week 05 — Wireshark & Network Security

| Day | Topic           | Practice                |
| --: | --------------- | ----------------------- |
|  29 | Wireshark       | Packet capture          |
|  30 | Packet Analysis | Protocol identification |
|  31 | TCP             | TCP handshake           |
|  32 | DNS             | DNS traffic             |
|  33 | HTTP            | HTTP traffic            |
|  34 | Network Defense | Firewall, IDS, IPS      |
|  35 | Packet Project  | Complete analysis       |

### Useful Wireshark Filters

```text
ip.addr == 192.168.1.10
```

```text
tcp
```

```text
udp
```

```text
dns
```

```text
http
```

```text
tcp.port == 443
```

Use your own lab traffic when analyzing packets.

---

# 🟤 Week 06 — Linux & Windows Security

| Day | Topic                  | Practice                 |
| --: | ---------------------- | ------------------------ |
|  36 | Linux PrivEsc Concepts | Security lab             |
|  37 | Linux Enumeration      | Permissions/capabilities |
|  38 | Services & Cron        | Lab                      |
|  39 | Credential Security    | Configuration analysis   |
|  40 | Windows Fundamentals   | Windows VM               |
|  41 | Windows Security       | PowerShell/services      |
|  42 | PrivEsc Assessment     | Authorized lab           |

### Linux Enumeration

```bash
id
whoami
groups
sudo -l
uname -a
```

SUID discovery in a lab:

```bash
find / -perm -4000 2>/dev/null
```

Capabilities:

```bash
getcap -r / 2>/dev/null
```

The purpose is to understand **why** a configuration is insecure, not simply to run automated exploit scripts.

---

# ⚫ Week 07 — Active Directory

| Day | Topic                | Focus               |
| --: | -------------------- | ------------------- |
|  43 | AD Fundamentals      | Domain, DC, OU      |
|  44 | Kerberos + LDAP      | Authentication      |
|  45 | SMB + AD Enumeration | Users/groups/shares |
|  46 | BloodHound           | Relationships       |
|  47 | Group Policy         | GPO                 |
|  48 | AD Defense           | Hardening           |
|  49 | AD Lab               | Full assessment     |

### AD Concepts

```text
Domain
Domain Controller
Forest
Tree
OU
Users
Groups
Computers
GPO
LDAP
Kerberos
NTLM
SMB
```

---

# 🟡 Week 08 — Python Security Automation

| Day | Topic             | Project              |
| --: | ----------------- | -------------------- |
|  50 | Python Networking | TCP checker          |
|  51 | HTTP Automation   | Header analyzer      |
|  52 | Log Analysis      | Log analyzer         |
|  53 | Network Inventory | Lab inventory        |
|  54 | Report Automation | Markdown/JSON report |
|  55 | Security Tool     | Combined project     |

### Python Libraries

```python
socket
requests
subprocess
json
re
argparse
asyncio
```

---

# 🔥 Week 09 — CTF + Professional Security

| Day | Topic              | Output           |
| --: | ------------------ | ---------------- |
|  56 | CTF Methodology    | Checklist        |
|  57 | CTF #1             | Write-up         |
|  58 | CTF #2             | Write-up         |
|  59 | Security Reporting | Final report     |
|  60 | Final Assessment   | Complete project |

---

# 🧪 Practice Platforms

## Beginner → Intermediate

### TryHackMe

Practice:

```text
Linux
Networking
Nmap
Web Security
Privilege Escalation
Active Directory
```

### PortSwigger Web Security Academy

Practice:

```text
HTTP
Authentication
Access Control
SQL Injection
XSS
CSRF
SSRF
File Upload
```

### OverTheWire

Practice:

```text
Linux
Command Line
Privilege Concepts
```

### Hack The Box

Use after building a foundation.

Practice:

```text
Recon
Enumeration
Web
Linux
Windows
Active Directory
```

### OWASP Juice Shop

Use for controlled web-security practice.

---

# 🧰 Main Toolset

## Reconnaissance

```text
WHOIS
Dig
Host
Amass
Subfinder
theHarvester
WhatWeb
```

## Scanning

```text
Nmap
Nmap NSE
```

## Enumeration

```text
Nmap
SMBClient
Enum4linux-ng
NetExec
Gobuster
Feroxbuster
Nikto
```

## Web Security

```text
Burp Suite
Curl
Browser DevTools
OWASP ZAP
```

## Network Analysis

```text
Wireshark
TShark
Tcpdump
```

## Linux Security

```text
sudo
find
ps
systemctl
journalctl
getcap
```

## Windows / AD

```text
PowerShell
BloodHound
NetExec
Impacket
```

## Automation

```text
Python
Bash
Git
```

---

# 🧠 Security Methodology

For every authorized target:

```text
01 ── Scope
      ↓
02 ── Reconnaissance
      ↓
03 ── Scanning
      ↓
04 ── Enumeration
      ↓
05 ── Vulnerability Analysis
      ↓
06 ── Controlled Validation
      ↓
07 ── Evidence Collection
      ↓
08 ── Risk Analysis
      ↓
09 ── Remediation
      ↓
10 ── Retest
      ↓
11 ── Report
```

---

# 📝 Finding Template

Every security finding should follow the same structure.

```markdown
# Finding: <Finding Name>

## Severity

Low / Medium / High / Critical

## Description

Explain the vulnerability.

## Affected Component

Identify the affected service/application.

## Root Cause

Explain why the weakness exists.

## Evidence

Document authorized evidence.

## Impact

Explain the potential security impact.

## Recommendation

Explain how the issue should be fixed.

## Verification

Explain how the remediation can be tested.
```

---

# 📁 Repository Structure

```text
cybersecurity-60-days/
│
├── README.md
│
├── 01-kali-foundation/
│   ├── notes.md
│   ├── commands.md
│   └── lab-report.md
│
├── 02-recon/
│   ├── recon-notes.md
│   ├── dns.md
│   ├── nmap.md
│   └── report.md
│
├── 03-enumeration/
│   ├── ftp.md
│   ├── ssh.md
│   ├── smb.md
│   ├── web.md
│   └── report.md
│
├── 04-web-security/
│   ├── http.md
│   ├── burp.md
│   ├── authentication.md
│   ├── authorization.md
│   ├── injection.md
│   └── owasp.md
│
├── 05-network-security/
│   ├── wireshark.md
│   ├── tcp.md
│   ├── dns.md
│   └── packet-analysis.md
│
├── 06-privilege-escalation/
│   ├── linux.md
│   └── windows.md
│
├── 07-active-directory/
│   ├── fundamentals.md
│   ├── kerberos.md
│   ├── ldap.md
│   ├── bloodhound.md
│   └── defense.md
│
├── 08-python-security/
│   ├── tcp-checker/
│   ├── header-analyzer/
│   ├── log-analyzer/
│   ├── network-inventory/
│   └── report-generator/
│
├── 09-ctf/
│   ├── machine-01.md
│   └── machine-02.md
│
├── reports/
│   └── final-assessment.md
│
└── screenshots/
```

---

# 📊 Progress Tracker

| Day | Topic             | Theory | Practice | Notes | Status |
| --: | ----------------- | :----: | :------: | :---: | :----: |
|  01 | Kali Setup        |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  02 | APT               |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  03 | Linux Security    |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  04 | Processes         |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  05 | Networking        |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  06 | Security Basics   |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  07 | Assessment        |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  08 | Recon             |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  09 | DNS               |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  10 | Subdomains        |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  11 | OSINT             |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  12 | Nmap              |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  13 | Nmap Advanced     |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  14 | Mini CTF          |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  15 | Enumeration       |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  16 | FTP               |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  17 | SSH               |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  18 | SMB               |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  19 | Web Enumeration   |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  20 | Enumeration       |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  21 | Assessment        |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  22 | HTTP              |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  23 | Burp Suite        |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  24 | Authentication    |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  25 | Authorization     |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  26 | Injection         |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  27 | File Security     |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  28 | OWASP             |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  29 | Wireshark         |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  30 | Packet Analysis   |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  31 | TCP               |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  32 | DNS Traffic       |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  33 | HTTP Traffic      |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  34 | Network Defense   |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  35 | Packet Project    |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  36 | Linux PrivEsc     |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  37 | Linux Enumeration |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  38 | Services          |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  39 | Credentials       |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  40 | Windows           |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  41 | Windows Security  |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  42 | PrivEsc Lab       |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  43 | Active Directory  |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  44 | Kerberos/LDAP     |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  45 | AD Enumeration    |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  46 | BloodHound        |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  47 | GPO               |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  48 | AD Defense        |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  49 | AD Assessment     |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  50 | Python Networking |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  51 | HTTP Automation   |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  52 | Log Analysis      |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  53 | Network Inventory |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  54 | Report Generator  |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  55 | Security Tool     |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  56 | CTF Methodology   |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  57 | CTF #1            |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  58 | CTF #2            |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  59 | Reporting         |    ⬜   |     ⬜    |   ⬜   |    ⬜   |
|  60 | Final Assessment  |    ⬜   |     ⬜    |   ⬜   |    ⬜   |

---

# 🏆 Final Projects

By the end of this roadmap, the repository should contain:

### 🔐 Security Header Analyzer

```text
Python
    ↓
HTTP Request
    ↓
Security Header Analysis
    ↓
Risk Identification
    ↓
Report
```

### 📊 Security Log Analyzer

```text
Logs
 ↓
Python
 ↓
Pattern Analysis
 ↓
Suspicious Events
 ↓
Report
```

### 🔎 Network Inventory

```text
Authorized Lab
      ↓
Discovery
      ↓
Service Information
      ↓
Inventory
```

### 📝 Security Report Generator

```text
Findings
   ↓
Python
   ↓
Markdown / JSON / CSV
   ↓
Professional Report
```

---

# 📈 Skill Development

Track your confidence from **1–10**.

| Skill              | Target |
| ------------------ | -----: |
| Kali Linux         |   8/10 |
| Networking         |   9/10 |
| Recon              |   8/10 |
| Nmap               |   9/10 |
| Enumeration        |   8/10 |
| Web Security       |   8/10 |
| Burp Suite         |   8/10 |
| Wireshark          |   8/10 |
| Linux Security     |   8/10 |
| Windows Security   |   7/10 |
| Active Directory   |   7/10 |
| Python Automation  |   8/10 |
| CTF                |   8/10 |
| Security Reporting |   8/10 |

These are **learning targets**, not claims of professional proficiency.

---

# 🧠 The Hacker Mindset

Do not think:

```text
"What command should I run?"
```

Think:

```text
"What am I trying to understand?"
             ↓
"What evidence do I have?"
             ↓
"What does this result mean?"
             ↓
"What security weakness could explain it?"
             ↓
"How can I safely validate it in my lab?"
             ↓
"How should the weakness be fixed?"
```

---

# 🔄 Daily Workflow

Every day:

```text
┌──────────────────────┐
│       LEARN          │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│       PRACTICE       │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│       DOCUMENT       │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│       REVIEW         │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│       BUILD          │
└──────────────────────┘
```

---

# 📌 Learning Rules

### Rule 01

Understand the command before using it.

### Rule 02

Understand the vulnerability before using an exploit.

### Rule 03

Practice inside authorized environments.

### Rule 04

Keep detailed notes.

### Rule 05

Do not blindly copy CTF walkthroughs.

### Rule 06

Learn defensive mitigation alongside offensive techniques.

### Rule 07

Build projects instead of only completing tutorials.

### Rule 08

Write professional reports.

---

# 🎯 60-Day End Goal

At the end of this roadmap, the target is to be able to approach an authorized lab systematically:

```text
Scope
 ↓
Recon
 ↓
Scanning
 ↓
Enumeration
 ↓
Vulnerability Analysis
 ↓
Controlled Validation
 ↓
Privilege Analysis
 ↓
Evidence
 ↓
Remediation
 ↓
Retest
 ↓
Professional Report
```

The objective is not simply:

> **"I know how to hack."**

The objective is:

> **"I understand how systems work, how security weaknesses arise, how to safely identify them in authorized environments, how to document them, and how they can be remediated."**

---

# ⭐ Repository Goal

**60 Days.
1 Roadmap.
Multiple Labs.
Multiple Projects.
Continuous Documentation.
One Strong Cybersecurity Foundation.**

```text
LEARN
  +
PRACTICE
  +
BUILD
  +
DOCUMENT
  =
CYBERSECURITY SKILL
```

---

## 📜 License

This repository contains educational material and personal learning notes.

Use responsibly and only for lawful cybersecurity education, authorized security testing, and defensive research.

---

<p align="center">
  <strong>🛡️ Learn Security. Build Skills. Practice Ethically.</strong>
</p>
