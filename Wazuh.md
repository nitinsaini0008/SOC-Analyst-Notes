# Wazuh

## About

Wazuh is a free and open-source security platform used for Threat Detection, Security Monitoring, File Integrity Monitoring (FIM), Vulnerability Detection, Log Analysis, Compliance Monitoring, and Incident Response.

It combines Host-based Intrusion Detection (HIDS), Security Information and Event Management (SIEM), and Extended Detection and Response (XDR) capabilities into a single platform.

Wazuh is widely used by SOC teams, security analysts, and organizations looking for an enterprise-grade open-source security solution.

---

# What is Wazuh?

Wazuh is an endpoint security platform that collects security events from endpoints, servers, cloud environments, and applications.

It provides:

- Log Collection
- Threat Detection
- Vulnerability Detection
- Malware Detection
- Compliance Monitoring
- File Integrity Monitoring
- Security Alerts

---

# Why Wazuh is Important

Wazuh helps organizations:

- Detect Cyber Attacks
- Monitor Endpoints
- Identify Security Misconfigurations
- Monitor File Changes
- Detect Malware
- Meet Compliance Requirements

---

# Wazuh Architecture

```
Endpoints

↓

Wazuh Agent

↓

Wazuh Manager

↓

Indexer

↓

Dashboard

↓

SOC Analyst
```

---

# Main Components

## 1. Wazuh Agent

Installed on endpoints.

Functions

- Collect Logs
- Monitor Files
- Detect Rootkits
- Monitor Processes
- Send Events to Manager

Supported Platforms

- Windows
- Linux
- macOS

---

## 2. Wazuh Manager

Receives data from agents.

Functions

- Analyze Logs
- Correlate Events
- Generate Alerts
- Apply Detection Rules

---

## 3. Wazuh Indexer

Stores and indexes security events.

Functions

- Store Logs
- Fast Searching
- Event Correlation

---

## 4. Wazuh Dashboard

Web interface used by SOC Analysts.

Features

- Security Dashboard
- Alerts
- Vulnerabilities
- Agent Status
- Threat Hunting
- Compliance Reports

---

# Data Sources

- Windows Event Logs
- Linux Logs
- Sysmon Logs
- Active Directory
- Web Servers
- Docker
- Kubernetes
- Cloud Platforms
- Endpoint Events

---

# Wazuh Modules

## File Integrity Monitoring (FIM)

Monitors important files for unauthorized changes.

Examples

- Configuration Files
- System Files
- Application Files

Detects

- File Modification
- File Deletion
- File Creation

---

## Vulnerability Detection

Identifies software vulnerabilities.

Checks

- Installed Packages
- Missing Security Updates
- CVEs

---

## Rootkit Detection

Detects hidden malicious software.

Examples

- Hidden Processes
- Hidden Files
- Suspicious Kernel Activity

---

## Log Analysis

Collects and analyzes logs.

Examples

- Authentication Logs
- SSH Logs
- Windows Logs
- Firewall Logs

---

## Security Configuration Assessment (SCA)

Checks systems against security best practices.

Examples

- CIS Benchmarks
- Password Policies
- SSH Configuration

---

## Active Response

Automatically responds to security events.

Examples

- Block IP Address
- Disable User
- Kill Process
- Stop Service

---

# Detection Rules

Wazuh uses XML-based rules to detect suspicious activity.

Example

```
Multiple Failed Logins

↓

Generate High Severity Alert
```

---

# Alert Levels

| Level | Severity |
|--------|----------|
| 0–3 | Low |
| 4–6 | Medium |
| 7–9 | High |
| 10–15 | Critical |

---

# Common SOC Use Cases

- Brute Force Detection
- Malware Detection
- File Integrity Monitoring
- Rootkit Detection
- Unauthorized Login Detection
- USB Device Monitoring
- Privilege Escalation Detection
- SSH Monitoring
- Compliance Auditing

---

# Dashboard Features

- Agent Status
- Active Alerts
- Vulnerability Reports
- File Integrity Changes
- Compliance Results
- Threat Intelligence
- Security Events

---

# Advantages

- Open Source
- Free to Use
- Cross-Platform Support
- File Integrity Monitoring
- Vulnerability Detection
- Compliance Monitoring
- Active Response
- Easy Integration with Elastic Stack

---

# Limitations

- Requires Initial Configuration
- Rule Tuning Needed
- Large Deployments Require More Resources
- Learning Curve for Custom Rules

---

# Best Practices

- Install Agents on All Critical Systems
- Enable File Integrity Monitoring
- Monitor Authentication Logs
- Update Detection Rules Regularly
- Review High-Severity Alerts Daily
- Perform Regular Vulnerability Scans
- Configure Active Response Carefully
- Backup Wazuh Configuration

---

# Real-Life Example

A Wazuh agent installed on a Linux server detects repeated failed SSH login attempts.

The Wazuh Manager correlates the events and generates a **High Severity Alert**.

An Active Response rule automatically blocks the attacker's IP address using the system firewall.

The SOC Analyst reviews the alert, confirms a brute-force attack, and documents the incident.

---

# Interview Questions

1. What is Wazuh?
2. Is Wazuh a SIEM or HIDS?
3. What is the role of the Wazuh Agent?
4. What is File Integrity Monitoring (FIM)?
5. What is Security Configuration Assessment (SCA)?
6. What is Active Response?
7. What are Wazuh detection rules?
8. What platforms does Wazuh support?
9. What are common Wazuh use cases?
10. Why is Wazuh popular among SOC teams?

---

# Summary

Topics Covered

- Wazuh
- Wazuh Architecture
- Wazuh Agent
- Wazuh Manager
- Wazuh Dashboard
- File Integrity Monitoring
- Vulnerability Detection
- Rootkit Detection
- Security Configuration Assessment
- Active Response
- Detection Rules
- Alert Levels
- Best Practices
- Interview Questions

Wazuh is a powerful open-source security platform that combines HIDS, SIEM, XDR, and compliance monitoring into a single solution. Its endpoint monitoring, file integrity monitoring, vulnerability detection, and automated response capabilities make it an excellent choice for modern Security Operations Centers.

**End of File**
