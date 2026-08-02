# Splunk

## About

Splunk is one of the world's most popular Security Information and Event Management (SIEM) platforms. It collects, indexes, searches, analyzes, and visualizes machine-generated data from servers, endpoints, applications, cloud services, and network devices.

Splunk is widely used by SOC Analysts to detect threats, investigate incidents, monitor systems, and create security dashboards.

---

# What is Splunk?

Splunk is a platform used to collect and analyze machine data in real time.

It helps organizations:

- Collect Logs
- Search Events
- Detect Threats
- Monitor Infrastructure
- Generate Alerts
- Create Dashboards
- Perform Incident Investigations

---

# Why Splunk is Important

Splunk enables security teams to:

- Centralize Logs
- Detect Suspicious Activities
- Investigate Security Incidents
- Perform Threat Hunting
- Meet Compliance Requirements
- Improve Visibility Across the Organization

---

# Splunk Architecture

```
Data Sources

↓

Forwarders

↓

Indexer

↓

Search Head

↓

SOC Analyst
```

---

# Splunk Components

## 1. Universal Forwarder (UF)

A lightweight agent installed on endpoints and servers to collect and forward logs.

Functions

- Collect Logs
- Compress Data
- Send Data Securely

---

## 2. Heavy Forwarder (HF)

Processes and filters logs before forwarding them.

Functions

- Parsing
- Filtering
- Routing
- Data Transformation

---

## 3. Indexer

Stores and indexes incoming log data.

Functions

- Index Logs
- Store Events
- Enable Fast Searching

---

## 4. Search Head

Allows users to search, analyze, visualize, and investigate data.

Functions

- Run Searches
- Create Dashboards
- Generate Reports
- Investigate Alerts

---

# Data Flow

```
Windows Logs

Linux Logs

Firewall Logs

Cloud Logs

↓

Forwarder

↓

Indexer

↓

Search Head

↓

SOC Analyst
```

---

# Splunk Data Types

- Windows Event Logs
- Linux Syslogs
- Firewall Logs
- VPN Logs
- DNS Logs
- Proxy Logs
- Web Server Logs
- Cloud Logs
- Antivirus Logs
- EDR Logs

---

# Important Splunk Terminology

## Index

A storage location for log data.

Example

```
index=windows
```

---

## Source

The file or service from which logs originate.

Example

```
source="WinEventLog:Security"
```

---

## Sourcetype

Defines the format of incoming data.

Examples

```
WinEventLog

syslog

apache_access
```

---

## Host

The system that generated the log.

Example

```
host=Server01
```

---

# Basic SPL (Search Processing Language)

## Show All Events

```spl
index=*
```

---

## Search Windows Logs

```spl
index=windows
```

---

## Search Security Events

```spl
index=windows sourcetype=WinEventLog:Security
```

---

## Failed Login Events

```spl
EventCode=4625
```

---

## Successful Login Events

```spl
EventCode=4624
```

---

## Search by Username

```spl
user=administrator
```

---

## Search by IP Address

```spl
src_ip=192.168.1.100
```

---

## Count Events

```spl
index=windows

| stats count
```

---

## Top 10 IP Addresses

```spl
index=windows

| top src_ip
```

---

## Failed Logins by User

```spl
EventCode=4625

| stats count by user
```

---

## Failed Logins Over Time

```spl
EventCode=4625

| timechart count
```

---

# Common SOC Use Cases

- Failed Login Detection
- Brute Force Detection
- Malware Investigation
- PowerShell Monitoring
- Ransomware Detection
- Suspicious Network Connections
- Privilege Escalation Detection
- USB Device Monitoring
- Account Creation Monitoring

---

# Splunk Dashboards

Dashboards provide graphical views of:

- Security Alerts
- Login Activity
- Top Attack Sources
- Malware Events
- System Health
- User Activity

---

# Alerts

Splunk can automatically generate alerts when predefined conditions are met.

Examples

- More than 10 failed logins in 5 minutes
- Administrator account created
- PowerShell executed with encoded commands
- Malware detected by antivirus
- Large number of failed VPN logins

---

# Best Practices

- Use Meaningful Index Names
- Normalize Log Data
- Tune Searches to Reduce False Positives
- Use Saved Searches
- Create Dashboards for Daily Monitoring
- Monitor Index Storage
- Apply Role-Based Access Control (RBAC)
- Backup Splunk Configuration Regularly

---

# Real-Life Example

A SOC Analyst receives an alert indicating multiple failed login attempts.

Splunk search:

```spl
EventCode=4625

| stats count by user, src_ip
```

Results show:

- 150 failed login attempts
- Same source IP
- Administrator account targeted

The analyst blocks the IP address, resets the account password, and escalates the incident for further investigation.

---

# Interview Questions

1. What is Splunk?
2. What is SPL?
3. What is an Index in Splunk?
4. What is a Sourcetype?
5. What is a Universal Forwarder?
6. What is an Indexer?
7. What is a Search Head?
8. Write an SPL query to find failed login events.
9. How does Splunk help SOC Analysts?
10. What are common Splunk use cases?

---

# Summary

Topics Covered

- Splunk
- Splunk Architecture
- Universal Forwarder
- Heavy Forwarder
- Indexer
- Search Head
- SPL Basics
- Index
- Source
- Sourcetype
- Dashboards
- Alerts
- SOC Use Cases
- Best Practices
- Interview Questions

Splunk is one of the most powerful SIEM platforms used in Security Operations Centers. Its ability to collect, search, correlate, and visualize large volumes of security logs enables SOC Analysts to detect threats quickly and respond effectively to cyber incidents.

**End of File**
