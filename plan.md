# 🛡️ Kali Linux & Ethical Hacking — Complete Learning Roadmap

> A practical cybersecurity learning path for someone who already knows **Networking + Linux**.

**Goal:** Become comfortable using Kali Linux for authorized security testing, CTFs, vulnerability assessment, web security, and defensive security analysis.

⚠️ **Ethical Use:** Only test systems that you own or have explicit permission to assess. Use intentionally vulnerable machines, CTF platforms, and local labs for exploitation practice.

---

## 🎯 Prerequisites

You already have a strong starting point if you know:

* Networking fundamentals
* TCP/IP
* IP addressing and subnetting
* DNS
* HTTP/HTTPS
* Ports and protocols
* Linux commands
* Filesystem permissions
* Processes and services
* SSH
* Bash basics
* Git basics
* Basic Python

Recommended additional knowledge:

```text
Networking
   ↓
Linux
   ↓
Kali Linux
   ↓
Security Fundamentals
   ↓
Reconnaissance
   ↓
Scanning
   ↓
Enumeration
   ↓
Vulnerability Analysis
   ↓
Web Security
   ↓
Privilege Escalation
   ↓
Active Directory
   ↓
CTF / Security Labs
   ↓
Defensive Security
```

---

# 1. 🐉 Kali Linux Fundamentals

## Objectives

Learn how Kali is organized and how its security tools are used.

### Topics

* Kali Linux architecture
* Package management
* Repositories
* Users and groups
* Permissions
* Services
* Processes
* Environment variables
* Bash
* SSH
* Networking configuration
* Logs
* System monitoring
* Virtual machines
* Snapshots
* Tool documentation

### Important commands

```bash
whoami
id
uname -a
hostname
pwd
ls -la
cd
cp
mv
rm
mkdir
cat
less
grep
find
which
whereis
history
```

Package management:

```bash
sudo apt update
sudo apt upgrade
apt search <package>
apt show <package>
sudo apt install <package>
sudo apt remove <package>
```

Network information:

```bash
ip addr
ip route
ip neigh
ss -tuln
ping <host>
traceroute <host>
```

Process management:

```bash
ps aux
top
htop
systemctl
journalctl
```

---

# 2. 🔐 Cybersecurity Fundamentals

Before learning exploitation, understand the security concepts behind the tools.

## Learn

### CIA Triad

```text
Confidentiality
Integrity
Availability
```

### Security concepts

* Authentication
* Authorization
* Accounting
* Encryption
* Hashing
* Digital signatures
* Access control
* Threat
* Vulnerability
* Exploit
* Risk
* Attack surface
* Security control
* Incident response

### Learn the difference

```text
Vulnerability
      ↓
Potential weakness

Exploit
      ↓
Method used to take advantage of weakness

Payload
      ↓
Action performed after exploitation

Privilege Escalation
      ↓
Obtaining higher privileges

Persistence
      ↓
Maintaining authorized access
```

---

# 3. 🔎 Reconnaissance

Learn how security professionals gather information about an authorized target.

## Passive Reconnaissance

Study:

* DNS information
* Domain information
* Public IP information
* Certificate information
* Publicly exposed services
* Technology identification
* Public documents
* Search-engine reconnaissance

Tools to learn:

```text
whois
dig
nslookup
host
theHarvester
Amass
Subfinder
WhatWeb
```

Example:

```bash
whois example.com
```

```bash
dig example.com
```

```bash
host example.com
```

### Practice

Use:

* Your own domain
* Local lab
* CTF environment
* Authorized training target

---

# 4. 🔍 Network Scanning

One of the most important areas of ethical hacking.

## Learn Nmap properly

Start with:

```bash
nmap <target>
```

Then learn:

```bash
nmap -sV <target>
```

```bash
nmap -O <target>
```

```bash
nmap -p- <target>
```

```bash
nmap -sC -sV <target>
```

