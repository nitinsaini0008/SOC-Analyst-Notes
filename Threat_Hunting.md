# Threat Hunting

## About

Threat Hunting is a proactive cybersecurity process in which security analysts actively search for hidden threats, malicious activities, and attacker behavior that may have bypassed automated security tools.

Unlike traditional security monitoring, Threat Hunting does not wait for alerts. Instead, analysts use hypotheses, threat intelligence, and behavioral analysis to discover advanced threats before they cause significant damage.

---

# What is Threat Hunting?

Threat Hunting is the proactive investigation of systems, endpoints, networks, and logs to identify threats that are not detected by automated security solutions.

Threat Hunters analyze attacker behavior instead of relying only on alerts.

---

# Why Threat Hunting is Important

Threat Hunting helps organizations:

- Detect Hidden Threats
- Discover Advanced Persistent Threats (APTs)
- Reduce Dwell Time
- Improve Detection Rules
- Strengthen Security Controls
- Prevent Future Attacks

---

# Threat Hunting Process

```
Create Hypothesis

↓

Collect Data

↓

Analyze Logs

↓

Identify Suspicious Activity

↓

Investigate

↓

Contain Threat

↓

Improve Detection Rules
```

---

# Types of Threat Hunting

## 1. Intelligence-Driven Hunting

Uses threat intelligence feeds to search for known attacker indicators.

Examples

- Malicious IP Addresses
- Known Domains
- File Hashes
- Threat Actor TTPs

---

## 2. Hypothesis-Driven Hunting

Analysts create a hypothesis based on attacker behavior.

Example

```
Attackers may use PowerShell with encoded commands.

↓

Search Sysmon Event ID 1

↓

Confirm Suspicious Activity
```

---

## 3. Analytics-Driven Hunting

Uses machine learning, statistical analysis, and behavioral analytics to identify anomalies.

Examples

- Unusual Login Times
- Abnormal Network Traffic
- Unusual Process Activity

---

# Threat Hunting Data Sources

- SIEM Logs
- Windows Event Logs
- Sysmon Logs
- Linux Logs
- Firewall Logs
- DNS Logs
- Proxy Logs
- EDR Alerts
- Cloud Logs
- Active Directory Logs

---

# Common Hunting Scenarios

## Suspicious PowerShell

Look for:

```
powershell.exe

+

EncodedCommand
```

---

## Credential Dumping

Look for:

```
lsass.exe

↓

Unauthorized Process Access
```

---

## Brute Force Attack

Look for:

```
Multiple Failed Logins

↓

Successful Login

↓

Privilege Escalation
```

---

## Lateral Movement

Indicators

- PsExec Usage
- RDP Connections
- SMB Activity
- Remote PowerShell

---

## Persistence

Look for:

- Scheduled Tasks
- Registry Run Keys
- Startup Folder
- New Services

---

# MITRE ATT&CK in Threat Hunting

Threat Hunters map suspicious activity to ATT&CK tactics.

Examples

| Tactic | Example |
|---------|----------|
| Initial Access | Phishing |
| Execution | PowerShell |
| Persistence | Scheduled Tasks |
| Credential Access | LSASS Dumping |
| Lateral Movement | RDP |
| Command & Control | HTTPS |
| Impact | Ransomware |

---

# Common Threat Hunting Tools

- Splunk
- Microsoft Sentinel
- IBM QRadar
- Wazuh
- Sysmon
- Wireshark
- Microsoft Defender XDR
- CrowdStrike Falcon
- Elastic Security
- MITRE ATT&CK Navigator

---

# Hunting Queries

Example SPL

```spl
EventCode=4625

| stats count by src_ip
```

---

Example KQL

```kql
SecurityEvent
| where EventID == 4625
```

---

# Threat Hunting Workflow

```
Collect Logs

↓

Search Indicators

↓

Correlate Events

↓

Validate Findings

↓

Contain Threat

↓

Document Investigation
```

---

# Best Practices

- Hunt Regularly
- Build Threat Hunting Hypotheses
- Use MITRE ATT&CK Mapping
- Combine IOC and IOA Analysis
- Tune SIEM Detection Rules
- Validate Findings Before Escalation
- Document Every Hunt
- Share Lessons Learned

---

# Real-Life Example

A Threat Hunter suspects attackers are abusing PowerShell.

Investigation reveals:

- PowerShell launched from **winword.exe**
- Encoded PowerShell command executed
- Connection established to an unknown external IP
- New scheduled task created

The activity matches multiple MITRE ATT&CK techniques.

The endpoint is isolated, malicious files are removed, and new SIEM detection rules are created to identify similar behavior in the future.

---

# Interview Questions

1. What is Threat Hunting?
2. How is Threat Hunting different from incident response?
3. What are the types of Threat Hunting?
4. What is hypothesis-driven hunting?
5. How does MITRE ATT&CK help Threat Hunting?
6. Name five Threat Hunting tools.
7. What are common Threat Hunting data sources?
8. What is attacker dwell time?
9. Why is behavioral analysis important?
10. What are common Threat Hunting best practices?

---

# Summary

Topics Covered

- Threat Hunting
- Threat Hunting Process
- Intelligence-Driven Hunting
- Hypothesis-Driven Hunting
- Analytics-Driven Hunting
- Data Sources
- Hunting Scenarios
- MITRE ATT&CK Mapping
- Threat Hunting Tools
- Hunting Workflow
- Best Practices
- Interview Questions

Threat Hunting is a proactive security practice that enables organizations to identify advanced threats before they cause significant damage. By combining threat intelligence, behavioral analysis, SIEM data, and MITRE ATT&CK mapping, Threat Hunters can uncover hidden attacker activity and continuously improve an organization's security posture.

**End of File**
