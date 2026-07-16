
# Brute Force & Account Compromise Investigation Lab

## Overview

This repository demonstrates an end-to-end Security Operations Center (SOC) investigation of a simulated Windows account compromise. The project focuses on detection engineering, threat hunting, incident response, and forensic analysis using enterprise security platforms including Splunk Enterprise, Microsoft Defender for Endpoint, Microsoft Sentinel, Sysmon, and Windows Security Event Logs.

The objective was not simply to generate alerts, but to perform a complete investigation by collecting evidence, correlating telemetry across platforms, reconstructing the attack timeline, mapping activity to the MITRE ATT&CK framework, documenting indicators of compromise (IOCs), and producing a professional incident response report.

---

# Objectives

- Simulate a brute-force attack against a Windows endpoint.
- Detect failed and successful authentication events.
- Investigate privilege escalation and administrative activity.
- Capture endpoint telemetry with Sysmon.
- Centralize Windows logs in Splunk Enterprise.
- Validate findings in Microsoft Defender and Microsoft Sentinel.
- Perform threat hunting using SPL and KQL.
- Produce SOC-ready documentation and evidence.

---

# Lab Architecture

## Infrastructure

| Component | Purpose |
|-----------|---------|
| Windows 11 Endpoint | Attack target |
| Ubuntu Server | Splunk Enterprise |
| Splunk Universal Forwarder | Log forwarding |
| Sysmon | Endpoint telemetry |
| Microsoft Defender for Endpoint | EDR visibility |
| Microsoft Sentinel | SIEM and threat hunting |
| Azure Virtual Network | Lab infrastructure |

---

# Simulated Attack Scenario

1. Multiple failed logon attempts (Event ID 4625).
2. Successful authentication (Event ID 4624).
3. Administrative PowerShell execution.
4. Privilege verification (`whoami /priv`, `whoami /groups`).
5. Administrator group enumeration.
6. Host, process, user, and network discovery.
7. SOC investigation and evidence correlation.

---

# Technologies

- Microsoft Azure
- Windows 11
- Ubuntu Linux
- Splunk Enterprise 10.x
- Splunk Universal Forwarder
- Sysmon
- Microsoft Defender for Endpoint
- Microsoft Sentinel
- Windows Event Viewer
- PowerShell

---

# MITRE ATT&CK Coverage

| Tactic | Technique | ID |
|---------|-----------|----|
| Initial Access | Brute Force | T1110 |
| Initial Access | Valid Accounts | T1078 |
| Execution | PowerShell | T1059.001 |
| Discovery | Process Discovery | T1057 |
| Discovery | System Information Discovery | T1082 |
| Discovery | Account Discovery | T1033 |
| Discovery | Permission Groups Discovery | T1069 |
| Discovery | Local Group Discovery | T1069.001 |
| Discovery | Network Discovery | T1016 |
| Discovery | Network Connections Discovery | T1049 |

---

# Investigation Workflow

1. Collect Windows Security and Sysmon logs.
2. Forward telemetry to Splunk.
3. Identify failed and successful logons.
4. Investigate PowerShell execution.
5. Correlate Defender timeline with Splunk evidence.
6. Perform Sentinel hunting.
7. Build attack timeline.
8. Document IOCs.
9. Produce incident report.

---

# Repository Structure

```text
Brute-Force-Account-Compromise-Lab
├── Incident_Report.pdf
├── IOC_Tracker.xlsx
├── Attack_Timeline.xlsx
├── MITRE_ATT&CK_Mapping.docx
├── Splunk_Investigation_Guide.docx
├── Microsoft_Sentinel_Hunting_Guide.docx
├── Containment_Remediation_Plan.docx
├── README.md
├── Queries/
├── Screenshots/
├── Diagrams/
└── Reports/
```

---

# Skills Demonstrated

- Security Operations Center (SOC)
- Incident Response
- Threat Hunting
- Splunk SPL
- Microsoft Sentinel KQL
- Microsoft Defender for Endpoint
- Sysmon Analysis
- Windows Event Analysis
- Authentication Investigation
- IOC Development
- MITRE ATT&CK Mapping
- Detection Engineering
- Log Correlation
- Digital Forensics
- Technical Reporting

---

# References

- MITRE ATT&CK Framework
- Microsoft Defender for Endpoint Documentation
- Microsoft Sentinel Documentation
- Splunk Enterprise Documentation
- Microsoft Sysmon Documentation

---

# License

This repository is intended for educational, research, and portfolio purposes. All attack simulations were performed within an isolated lab environment.
