# Architecture
## Technology Stack

| Layer | Technology |
|---|---|
| Virtualization | VMware Workstation Pro |
| Domain Services | Active Directory Domain Services |
| DNS | Microsoft DNS |
| Server Operating System | Windows Server 2022 |
| Endpoint Operating System | Windows 11 Enterprise |
| SIEM | Splunk Enterprise 10.4.2 |
| Log Forwarding | Splunk Universal Forwarder |
| Endpoint Telemetry | Microsoft Sysmon |
| Endpoint Protection | Microsoft Defender Antivirus |
| Host Firewall | Windows Defender Firewall |
| Endpoint Management | Group Policy |
| Security Logging | Windows Event Logs |
| PowerShell Visibility | PowerShell Script Block Logging |
| Detection Language | Splunk Search Processing Language (SPL) |
| Detection Framework | MITRE ATT&CK |
| Vulnerability Management | Manual Windows security and configuration assessment |
| Incident Response | Splunk-based investigation, evidence collection, containment, and remediation |

---

## Data Flow

```text
DC01
├── Windows Security Logs
├── Windows System Logs
├── Sysmon Operational Logs
└── Splunk Universal Forwarder
          │
          │ TCP 9997
          ▼
       SIEM01
  Splunk Enterprise
          ▲
          │ TCP 9997
          │
WIN11-01
├── Windows Security Logs
├── Windows System Logs
├── Windows Application Logs
├── Sysmon Operational Logs
├── PowerShell Operational Logs
└── Splunk Universal Forwarder

Windows and Sysmon Events
          │
          ▼
Splunk Universal Forwarder
          │
          ▼
Splunk Enterprise on SIEM01
          │
          ├── windows index
          ├── sysmon index
          └── powershell index
          │
          ▼
SOC Monitoring and Analysis
          │
          ├── Dashboards
          ├── Reports
          ├── Scheduled Alerts
          ├── Threat Hunting
          ├── Detection Engineering
          ├── Vulnerability Monitoring
          └── Incident Response
