# Threat Intelligence

## About

Threat Intelligence (TI) is the collection, analysis, and sharing of information about current and emerging cyber threats. It helps organizations understand attacker behavior, identify risks, and improve their ability to detect, prevent, and respond to cyber attacks.

Threat Intelligence is widely used by SOC Analysts, Threat Hunters, Incident Responders, and Security Engineers.

---

# What is Threat Intelligence?

Threat Intelligence is evidence-based information about cyber threats, threat actors, attack techniques, vulnerabilities, and Indicators of Compromise (IOCs).

It helps organizations make informed security decisions instead of reacting only after an attack occurs.

---

# Why Threat Intelligence is Important

Threat Intelligence helps organizations:

- Detect Threats Earlier
- Improve Incident Response
- Reduce Security Risks
- Strengthen Detection Rules
- Improve Threat Hunting
- Understand Attacker Behavior
- Prioritize Security Efforts

---

# Threat Intelligence Lifecycle

```
Planning

↓

Collection

↓

Processing

↓

Analysis

↓

Dissemination

↓

Feedback
```

---

# Types of Threat Intelligence

## 1. Strategic Intelligence

High-level information for executives and management.

Focus

- Business Risk
- Industry Trends
- Nation-State Threats
- Security Strategy

---

## 2. Tactical Intelligence

Information about attacker tactics, techniques, and procedures (TTPs).

Examples

- MITRE ATT&CK Techniques
- Malware Behavior
- Attack Patterns

---

## 3. Operational Intelligence

Information about ongoing or planned attacks.

Examples

- Threat Campaigns
- Ransomware Operations
- Threat Actor Activity

---

## 4. Technical Intelligence

Technical indicators used for detection.

Examples

- IP Addresses
- Domains
- URLs
- File Hashes
- YARA Rules
- Sigma Rules

---

# Threat Intelligence Sources

## Open Source Intelligence (OSINT)

Examples

- VirusTotal
- AlienVault OTX
- MalwareBazaar
- AbuseIPDB
- MITRE ATT&CK
- CISA Advisories

---

## Commercial Intelligence

Examples

- Recorded Future
- CrowdStrike Intelligence
- Microsoft Threat Intelligence
- Palo Alto Unit 42

---

## Internal Intelligence

Collected from:

- SIEM
- EDR
- Firewall Logs
- Incident Reports
- Threat Hunting Results

---

# Indicators Used in Threat Intelligence

- Malicious IP Addresses
- Domains
- URLs
- Email Addresses
- File Hashes
- Registry Keys
- Process Names
- User Agents

---

# Threat Intelligence Workflow

```
Threat Feed

↓

Collect Indicators

↓

Validate

↓

Import into SIEM

↓

Generate Alerts

↓

SOC Investigation
```

---

# Threat Intelligence Platforms (TIP)

Popular platforms include:

- MISP
- OpenCTI
- ThreatConnect
- Anomali
- IBM X-Force Exchange

---

# Threat Intelligence in a SOC

SOC Analysts use Threat Intelligence to:

- Enrich Security Alerts
- Validate IOCs
- Prioritize Incidents
- Improve Detection Rules
- Support Threat Hunting
- Block Malicious Indicators

---

# Threat Intelligence and MITRE ATT&CK

Threat Intelligence is often mapped to MITRE ATT&CK techniques.

Example

```
Phishing Email

↓

PowerShell Execution

↓

Credential Dumping

↓

Command & Control

↓

Mapped to ATT&CK
```

This helps analysts understand attacker behavior and improve detection coverage.

---

# Common Threat Intelligence Tools

- VirusTotal
- AlienVault OTX
- MISP
- OpenCTI
- MalwareBazaar
- Microsoft Defender Threat Intelligence
- Recorded Future

---

# Best Practices

- Validate Threat Intelligence Before Use
- Continuously Update IOC Feeds
- Remove Outdated Indicators
- Integrate Intelligence with SIEM
- Correlate Intelligence with Internal Logs
- Share Intelligence Across Teams
- Map Intelligence to MITRE ATT&CK

---

# Real-Life Example

A Threat Intelligence feed reports a new phishing campaign targeting financial organizations.

The feed includes:

- Malicious IP addresses
- Domains
- SHA-256 file hashes
- Associated MITRE ATT&CK techniques

The SOC team imports these indicators into Microsoft Sentinel and Splunk.

A few hours later, Sentinel detects communication with one of the malicious domains.

The analyst investigates, isolates the affected endpoint, blocks the indicators across the organization, and confirms the phishing attack before additional systems are compromised.

---

# Interview Questions

1. What is Threat Intelligence?
2. What are the four types of Threat Intelligence?
3. What is the Threat Intelligence lifecycle?
4. What are Indicators of Compromise (IOCs)?
5. Name five Threat Intelligence sources.
6. What is a Threat Intelligence Platform (TIP)?
7. How does Threat Intelligence help SOC Analysts?
8. Why is MITRE ATT&CK used with Threat Intelligence?
9. What are common Threat Intelligence tools?
10. Why should Threat Intelligence be validated before use?

---

# Summary

Topics Covered

- Threat Intelligence
- Threat Intelligence Lifecycle
- Strategic Intelligence
- Tactical Intelligence
- Operational Intelligence
- Technical Intelligence
- Threat Intelligence Sources
- Threat Intelligence Platforms
- IOCs
- MITRE ATT&CK Mapping
- SOC Use Cases
- Best Practices
- Interview Questions

Threat Intelligence enables organizations to anticipate, detect, and respond to cyber threats using reliable information about attacker behavior, infrastructure, and techniques. Integrating threat intelligence into SOC operations significantly improves detection accuracy and incident response effectiveness.

**End of File**
