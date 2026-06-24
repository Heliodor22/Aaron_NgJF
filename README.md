# Aaron Ng Ji Fu — Cybersecurity Portfolio

### About Me

Cybersecurity career changer focused on Blue Team operations, digital forensics and incident response, security engineering, and cloud security.

I am currently pursuing a Bachelor’s Degree in Applied Cybersecurity with the SANS Technology Institute, graduating in early September 2026 and building a practical cybersecurity portfolio through homelabs, CTFs, detection engineering practice, log analysis, and security infrastructure projects.

This repository documents my hands-on work with enterprise-style defensive environments, including pfSense, Active Directory, Windows Event Forwarding, Wazuh, Security Onion, DShield Honeypot, Elastic, Suricata, Zeek, and DFIR tooling.

My long-term goal is to grow into cybersecurity architecture by building strong hands-on foundations in security operations, infrastructure security, incident response, detection engineering, and cloud security.

---

## Target Cybersecurity Roles

I am building practical skills toward the following areas:

* Security Engineer
* SOC Analyst / Blue Team Analyst
* Digital Forensics and Incident Response
* Threat Hunting
* Cloud Security
* Future goal: Cybersecurity Architect

---

## Current Focus Areas

### Blue Team Operations

* SIEM monitoring and alert triage
* Log analysis and event correlation
* Windows Event Forwarding
* Endpoint monitoring with Wazuh
* Network security monitoring with Security Onion, Suricata, and Zeek
* Firewall rule design and traffic segmentation with pfSense

### Digital Forensics and Incident Response

* Incident investigation workflow
* Evidence preservation concepts
* Timeline analysis
* Windows security event analysis
* Memory and disk forensics learning path
* DFIR tooling practice through SANS, CTFs, and lab environments

### Network and Infrastructure Security

* pfSense firewall configuration
* VLAN/subnet segmentation
* IDS/IPS placement and tuning
* Honeypot network monitoring
* Syslog collection
* Secure Active Directory lab design
* Linux and Windows server administration

### Cloud Security

* Cloud security fundamentals
* Identity and access management concepts
* Cloud logging and monitoring
* Cloud misconfiguration awareness
* CSA CCSK knowledge foundation

---

## Certifications and Education

### In Progress

* Bachelor’s Degree in Applied Cybersecurity — SANS Technology Institute
* Upcoming - GIAC Machine Learning Engineer (GMLE)

### Completed Cybersecurity Certifications

* GIAC Certified Forensic Analyst (GCFA)
* GIAC Certified Intrusion Analyst (GCIA)
* GIAC Continuous Monitoring Certification (GMON)
* GIAC Certified Python Coder (GPYC)
* GIAC Certified Incident Handler (GCIH)
* GIAC Security Essentials (GSEC)
* GIAC Information Security Fundamentals (GISF)
* GIAC Foundational Cybersecurity Technologies (GFACT)
* Certificate of Cloud Security Knowledge v5 (Cloud Security Alliance)
* ISC2 Certified in Cybersecurity (CC)
* Cisco CCNA

### Previous Education

* Bachelor of Dramatic Arts (Production)

---

## Cybersecurity Homelab

My homelab is designed to simulate a small enterprise environment with segmented networks, defensive monitoring, endpoint logging, vulnerable systems, and honeypot telemetry.

### Core Lab Components

| Component                       | Purpose                                                                                | Skills Demonstrated                                          |
| ------------------------------- | -------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| pfSense Firewall                | Network segmentation, routing, firewall rules, NAT, NTP, DNS control, IDS/IPS planning | Network security, firewall administration, access control    |
| Windows Server Active Directory | Domain controller, DNS, Group Policy, domain-joined Windows clients                    | Active Directory administration, Windows enterprise security |
| Windows 10 / Windows 11 Clients | Domain-joined endpoint simulation                                                      | Endpoint monitoring, Windows event analysis                  |
| Windows Event Forwarding        | Centralized Windows event collection from AD and clients                               | Log forwarding, event correlation, detection preparation     |
| Wazuh                           | Endpoint monitoring and security event analysis                                        | HIDS, policy monitoring, endpoint telemetry                  |
| Security Onion                  | Network security monitoring using Zeek and Suricata                                    | IDS, network traffic analysis, packet-based investigation    |
| DShield Honeypot                | Internet-facing honeypot telemetry collection                                          | Threat observation, attacker behavior analysis               |
| DShield SIEM / Elastic          | Dashboarding and analysis of honeypot logs                                             | SIEM usage, log parsing, attack trend observation            |
| Rocky Linux Log Server          | Linux syslog and centralized logging practice                                          | Linux administration, log management                         |
| Vulnerable Linux Systems        | Controlled attack and detection testing                                                | Detection validation, attack simulation                      |
| Kali Linux                      | Controlled attacker machine for lab testing                                            | Ethical hacking workflow, validation of defensive controls   |
| SIFT Workstation                | DFIR analysis workstation                                                              | Forensics tooling and investigation workflow                 |

---

## Current Homelab Progress

Completed or actively configured:

* Built a segmented VMware and Proxmox-based cybersecurity lab
* Configured pfSense firewall routing, NAT, DNS, NTP, and interface rules
* Created a Windows Active Directory domain
* Joined Windows 10 and Windows 11 clients to the AD domain
* Configured Group Policy baseline settings
* Configured Windows Event Forwarding from Windows clients and AD server
* Deployed Wazuh for endpoint monitoring
* Deployed Security Onion for network security monitoring
* Built a DShield Honeypot environment
* Built a DShield SIEM / Elastic dashboarding environment
* Investigated SSH brute-force and password spray activity in honeypot logs
* Designed isolation between home, management, NAS, honeypot, and cybersecurity lab networks
* Practiced safe monitoring boundaries between honeypot traffic and internal systems

---

## Capture The Flag and Practical Challenges

### National Cyber League / Cyber Skyline

Recent NCL results and scouting reports are included in this repository.

* NCL Spring 2026 — 100th Percentile Overall Team Game
* NCL Spring 2026 — 96th Percentile Overall Individual Game
* NCL Fall 2025 — 99th Percentile Overall Team Game
* NCL Fall 2025 — 97th Percentile Overall Individual Game
* NCL Spring 2025 — 99th Percentile Overall Team Game
* NCL Spring 2025 — 98th Percentile Overall Individual Game
* NCL Fall 2024 — 82nd Percentile Overall Team Game
* NCL Fall 2024 — 72nd Percentile Overall Individual Game

### Other Practice Platforms

* TryHackMe: 140+ rooms completed
* TryHackMe Cybersecurity 101 completed
* TryHackMe Cybersecurity Engineer pathway in progress
* Planning to progress through SOC Analyst learning path
* OverTheWire Bandit completed through Level 34
* National Cyber League CyberSkyline Professional practice

---

## Technical Skills

### Security Tools

* Wazuh
* Security Onion
* Elastic / Kibana
* Suricata
* Zeek
* pfSense
* DShield Honeypot
* SIFT Workstation
* Volatility / MemProcFs learning path
* Wireshark
* Nmap
* Kali Linux

### Operating Systems

* Windows Server
* Windows 10 / Windows 11
* Rocky Linux
* Ubuntu
* Kali Linux
* pfSense
* Proxmox
* VMware Workstation

### Defensive Security

* SIEM monitoring
* Endpoint monitoring
* Network security monitoring
* Log analysis
* Windows event analysis
* Incident response fundamentals
* Firewall rule design
* IDS/IPS concepts
* Honeypot monitoring
* Threat detection fundamentals

### Infrastructure

* Active Directory
* Group Policy
* DNS
* DHCP
* NTP
* NAT
* VLANs and subnetting
* Syslog
* Centralized logging
* Virtualization
* NAS-aware network design

### Programming and Scripting

* Python
* Bash fundamentals
* PowerShell fundamentals
* Log parsing concepts
* Automation scripting

---

## Previous Professional Background

Before transitioning into cybersecurity, I worked in Audio-Visual, Lighting, CCTV and Control systems at Resorts World Sentosa Singapore, supporting infrastructure across Universal Studios Singapore and other resort attractions.

This experience gave me a strong foundation in:

* Enterprise operations
* Technical troubleshooting
* Infrastructure reliability
* Vendor coordination
* Team leadership
* Documentation
* Risk awareness
* Operational discipline

I was promoted multiple times across my career and regularly handled responsibilities involving system reliability, incident response, team coordination, and operational continuity.

---

## Portfolio Projects in Progress

The following projects are being developed from my cybersecurity homelab as I continue collecting logs, testing detections, and documenting investigation workflows.

* Homelab architecture
* Windows Event Forwarding and Active Directory Logging
* DShield Honeypot Attack Observations
* Security Onion, Zeek, and Suricata Network Monitoring
* Wazuh Endpoint Monitoring Use Case
* DFIR Practice Case Studies

Upcoming additions may include:

* Detailed homelab network diagrams
* DShield honeypot attack observations
* Wazuh detection notes
* Security Onion investigation walkthroughs
* Windows Event Forwarding documentation
* Active Directory hardening notes
* Python log parser projects
* Cloud security mini-projects

---

 ## Other Certificates and Short Courses
* Cybersecurity Related Udemy Courses
* WSQ Work as a Team
* Personal Effectiveness
* ENiBLE Aspiring Supervisors Program
* Greensafe International WSH and Risk Management Courses
* ICDL Advanced Excel Course
* Work at Height Course
* Fundamentals of Fiber Optics Testing Workshop
* Troubleshooting your CCTV Networks with LINKIQ
* Fundamentals of Network Copper Testing Workshop
* Q-Sys Audio DSP Lvl 1 & 2 Certificate
* Q-Sys Control 101 & 102
* Audinate Dante Lvl 1-3(2019)
* ETC Lighting Systems (Various)
* BoomLift, ScissorLift, Personal Platform Operator Course (2022)

---

## Contact

This portfolio is maintained as part of my cybersecurity career transition and continuous learning journey.

* **GitHub:** [Heliodor22](https://github.com/Heliodor22)
* **Linkedin** [Aaron Ng](https://www.linkedin.com/in/aaron-ng-52a51255/)
---
