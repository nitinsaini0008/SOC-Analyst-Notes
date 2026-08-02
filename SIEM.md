# SIEM (Security Information and Event Management)

## About

Security Information and Event Management (SIEM) is a cybersecurity solution that collects, stores, analyzes, and correlates security logs from multiple sources in real time. It helps security teams detect threats, investigate incidents, and respond quickly.

SIEM is one of the most important technologies used inside a Security Operations Center (SOC).

---

# What is SIEM?

SIEM combines two major functions:

- Security Information Management (SIM)
- Security Event Management (SEM)

It provides centralized log collection, event correlation, alert generation, and reporting.

---

# Objectives of SIEM

- Collect Logs
- Centralize Security Events
- Detect Threats
- Correlate Events
- Generate Alerts
- Support Incident Response
- Meet Compliance Requirements

---

# How SIEM Works

```
Endpoints
Servers
Firewalls
Routers
Applications
Cloud Services

        │
        ▼

Log Collection

        │
        ▼

SIEM Platform

        │
        ▼

Correlation Rules

        │
        ▼

Alerts Generated

        │
        ▼

SOC Analyst Investigation
```

---

# SIEM Components

## 1. Log Collection

Collects logs from different devices and applications.

Examples

- Windows Event Logs
- Linux Syslogs
- Firewall Logs
- VPN Logs
- DNS Logs
- Web Server Logs
- Antivirus Logs
- Cloud Logs

---

## 2. Log Normalization

Converts logs from different formats into a standardized format for easier analysis.

Benefits

- Consistent Data
- Easier Searching
- Better Correlation

---

## 3. Event Correlation

Links related events together to identify suspicious behavior.

Example

```
10 Failed Logins

↓

Successful Login

↓

Privilege Escalation

↓

Critical Alert
```

---

## 4. Alert Generation

Creates alerts when predefined rules or suspicious activities are detected.

Examples

- Multiple Failed Logins
- Malware Detection
- Impossible Travel
- Suspicious PowerShell Execution
- New Administrator Account Created

---

## 5. Dashboards

Provide real-time visualization of:

- Security Events
- Active Incidents
- Threat Trends
- System Health

---

## 6. Reporting

Generate reports for:

- Security Audits
- Compliance
- Incident Summaries
- Executive Management

---

# SIEM Workflow

```
Collect Logs

↓

Normalize Logs

↓

Correlate Events

↓

Generate Alert

↓

SOC Investigation

↓

Incident Response
```

---

# Common Log Sources

| Source | Example |
|---------|----------|
| Windows | Event Viewer |
| Linux | Syslog |
| Firewall | Fortinet, Palo Alto |
| EDR | CrowdStrike, Defender |
| Active Directory | Authentication Logs |
| VPN | Cisco AnyConnect |
| Proxy | Blue Coat |
| DNS | Windows DNS |
| Web Server | Apache, Nginx |
| Cloud | Microsoft Azure, AWS |

---

# Popular SIEM Platforms

## Splunk Enterprise Security

- Powerful Search
- Dashboards
- Threat Detection
- Large Enterprise Support

---

## Microsoft Sentinel

- Cloud-Based SIEM
- Azure Integration
- Automation
- Threat Intelligence

---

## IBM QRadar

- Advanced Correlation
- Enterprise SOC
- Threat Detection

---

## Wazuh

- Open Source
- Endpoint Monitoring
- Log Collection
- File Integrity Monitoring

---

## Elastic Security

- Elasticsearch-Based
- Fast Log Search
- Visualization
- Detection Rules

---

# SIEM Use Cases

- Failed Login Detection
- Brute Force Detection
- Malware Alerts
- Insider Threat Detection
- Data Exfiltration Detection
- Privilege Escalation Monitoring
- Ransomware Detection
- Unauthorized USB Usage
- VPN Login Monitoring

---

# Advantages

- Centralized Log Management
- Faster Threat Detection
- Better Visibility
- Compliance Reporting
- Incident Investigation
- Automated Alerting

---

# Limitations

- Large Storage Requirements
- High Cost (Commercial SIEMs)
- False Positives
- Rule Tuning Required
- Skilled Analysts Needed

---

# Best Practices

- Collect Logs from All Critical Systems
- Synchronize Time Using NTP
- Create High-Quality Detection Rules
- Tune Alerts to Reduce False Positives
- Monitor Dashboards Continuously
- Retain Logs According to Compliance Requirements
- Regularly Update Detection Content

---

# Real-Life Example

A company uses Microsoft Sentinel to collect logs from Windows servers, Microsoft Defender, Azure Active Directory, and firewalls.

A user account generates 25 failed login attempts followed by a successful login from a foreign country.

The SIEM correlates these events and generates a **High Severity Alert**.

The SOC Analyst investigates the logs, confirms suspicious activity, disables the account, and initiates the incident response process.

---

# Interview Questions

1. What is SIEM?
2. What is the difference between SIM and SEM?
3. Why is SIEM important in a SOC?
4. What is log normalization?
5. What is event correlation?
6. Name five SIEM tools.
7. What are common log sources?
8. Why are SIEM alerts generated?
9. What are the advantages of SIEM?
10. Explain the SIEM workflow.

---

# Summary

Topics Covered

- SIEM
- SIM
- SEM
- Log Collection
- Log Normalization
- Event Correlation
- Alert Generation
- Dashboards
- Reporting
- SIEM Workflow
- Log Sources
- SIEM Platforms
- Use Cases
- Best Practices
- Interview Questions

SIEM is the backbone of a modern Security Operations Center. It centralizes security data, correlates events from multiple sources, and helps analysts rapidly detect, investigate, and respond to cyber threats.

**End of File**
