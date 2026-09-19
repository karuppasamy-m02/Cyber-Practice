# 🛡️ 60-DAY CYBERSECURITY & ETHICAL HACKING MASTERY ROADMAP

**Level:** Networking + Linux already known
**Platform:** Kali Linux
**Duration:** 60 Days
**Recommended Time:** 2–3 hours/day
**Method:** Learn → Practice → Document → Review

> ⚠️ **Legal Lab Rule:** Run scanning, exploitation, credential testing, wireless testing, and privilege-escalation exercises only against systems you own or explicitly have permission to test. Use CTFs and intentionally vulnerable machines for practice.

---

# 🎯 60-DAY OBJECTIVE

By Day 60, you should be comfortable with:

```text
Kali Linux
     ↓
Cybersecurity Fundamentals
     ↓
Reconnaissance
     ↓
Nmap
     ↓
Enumeration
     ↓
Network Analysis
     ↓
Web Security
     ↓
Burp Suite
     ↓
OWASP
     ↓
Vulnerability Analysis
     ↓
Linux Privilege Escalation
     ↓
Windows Security
     ↓
Active Directory
     ↓
Python Security Automation
     ↓
CTF Methodology
     ↓
Security Reporting
```

---

# 🧰 LAB SETUP

Build an isolated cybersecurity lab before serious practice.

Recommended:

```text
Windows Host
│
├── VMware / VirtualBox
│
├── Kali Linux
│
├── Ubuntu / Linux Lab
│
├── OWASP Juice Shop
│
├── Metasploitable
│
└── Windows Evaluation VM
```

Recommended practice platforms:

```text
TryHackMe
Hack The Box
PortSwigger Web Security Academy
OverTheWire
picoCTF
VulnHub
OWASP Juice Shop
```

Keep vulnerable machines isolated from your normal network.

---

# 📅 DAILY STUDY FORMAT

Use this structure every day.

| Session   |   Time | Activity          |
| --------- | -----: | ----------------- |
| Theory    | 30 min | Learn concepts    |
| Kali/Tool | 30 min | Learn tool        |
| Practice  | 60 min | Authorized lab    |
| Notes     | 20 min | Document findings |
| Review    | 10 min | Recall yesterday  |

**Total:** ~2.5 hours/day

If you have only 1 hour:

```text
20 min Theory
30 min Practice
10 min Notes
```

---

# 🟢 WEEK 1 — KALI + SECURITY FOUNDATION

## DAY 01 — Kali Linux Environment

### Learn

* Kali Linux purpose
* Kali tool categories
* VM networking
* NAT vs Host-only
* Snapshots
* Terminal workflow
* Kali filesystem

### Commands

```bash
whoami
id
hostname
uname -a
pwd
ls -la
cd
history
which nmap
```

### Practice

```text
✓ Create Kali VM
✓ Take snapshot
✓ Configure isolated lab network
✓ Identify Kali IP
✓ Identify default route
```

### Task

Create:

```text
~/cyber-lab/
~/cyber-notes/
~/tools/
~/reports/
```

---

# DAY 02 — Kali Package Management

### Learn

* APT
* Packages
* Repositories
* Updates
* Installed software

### Commands

```bash
sudo apt update
apt search nmap
apt show nmap
dpkg -l
which nmap
```

Practice:

```bash
nmap --version
burpsuite --version
```

### Task

Create a list of 20 Kali tools and write what each tool does.

---

# DAY 03 — Linux Security

### Learn

* Users
* Groups
* Permissions
* Ownership
* sudo
* SUID
* SGID

### Commands

```bash
id
groups
ls -la
chmod
chown
sudo -l
```

Practice:

```bash
touch test.txt
ls -l test.txt
chmod 600 test.txt
ls -l test.txt
```

### Understand

```text
r = read
w = write
x = execute
```

---

# DAY 04 — Processes + Services

### Learn

* Processes
* Services
* Ports
* System logs

### Commands

```bash
ps aux
top
htop
systemctl
systemctl --type=service
journalctl
```

Practice:

```bash
ss -tuln
```

### Task

Identify 10 running processes and explain their purpose.

---

# DAY 05 — Linux Networking

### Learn

* Interface
* IP
* Gateway
* DNS
* Routing
* ARP/neighbour discovery

### Commands

```bash
ip addr
ip route
ip neigh
ss -tuln
ping 127.0.0.1
```

### Task

Draw your Kali network:

```text
Kali
 ↓
Virtual Interface
 ↓
Virtual Network
 ↓
Gateway
 ↓
Internet / Lab
```

---

# DAY 06 — Cybersecurity Fundamentals

