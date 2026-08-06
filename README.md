# Enterprise-SOC-and-Detection-Engineering
Enterprise SOC lab featuring Active Directory, Splunk SIEM, Sysmon, Group Policy, detection engineering, and incident response
---

# Project Overview

This project documents the design, deployment, hardening, monitoring, and defense of a simulated enterprise Windows environment using VMware Workstation. The lab was built to develop practical Security Operations Center (SOC) skills commonly used by enterprise cybersecurity teams.

The environment was developed over twelve structured sprints, beginning with infrastructure deployment and ending with a complete incident response investigation. Throughout the project, Windows security events, Sysmon telemetry, and PowerShell logging were centralized into Splunk Enterprise to create a fully functioning enterprise monitoring environment.

The project emphasizes real-world SOC workflows including:

- Active Directory administration
- Enterprise Windows security
- SIEM administration
- Detection engineering
- Threat hunting
- Incident response
- Vulnerability management
- Security hardening
- Security documentation

---

# Objectives

- Build an enterprise Active Directory environment
- Deploy centralized logging with Splunk Enterprise
- Collect Windows Security, Sysmon, and PowerShell telemetry
- Develop custom detections using SPL
- Create SOC dashboards, reports, and alerts
- Perform structured threat hunting
- Conduct vulnerability assessments
- Execute an end-to-end incident response investigation
- Document all work in an enterprise-style portfolio

---

## Repository Contents

-  [Architecture](architecture/)
-  [Detection Engineering](detection-engineering/)
-  [Vulnerability Management](vulnerability-management/)
-  [Incident Response](incident-response/)
-  [Sprint Logs](sprint-logs/)
-  [Screenshots](screenshots/)

---

# Lab Architecture

```
Host Laptop
│
└── VMware Workstation Pro
    │
    ├── DC01
    │   ├── Windows Server 2022
    │   ├── Active Directory Domain Services
    │   ├── DNS
    │   ├── Group Policy
    │   ├── Sysmon
    │   └── Splunk Universal Forwarder
    │
    ├── WIN11-01
    │   ├── Windows 11 Enterprise
    │   ├── Domain Joined
    │   ├── Microsoft Defender
    │   ├── Sysmon
    │   ├── PowerShell Logging
    │   └── Splunk Universal Forwarder
    │
    └── SIEM01
        ├── Windows Server 2022
        ├── Splunk Enterprise
        ├── Windows Event Index
        ├── Sysmon Index
        ├── PowerShell Index
        ├── Dashboards
        ├── Reports
        └── Alerts
```

---

# Environment

| Host | Role | Operating System |
|------|------|------------------|
| DC01 | Domain Controller | Windows Server 2022 |
| WIN11-01 | Enterprise Workstation | Windows 11 Enterprise |
| SIEM01 | Splunk SIEM | Windows Server 2022 |

---

# Technologies Used

## Infrastructure

- VMware Workstation Pro
- Windows Server 2022
- Windows 11 Enterprise
- Active Directory
- DNS
- Group Policy

## Security

- Splunk Enterprise
- Splunk Universal Forwarder
- Microsoft Sysmon
- Microsoft Defender
- Windows Defender Firewall
- Windows Event Logging
- PowerShell Script Block Logging

## Detection Engineering

- SPL (Search Processing Language)
- MITRE ATT&CK Mapping
- Custom Detection Rules
- Scheduled Alerts
- Threat Hunting Queries

---

# Sprint Roadmap

## Sprint 1
### VMware & Windows Server Deployment

- Built VMware environment
- Installed Windows Server 2022
- Configured networking
- Established enterprise lab foundation

---

## Sprint 2
### Active Directory & DNS

- Installed AD DS
- Promoted DC01
- Configured DNS
- Created corp.lab domain

---

## Sprint 3
### Active Directory Administration

- Organizational Units
- Administrative accounts
- Security groups
- Delegation concepts

---

## Sprint 4
### Windows Enterprise Workstation

- Installed Windows 11 Enterprise
- Joined workstation to domain
- Verified authentication
- Tested enterprise connectivity

---

## Sprint 5
### Security Hardening & Sysmon

- Installed Sysmon
- Configured audit policies
- Enabled PowerShell logging
- Applied Group Policy hardening

---

## Sprint 6
### Splunk SIEM Deployment

- Installed Splunk Enterprise
- Configured Universal Forwarders
- Created indexes
- Validated centralized logging

---

## Sprint 7
### SOC Dashboard & Threat Hunting

- Built SOC Overview dashboard
- Created reports
- Developed threat hunting searches
- Validated event visibility

---

## Sprint 8
### Detection Engineering

Developed detections for:

- PowerShell
- CMD
- Certutil
- Service creation
- Local administrators
- Account creation
- Failed authentication
- Network activity

---

## Sprint 9
### Detection Validation

- Tested detections
- Generated Windows telemetry
- Tuned searches
- Validated Splunk alerts

