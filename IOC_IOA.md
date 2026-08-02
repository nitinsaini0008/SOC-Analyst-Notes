# IOC and IOA (Indicators of Compromise & Indicators of Attack)

## About

Indicators of Compromise (IOCs) and Indicators of Attack (IOAs) are essential concepts in cybersecurity used by SOC Analysts, Threat Hunters, and Incident Responders to detect and investigate malicious activity.

While **IOCs** indicate that a system has likely been compromised, **IOAs** focus on attacker behavior and techniques that may reveal an attack in progress, even before a compromise is confirmed.

---

# What is an IOC?

An Indicator of Compromise (IOC) is a piece of forensic evidence that suggests a system, network, or device has been compromised.

Examples

- Malicious IP Address
- Malicious Domain
- File Hash (MD5, SHA-256)
- Registry Changes
- Suspicious File
- Malware Signature
- Command and Control (C2) Server

---

# What is an IOA?

An Indicator of Attack (IOA) identifies suspicious attacker behavior instead of known malicious artifacts.

Examples

- PowerShell Executing Encoded Commands
- Credential Dumping
- Lateral Movement
- Privilege Escalation
- Process Injection
- Suspicious Parent-Child Processes

---

# IOC vs IOA

| IOC | IOA |
|------|------|
| Evidence of compromise | Evidence of attacker behavior |
| Reactive detection | Proactive detection |
| Detects known threats | Detects unknown threats |
| Based on artifacts | Based on techniques |
| Easier to evade | Harder to evade |

---

# Common IOC Examples

## Network IOCs

- Malicious IP Address
- Suspicious Domain
- URL
- DNS Requests
- C2 Server Address

---

## File IOCs

- MD5 Hash
- SHA-1 Hash
- SHA-256 Hash
- Malicious Executable
- Suspicious DLL

---

## Host IOCs

- Registry Changes
- Scheduled Tasks
- New User Account
- Startup Folder Entries
- Unauthorized Services

---

## Email IOCs

- Malicious Attachment
- Phishing URL
- Fake Sender Address
- Suspicious Subject Line

---

# Common IOA Examples

- PowerShell with EncodedCommand
- CMD Launching PowerShell
- Office Application Spawning CMD
- LSASS Access
- Process Injection
- RDP Login Followed by Privilege Escalation
- Multiple Failed Logins Followed by Success
- Unusual Account Activity
- Data Compression Before Network Transfer

---

# IOC Sources

SOC Analysts obtain IOCs from:

- Threat Intelligence Feeds
- VirusTotal
- MISP
- AlienVault OTX
- Security Vendors
- Incident Response Reports
- Malware Analysis

---

# IOC Lifecycle

```
Threat Intelligence

↓

IOC Collected

↓

SIEM Detection Rule

↓

Alert Generated

↓

SOC Investigation

↓

Incident Response
```

---

# IOA Detection Workflow

```
User Activity

↓

Behavior Analysis

↓

Suspicious Pattern

↓

Detection Rule

↓

SOC Investigation
```

---

# IOC Examples in SIEM

Malicious IP Search

```text
src_ip = 185.220.101.10
```

---

Malicious Hash Search

```text
SHA256 = abcd1234...
```

---

Suspicious Domain

```text
evil-example.com
```

---

# IOA Investigation Example

Suspicious Behavior

```
winword.exe

↓

cmd.exe

↓

powershell.exe

↓

EncodedCommand

↓

Network Connection

↓

Possible Malware Execution
```

This sequence is an IOA because it identifies attacker behavior rather than relying on a known malware hash.

---

# IOC Management

Organizations should:

- Collect IOCs
- Validate IOCs
- Update IOC Database
- Remove Expired IOCs
- Share Threat Intelligence
- Monitor Detection Results

---

# Benefits of IOA Detection

- Detect Unknown Malware
- Detect Zero-Day Attacks
- Reduce Dependence on Signatures
- Improve Threat Hunting
- Identify Advanced Persistent Threats (APTs)

---

# Best Practices

- Combine IOC and IOA Detection
- Continuously Update Threat Intelligence
- Monitor High-Risk User Activity
- Correlate Multiple Events
- Map Activity to MITRE ATT&CK
- Validate Alerts Before Escalation
- Document Investigation Results

---

# Real-Life Example

A phishing email delivers a malicious Word document.

No known malware hash is detected.

However, the SOC Analyst observes:

- **winword.exe** launches **powershell.exe**
- PowerShell executes an encoded command.
- A connection is made to an unknown external IP.
- A new scheduled task is created.

Although there is no known IOC, the attacker behavior matches multiple IOAs, allowing the SOC team to detect and stop the attack before further damage occurs.

---

# Interview Questions

1. What is an IOC?
2. What is an IOA?
3. What is the difference between IOC and IOA?
4. Give three examples of IOCs.
5. Give three examples of IOAs.
6. Why are IOAs important for detecting advanced attacks?
7. What are common IOC sources?
8. How do SIEM platforms use IOCs?
9. Why should IOC and IOA detection be combined?
10. How does MITRE ATT&CK relate to IOA detection?

---

# Summary

Topics Covered

- Indicators of Compromise (IOC)
- Indicators of Attack (IOA)
- IOC vs IOA
- Network IOCs
- File IOCs
- Host IOCs
- Email IOCs
- Behavioral Detection
- Threat Intelligence
- IOC Management
- Best Practices
- Interview Questions

IOCs and IOAs complement each other in modern cybersecurity. IOCs help identify known compromises, while IOAs detect suspicious attacker behavior that may indicate ongoing or previously unknown attacks. Using both approaches together significantly improves threat detection and incident response.

**End of File**
