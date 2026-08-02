# SOC Analyst Interview Questions & Answers

## About

This document contains frequently asked SOC Analyst interview questions with concise answers. It is designed for beginners preparing for SOC L1 interviews and covers networking, operating systems, SIEM, incident response, threat hunting, malware, Windows, Linux, and cloud security concepts.

---

# Basic SOC Questions

## 1. What is a SOC?

A Security Operations Center (SOC) is a team responsible for continuously monitoring, detecting, investigating, and responding to cybersecurity threats.

---

## 2. What does a SOC Analyst do?

A SOC Analyst monitors security alerts, investigates suspicious activities, analyzes logs, escalates incidents, and helps protect organizational assets.

---

## 3. What is SIEM?

SIEM (Security Information and Event Management) collects, correlates, and analyzes security logs from multiple sources to detect threats.

Examples:

- Splunk
- Microsoft Sentinel
- IBM QRadar
- Wazuh

---

## 4. What is the difference between SIEM and SOAR?

SIEM detects and analyzes threats, while SOAR automates incident response using predefined playbooks.

---

## 5. What is a security incident?

A security incident is any event that compromises or threatens the confidentiality, integrity, or availability (CIA) of information systems.

---

## Windows Questions

## 6. What is Event ID 4624?

Successful Windows logon.

---

## 7. What is Event ID 4625?

Failed Windows logon.

---

## 8. What is Sysmon?

Sysmon is a Microsoft Sysinternals tool that provides detailed endpoint logging such as process creation, network connections, and registry modifications.

---

## 9. Which Windows log is most important for SOC Analysts?

Security Log.

---

## 10. What is Event Viewer?

A Windows utility used to view and analyze system, application, and security logs.

---

# Linux Questions

## 11. Where are Linux logs stored?

```
/var/log/
```

---

## 12. Which log stores SSH authentication?

Ubuntu:

```
/var/log/auth.log
```

Red Hat:

```
/var/log/secure
```

---

## 13. Which command shows failed login attempts?

```bash
lastb
```

---

## 14. What does journalctl do?

Displays logs collected by systemd.

---

## Networking Questions

## 15. What is DNS?

Domain Name System converts domain names into IP addresses.

---

## 16. Difference between TCP and UDP?

TCP is connection-oriented and reliable.

UDP is connectionless and faster.

---

## 17. What is a firewall?

A firewall filters network traffic based on security rules.

---

## 18. What is a VPN?

A Virtual Private Network encrypts network traffic over public networks.

---

## 19. What is a port scan?

A technique used to discover open ports and services on a target.

---

# Threat Detection

## 20. What is an IOC?

Indicator of Compromise.

Examples:

- Malicious IP
- Hash
- Domain

---

## 21. What is an IOA?

Indicator of Attack.

Focuses on attacker behavior.

Example:

PowerShell → EncodedCommand → Network Connection.

---

## 22. What is Threat Hunting?

Proactively searching for hidden threats that bypass automated detection.

---

## 23. What is MITRE ATT&CK?

A framework that documents attacker tactics and techniques based on real-world attacks.

---

## Malware Questions

## 24. Difference between Virus, Worm, and Trojan?

Virus:

Requires user action.

Worm:

Self-replicates automatically.

Trojan:

Pretends to be legitimate software.

---

## 25. What is ransomware?

Malware that encrypts files and demands payment.

---

## 26. What is phishing?

A social engineering attack that tricks users into revealing sensitive information.

---

## 27. What is YARA?

A rule-based malware detection language used to identify malicious files.

---

## 28. What are Sigma Rules?

Portable SIEM detection rules written in YAML format.

---

# Incident Response

## 29. What are the phases of Incident Handling?

- Preparation
- Identification
- Containment
- Eradication
- Recovery
- Lessons Learned

---

## 30. What is containment?

Preventing an incident from spreading.

---

## 31. What is eradication?

Removing the root cause of an incident.

---

## 32. What is recovery?

Restoring systems safely after an incident.

---

## SIEM Questions

## 33. Name three SIEM tools.

- Splunk
- Microsoft Sentinel
- IBM QRadar

---

## 34. What is log normalization?

Converting logs into a standard format for easier analysis.

---

## 35. What is event correlation?

Connecting related events to identify suspicious behavior.

---

# EDR/XDR Questions

## 36. What is EDR?

Endpoint Detection and Response.

---

## 37. What is XDR?

Extended Detection and Response.

Collects security data from multiple sources.

---

## 38. Name some EDR tools.

- CrowdStrike Falcon
- Microsoft Defender XDR
- SentinelOne
- Cortex XDR

---

# Threat Intelligence

## 39. What is Threat Intelligence?

Evidence-based information about cyber threats used to improve detection and response.

---

## 40. Name some Threat Intelligence sources.

- VirusTotal
- MISP
- AlienVault OTX
- MalwareBazaar
- CISA Advisories

---

# Scenario-Based Questions

## 41. What would you do if you receive 100 failed login alerts?

- Validate alerts.
- Identify affected accounts.
- Check source IPs.
- Review authentication logs.
- Determine whether it is a brute-force attack.
- Escalate if necessary.

---

## 42. How would you investigate a phishing email?

- Analyze headers.
- Check SPF/DKIM/DMARC.
- Inspect URLs.
- Scan attachments.
- Search threat intelligence.
- Block indicators.

---

## 43. What would you do if PowerShell executed an encoded command?

- Review Sysmon logs.
- Analyze parent process.
- Check network connections.
- Isolate endpoint.
- Investigate further.

---

## 44. What should you do after detecting malware?

- Isolate the endpoint.
- Collect evidence.
- Remove malware.
- Reset credentials if required.
- Restore affected systems.
- Document the incident.

---

## 45. Why do you want to become a SOC Analyst?

Example Answer:

"I enjoy cybersecurity, problem-solving, and investigating security incidents. I want to build my career in Blue Team security by protecting organizations from cyber threats while continuously improving my technical skills."

---

# Rapid Fire Questions

- Difference between IOC and IOA?
- What is Sysmon?
- What is Event ID 4625?
- What is MITRE ATT&CK?
- What is SIEM?
- What is SOAR?
- What is YARA?
- What are Sigma Rules?
- What is EDR?
- What is XDR?
- What is Threat Hunting?
- What is DNS?
- What is VPN?
- What is a Firewall?
- What is Event Correlation?

---

# Interview Tips

- Explain concepts clearly.
- Give practical examples whenever possible.
- Think before answering scenario-based questions.
- Mention investigation steps in the correct order.
- Be honest if you do not know an answer.
- Demonstrate a structured troubleshooting approach.

---

# Summary

Topics Covered

- SOC Fundamentals
- SIEM
- SOAR
- Windows
- Linux
- Networking
- Threat Hunting
- IOC & IOA
- MITRE ATT&CK
- Malware
- YARA
- Sigma
- EDR/XDR
- Threat Intelligence
- Incident Response
- Scenario-Based Questions

This document provides a strong foundation for SOC L1 interview preparation. Review these questions regularly, practice explaining concepts aloud, and perform hands-on labs to reinforce your knowledge.

**End of File**