Understand what each option does rather than memorizing commands.

### Learn

* TCP scanning
* UDP scanning
* Port states
* Service detection
* OS detection
* NSE
* Scan timing
* Output formats
* Network filtering
* Firewalls

### Practice Questions

After every scan ask:

```text
What ports are open?
What services are running?
What versions are detected?
What protocols are exposed?
What should be investigated next?
```

---

# 5. 🧩 Enumeration

Scanning tells you that a service exists.

Enumeration helps you understand the service.

Study:

```text
HTTP
HTTPS
SSH
FTP
SMB
DNS
SMTP
SNMP
LDAP
RDP
Databases
```

Tools:

```text
Nmap
Netcat
Gobuster
Feroxbuster
Nikto
Enum4linux-ng
SMBClient
SNMP tools
```

Example:

```bash
nmap -sC -sV <lab-target>
```

For web content discovery in your lab:

```bash
gobuster dir -u http://<lab-target> -w <wordlist>
```

---

# 6. 🌐 Web Application Security

This should become one of your strongest areas.

## Learn HTTP deeply

Understand:

```text
GET
POST
PUT
PATCH
DELETE
HEAD
OPTIONS
```

Study:

* Headers
* Cookies
* Sessions
* Authentication
* Authorization
* JWT
* CORS
* Same-Origin Policy
* HTTP status codes
* Request/response structure
* File uploads
* APIs

---

# 7. 🕷️ OWASP Web Security

Learn the OWASP Top 10 and understand the underlying vulnerability classes.

Focus on:

* Broken access control
* Cryptographic failures
* Injection
* Insecure design
* Security misconfiguration
* Vulnerable components
* Authentication failures
* Software/data integrity issues
* Logging/monitoring failures
* SSRF

### Main Tool

## Burp Suite

Learn:

```text
Proxy
Repeater
Intruder
Decoder
Comparer
HTTP history
Site map
Extensions
```

Practice workflow:

```text
Browser
   ↓
Burp Proxy
   ↓
Capture Request
   ↓
Understand Request
   ↓
Modify Request
   ↓
Send
   ↓
Analyze Response
```

Use deliberately vulnerable applications such as OWASP Juice Shop or Web Security Academy labs.

---

# 8. 💉 Injection Vulnerabilities

Learn the concepts and practice only in authorized labs.

Study:

```text
SQL Injection
Command Injection
LDAP Injection
NoSQL Injection
Template Injection
```

For SQL injection, understand:

```text
Application
    ↓
User Input
    ↓
SQL Query
    ↓
Database
```

Learn why unsafe input handling creates vulnerabilities.

Also learn the defensive solutions:

* Parameterized queries
* Prepared statements
* Input validation
* Least privilege
* Output encoding

---

# 9. 📁 File & Authentication Security

Study:

### File vulnerabilities

* Path traversal
* Local file inclusion
* Remote file inclusion
* Unsafe file upload
* File permission problems

### Authentication

* Weak passwords
* Password policies
* Session management
* MFA
* Account lockout
* Credential storage
* Password hashing

Learn password hashing algorithms:

```text
MD5       → insecure
SHA-1     → deprecated for security use
bcrypt    → commonly used
scrypt    → memory-hard
Argon2    → modern password hashing
```

---

# 10. 🧗 Privilege Escalation

Learn how security testers identify misconfigurations that could allow a low-privileged account to gain higher privileges.

## Linux Privilege Escalation

Study:

```text
sudo permissions
SUID/SGID
Linux capabilities
Cron jobs
PATH issues
Writable files
Services
Weak permissions
Credentials
Environment variables
Kernel vulnerabilities
```

Useful commands:

```bash
id
sudo -l
find / -perm -4000 2>/dev/null
getcap -r / 2>/dev/null
```

Do not blindly run exploit scripts.

Understand why the vulnerability exists.

---

# 11. 🪟 Windows Security

Do not focus only on Kali.

