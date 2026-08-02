# MITRE ATT&CK Framework

## About

MITRE ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge) is a globally recognized knowledge base of adversary tactics and techniques based on real-world cyber attacks.

It helps SOC Analysts, Threat Hunters, Incident Responders, and Security Engineers understand attacker behavior, improve detections, and strengthen defenses.

---

# What is MITRE ATT&CK?

MITRE ATT&CK is a framework that documents how attackers compromise systems, move through networks, steal data, and achieve their objectives.

Instead of focusing on malware, ATT&CK focuses on attacker behavior.

---

# Why MITRE ATT&CK is Important

It helps organizations:

- Understand Attack Techniques
- Improve Threat Detection
- Map Security Alerts
- Perform Threat Hunting
- Build Detection Rules
- Improve Incident Response
- Strengthen Security Controls

---

# ATT&CK Matrix

The ATT&CK Matrix is divided into **Tactics** and **Techniques**.

```
Tactics

↓

Techniques

↓

Sub-Techniques
```

---

# What is a Tactic?

A tactic represents the attacker's objective during a specific phase of an attack.

Example:

```
Credential Access
```

---

# What is a Technique?

A technique describes **how** an attacker achieves a tactic.

Example:

```
Brute Force
```

Technique ID

```
T1110
```

---

# What is a Sub-Technique?

A sub-technique provides more detail about a technique.

Example

```
Password Spraying

↓

T1110.003
```

---

# MITRE ATT&CK Tactics

## 1. Reconnaissance (TA0043)

Gather information about the target.

Examples

- WHOIS Lookup
- Employee Research
- DNS Enumeration

---

## 2. Resource Development (TA0042)

Prepare resources for an attack.

Examples

- Purchase Domains
- Register Servers
- Create Malware

---

## 3. Initial Access (TA0001)

Gain access to the target environment.

Examples

- Phishing
- Exploiting Public Applications
- Valid Accounts

---

## 4. Execution (TA0002)

Run malicious code.

Examples

- PowerShell
- Command Prompt
- Scheduled Tasks

---

## 5. Persistence (TA0003)

Maintain long-term access.

Examples

- Registry Run Keys
- Startup Folder
- Scheduled Tasks

---

## 6. Privilege Escalation (TA0004)

Obtain higher privileges.

Examples

- Token Manipulation
- Exploiting Vulnerabilities

---

## 7. Defense Evasion (TA0005)

Avoid detection.

Examples

- Disable Antivirus
- Obfuscated Files
- Process Injection

---

## 8. Credential Access (TA0006)

Steal usernames and passwords.

Examples

- Credential Dumping
- Keylogging
- Brute Force

---

## 9. Discovery (TA0007)

Collect information about the environment.

Examples

- Account Discovery
- Network Discovery
- Process Discovery

---

## 10. Lateral Movement (TA0008)

Move to other systems.

Examples

- Remote Desktop
- SMB
- PsExec

---

## 11. Collection (TA0009)

Collect valuable information.

Examples

- Screenshot Capture
- Clipboard Data
- File Collection

---

## 12. Command and Control (TA0011)

Communicate with attacker-controlled infrastructure.

Examples

- HTTPS
- DNS
- Web Protocols

---

## 13. Exfiltration (TA0010)

Steal data from the organization.

Examples

- Cloud Storage
- FTP
- HTTPS Upload

---

## 14. Impact (TA0040)

Disrupt business operations.

Examples

- Ransomware
- Data Destruction
- Service Stop

---

# ATT&CK IDs

Examples

| Technique | ID |
|-----------|----|
| Phishing | T1566 |
| PowerShell | T1059.001 |
| Command Prompt | T1059.003 |
| Credential Dumping | T1003 |
| Brute Force | T1110 |
| PsExec | T1569 |
| Scheduled Task | T1053 |
| Remote Desktop | T1021.001 |

---

# ATT&CK in SOC

SOC Analysts use MITRE ATT&CK to:

- Classify Alerts
- Map Incidents
- Perform Threat Hunting
- Improve Detection Rules
- Create Sigma Rules
- Analyze Malware Behavior

---

# Detection Example

```
PowerShell

↓

EncodedCommand

↓

Network Connection

↓

Credential Dumping

↓

MITRE Mapping

Execution
Credential Access
Command & Control
```

---

# MITRE ATT&CK Navigator

Navigator is a visualization tool used to:

- Map Techniques
- Assess Coverage
- Identify Detection Gaps
- Perform Threat Hunting

---

# Benefits

- Standardized Framework
- Real-World Attack Data
- Better Detection Coverage
- Improved Threat Intelligence
- Easier Incident Investigation
- Common Language for Security Teams

---

# Best Practices

- Map Alerts to ATT&CK Techniques
- Review Detection Coverage
- Update Detection Rules
- Use ATT&CK During Threat Hunting
- Train Analysts Using ATT&CK
- Integrate ATT&CK with SIEM and EDR

---

# Real-Life Example

A phishing email delivers a malicious Microsoft Word document.

The user enables macros, which launch PowerShell.

PowerShell downloads malware, steals credentials from the victim's system, and communicates with an attacker-controlled server.

The activity can be mapped to:

- Initial Access (Phishing)
- Execution (PowerShell)
- Credential Access (Credential Dumping)
- Command and Control (HTTPS)
- Impact (Ransomware)

This mapping helps the SOC team understand the complete attack chain and improve future detections.

---

# Interview Questions

1. What is MITRE ATT&CK?
2. What is the difference between a Tactic and a Technique?
3. What is a Sub-Technique?
4. What is the purpose of the ATT&CK Matrix?
5. What is Credential Access?
6. What is Initial Access?
7. How does MITRE ATT&CK help SOC Analysts?
8. What is ATT&CK Navigator?
9. Why is ATT&CK important for Threat Hunting?
10. Name five MITRE ATT&CK tactics.

---

# Summary

Topics Covered

- MITRE ATT&CK
- Tactics
- Techniques
- Sub-Techniques
- ATT&CK Matrix
- ATT&CK IDs
- Threat Hunting
- Detection Mapping
- ATT&CK Navigator
- SOC Use Cases
- Best Practices
- Interview Questions

MITRE ATT&CK is one of the most valuable frameworks in modern cybersecurity. By mapping attacker behavior to standardized tactics and techniques, SOC teams can improve detection, investigation, threat hunting, and overall security operations.

**End of File**
