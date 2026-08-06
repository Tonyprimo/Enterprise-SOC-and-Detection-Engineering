# Detection Engineering

This folder contains the custom Splunk detections developed throughout the Enterprise SOC Lab.

## Objectives

- Detect common Windows attack techniques
- Map detections to MITRE ATT&CK
- Validate detections using controlled lab activity
- Document detection logic and expected behavior

## Technologies

- Splunk Enterprise
- SPL
- Sysmon
- Windows Security Logs
- PowerShell Operational Logs

## Detection Library

| Detection | Data Source | Status |
|-----------|------------|--------|
| PowerShell Execution | Sysmon / PowerShell | Complete |
| Command Prompt Execution | Sysmon | Complete |
| Certutil Execution | Sysmon | Complete |
| Local Administrator Changes | Windows Security | Complete |
| Domain Account Creation | Windows Security | Complete |
| Service Installation | Windows Security | Complete |