Learn Windows internals.

Topics:

* Windows users/groups
* NTFS permissions
* PowerShell
* Services
* Registry
* Windows authentication
* Kerberos
* NTLM
* SMB
* RDP
* Active Directory
* Group Policy

Important tools to learn in authorized labs:

```text
BloodHound
Impacket
NetExec
Mimikatz concepts
PowerView concepts
```

---

# 12. 🏢 Active Directory

This is a major cybersecurity skill.

Learn:

```text
Domain
Domain Controller
Forest
Tree
OU
GPO
Users
Groups
Computers
SPNs
Kerberos
LDAP
NTLM
SMB
```

Understand attack paths conceptually:

```text
Low Privileged User
       ↓
Enumeration
       ↓
Misconfiguration
       ↓
Privilege Increase
       ↓
Credential / Access Discovery
       ↓
Higher Privilege
```

Build your own Windows lab before practicing advanced AD techniques.

---

# 13. 📡 Wireless Security

Learn the theory first.

Topics:

* Wi-Fi architecture
* SSID
* BSSID
* Channels
* WPA2
* WPA3
* Authentication
* Encryption
* Handshakes
* Rogue access points
* Evil Twin concepts
* Wireless monitoring

Tools to understand:

```text
Aircrack-ng
Kismet
Wireshark
```

Practice only on your own lab network or authorized wireless lab.

---

# 14. 📦 Metasploit Framework

Do not learn Metasploit as a "press exploit" tool.

Understand its architecture.

```text
Exploit
Payload
Module
Auxiliary
Encoder
Post
```

Learn:

```text
search
info
use
show options
set
run
```

Understand:

```text
Target
 ↓
Vulnerability
 ↓
Exploit
 ↓
Payload
 ↓
Session
 ↓
Post-exploitation
```

Always understand the underlying vulnerability before using an automated module.

---

# 15. 🧪 Exploit Development Basics

After learning security fundamentals, start understanding how exploits work.

Learn:

* Memory layout
* Stack
* Heap
* Registers
* Buffer overflow concepts
* Assembly basics
* x86/x64
* Debuggers
* Calling conventions
* Shellcode concepts
* ASLR
* DEP/NX
* Stack canaries

Recommended supporting skills:

```text
C
C++
Python
Assembly
GDB
pwndbg
```

---

# 16. 🐍 Python for Cybersecurity

You already know Python basics, so build security automation skills.

Learn:

```text
socket
requests
subprocess
os
sys
json
re
argparse
asyncio
scapy
```

Projects:

### Project 1

TCP connectivity checker

```text
Input:
Host + ports

Output:
Reachable / unavailable
```

### Project 2

HTTP security-header checker

```text
URL
 ↓
HTTP response
 ↓
Analyze headers
 ↓
Security report
```

### Project 3

Log analyzer

```text
Apache/Nginx logs
       ↓
Python
       ↓
Suspicious requests
       ↓
Report
```

### Project 4

Network inventory tool

```text
Subnet
 ↓
Discover hosts
 ↓
Collect basic service information
 ↓
Generate report
```

---

# 17. 🦈 Wireshark

Learn packet analysis deeply.

Start with:

```text
Ethernet
ARP
ICMP
TCP
UDP
DNS
HTTP
TLS
DHCP
```

Important concepts:

```text
Packet
Frame
Protocol
Source
Destination
Port
Flags
Payload
```

Learn filters such as:

```text
ip.addr == 192.168.1.10
```

```text
tcp
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

---

# 18. 🛡️ Defensive Security

Ethical hacking becomes much more useful when you understand defense.

Learn:

* Logs
* SIEM
* IDS
* IPS
* EDR
* Firewalls
* Authentication logs
* Network monitoring
* Incident response
* Threat intelligence
* IOC
* Detection rules

Tools/platforms to explore:

```text
Wazuh
Security Onion
Splunk
Elastic
Zeek
Suricata
```

---

# 19. 🧠 CTF Methodology

When solving a legal CTF:

```text
1. Recon
      ↓