### Learn

* CIA Triad
* Threat
* Vulnerability
* Exploit
* Risk
* Attack surface
* Authentication
* Authorization
* Encryption
* Hashing

### Practice

For 10 examples identify:

```text
Threat
Vulnerability
Impact
Mitigation
```

---

# DAY 07 — WEEK 1 ASSESSMENT

### Practical

Perform:

```text
✓ Kali system inspection
✓ Network configuration
✓ Process inspection
✓ Service inspection
✓ Permission analysis
```

### Deliverable

Create:

```text
Week-01-Kali-Fundamentals.md
```

Include:

```text
Commands learned
Tools learned
Important concepts
Problems encountered
Solutions
What I learned
```

---

# 🔵 WEEK 2 — RECONNAISSANCE

# DAY 08 — Reconnaissance Concepts

Learn:

```text
Passive Recon
Active Recon
Attack Surface
OSINT
```

Understand the difference.

### Tools

```text
whois
dig
host
nslookup
```

### Commands

```bash
whois example.com
dig example.com
host example.com
nslookup example.com
```

Only use domains you own or are authorized to assess.

---

# DAY 09 — DNS

### Learn

* A
* AAAA
* MX
* NS
* TXT
* CNAME
* PTR
* DNS hierarchy

### Commands

```bash
dig example.com
dig example.com MX
dig example.com NS
dig example.com TXT
```

### Practice

Create a DNS record map.

---

# DAY 10 — Subdomains

### Learn

* Subdomain enumeration
* DNS records
* Certificate transparency
* Passive discovery

Tools:

```text
Amass
Subfinder
```

### Practice

Use your own domain or a CTF target.

---

# DAY 11 — OSINT

Learn:

```text
Public information
DNS information
Technology information
Public documents
Certificate information
```

Tools:

```text
theHarvester
WhatWeb
Amass
```

### Deliverable

Create:

```text
Recon-Report.md
```

---

# DAY 12 — NMAP FUNDAMENTALS

### Learn

* Port
* TCP
* UDP
* Open
* Closed
* Filtered
* Service detection

### Commands

```bash
nmap <LAB-IP>
nmap -p 22,80,443 <LAB-IP>
nmap -sV <LAB-IP>
```

### Practice

Scan your own lab VM.

---

# DAY 13 — NMAP DEEP DIVE

Learn:

```text
Service detection
OS detection
Default scripts
Port ranges
Output formats
NSE
```

Commands:

```bash
nmap -sC -sV <LAB-IP>
nmap -O <LAB-IP>
nmap -p- <LAB-IP>
```

### Task

Create:

```text
Nmap-Notes.md
```

---

# DAY 14 — WEEK 2 MINI CTF

Perform:

```text
Recon
 ↓
DNS
 ↓
Scan
 ↓
Service identification
 ↓
Enumeration
```

Do not exploit anything yet.

### Deliverable

```text
Week-02-Recon-Report.md
```

---

# 🟠 WEEK 3 — ENUMERATION

# DAY 15 — Service Enumeration

Study:

```text
SSH
FTP
HTTP
HTTPS
SMB
DNS
SMTP
SNMP
```

Learn what information each service can expose.

---

# DAY 16 — FTP

Learn:

```text
FTP architecture
Anonymous access
Authentication
File permissions
FTP security
```

Practice against a lab.

Commands:

```bash
ftp <LAB-IP>
```

---

# DAY 17 — SSH

Learn:

```text
SSH authentication
Keys
Password authentication
Configuration
SSH security
```

Commands:

```bash
ssh user@<LAB-IP>
```

Defensive practice:

```bash
sshd -T
```

---

# DAY 18 — SMB

Learn:

```text
SMB
Windows shares
Users
Permissions
Authentication
```

Tools:

```text
smbclient
enum4linux-ng
Nmap
```

Practice only against your lab.

---

# DAY 19 — Web Enumeration

Learn:

```text
Web server
Directories
Files
robots.txt
HTTP headers
Technology detection
```

Tools:

```text
WhatWeb
Gobuster
Feroxbuster
Nikto
```

Example lab command:

```bash
whatweb http://<LAB-IP>
```

---

# DAY 20 — Enumeration Methodology

Create your own checklist:

```text
[ ] IP
[ ] Ports
[ ] Services
[ ] Versions
[ ] Web technologies
[ ] Users
[ ] Shares
[ ] DNS
[ ] Interesting files
[ ] Potential vulnerabilities
```

---

# DAY 21 — WEEK 3 ASSESSMENT

Perform a complete enumeration exercise against a legal lab.

Deliver:

```text
Target
Scope
Ports
Services
Versions
Findings
Evidence
Potential risks
Recommended next steps
```

---

# 🔴 WEEK 4 — WEB SECURITY

# DAY 22 — HTTP

Learn deeply:

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

```text
Headers
Cookies
Sessions
Status codes
Methods
Parameters
Request body
Response body
```

---

# DAY 23 — Burp Suite

Learn:

```text
Proxy
HTTP History
Repeater
Decoder
Comparer
Site Map
```

Workflow:

```text
Browser
 ↓
Burp
 ↓
Capture request
 ↓
Inspect
 ↓
Modify
 ↓
Send
 ↓
Analyze response
```

---

# DAY 24 — Authentication

Study:

```text
Login
Sessions
Cookies
Passwords
MFA
Session expiration
Account recovery
```

Practice with Web Security Academy labs.

---

# DAY 25 — Authorization

Learn:

```text
Authentication ≠ Authorization
```

Study:

```text
Horizontal access control
Vertical access control
IDOR / BOLA
Role-based access
```

---

# DAY 26 — Injection

Learn the concepts behind:

```text
SQL Injection
Command Injection
NoSQL Injection
LDAP Injection
Template Injection
```

Focus on:

```text
Root cause
Detection
Impact
Prevention
```

---

# DAY 27 — File Security

Study:

```text
Path traversal
File upload
LFI concepts
RFI concepts
File permissions
Content validation
```

Practice in intentionally vulnerable applications.

---

# DAY 28 — OWASP TOP 10 REVIEW

Create a table:

| Vulnerability          | Meaning                     | Example       | Impact               | Defense               |
| ---------------------- | --------------------------- | ------------- | -------------------- | --------------------- |
| Broken Access Control  | Unauthorized access         | IDOR          | Data exposure        | Authorization         |
| Injection              | Untrusted input interpreted | SQLi          | Data/system impact   | Parameterized queries |
| Misconfiguration       | Unsafe configuration        | Debug enabled | Information exposure | Secure configuration  |
| Authentication Failure | Weak authentication         | Weak session  | Account compromise   | Strong auth           |

Complete additional OWASP labs.

---

# 🟣 WEEK 5 — NETWORK SECURITY + WIRESHARK

# DAY 29 — Wireshark

Learn:

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

---

# DAY 30 — Packet Analysis

Learn:

```text
ARP
ICMP
TCP
UDP
DNS
HTTP
TLS
DHCP
```

Filters:

```text
ip.addr == 192.168.1.10
tcp
udp
dns
http
tcp.port == 443
```

Use traffic generated by your own lab.

---

# DAY 31 — TCP Analysis

Understand:

```text
SYN
SYN-ACK
ACK
FIN
RST
```

Study:

```text
Three-way handshake
Connection termination
TCP flags
```

---

# DAY 32 — DNS Analysis

Capture DNS traffic in your lab.

Identify:

```text
Client
DNS server
Query
Response
Record
```

---

# DAY 33 — HTTP Analysis

Capture your own HTTP traffic.

Identify:

```text
Request
Response
Headers
Cookies
Parameters
Status code
```

---

# DAY 34 — Network Security

Learn:

```text
Firewall
IDS
IPS
VPN
Proxy
NAT
Segmentation
Zero Trust
```

---

# DAY 35 — WEEK 5 PROJECT

Build a packet-analysis report.

Include:

```text
Traffic captured
Protocols observed
Interesting packets
Potential security issues
Defensive recommendations
Screenshots
```

---

# 🟤 WEEK 6 — PRIVILEGE ESCALATION

# DAY 36 — Linux Privilege Escalation Concepts

Learn:

```text
Users
Groups
sudo
SUID
SGID
Capabilities
Cron
Services
PATH
Writable files
Credentials
```

---

# DAY 37 — Linux Enumeration

Commands:

```bash
id
whoami
groups
sudo -l
uname -a
```

Find SUID files in your lab:

```bash
find / -perm -4000 2>/dev/null
```

Capabilities:

```bash
getcap -r / 2>/dev/null
```

---

# DAY 38 — Linux Services

Study:

```text
Systemd
Services
Cron
Scheduled tasks
Writable service files
Configuration files
```

Understand the vulnerability rather than blindly using automated scripts.

---

# DAY 39 — Linux Credentials

Learn where credentials can accidentally appear:

```text
Configuration files
Environment variables
History files
Application files
Backups
Logs
```

Practice only inside your lab.

---

# DAY 40 — Windows Fundamentals

Learn:

```text
Users
Groups
Services
Processes
Registry
NTFS
PowerShell
Event Logs
```

