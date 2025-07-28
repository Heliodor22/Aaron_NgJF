# Aaron's Cybersecurity Homelab 

## Homelab Overview

This is a work-in-progress homelab system and document is a fully virtualized, enterprise-grade cybersecurity environment built using VMware Workstation Pro and segmented with pfSense firewall. It is designed to simulate real-world infrastructure for practicing Blue Team operations, log management, network monitoring, incident response, and vulnerability testing in a secure, isolated environment.

## Objectives

- Simulate enterprise network segmentation and traffic flow
- Gain hands-on experience with SIEM tools, IDS/IPS, log correlation, and system hardening
- Practice threat simulation and monitoring from attacker and defender perspectives

## Infrastructure Layout

| Component             | Role                                                                 |
|----------------------|----------------------------------------------------------------------|
| **pfSense**          | Firewall, NAT, VLAN segmentation, NTP                                |
| **Security Onion**   | Network Security Monitoring (NSM) using Suricata, Zeek, Kibana       |
| **Wazuh Manager**    | Host-based IDS, centralized log collection, and alerting             |
| **Rocky Log Server** | rsyslog server for centralized log collection and NAS log offloading |
| **Windows Server 2019** | Active Directory Domain Controller, DNS, GPO management          |
| **Windows 10/11 Pro**| Domain-joined endpoints for monitoring and testing                   |
| **Kali Linux**       | Attack simulation, CTFs, red teaming, internet-enabled               |
| **Metasploitable 2 / VulnLinux** | Vulnerable targets for exploitation and alert testing |
| **SIFT Workstation** | Digital forensics and incident response workstation                  |

## Network Segmentation
- WAN (Bridged) – pfSense WAN for internet access
- OPT/VLANs – Internal LAN segments for:
    - Windows AD infrastructure
    - Blue Team - Security Monitoring, Forensics and Incident Response
    - SIEM - IDS Monitoring
    - Red Team - Attacker Simulation
    - Other Endpoints - Endpoint Machines Simulation

## Tools & Technologies

- **SIEM**: Wazuh, ELK Stack, Security Onion
- **Firewall**: pfSense
- **NSM**: Suricata, Zeek, Hunt, Kibana, Wireshark
- **Log Management**: rsyslog, Filebeat, Winlogbeat
- **Threat Simulation**: Metasploit, Nmap, Hashcat, Kali tools
- **DFIR**: SIFT, CyberChef, Log analysis
- **Endpoint Monitoring**: Osquery, Wazuh Agent, Security Onion Fleet

## Key Features
- Multiple Interfaces/subnets via pfSense for segmented lab traffic
- Sysmon/Windows Event Forwarding to centralized log servers
- Full packet capture and detection through Security Onion
- Realistic log ingestion with retention, parsing, and visualization
- Hardened systems (e.g., no direct internet access to Security Onion, Windows 11, etc.)
- Periodic snapshots for rollback and repeatable simulations