---

## Sprint 10
### Endpoint Hardening

- Microsoft Defender review
- Firewall validation
- Local administrator auditing
- PowerShell logging
- Group Policy improvements

---

## Sprint 11
### Vulnerability Management

- Asset inventory
- Patch assessment
- Software inventory
- Defender assessment
- Firewall assessment
- Listening port review
- SMBv1 validation
- Vulnerability findings
- Risk prioritization
- Remediation planning
- Validation

---

## Sprint 12
### Incident Response

Simulated:

- PowerShell activity
- Command Prompt execution
- Certutil execution
- Active Directory account creation
- Privilege escalation
- Security investigation
- Containment
- Remediation
- Executive reporting

---

# Security Controls

- Active Directory
- Group Policy
- Windows Defender
- Windows Firewall
- Sysmon
- PowerShell Script Block Logging
- Windows Security Auditing
- Splunk Universal Forwarder

---

# SIEM Implementation

Splunk Enterprise was configured to ingest:

- Windows Security Logs
- Sysmon Operational Logs
- PowerShell Operational Logs

The SIEM provides:

- Centralized log collection
- Dashboards
- Reports
- Alerts
- Threat hunting
- Investigation workflows

---

# Detection Engineering

Developed detections include:

- PowerShell Execution
- Encoded PowerShell
- Command Prompt Execution
- Certutil Activity
- Service Installation
- Local Administrator Changes
- New Domain Accounts
- Failed Logons
- Successful Logons
- Windows Defender Changes
- PowerShell Script Block Logging

Each detection includes:

- SPL search
- MITRE ATT&CK mapping
- Validation
- Documentation

---

# Vulnerability Management

Performed:

- Asset Inventory
- Patch Assessment
- Software Inventory
- Microsoft Defender Review
- Windows Firewall Review
- Local Administrator Audit
- Listening Port Analysis
- SMBv1 Review
- Remote Desktop Review
- PowerShell Logging Validation

Produced:

- Findings Register
- Risk Ratings
- Remediation Plan
- Validation Documentation

---

# Incident Response

Conducted a complete incident response exercise including:

- Event identification
- Timeline creation
- Evidence collection
- Investigation
- Severity assessment
- Containment
- Remediation
- Validation
- Executive reporting

---

# Skills Demonstrated

- Active Directory Administration
- Windows Security
- Enterprise Networking
- DNS Administration
- Group Policy
- SIEM Administration
- Splunk Enterprise
- Splunk Universal Forwarder
- SPL Query Development
- Detection Engineering
- Threat Hunting
- Sysmon Administration
- Windows Event Analysis
- PowerShell Logging
- Security Monitoring
- Vulnerability Management
- Risk Assessment
- Incident Response
- Security Documentation
- MITRE ATT&CK Mapping

---

# Repository Structure

```
Enterprise-SOC-Lab/
│
├── detection-engineering/
├── vulnerability-management/
├── incident-response/
├── dashboards/
├── screenshots/
├── sprint-logs/
└── README.md
```

---

# Key Deliverables

- Enterprise Active Directory environment
- Splunk SIEM deployment
- Sysmon implementation
- Security dashboards
- Detection library
- Threat hunting reports
- Scheduled alerts
- Vulnerability assessment
- Incident response investigation
- Executive documentation

---

# Screenshots

Recommended screenshots:

- Lab architecture
- VMware environment
- Active Directory Users and Computers
- Group Policy
- Sysmon installation
- Splunk indexes
- SOC Dashboard
- Detection searches
- Alerts
- Reports
- Threat hunting
- Incident timeline
- Vulnerability assessment
- Incident response investigation

---

# Lessons Learned

This project reinforced the importance of centralized logging, endpoint visibility, layered security controls, and structured investigation methodologies. Building the environment from the ground up provided practical experience with enterprise Windows administration, SIEM engineering, detection development, vulnerability management, and incident response.

The project also highlighted the operational challenges of enterprise environments, including troubleshooting log forwarding, validating telemetry, tuning detections, and maintaining security visibility while implementing configuration changes.

---

# Resume Highlights

- Built a multi-system enterprise Active Directory lab using VMware Workstation, Windows Server 2022, and Windows 11 Enterprise.
- Deployed Splunk Enterprise and centralized Windows Security, Sysmon, and PowerShell telemetry using Universal Forwarders.
- Developed custom SPL detections, dashboards, reports, and alerts mapped to MITRE ATT&CK techniques.
- Conducted structured threat hunting, vulnerability management, and incident response investigations using enterprise security workflows.
- Documented security architecture, detections, remediation plans, and executive reporting in a production-style portfolio.

---

# Disclaimer

This environment was built exclusively for educational purposes in an isolated virtual lab. All security testing, detections, and incident response activities were performed on systems owned and controlled by the author. No unauthorized testing was conducted against external systems.