---

# DAY 41 — Windows Security

Study:

```text
UAC
Windows Defender
Windows Firewall
Authentication
NTLM
Kerberos
SMB
RDP
```

---

# DAY 42 — WEEK 6 LAB

Perform a controlled privilege-escalation assessment against a deliberately vulnerable VM.

Document:

```text
Initial account
Enumeration
Misconfiguration
Security impact
Evidence
Root cause
Remediation
```

---

# ⚫ WEEK 7 — ACTIVE DIRECTORY

# DAY 43 — Active Directory Fundamentals

Learn:

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
```

---

# DAY 44 — Kerberos + LDAP

Learn:

```text
Kerberos
Tickets
SPN
LDAP
NTLM
Authentication flow
```

Draw the authentication process.

---

# DAY 45 — SMB + AD Enumeration

Study:

```text
Shares
Users
Groups
Permissions
Domain information
```

Tools:

```text
Nmap
SMBClient
NetExec
```

Use only your AD lab.

---

# DAY 46 — BloodHound

Learn the concept of:

```text
Attack Paths
Relationships
Permissions
Group Membership
Delegation
```

Understand why a relationship can create privilege escalation.

---

# DAY 47 — Group Policy

Learn:

```text
GPO
Domain policies
Password policies
User rights
Software deployment
Security configuration
```

---

# DAY 48 — AD Security

Study defensive concepts:

```text
Least privilege
MFA
Privileged accounts
Tiered administration
Monitoring
Credential protection
LAPS concepts
```

---

# DAY 49 — AD LAB

Complete an authorized AD lab.

Document:

```text
Domain
Users
Groups
Machines
Relationships
Security weaknesses
Recommended fixes
```

---

# 🟡 WEEK 8 — PYTHON + SECURITY AUTOMATION

# DAY 50 — Python Networking

Learn:

```python
socket
requests
subprocess
json
re
argparse
```

Build:

```text
TCP connection checker
```

---

# DAY 51 — HTTP Security Tool

Build:

```text
Security Header Analyzer
```

Input:

```text
URL
```

Output:

```text
CSP
HSTS
X-Frame-Options
X-Content-Type-Options
Referrer-Policy
```

---

# DAY 52 — Log Analyzer

Build a Python application that reads sample logs.

Detect:

```text
Repeated failed logins
Suspicious paths
Large request counts
Unusual status codes
```

---

# DAY 53 — Network Inventory

Build:

```text
Authorized Lab Network Inventory
```

Input:

```text
Lab subnet
```

Output:

```text
Host
IP
Reachability
Known services
```

Do not design it for unauthorized internet scanning.

---

# DAY 54 — Report Generator

Create a Python script that converts findings into:

```text
Markdown
JSON
CSV
```

Example:

```text
Target
Finding
Severity
Evidence
Recommendation
```

---

# DAY 55 — SECURITY AUTOMATION PROJECT

Combine your skills:

```text
Python
   +
Nmap
   +
HTTP analysis
   +
Report generation
```

Create:

# 🔐 CyberLab Security Scanner

Features:

```text
✓ Lab target input
✓ Port information
✓ Service information
✓ HTTP checks
✓ Security headers
✓ JSON output
✓ Markdown report
```

---

# 🔥 WEEK 9 — CTF + PROFESSIONAL METHODOLOGY

# DAY 56 — CTF Methodology

Use:

```text
1. Scope
2. Recon
3. Scan
4. Enumerate
5. Analyze
6. Validate
7. Exploit in authorized environment
8. Privilege analysis
9. Evidence
10. Report
```

---

# DAY 57 — CTF 1

Complete one beginner/intermediate machine.

Do not immediately read the walkthrough.

Use:

```text
Recon
Nmap
Enumeration
Web analysis
Linux commands
Notes
```

---

# DAY 58 — CTF 2

Complete another machine.

Focus on:

```text
Web
Linux
Enumeration
Privilege escalation
```

---

# DAY 59 — PROFESSIONAL SECURITY REPORT

Create a real penetration-testing-style report for your lab.

Structure:

```text
1. Executive Summary

2. Scope

3. Methodology

4. Target Information

5. Findings

6. Evidence

7. Risk Explanation

8. Technical Details

9. Remediation

