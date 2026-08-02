# SOC Team Roles

## About

A Security Operations Center (SOC) consists of multiple cybersecurity professionals working together to detect, investigate, respond to, and prevent cyber threats. Each team member has specific responsibilities that contribute to the organization's overall security.

---

# Why SOC Team Roles are Important

A well-defined SOC team helps to:

- Detect threats quickly
- Reduce incident response time
- Improve security monitoring
- Minimize business impact
- Ensure proper communication during incidents

---

# SOC Team Structure

```
SOC Manager
      │
────────────────────────────
│            │            │
L3         Threat      Incident
Analyst    Hunter      Responder
│
L2 Analyst
│
L1 Analyst
```

---

# 1. SOC Analyst Level 1 (L1)

## Primary Responsibility

Monitor security alerts and perform initial investigation.

### Daily Tasks

- Monitor SIEM dashboards
- Validate alerts
- Identify false positives
- Create incident tickets
- Escalate confirmed incidents
- Document findings

### Skills

- Networking Basics
- Windows Logs
- Linux Basics
- SIEM Fundamentals
- Communication Skills

---

# 2. SOC Analyst Level 2 (L2)

## Primary Responsibility

Investigate and respond to security incidents.

### Daily Tasks

- Analyze logs
- Investigate malware alerts
- Perform IOC analysis
- Validate suspicious activities
- Support containment efforts
- Perform root cause analysis

### Skills

- Incident Response
- Threat Analysis
- Active Directory
- Windows Internals
- Network Analysis

---

# 3. SOC Analyst Level 3 (L3)

## Primary Responsibility

Handle advanced threats and improve security detection.

### Daily Tasks

- Threat Hunting
- Malware Analysis
- Detection Engineering
- Develop SIEM Rules
- Create Sigma Rules
- Improve SOC Processes

### Skills

- Threat Intelligence
- YARA
- Sigma
- Memory Analysis
- Python Basics

---

# 4. Threat Hunter

## Primary Responsibility

Proactively search for hidden threats before automated tools detect them.

### Responsibilities

- Analyze Threat Intelligence
- Hunt Advanced Persistent Threats (APTs)
- Search for Indicators of Compromise (IOCs)
- Improve Detection Logic
- Recommend Security Improvements

### Common Tools

- Splunk
- Sentinel
- MITRE ATT&CK
- Sigma
- VirusTotal

---

# 5. Incident Responder

## Primary Responsibility

Contain, eradicate, and recover from security incidents.

### Responsibilities

- Isolate Affected Systems
- Remove Malware
- Restore Services
- Coordinate Recovery
- Preserve Evidence
- Document Incidents

---

# 6. Detection Engineer

## Primary Responsibility

Develop and improve detection rules used by SIEM and EDR platforms.

### Responsibilities

- Create Detection Rules
- Tune Existing Rules
- Reduce False Positives
- Develop Sigma Rules
- Improve Alert Quality

---

# 7. Malware Analyst

## Primary Responsibility

Analyze malicious software to understand its behavior and impact.

### Responsibilities

- Analyze Malware Samples
- Identify Indicators of Compromise
- Reverse Engineering (Basic/Advanced)
- Generate Detection Signatures
- Support Incident Response

---

# 8. Digital Forensics Analyst

## Primary Responsibility

Collect, preserve, and analyze digital evidence after security incidents.

### Responsibilities

- Collect Evidence
- Perform Disk Imaging
- Analyze Memory Dumps
- Recover Deleted Files
- Maintain Chain of Custody

---

# 9. Threat Intelligence Analyst

## Primary Responsibility

Collect and analyze information about emerging cyber threats.

### Responsibilities

- Monitor Threat Feeds
- Analyze IOC Data
- Research Threat Actors
- Share Intelligence with SOC Teams
- Recommend Defensive Measures

---

# 10. SOC Manager

## Primary Responsibility

Lead the Security Operations Center and manage security operations.

### Responsibilities

- Team Management
- Incident Coordination
- Security Reporting
- Compliance
- Resource Planning
- Performance Monitoring
- Executive Communication

---

# Communication Flow

```
Security Alert

↓

SOC L1

↓

SOC L2

↓

SOC L3

↓

Incident Response

↓

SOC Manager

↓

Management
```

---

# Skills Required by All SOC Members

Technical Skills

- Networking
- Windows
- Linux
- SIEM
- Log Analysis
- Incident Response
- MITRE ATT&CK
- Cyber Security Fundamentals

Soft Skills

- Communication
- Documentation
- Teamwork
- Critical Thinking
- Time Management
- Problem Solving

---

# Common Tools Used by SOC Teams

| Tool | Purpose |
|------|---------|
| Splunk | SIEM |
| Microsoft Sentinel | Cloud SIEM |
| IBM QRadar | SIEM |
| Wazuh | Security Monitoring |
| Wireshark | Packet Analysis |
| VirusTotal | Threat Intelligence |
| CrowdStrike Falcon | EDR |
| Microsoft Defender XDR | Endpoint Protection |
| ServiceNow | Ticketing |
| Jira | Incident Tracking |

---

# Best Practices

- Follow Standard Operating Procedures (SOPs)
- Document Every Investigation
- Communicate Clearly
- Escalate High-Severity Incidents Quickly
- Continuously Improve Detection Rules
- Participate in Security Training
- Review Lessons Learned After Incidents

---

# Real-Life Example

A ransomware alert is generated by Microsoft Defender.

- **L1 Analyst** validates the alert and opens an incident ticket.
- **L2 Analyst** investigates endpoint logs and confirms malicious activity.
- **L3 Analyst** develops a new detection rule to identify similar attacks.
- **Incident Responder** isolates the infected device and restores data from backups.
- **Threat Intelligence Analyst** checks whether the ransomware group is linked to known campaigns.
- **SOC Manager** reviews the incident, updates leadership, and approves improvements to security controls.

---

# Interview Questions

1. What are the different roles in a SOC?
2. What is the responsibility of a SOC L1 Analyst?
3. What does a Threat Hunter do?
4. What is the role of a Detection Engineer?
5. What is Digital Forensics?
6. What is the role of a Malware Analyst?
7. What does an Incident Responder do?
8. Which tools are commonly used in a SOC?
9. Why is documentation important in a SOC?
10. How do different SOC team members work together during an incident?

---

# Summary

Topics Covered

- SOC Team Structure
- L1 Analyst
- L2 Analyst
- L3 Analyst
- Threat Hunter
- Incident Responder
- Detection Engineer
- Malware Analyst
- Digital Forensics Analyst
- Threat Intelligence Analyst
- SOC Manager
- SOC Workflow
- Common Tools
- Best Practices
- Interview Questions

A successful Security Operations Center depends on collaboration between specialized team members. Each role contributes unique expertise to detect, investigate, contain, and prevent cyber threats while ensuring the organization's security posture continues to improve.

**End of File**
