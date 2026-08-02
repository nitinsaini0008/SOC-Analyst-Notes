# EDR and XDR

## About

Endpoint Detection and Response (EDR) and Extended Detection and Response (XDR) are modern cybersecurity technologies designed to detect, investigate, and respond to security threats across endpoints and enterprise environments.

SOC Analysts use EDR and XDR platforms to monitor endpoint activities, investigate suspicious behavior, contain attacks, and automate incident response.

---

# What is EDR?

Endpoint Detection and Response (EDR) focuses on monitoring and protecting endpoint devices such as:

- Laptops
- Desktops
- Servers
- Virtual Machines

EDR continuously records endpoint activities and generates alerts when suspicious behavior is detected.

---

# What is XDR?

Extended Detection and Response (XDR) expands EDR by collecting and correlating security data from multiple sources.

These include:

- Endpoints
- Email
- Identity
- Cloud
- Firewall
- Network
- Applications
- SIEM

XDR provides a unified view of security events across the organization.

---

# EDR vs XDR

| EDR | XDR |
|------|------|
| Protects Endpoints | Protects Entire Environment |
| Endpoint Visibility | Cross-Domain Visibility |
| Endpoint Investigation | Centralized Investigation |
| Limited Correlation | Advanced Correlation |
| Endpoint Focus | Organization-Wide Focus |

---

# Why EDR and XDR are Important

They help organizations:

- Detect Malware
- Identify Ransomware
- Stop Credential Theft
- Detect Lateral Movement
- Investigate Incidents
- Reduce Response Time
- Improve Visibility

---

# EDR Architecture

```
Endpoint

↓

EDR Agent

↓

EDR Console

↓

SOC Analyst

↓

Incident Response
```

---

# XDR Architecture

```
Endpoints

Email

Firewall

Cloud

Identity

↓

XDR Platform

↓

Correlation Engine

↓

SOC Analyst

↓

Automated Response
```

---

# Common EDR Features

- Process Monitoring
- File Monitoring
- Registry Monitoring
- Network Connection Monitoring
- Threat Detection
- Malware Detection
- Ransomware Detection
- Endpoint Isolation
- Live Response

---

# Common XDR Features

- Multi-Source Data Collection
- Threat Correlation
- Threat Intelligence Integration
- Automated Investigation
- Incident Timeline
- Automated Response
- AI-Based Detection

---

# Common EDR Events

- Process Created
- Process Terminated
- File Created
- Registry Modified
- Network Connection
- PowerShell Execution
- USB Device Connected
- New Service Created

---

# Common Detection Scenarios

## Ransomware

Indicators

- Mass File Encryption
- File Renaming
- High CPU Usage
- Shadow Copy Deletion

---

## Credential Theft

Indicators

- LSASS Access
- Credential Dumping
- Privilege Escalation

---

## PowerShell Abuse

Indicators

- EncodedCommand
- DownloadString
- Invoke-Expression

---

## Lateral Movement

Indicators

- PsExec
- Remote PowerShell
- RDP Login
- SMB Connections

---

# Response Actions

EDR/XDR platforms allow analysts to:

- Isolate Endpoint
- Kill Process
- Quarantine File
- Block Hash
- Block IP Address
- Disable User Account
- Collect Forensic Data

---

# Popular EDR/XDR Solutions

- Microsoft Defender XDR
- CrowdStrike Falcon
- SentinelOne
- Sophos Intercept X
- Trellix HX
- VMware Carbon Black
- Cortex XDR

---

# EDR Investigation Workflow

```
Alert Generated

↓

Review Alert

↓

Analyze Process Tree

↓

Check Network Connections

↓

Review File Activity

↓

Contain Threat

↓

Document Incident
```

---

# Best Practices

- Deploy Agents on All Endpoints
- Keep Detection Rules Updated
- Investigate High-Severity Alerts First
- Enable Automatic Isolation
- Integrate with SIEM
- Review Endpoint Activity Regularly
- Update Threat Intelligence Feeds
- Perform Regular Threat Hunting

---

# Real-Life Example

An employee opens a malicious email attachment.

The EDR agent detects:

- PowerShell execution with an encoded command.
- A new executable dropped into the Downloads folder.
- Communication with a known malicious IP.
- An attempt to access **lsass.exe**.

The EDR platform automatically isolates the endpoint.

The SOC Analyst investigates the alert, confirms malware execution, blocks the file hash and IP address, resets the user's credentials, and restores the affected system.

---

# Interview Questions

1. What is EDR?
2. What is XDR?
3. What is the difference between EDR and XDR?
4. What are common EDR response actions?
5. How does EDR detect ransomware?
6. What is endpoint isolation?
7. Name five EDR/XDR tools.
8. Why is process tree analysis important?
9. How does XDR improve threat detection?
10. How do SOC Analysts use EDR during incident response?

---

# Summary

Topics Covered

- EDR
- XDR
- EDR vs XDR
- Architecture
- Endpoint Monitoring
- Threat Detection
- Response Actions
- Investigation Workflow
- Popular Tools
- Best Practices
- Interview Questions

EDR and XDR are essential technologies in modern SOC environments. They provide deep visibility into endpoint and enterprise-wide activities, enabling analysts to detect, investigate, contain, and respond to cyber threats quickly and effectively.

**End of File**