2. Scan
      ↓
3. Enumerate
      ↓
4. Identify vulnerability
      ↓
5. Validate
      ↓
6. Exploit
      ↓
7. Privilege escalation
      ↓
8. Document
```

Never randomly run commands.

Maintain notes.

Example:

```text
Target:
10.10.x.x

Open ports:
22
80
445

Web:
Apache

Interesting:
robots.txt

Potential vulnerability:
...

Next action:
...
```

---

# 20. 🧪 Recommended Legal Practice Labs

Use intentionally vulnerable environments.

### Beginner

* TryHackMe
* PortSwigger Web Security Academy
* OverTheWire
* PicoCTF

### Intermediate

* Hack The Box
* VulnHub
* OWASP Juice Shop

### Advanced

* Hack The Box machines
* Active Directory labs
* Exploit development labs
* Malware-analysis labs

Always follow the platform's rules and scope.

---

# 21. 🏗️ Build Your Own Cybersecurity Lab

Recommended setup:

```text
Windows Host
      │
      └── VMware / VirtualBox
              │
              ├── Kali Linux
              │
              ├── OWASP Juice Shop
              │
              ├── Metasploitable
              │
              ├── Ubuntu Server
              │
              └── Windows Evaluation VM
```

Use an isolated virtual network for vulnerable machines.

Take snapshots before experiments.

Never expose deliberately vulnerable machines directly to the public internet.

---

# 22. 📅 30-Day Kali Linux Plan

## Week 1 — Kali + Security Foundation

### Day 1

Kali installation + VM configuration

### Day 2

Kali filesystem + package management

### Day 3

Users, groups, permissions

### Day 4

Processes + services + logs

### Day 5

Networking commands

### Day 6

Cybersecurity fundamentals

### Day 7

Build your first isolated lab

---

# Week 2 — Recon + Enumeration

### Day 8

Passive reconnaissance

### Day 9

DNS enumeration

### Day 10

Nmap fundamentals

### Day 11

Advanced Nmap concepts

### Day 12

Service enumeration

### Day 13

SMB / FTP / SSH enumeration

### Day 14

Mini CTF

---

# Week 3 — Web Security

### Day 15

HTTP fundamentals

### Day 16

Burp Suite

### Day 17

Authentication

### Day 18

Authorization / access control

### Day 19

Injection concepts

### Day 20

File vulnerabilities

### Day 21

OWASP Juice Shop challenge

---

# Week 4 — Privilege Escalation + CTF

### Day 22

Linux privilege escalation

### Day 23

Windows fundamentals

### Day 24

Windows privilege escalation concepts

### Day 25

Metasploit fundamentals

### Day 26

Wireshark

### Day 27

Python security automation

### Day 28

CTF

### Day 29

Write a penetration-testing report

### Day 30

Complete assessment

---

# 23. 🚀 60-Day Intermediate Roadmap

After the first 30 days:

```text
Days 31–35
Advanced Web Security

Days 36–40
Linux Privilege Escalation

Days 41–45
Windows Security

Days 46–50
Active Directory

Days 51–54
Python Security Automation

Days 55–57
Wireshark + Network Security

Days 58–60
Full CTF + Security Report
```

---

# 24. 🏆 90-Day Cybersecurity Roadmap

## Month 1

```text
Kali
Linux
Networking
Recon
Nmap
Enumeration
Wireshark
```

## Month 2

```text
Web Security
Burp Suite
OWASP
Authentication
Authorization
Injection
Linux PrivEsc
Windows PrivEsc
```

## Month 3

```text
Active Directory
Python Automation
Metasploit
CTFs
Defensive Security
Security Reporting
Portfolio Projects
```

---

# 25. 💼 Portfolio Projects

Build projects that demonstrate understanding rather than simply copying tools.

### Project 1 — Network Recon Dashboard

```text
Python
   +