10. Retest Recommendation
```

For every finding:

```text
Finding
Severity
Description
Evidence
Impact
Root Cause
Recommendation
```

---

# 🏆 DAY 60 — FINAL CYBERSECURITY ASSESSMENT

This is your final exam.

Set up a legal lab target.

You should complete:

```text
                TARGET
                   ↓
              RECON
                   ↓
                NMAP
                   ↓
            ENUMERATION
                   ↓
         VULNERABILITY ANALYSIS
                   ↓
          CONTROLLED VALIDATION
                   ↓
       PRIVILEGE ANALYSIS
                   ↓
              EVIDENCE
                   ↓
               REPORT
                   ↓
             REMEDIATION
```

### Final Deliverables

Create:

```text
Cybersecurity-60-Day/
│
├── README.md
│
├── notes/
│   ├── kali.md
│   ├── networking.md
│   ├── nmap.md
│   ├── enumeration.md
│   ├── web-security.md
│   ├── burp.md
│   ├── wireshark.md
│   ├── linux-privesc.md
│   ├── windows.md
│   ├── active-directory.md
│   └── python-security.md
│
├── projects/
│   ├── security-header-analyzer/
│   ├── log-analyzer/
│   ├── network-inventory/
│   └── security-report-generator/
│
├── ctf/
│   ├── machine-01.md
│   └── machine-02.md
│
└── reports/
    └── final-security-assessment.md
```

---

# 📊 60-DAY MASTER TRACKER

| Day | Topic            | Tool           | Practice           | Deliverable    |
| --: | ---------------- | -------------- | ------------------ | -------------- |
|  01 | Kali Setup       | Terminal       | VM/Lab             | Lab setup      |
|  02 | APT              | apt            | Packages           | Tool list      |
|  03 | Linux Security   | chmod/sudo     | Permissions        | Notes          |
|  04 | Processes        | ps/systemctl   | Services           | Process report |
|  05 | Networking       | ip/ss          | Network            | Diagram        |
|  06 | Security Basics  | —              | CIA/Risk           | Notes          |
|  07 | Assessment       | Kali           | Mini lab           | Report         |
|  08 | Recon            | whois          | Passive recon      | Notes          |
|  09 | DNS              | dig            | DNS lab            | DNS map        |
|  10 | Subdomains       | Amass          | Lab recon          | Results        |
|  11 | OSINT            | theHarvester   | Authorized target  | Report         |
|  12 | Nmap             | Nmap           | Port scan          | Results        |
|  13 | Nmap Advanced    | Nmap           | Enumeration        | Notes          |
|  14 | Mini CTF         | Nmap           | Recon              | Report         |
|  15 | Services         | Nmap           | Enumeration        | Notes          |
|  16 | FTP              | FTP            | Lab                | Findings       |
|  17 | SSH              | SSH            | Lab                | Notes          |
|  18 | SMB              | SMB tools      | Lab                | Findings       |
|  19 | Web Enum         | Gobuster       | Juice Shop/Lab     | Results        |
|  20 | Methodology      | Multiple       | Full enum          | Checklist      |
|  21 | Assessment       | Multiple       | Lab                | Report         |
|  22 | HTTP             | Browser/Burp   | Requests           | Notes          |
|  23 | Burp             | Burp Suite     | Proxy              | Lab report     |
|  24 | Auth             | Burp           | Web lab            | Findings       |
|  25 | Authorization    | Burp           | Access control lab | Findings       |
|  26 | Injection        | Burp           | OWASP lab          | Notes          |
|  27 | File Security    | Burp           | Web lab            | Findings       |
|  28 | OWASP            | Burp           | Labs               | Review         |
|  29 | Wireshark        | Wireshark      | Packet capture     | PCAP           |
|  30 | Packets          | Wireshark      | Analysis           | Report         |
|  31 | TCP              | Wireshark      | TCP analysis       | Notes          |
|  32 | DNS Traffic      | Wireshark      | DNS analysis       | Report         |
|  33 | HTTP Traffic     | Wireshark      | HTTP analysis      | Report         |
|  34 | Network Defense  | —              | Architecture       | Diagram        |
|  35 | Packet Project   | Wireshark      | Full analysis      | Report         |
|  36 | Linux PrivEsc    | Linux          | Lab                | Notes          |
|  37 | Linux Enum       | find/getcap    | Lab                | Findings       |
|  38 | Services         | systemd/cron   | Lab                | Findings       |
|  39 | Credentials      | Linux          | Lab                | Security notes |
|  40 | Windows          | Windows        | VM                 | Notes          |
|  41 | Windows Security | PowerShell     | VM                 | Report         |
|  42 | PrivEsc Lab      | Linux/Windows  | Lab                | Assessment     |
|  43 | AD               | Windows Server | Lab                | AD map         |
|  44 | Kerberos/LDAP    | AD tools       | Lab                | Diagram        |
|  45 | SMB/AD           | Net            |                    |                |
