# SOC Metrics (Security Operations Center Metrics)

## About

SOC Metrics are measurable values used to evaluate the performance, efficiency, and effectiveness of a Security Operations Center (SOC). These metrics help organizations understand how well their security team detects, investigates, and responds to cyber threats.

SOC Managers and Analysts use these metrics to improve security operations, reduce risks, and optimize incident response.

---

# What are SOC Metrics?

SOC Metrics are Key Performance Indicators (KPIs) that measure the performance of SOC operations.

They answer questions such as:

- How quickly are threats detected?
- How fast are incidents resolved?
- How many alerts are investigated?
- How effective are detection rules?

---

# Why SOC Metrics are Important

SOC Metrics help organizations:

- Improve Incident Response
- Measure SOC Performance
- Reduce Security Risks
- Improve Detection Accuracy
- Identify Process Gaps
- Support Compliance Audits

---

# Common SOC Metrics

## 1. Mean Time to Detect (MTTD)

The average time required to detect a security incident.

Formula

```
MTTD = Total Detection Time

        ÷

Number of Incidents
```

Lower values indicate better detection performance.

---

## 2. Mean Time to Respond (MTTR)

The average time required to respond to and contain a security incident.

Formula

```
MTTR = Total Response Time

        ÷

Number of Incidents
```

Lower MTTR means faster response.

---

## 3. Mean Time to Investigate (MTTI)

Measures how long analysts take to investigate an alert before determining whether it is a true or false incident.

---

## 4. Mean Time to Contain (MTTC)

Measures the time required to stop an attack from spreading.

Example

- Isolating an endpoint
- Blocking a malicious IP
- Disabling a compromised account

---

## 5. Mean Time to Recover (MTTRc)

Measures the time required to restore systems after an incident.

Examples

- Restore Backups
- Recover Servers
- Resume Business Operations

---

# Alert Metrics

## Total Alerts

Total number of alerts received.

---

## True Positives

Actual security incidents.

---

## False Positives

Alerts incorrectly identified as malicious.

Goal

Reduce false positives through better detection tuning.

---

## False Negatives

Actual attacks that were not detected.

These are highly dangerous because attackers remain unnoticed.

---

# Incident Metrics

- Total Incidents
- Open Incidents
- Closed Incidents
- High Severity Incidents
- Critical Incidents

---

# Threat Detection Metrics

Measure:

- Malware Detections
- Phishing Incidents
- Brute Force Attacks
- Insider Threats
- Data Exfiltration Attempts
- Ransomware Events

---

# Analyst Performance Metrics

Examples

- Alerts Investigated
- Cases Closed
- Average Investigation Time
- Documentation Quality
- Escalation Accuracy

---

# Detection Rule Metrics

Evaluate:

- Rule Accuracy
- Rule Coverage
- Detection Rate
- Alert Volume
- False Positive Rate

---

# Dashboard Example

```
SOC Dashboard

Total Alerts: 1,250

True Positives: 140

False Positives: 1,020

Critical Incidents: 18

Average MTTD: 12 Minutes

Average MTTR: 28 Minutes
```

---

# KPI Examples

| KPI | Target |
|------|---------|
| MTTD | Less than 15 minutes |
| MTTR | Less than 30 minutes |
| False Positive Rate | Less than 10% |
| SLA Compliance | Greater than 95% |
| Critical Incident Response | Less than 15 minutes |

---

# Service Level Agreement (SLA)

SOC teams often work according to predefined SLAs.

Example

| Severity | Response Time |
|----------|---------------|
| Critical | 15 Minutes |
| High | 30 Minutes |
| Medium | 2 Hours |
| Low | 8 Hours |

---

# Benefits of Measuring SOC Metrics

- Better Visibility
- Improved Decision Making
- Faster Incident Response
- Higher Detection Quality
- Continuous Improvement
- Better Resource Planning

---

# Common Challenges

- High Alert Volume
- Alert Fatigue
- Incomplete Data
- Poor Rule Tuning
- Staff Shortages
- Complex Security Environments

---

# Best Practices

- Track Metrics Continuously
- Reduce False Positives
- Review Detection Rules Regularly
- Improve Analyst Training
- Automate Repetitive Tasks
- Monitor SLA Compliance
- Present Metrics Through Dashboards

---

# Real-Life Example

A SOC receives **2,000 alerts** in one week.

Analysis shows:

- 1,700 are false positives.
- Average MTTD is **10 minutes**.
- Average MTTR is **25 minutes**.
- Two critical ransomware incidents were contained within **12 minutes**, meeting the organization's SLA.

Based on these metrics, the SOC tunes several detection rules, reducing false positives by **35%** the following month and improving analyst efficiency.

---

# Interview Questions

1. What are SOC Metrics?
2. What is MTTD?
3. What is MTTR?
4. What is the difference between True Positives and False Positives?
5. Why are False Negatives dangerous?
6. What is an SLA in a SOC?
7. Why should SOC metrics be monitored?
8. What are common SOC KPIs?
9. How can false positives be reduced?
10. Why are dashboards important in SOC operations?

---

# Summary

Topics Covered

- SOC Metrics
- MTTD
- MTTR
- MTTI
- MTTC
- Mean Time to Recover
- Alert Metrics
- Incident Metrics
- Analyst Performance
- Detection Rule Metrics
- SLA
- KPIs
- Best Practices
- Interview Questions

SOC Metrics are essential for measuring and improving the effectiveness of security operations. By tracking detection speed, response time, alert quality, and analyst performance, organizations can continuously strengthen their cybersecurity posture and ensure efficient incident response.

**End of File**
