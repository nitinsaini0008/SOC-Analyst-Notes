# Web Log Analysis

## About

Web Log Analysis is the process of examining web server logs to identify suspicious activities, security incidents, performance issues, and attacker behavior.

SOC Analysts use web logs to detect web attacks such as SQL Injection, Cross-Site Scripting (XSS), Directory Traversal, Brute Force attacks, Web Shell activity, and Denial of Service (DoS).

---

# What are Web Logs?

Web logs record every request made to a web server.

Each request contains useful information such as:

- Client IP Address
- Request Time
- HTTP Method
- Requested URL
- Response Code
- User Agent
- Referrer

---

# Why Web Log Analysis is Important

Web Log Analysis helps organizations:

- Detect Web Attacks
- Investigate Security Incidents
- Monitor Website Activity
- Identify Attack Patterns
- Troubleshoot Web Issues
- Improve Security Monitoring

---

# Common Web Servers

- Apache HTTP Server
- Nginx
- Microsoft IIS
- Tomcat
- LiteSpeed

---

# Common Log Files

## Apache

Access Log

```
/var/log/apache2/access.log
```

Error Log

```
/var/log/apache2/error.log
```

---

## Nginx

Access Log

```
/var/log/nginx/access.log
```

Error Log

```
/var/log/nginx/error.log
```

---

## IIS

Logs

```
C:\inetpub\logs\LogFiles\
```

---

# Log Format

Example

```
192.168.1.20 - - [02/Aug/2026:14:20:15]

"GET /index.html HTTP/1.1"

200

1024

"Mozilla/5.0"
```

---

# Important Log Fields

| Field | Description |
|--------|-------------|
| Source IP | Client IP Address |
| Timestamp | Date and Time |
| HTTP Method | GET, POST, PUT, DELETE |
| URL | Requested Resource |
| Status Code | Server Response |
| User Agent | Browser or Client |
| Referrer | Previous Page |

---

# HTTP Methods

| Method | Purpose |
|---------|----------|
| GET | Retrieve Data |
| POST | Submit Data |
| PUT | Update Resource |
| DELETE | Delete Resource |
| HEAD | Retrieve Headers Only |

---

# Common HTTP Status Codes

| Code | Meaning |
|------|----------|
| 200 | OK |
| 301 | Redirect |
| 302 | Temporary Redirect |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |
| 502 | Bad Gateway |
| 503 | Service Unavailable |

---

# Common Web Attacks

## SQL Injection

Indicators

- `' OR 1=1`
- `UNION SELECT`
- `information_schema`

---

## Cross-Site Scripting (XSS)

Indicators

```html
<script>alert(1)</script>
```

---

## Directory Traversal

Indicators

```
../../../etc/passwd
```

---

## Brute Force Attack

Indicators

- Multiple Login Attempts
- Same Source IP
- Repeated Authentication Failures

---

## Web Shell Activity

Indicators

- Suspicious PHP Files
- Unexpected POST Requests
- New Script Uploads

---

## Command Injection

Indicators

```
cmd.exe

bash

powershell
```

appearing in request parameters.

---

# Web Log Analysis Workflow

```
Collect Logs

↓

Identify Suspicious Requests

↓

Analyze IP Addresses

↓

Review HTTP Status Codes

↓

Correlate Events

↓

Investigate

↓

Report Findings
```

---

# Useful Linux Commands

Search Requests

```bash
grep "POST" access.log
```

---

Search Errors

```bash
grep "404" access.log
```

---

Top Client IPs

```bash
awk '{print $1}' access.log | sort | uniq -c | sort -nr
```

---

Real-Time Monitoring

```bash
tail -f access.log
```

---

# Common SOC Use Cases

- Detect SQL Injection
- Detect XSS Attempts
- Identify Web Shell Uploads
- Monitor Login Attempts
- Detect Directory Traversal
- Investigate 500 Errors
- Identify Malicious User Agents
- Detect DoS Activity

---

# Common Analysis Tools

- Splunk
- Microsoft Sentinel
- Elastic Security
- Wireshark
- GoAccess
- Graylog
- Wazuh

---

# Best Practices

- Monitor Access Logs Daily
- Review Error Logs
- Enable Web Application Firewall (WAF)
- Correlate Web Logs with Firewall Logs
- Monitor Failed Login Attempts
- Detect Unusual User Agents
- Retain Logs Securely
- Forward Logs to SIEM

---

# Real-Life Example

A SOC Analyst notices repeated requests containing:

```
' OR 1=1 --
```

from the same external IP address.

The web server responds with multiple **500 Internal Server Error** messages.

The analyst correlates the web logs with WAF alerts and identifies an SQL Injection attack.

The malicious IP is blocked, vulnerable application code is patched, and new SIEM detection rules are created.

---

# Interview Questions

1. What is Web Log Analysis?
2. What information is stored in web logs?
3. What is the difference between an Access Log and an Error Log?
4. What are common HTTP status codes?
5. How can SQL Injection be identified in web logs?
6. What is Directory Traversal?
7. Which log file stores Apache access logs?
8. What tools are used for web log analysis?
9. Why should web logs be forwarded to a SIEM?
10. What are common web attack indicators?

---

# Summary

Topics Covered

- Web Log Analysis
- Apache Logs
- Nginx Logs
- IIS Logs
- HTTP Methods
- HTTP Status Codes
- SQL Injection
- XSS
- Directory Traversal
- Web Shell Detection
- Log Analysis Workflow
- Best Practices
- Interview Questions

Web Log Analysis is an essential skill for SOC Analysts. By understanding web server logs, HTTP requests, status codes, and common attack patterns, analysts can quickly identify web-based attacks and respond effectively to protect web applications and infrastructure.