Nmap
   +
FastAPI
   +
React
```

Features:

* Authorized target input
* Scan results
* Open ports
* Services
* Version information
* Export report

---

### Project 2 — Web Security Header Analyzer

```text
Python
FastAPI
React
```

Check:

```text
CSP
HSTS
X-Frame-Options
X-Content-Type-Options
Referrer-Policy
Cookie flags
```

---

### Project 3 — Log Detection System

```text
Python
   +
Regex
   +
FastAPI
   +
Dashboard
```

Detect suspicious patterns from sample logs.

---

### Project 4 — Security Lab Documentation

Create GitHub documentation for:

```text
Lab setup
Recon
Enumeration
Vulnerability
Root cause
Mitigation
Evidence
Final report
```

Do not publish real credentials, private data, or unauthorized target information.

---

# 26. 📚 Daily Learning Routine

Recommended:

```text
30 min — Theory

45 min — Kali/tools

60 min — Hands-on lab

30 min — CTF

15 min — Notes
```

Total:

```text
≈ 3 hours/day
```

If college workload is high:

```text
30 min Theory
45 min Lab
30 min CTF
15 min Notes
```

---

# 27. 📝 Keep a Hacker Notebook

For every lab, record:

```text
Target
Scope
Date
Recon
Open Ports
Services
Technologies
Potential Vulnerabilities
Evidence
Commands
Results
Root Cause
Mitigation
Lessons Learned
```

Useful tools:

```text
Obsidian
CherryTree
Joplin
Markdown + GitHub
```

Never store real passwords or private keys in your notes repository.

---

# 28. 🧭 The Golden Rule

Do not memorize hundreds of Kali commands.

Instead learn:

```text
WHY
 ↓
WHAT
 ↓
HOW
 ↓
RESULT
 ↓
MITIGATION
```

For example:

```text
Why is port 80 open?
        ↓
What web server is running?
        ↓
How can I enumerate it?
        ↓
What information did I discover?
        ↓
Is there a security issue?
        ↓
How should it be fixed?
```

This mindset is more valuable than memorizing tool commands.

---

# 29. 🔥 Final Skill Tree

```text
                    CYBERSECURITY
                         │
        ┌────────────────┼────────────────┐
        │                │                │
    Networking         Linux           Security
        │                │                │
        └────────────────┼────────────────┘
                         │
                    Kali Linux
                         │
        ┌────────────────┼────────────────┐
        │                │                │
      Recon            Web             Network
        │                │                │
      Nmap             Burp           Wireshark
        │                │                │
   Enumeration        OWASP          Analysis
        │                │                │
        └────────────────┼────────────────┘
                         │
                 Vulnerability Analysis
                         │
              ┌──────────┴──────────┐
              │                     │
          Linux PrivEsc        Windows / AD
              │                     │
              └──────────┬──────────┘
                         │
                   CTF / Security Labs
                         │
                  Python Automation
                         │
                 Defensive Security
                         │
                   Security Engineer
```

# 🎯 End Goal

By the end of this roadmap, you should be able to:

* Navigate Kali Linux confidently
* Analyze network traffic
* Perform authorized reconnaissance
* Perform network scanning
* Enumerate services
* Analyze web applications
* Use Burp Suite
* Understand OWASP vulnerabilities
* Perform controlled exploitation in labs
* Understand Linux privilege escalation
* Understand Windows security
* Understand Active Directory
* Automate security tasks with Python
* Analyze packets with Wireshark
* Complete CTF challenges
* Write professional security reports
* Explain vulnerabilities and their mitigations
* Build cybersecurity projects for your portfolio

## ⚠️ Professional Standard

The objective is not:

> "I know how to hack."

The objective is:

> **"I can identify, validate, explain, document, and help remediate security weaknesses in systems I am authorized to test."**

That is the mindset to carry into cybersecurity.
