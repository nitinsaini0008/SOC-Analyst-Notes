# Sigma Rules

## About

Sigma is an open and generic signature format used to describe log detection rules in a SIEM-independent way. It enables SOC Analysts, Threat Hunters, and Detection Engineers to write detection rules once and convert them into queries for different SIEM platforms such as Splunk, Microsoft Sentinel, Elastic Security, QRadar, and others.

Sigma makes threat detection portable and easier to maintain across different security environments.

---

# What are Sigma Rules?

Sigma Rules are YAML-based detection rules that describe suspicious activities found in security logs.

A Sigma rule contains:

- Metadata
- Log Source
- Detection Logic
- False Positives
- Severity Level
- References

---

# Why Sigma is Important

Sigma helps organizations:

- Standardize Detection Rules
- Share Detection Content
- Improve Threat Detection
- Support Multiple SIEM Platforms
- Reduce Rule Development Time

---

# Sigma Rule Structure

```yaml
title: Suspicious PowerShell Execution
id: 12345678-1234-5678-1234-123456789012
status: stable
description: Detects suspicious PowerShell usage
author: SOC Team
date: 2026-08-02

logsource:
  product: windows

detection:
  selection:
    Image: powershell.exe
  condition: selection

level: high
```

---

# Main Fields

## Title

Name of the detection rule.

Example

```yaml
title: Multiple Failed Logins
```

---

## ID

Unique identifier for the rule.

---

## Description

Explains what the rule detects.

---

## Author

Person or team who created the rule.

---

## Logsource

Specifies where the logs originate.

Examples

```yaml
product: windows
```

```yaml
product: linux
```

```yaml
category: process_creation
```

---

## Detection

Defines the detection logic.

Example

```yaml
detection:
  selection:
    EventID: 4625
  condition: selection
```

---

## Level

Severity of the alert.

Values

- low
- medium
- high
- critical

---

# Common Sigma Detection Examples

## Failed Login Detection

```yaml
title: Multiple Failed Logins

logsource:
  product: windows

detection:
  selection:
    EventID: 4625

  condition: selection

level: medium
```

---

## PowerShell Detection

```yaml
selection:
  Image: powershell.exe
```

---

## Command Prompt Detection

```yaml
selection:
  Image: cmd.exe
```

---

## Registry Run Key Modification

```yaml
category: registry_event
```

---

## Process Creation

```yaml
category: process_creation
```

---

# Sigma Rule Lifecycle

```
Threat Intelligence

↓

Create Rule

↓

Test Rule

↓

Deploy

↓

Generate Alert

↓

SOC Investigation

↓

Improve Rule
```

---

# Sigma Conversion

Sigma rules can be converted into SIEM-specific queries.

Examples

- Splunk SPL
- Microsoft Sentinel KQL
- Elastic Query
- QRadar AQL
- ArcSight Queries

Common conversion tool:

- Sigma CLI (sigmac)

---

# MITRE ATT&CK Mapping

Sigma rules often include ATT&CK techniques.

Example

```yaml
tags:
- attack.execution
- attack.t1059
```

Benefits

- Standardized Detection
- Easier Threat Hunting
- Better Reporting

---

# Common Sigma Rule Categories

- Process Creation
- Registry Events
- File Creation
- Authentication
- Network Connections
- PowerShell
- DNS Activity
- Scheduled Tasks
- Services
- USB Events

---

# Best Practices

- Use Clear Rule Titles
- Test Rules Before Deployment
- Reduce False Positives
- Map Rules to MITRE ATT&CK
- Review Rules Regularly
- Document Detection Logic
- Tune Rules for Your Environment

---

# Real-Life Example

A Detection Engineer creates a Sigma rule to detect PowerShell executed with encoded commands.

The rule is converted into a Splunk SPL query and a Microsoft Sentinel KQL query.

During monitoring, the rule detects suspicious PowerShell activity originating from **winword.exe**.

The SOC Analyst investigates the alert, confirms malicious behavior, isolates the endpoint, and updates additional detection rules to improve future visibility.

---

# Interview Questions

1. What is Sigma?
2. Why are Sigma Rules useful?
3. What format is used to write Sigma Rules?
4. What is the purpose of the `logsource` field?
5. What is the `detection` section?
6. How are Sigma Rules converted for different SIEMs?
7. Why is MITRE ATT&CK mapping important?
8. What are common Sigma rule categories?
9. How can Sigma Rules reduce false positives?
10. How do Sigma Rules help SOC Analysts?

---

# Summary

Topics Covered

- Sigma Rules
- YAML Structure
- Detection Logic
- Log Sources
- Severity Levels
- Rule Lifecycle
- Sigma Conversion
- MITRE ATT&CK Mapping
- Best Practices
- Interview Questions

Sigma Rules provide a standardized, SIEM-independent way to write and share detection logic. They help SOC teams improve threat detection, simplify rule management, and deploy consistent security monitoring across multiple platforms.

**End of File**