**End of File**# Web Log Analysis

## About

Web Log Analysis is the process of examining web server logs to identify suspicious activities, security incidents, performance issues, and attacker behavior.

SOC Analysts use web logs to detect web attacks such as SQL Injection, Cross-Site Scripting (XSS), Directory Traversal, Brute Force attacks, Web Shell activity, and Denial of Service (DoS).

---

# What are Web Logs?

Web logs record every request made to a web server.

Each request contains useful information such as:

- Client IP Address
- Request Time
- HTTP Method
- Requested URL
- Response Code
- User Agent
- Referrer

---

# Why Web Log Analysis is Important

Web Log Analysis helps organizations:

- Detect Web Attacks
- Investigate Security Incidents
- Monitor Website Activity
- Identify Attack Patterns
- Troubleshoot Web Issues
- Improve Security Monitoring

---

# Common Web Servers

- Apache HTTP Server
- Nginx
- Microsoft IIS
- Tomcat
- LiteSpeed

---

# Common Log Files

## Apache

Access Log

```
/var/log/apache2/access.log
```

Error Log

```
/var/log/apache2/error.log
```

---

## Nginx

Access Log

```
/var/log/nginx/access.log
```

Error Log

```
/var/log/nginx/error.log
```

---

## IIS

Logs

```
C:\inetpub\logs\LogFiles\
```

---

# Log Format

Example

```
192.168.1.20 - - [02/Aug/2026:14:20:15]

"GET /index.html HTTP/1.1"

200

1024

"Mozilla/5.0"
```

---

# Important Log Fields

| Field | Description |
|--------|-------------|
| Source IP | Client IP Address |
| Timestamp | Date and Time |
| HTTP Method | GET, POST, PUT, DELETE |
| URL | Requested Resource |
| Status Code | Server Response |
| User Agent | Browser or Client |
| Referrer | Previous Page |

---

# HTTP Methods

| Method | Purpose |
|---------|----------|
| GET | Retrieve Data |
| POST | Submit Data |
| PUT | Update Resource |
| DELETE | Delete Resource |
| HEAD | Retrieve Headers Only |

---

# Common HTTP Status Codes

| Code | Meaning |
|------|----------|
| 200 | OK |
| 301 | Redirect |
| 302 | Temporary Redirect |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |
| 502 | Bad Gateway |
| 503 | Service Unavailable |

---

# Common Web Attacks

## SQL Injection

Indicators

- `' OR 1=1`
- `UNION SELECT`
- `information_schema`

---

## Cross-Site Scripting (XSS)

Indicators

```html
<script>alert(1)</script>
```

---

## Directory Traversal

Indicators

```
../../../etc/passwd
```

---

## Brute Force Attack

Indicators

- Multiple Login Attempts
- Same Source IP
- Repeated Authentication Failures

---

## Web Shell Activity

Indicators

- Suspicious PHP Files
- Unexpected POST Requests
- New Script Uploads

---

## Command Injection

Indicators

```
cmd.exe

bash

powershell
```

appearing in request parameters.

---

# Web Log Analysis Workflow

```
Collect Logs

↓

Identify Suspicious Requests

↓

Analyze IP Addresses

↓

Review HTTP Status Codes

↓

Correlate Events

↓

Investigate

↓

Report Findings
```

---

# Useful Linux Commands

Search Requests

```bash
grep "POST" access.log
```

---

Search Errors

```bash
grep "404" access.log
```

---

Top Client IPs

```bash
awk '{print $1}' access.log | sort | uniq -c | sort -nr
```

---

Real-Time Monitoring

```bash
tail -f access.log
```

---

# Common SOC Use Cases

- Detect SQL Injection
- Detect XSS Attempts
- Identify Web Shell Uploads
- Monitor Login Attempts
- Detect Directory Traversal
- Investigate 500 Errors
- Identify Malicious User Agents
- Detect DoS Activity

---

# Common Analysis Tools

- Splunk
- Microsoft Sentinel
- Elastic Security
- Wireshark
- GoAccess
- Graylog
- Wazuh

---

# Best Practices

- Monitor Access Logs Daily
- Review Error Logs
- Enable Web Application Firewall (WAF)
- Correlate Web Logs with Firewall Logs
- Monitor Failed Login Attempts
- Detect Unusual User Agents
- Retain Logs Securely
- Forward Logs to SIEM

---

# Real-Life Example

A SOC Analyst notices repeated requests containing:

```
' OR 1=1 --
```

from the same external IP address.

The web server responds with multiple **500 Internal Server Error** messages.

The analyst correlates the web logs with WAF alerts and identifies an SQL Injection attack.

The malicious IP is blocked, vulnerable application code is patched, and new SIEM detection rules are created.

---

# Interview Questions

1. What is Web Log Analysis?
2. What information is stored in web logs?
3. What is the difference between an Access Log and an Error Log?
4. What are common HTTP status codes?
5. How can SQL Injection be identified in web logs?
6. What is Directory Traversal?
7. Which log file stores Apache access logs?
8. What tools are used for web log analysis?
9. Why should web logs be forwarded to a SIEM?
10. What are common web attack indicators?

---

# Summary

Topics Covered

- Web Log Analysis
- Apache Logs
- Nginx Logs
- IIS Logs
- HTTP Methods
- HTTP Status Codes
- SQL Injection
- XSS
- Directory Traversal
- Web Shell Detection
- Log Analysis Workflow
- Best Practices
- Interview Questions

Web Log Analysis is an essential skill for SOC Analysts. By understanding web server logs, HTTP requests, status codes, and common attack patterns, analysts can quickly identify web-based attacks and respond effectively to protect web applications and infrastructure.

**End of File**
