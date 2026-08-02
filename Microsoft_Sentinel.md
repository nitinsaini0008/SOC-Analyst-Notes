# Microsoft Sentinel

## About

Microsoft Sentinel is a cloud-native Security Information and Event Management (SIEM) and Security Orchestration, Automation, and Response (SOAR) platform provided by Microsoft Azure.

It helps organizations collect, analyze, detect, investigate, and respond to cyber threats using artificial intelligence, threat intelligence, automation, and cloud-scale analytics.

Microsoft Sentinel is widely used by SOC Analysts to monitor cloud, on-premises, and hybrid environments.

---

# What is Microsoft Sentinel?

Microsoft Sentinel collects security data from multiple sources into Azure Log Analytics Workspace.

It provides:

- Centralized Log Collection
- Threat Detection
- Incident Investigation
- Threat Hunting
- Automated Response
- Interactive Dashboards

---

# Why Microsoft Sentinel is Important

Sentinel helps organizations to:

- Detect Threats Faster
- Investigate Security Incidents
- Automate Security Operations
- Reduce Response Time
- Improve Visibility
- Meet Compliance Requirements

---

# Microsoft Sentinel Architecture

```
Data Sources

↓

Data Connectors

↓

Log Analytics Workspace

↓

Analytics Rules

↓

Incidents

↓

SOC Analyst

↓

Automation (SOAR)
```

---

# Core Components

## 1. Data Connectors

Used to collect logs from various sources.

Examples

- Microsoft Defender
- Azure Active Directory
- Office 365
- Windows Servers
- Linux Servers
- AWS
- Google Cloud
- Cisco Firewalls
- Palo Alto Firewalls

---

## 2. Log Analytics Workspace

Stores all collected logs.

Functions

- Store Data
- Query Logs
- Threat Hunting
- Reporting

---

## 3. Analytics Rules

Rules that detect suspicious activities.

Examples

- Brute Force Attack
- Impossible Travel
- Privilege Escalation
- Malware Detection
- Suspicious PowerShell Activity

---

## 4. Incidents

Related alerts are grouped together into a single incident.

Benefits

- Easier Investigation
- Better Correlation
- Reduced Alert Fatigue

---

## 5. Workbooks

Interactive dashboards used to visualize security information.

Examples

- Login Activity
- Threat Trends
- User Activity
- Network Events
- Incident Statistics

---

## 6. Automation Rules

Automatically perform actions when incidents occur.

Examples

- Create Ticket
- Send Email
- Run Playbook
- Notify Security Team

---

## 7. Playbooks

Playbooks automate incident response using Azure Logic Apps.

Examples

- Disable User Account
- Block Malicious IP
- Send Teams Notification
- Collect Additional Evidence

---

# Data Sources

Microsoft

- Azure AD
- Microsoft Defender
- Office 365
- Microsoft Entra ID

Operating Systems

- Windows
- Linux

Network

- Firewalls
- VPN
- IDS/IPS
- Proxy Servers

Cloud

- AWS
- Azure
- Google Cloud

Applications

- SQL Server
- Apache
- Nginx
- Custom Applications

---

# KQL (Kusto Query Language)

Microsoft Sentinel uses **KQL** to search and analyze logs.

---

## Show All Security Events

```kql
SecurityEvent
```

---

## Failed Logins

```kql
SecurityEvent
| where EventID == 4625
```

---

## Successful Logins

```kql
SecurityEvent
| where EventID == 4624
```

---

## Search by Username

```kql
SecurityEvent
| where Account == "Administrator"
```

---

## Count Events

```kql
SecurityEvent
| summarize count()
```

---

## Top Source IP Addresses

```kql
SecurityEvent
| summarize Count=count() by IPAddress
| top 10 by Count
```

---

# Common SOC Use Cases

- Brute Force Detection
- Malware Detection
- Impossible Travel
- Suspicious Login Activity
- Privilege Escalation
- PowerShell Monitoring
- USB Device Monitoring
- Data Exfiltration Detection
- VPN Monitoring

---

# Threat Hunting

SOC Analysts use Sentinel to search for hidden threats using KQL.

Example

```
Failed Login

↓

Successful Login

↓

Administrator Activity

↓

Possible Account Compromise
```

---

# Advantages

- Cloud Native
- Scalable
- AI-Based Threat Detection
- Built-in Threat Intelligence
- Easy Integration with Microsoft Products
- Automation Support
- Interactive Dashboards

---

# Limitations

- Azure Knowledge Required
- Cost Depends on Data Ingestion
- KQL Learning Curve
- Requires Proper Rule Tuning

---

# Best Practices

- Enable All Required Data Connectors
- Create Custom Analytics Rules
- Tune Detection Rules
- Monitor Incidents Daily
- Use Automation Rules
- Perform Threat Hunting Regularly
- Secure Access with RBAC
- Monitor Data Retention

---

# Real-Life Example

A company uses Microsoft Sentinel to monitor Microsoft Defender, Azure AD, and Office 365.

Sentinel detects:

- 40 failed login attempts
- Successful login from a foreign country
- Administrator privilege assignment

An incident is automatically created.

A playbook disables the compromised account, notifies the SOC team through Microsoft Teams, and creates a ServiceNow ticket for investigation.

---

# Interview Questions

1. What is Microsoft Sentinel?
2. Is Microsoft Sentinel a SIEM or SOAR?
3. What is Log Analytics Workspace?
4. What are Data Connectors?
5. What is KQL?
6. What are Analytics Rules?
7. What is the difference between Alerts and Incidents?
8. What are Playbooks?
9. What are Automation Rules?
10. How does Microsoft Sentinel help SOC Analysts?

---

# Summary

Topics Covered

- Microsoft Sentinel
- SIEM
- SOAR
- Data Connectors
- Log Analytics Workspace
- Analytics Rules
- Incidents
- Workbooks
- Automation Rules
- Playbooks
- KQL
- Threat Hunting
- Best Practices
- Interview Questions

Microsoft Sentinel is a modern cloud-native SIEM and SOAR platform that helps SOC Analysts detect, investigate, and respond to cyber threats efficiently. Its powerful KQL queries, automation capabilities, and seamless Microsoft ecosystem integration make it one of the most widely used security platforms today.

**End of File**
