# Cybersecurity Homelab

This homelab is a hands-on cybersecurity environment designed to simulate a small enterprise-style network with segmented infrastructure, Windows Active Directory, endpoint monitoring, network security monitoring, centralized logging, vulnerable systems, and honeypot telemetry.

The purpose of this lab is to build practical skills in Blue Team operations, security engineering, digital forensics and incident response, network monitoring, log analysis, and defensive architecture.

> **Security Note:** This homelab documentation is intentionally sanitized. Specific IP addresses, VLAN IDs, hostnames, management interfaces, firewall rules, credentials, and sensitive network details have been intentionally generalized before publication.

---

## Lab Objectives

The homelab is designed to help me practice and demonstrate:

* Enterprise-style network segmentation
* Firewall rule design and traffic control
* Active Directory administration and monitoring
* Windows endpoint logging and event forwarding
* Endpoint security monitoring with Wazuh
* Network security monitoring with Security Onion, Zeek, and Suricata
* Honeypot deployment and attacker behavior observation
* SIEM dashboarding and log analysis
* DFIR investigation workflow
* Safe separation between home, lab, management, storage, and honeypot networks
* Security engineering documentation and architecture thinking

---

## High-Level Architecture

The lab is built across VMware Workstation and Proxmox-based virtualization environments, with pfSense used for routing, segmentation, firewall policy enforcement, and traffic control.

At a high level, the lab includes the following security zones:

| Zone                       | Purpose                                                                     |
| -------------------------- | --------------------------------------------------------------------------- |
| Home Network               | Personal trusted devices and normal household usage                         |
| Management Network         | Administrative access to infrastructure and virtualization hosts            |
| Cybersecurity Lab Network  | Active Directory, Windows clients, Linux systems, and test services         |
| Monitoring Network         | SIEM, Wazuh, Security Onion, log collection, and network monitoring systems |
| Honeypot Network           | Isolated environment for observing unsolicited internet-facing activity     |
| Storage / NAS Network      | Backup and storage services separated from the main lab environment         |
| Vulnerable Systems Network | Intentionally vulnerable systems used only for controlled testing           |

The public version of the architecture intentionally avoids exact addressing and sensitive routing details.

```text
Internet
   |
[Edge Firewall / pfSense]
   |
   +-- Home Network
   |
   +-- Management Network
   |
   +-- Cybersecurity Lab Network
   |      +-- Windows Server / Active Directory
   |      +-- Windows 10 Client
   |      +-- Windows 11 Client
   |      +-- Linux Test Systems
   |      +-- Vulnerable Systems
   |
   +-- Monitoring Network
   |      +-- Wazuh
   |      +-- Security Onion
   |      +-- Elastic / DShield SIEM
   |      +-- Rocky Linux Log Server
   |
   +-- Honeypot Network
   |      +-- DShield Honeypot Sensor
   |
   +-- Storage / NAS Network
```

---

## Core Components

| Component                       | Purpose                                                        | Skills Practiced                                           |
| ------------------------------- | -------------------------------------------------------------- | ---------------------------------------------------------- |
| pfSense                         | Firewall, routing, NAT, DNS, NTP, segmentation, access control | Network security, firewall administration, traffic control |
| Proxmox                         | Virtualization platform for selected lab systems               | Virtualization, host networking, VM isolation              |
| VMware Workstation              | Desktop virtualization for lab systems                         | VM networking, lab deployment, endpoint testing            |
| Windows Server                  | Active Directory Domain Services, DNS, Group Policy            | Windows enterprise administration, identity basics         |
| Windows 10 / Windows 11 Clients | Domain-joined endpoints                                        | Endpoint logging, Windows event analysis                   |
| Windows Event Forwarding        | Centralized Windows event collection                           | Log forwarding, security monitoring, event correlation     |
| Wazuh                           | Endpoint monitoring and security event analysis                | HIDS, endpoint telemetry, alert triage                     |
| Security Onion                  | Network security monitoring platform                           | NSM, Zeek, Suricata, packet analysis                       |
| Zeek                            | Network metadata generation                                    | Connection analysis, protocol visibility                   |
| Suricata                        | IDS/IPS alerting engine                                        | Signature-based detection, alert review                    |
| DShield Honeypot                | Internet-facing honeypot telemetry                             | Threat observation, attack pattern review                  |
| DShield SIEM / Elastic          | Honeypot log analysis and dashboards                           | SIEM usage, search, dashboard review                       |
| Rocky Linux Log Server          | Centralized Linux logging practice                             | Syslog, Linux administration, log management               |
| Kali Linux                      | Controlled attacker/test system                                | Validation of detections in a lab-only environment         |
| SIFT Workstation                | DFIR analysis workstation                                      | Forensic analysis workflow                                 |
| Vulnerable Linux Systems        | Controlled vulnerable targets                                  | Detection testing, attack simulation, alert validation     |

---

## Current Build Status

The lab is currently in the **build, integration, and documentation phase**.

Completed or actively configured:

* Built a segmented cybersecurity homelab using VMware Workstation and Proxmox
* Configured pfSense firewall interfaces, routing, NAT, DNS, NTP, and firewall rules
* Created a Windows Active Directory domain
* Joined Windows 10 and Windows 11 systems to the domain
* Configured Group Policy baseline settings
* Configured Windows Event Forwarding with Windows clients and Active Directory server as event sources
* Deployed Wazuh for endpoint monitoring practice
* Deployed Security Onion for network security monitoring practice
* Deployed DShield Honeypot for observing unsolicited internet-facing activity
* Deployed DShield SIEM / Elastic for honeypot log review and dashboard analysis
* Began reviewing honeypot activity such as SSH brute-force and password spray behavior
* Designed separation between home, management, NAS, honeypot, and cybersecurity lab networks
* Practiced safe monitoring boundaries between honeypot systems and internal environments

---

## Lab Design Principles

### 1. Segmentation First

The lab is designed around separation of security zones. Home systems, management access, monitoring tools, vulnerable systems, honeypots, and storage services are kept logically separated.

This supports:

* Reduced blast radius
* Safer testing
* Clearer traffic flow
* Better monitoring placement
* More realistic enterprise-style design

---

### 2. Monitoring and Visibility

The lab uses multiple layers of monitoring:

| Monitoring Layer       | Tools / Sources                          |
| ---------------------- | ---------------------------------------- |
| Endpoint Monitoring    | Wazuh, Windows Event Logs                |
| Windows Log Collection | Windows Event Forwarding                 |
| Network Monitoring     | Security Onion, Zeek, Suricata           |
| Honeypot Monitoring    | DShield Honeypot, DShield SIEM / Elastic |
| Firewall Visibility    | pfSense logs                             |
| Linux Logging          | Syslog / Rocky Linux Log Server          |

The goal is to understand how different telemetry sources complement one another during security investigations.

---

### 3. Safe Honeypot Isolation

The honeypot environment is treated as a higher-risk zone because it is designed to observe unsolicited external activity.

Security considerations include:

* Keeping honeypot systems separated from trusted home and management networks
* Restricting communication paths between honeypot and internal systems
* Avoiding unnecessary access from honeypot systems into trusted environments
* Reviewing firewall rules carefully
* Sanitizing honeypot findings before publishing screenshots or logs

---

### 4. Enterprise-Style Windows Environment

The Windows portion of the lab is designed to simulate a small domain environment.

Current Windows lab components include:

* Windows Server running Active Directory Domain Services
* Domain-joined Windows 10 client
* Domain-joined Windows 11 client
* Group Policy configuration
* Windows Event Forwarding
* Windows security event analysis practice

This environment supports future investigation and monitoring projects involving authentication activity, privileged account usage, endpoint telemetry, and Windows event correlation.

---

### 5. Defensive Validation

The lab is intended to support controlled testing of defensive visibility.

Examples of future validation activities:

* Generate failed logon events and verify Windows Event Forwarding collection
* Review privileged logon events in Windows security logs
* Generate benign Nmap scans in the lab and review Zeek / Suricata output
* Review Wazuh endpoint alerts from Windows and Linux systems
* Observe SSH brute-force behavior against the DShield Honeypot
* Compare network, endpoint, firewall, and SIEM visibility for the same event

---

## Skills Demonstrated

This homelab is being used to demonstrate practical skills in:

### Security Engineering

* Network segmentation
* Firewall policy design
* Secure lab architecture
* System isolation
* Defensive infrastructure planning

### Blue Team Operations

* SIEM monitoring
* Alert triage
* Log review
* Event correlation
* Endpoint visibility
* Network visibility

### Digital Forensics and Incident Response

* Investigation scoping
* Timeline building
* Evidence review
* Windows event analysis
* Forensic workstation usage
* Incident documentation

### Network Security Monitoring

* Zeek log review
* Suricata alert analysis
* Packet capture concepts
* Connection analysis
* IDS/NSM deployment

### Windows Security

* Active Directory basics
* Group Policy
* Domain-joined endpoints
* Windows Event Forwarding
* Authentication event analysis

### Linux and Infrastructure

* Linux server administration
* Syslog concepts
* Virtualization
* Routing and NAT
* DNS and NTP configuration

---

## Roadmap

The lab is currently in the build and integration phase. 

The next phase of this homelab is to convert deployed lab components into documented security projects and investigation writeups.

Planned work includes:

* Sanitized architecture and log flow diagrams
* Windows Event Forwarding and Active Directory logging documentation
* DShield Honeypot SSH brute-force observation writeup
* DShield SIEM / Elastic dashboard analysis
* Security Onion investigation using Zeek and Suricata
* Wazuh endpoint monitoring use case
* DFIR practice case study
* Python log parser project
* Beginner cloud security lab projects

---

## Summary

This homelab is a long-term practical learning environment for developing cybersecurity skills across Blue Team operations, security engineering, DFIR, network monitoring, and defensive architecture.

The current focus is on building reliable lab infrastructure, collecting useful telemetry, and converting hands-on practice into clear, sanitized, portfolio-ready documentation.



