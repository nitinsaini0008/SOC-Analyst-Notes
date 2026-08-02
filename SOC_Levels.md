# SOC Levels

## About

A Security Operations Center (SOC) is organized into multiple levels based on responsibilities, expertise, and incident handling capabilities. Each SOC level plays a specific role in detecting, investigating, and responding to cyber threats.

The most common SOC hierarchy includes:

- SOC Level 1 (L1)
- SOC Level 2 (L2)
- SOC Level 3 (L3)
- Threat Hunters
- SOC Manager

---

# SOC Hierarchy

```
SOC Manager

      ▲

Threat Hunters

      ▲

SOC Analyst L3

      ▲

SOC Analyst L2

      ▲

SOC Analyst L1
```

---

# SOC Level 1 (L1)

## Role

Security Monitoring and Alert Triage

L1 Analysts are the first line of defense.

They continuously monitor SIEM dashboards and investigate security alerts.

---

## Responsibilities

- Monitor SIEM Alerts
- Validate Alerts
- Identify False Positives
- Create Incident Tickets
- Escalate Serious Incidents
- Perform Basic Log Analysis
- Follow Standard Operating Procedures (SOPs)

---

## Common Tools

- Splunk
- Microsoft Sentinel
- QRadar
- Wazuh
- Defender
- ServiceNow

---

## Required Skills

- Networking Basics
- Windows Logs
- Linux Basics
- SIEM
- Incident Classification
- Basic Cyber Security Knowledge

---

## Typical Salary (India)

Approx.

₹3 LPA – ₹6 LPA

---

# SOC Level 2 (L2)

## Role

Incident Investigation

L2 Analysts investigate incidents escalated by L1.

---

## Responsibilities

- Deep Log Analysis
- Malware Investigation
- IOC Analysis
- Threat Validation
- Incident Containment Support
- Root Cause Analysis

---

## Common Tools

- Splunk
- Sentinel
- Wireshark
- VirusTotal
- MITRE ATT&CK
- CrowdStrike
- Defender XDR

---

## Required Skills

- Windows Internals
- Linux
- Active Directory
- Threat Hunting Basics
- Network Analysis
- Incident Response

---

## Typical Salary (India)

Approx.

₹6 LPA – ₹12 LPA

---

# SOC Level 3 (L3)

## Role

Advanced Security Investigation

L3 Analysts handle sophisticated attacks.

---

## Responsibilities

- Advanced Threat Hunting
- Malware Analysis
- Reverse Engineering Coordination
- Detection Engineering
- Develop Detection Rules
- Improve Security Controls

---

## Common Tools

- Splunk Enterprise
- Microsoft Sentinel
- Sigma
- YARA
- Volatility
- Cortex XDR
- MISP

---

## Required Skills

- Malware Analysis
- Memory Analysis
- Threat Intelligence
- Detection Engineering
- Python Basics
- Advanced Networking

---

## Typical Salary (India)

Approx.

₹12 LPA – ₹20+ LPA

---

# Threat Hunter

## Role

Proactively searches for hidden threats that automated systems may not detect.

---

## Responsibilities

- Hunt Advanced Threats
- Analyze Threat Intelligence
- Develop Detection Logic
- Improve SOC Detection Capabilities

---

## Skills

- MITRE ATT&CK
- Threat Intelligence
- Sigma Rules
- YARA
- SIEM
- Scripting

---

# SOC Manager

## Responsibilities

- Manage SOC Operations
- Incident Coordination
- Team Management
- Reporting
- Compliance
- Security Strategy
- Performance Monitoring

---

# SOC Escalation Flow

```
Alert

↓

SOC L1

↓

SOC L2

↓

SOC L3

↓

Incident Response

↓

Management
```

---

# Skills Progression

## L1

- Networking
- Windows
- Linux
- SIEM
- Log Analysis

↓

## L2

- Threat Hunting
- Incident Response
- Malware Investigation
- Active Directory

↓

## L3

- Detection Engineering
- Malware Analysis
- Threat Intelligence
- Reverse Engineering Basics

---

# Career Path

```
IT Support

↓

SOC Analyst L1

↓

SOC Analyst L2

↓

SOC Analyst L3

↓

Threat Hunter

↓

SOC Lead

↓

SOC Manager
```

---

# Certifications for Each Level

## Beginner

- Google Cybersecurity Professional Certificate
- CompTIA Security+
- Microsoft SC-900

---

## Intermediate

- Microsoft SC-200
- Blue Team Level 1 (BTL1)
- Splunk Core Certified User

---

## Advanced

- CompTIA CySA+
- GIAC Certified Incident Handler (GCIH)
- Certified Ethical Hacker (CEH)
- OffSec SOC-200 (where applicable)

---

# Real-Life Example

A suspicious login alert is generated in Splunk.

- **L1 Analyst** validates the alert and confirms it is suspicious.
- **L2 Analyst** investigates logs, checks user activity, and identifies compromised credentials.
- **L3 Analyst** develops a new detection rule to identify similar attacks in the future.
- The **SOC Manager** reviews the incident report and recommends additional security controls.

---

# Interview Questions

1. What are the different SOC levels?
2. What does a SOC L1 Analyst do?
3. What is the role of a SOC L2 Analyst?
4. What are the responsibilities of a SOC L3 Analyst?
5. What is Threat Hunting?
6. What skills are required for SOC L1?
7. What is the SOC escalation process?
8. Which certifications are useful for SOC Analysts?
9. What tools are commonly used by SOC Analysts?
10. Explain the career path of a SOC Analyst.

---

# Summary

Topics Covered

- SOC Levels
- L1 Responsibilities
- L2 Responsibilities
- L3 Responsibilities
- Threat Hunter
- SOC Manager
- SOC Escalation
- Career Path
- Certifications
- Skills
- Interview Questions

Understanding SOC levels helps define the responsibilities and career progression within a Security Operations Center. Building strong networking, operating system, SIEM, and incident response skills is the foundation for advancing from SOC L1 to L3 and beyond.

**End of File**
