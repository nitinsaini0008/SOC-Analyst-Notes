# Sysmon (System Monitor)

## About

Sysmon (System Monitor) is a Windows system service and device driver developed by Microsoft Sysinternals. It provides detailed logging of system activities that are not available in standard Windows Event Logs.

SOC Analysts use Sysmon to detect malware, investigate incidents, monitor suspicious processes, and identify attacker behavior.

---

# What is Sysmon?

Sysmon continuously monitors system activity and records detailed events into the Windows Event Log.

Unlike standard Windows logging, Sysmon provides detailed visibility into:

- Process Creation
- Network Connections
- File Creation
- Registry Changes
- Driver Loading
- Process Injection
- DNS Queries

---

# Why Sysmon is Important

Sysmon helps analysts:

- Detect Malware
- Identify Persistence Mechanisms
- Investigate Incidents
- Monitor Lateral Movement
- Detect PowerShell Abuse
- Track Parent-Child Processes

---

# Sysmon Architecture

```
Windows System

        │

Sysmon Service

        │

Collect Events

        │

Windows Event Log

        │

SIEM

        │

SOC Analyst
```

---

# Installing Sysmon

Download Sysmon from Microsoft Sysinternals.

Example Installation

```cmd
Sysmon64.exe -i
```

Install with Configuration File

```cmd
Sysmon64.exe -i sysmonconfig.xml
```

---

# Sysmon Event Logs

Sysmon logs are stored in:

```
Applications and Services Logs

↓

Microsoft

↓

Windows

↓

Sysmon

↓

Operational
```

---

# Important Sysmon Event IDs

## Event ID 1

### Process Creation

Logs every newly created process.

Information Available

- Process Name
- Command Line
- Parent Process
- User
- Process ID
- Hash

Example

```
powershell.exe
```

---

## Event ID 2

### File Creation Time Changed

Detects timestamp modification.

Commonly used by attackers to hide malicious files.

---

## Event ID 3

### Network Connection

Logs outbound network connections.

Information

- Source IP
- Destination IP
- Destination Port
- Process Name

Useful for detecting:

- Malware C2 Communication
- Suspicious External Connections

---

## Event ID 5

### Process Terminated

Logs process termination.

Useful during investigations.

---

## Event ID 6

### Driver Loaded

Logs kernel driver loading.

Helps detect:

- Rootkits
- Malicious Drivers

---

## Event ID 7

### Image Loaded

Logs DLL loading events.

Useful for:

- DLL Hijacking Detection
- Malware Analysis

---

## Event ID 8

### CreateRemoteThread

Detects process injection techniques.

Commonly associated with malware.

---

## Event ID 10

### Process Access

Logs when one process accesses another.

Useful for detecting:

- Credential Dumping
- LSASS Access

---

## Event ID 11

### File Create

Logs newly created files.

Useful for:

- Malware Dropping Files
- Ransomware Activity

---

## Event ID 12

### Registry Object Created

Logs registry key creation.

---

## Event ID 13

### Registry Value Set

Logs registry value modifications.

Useful for detecting persistence.

---

## Event ID 15

### FileCreateStreamHash

Detects Alternate Data Streams (ADS).

Useful for detecting hidden malware.

---

## Event ID 22

### DNS Query

Logs DNS requests made by applications.

Useful for:

- Detecting C2 Domains
- DNS Tunneling
- Malicious Domains

---

# Common Detection Use Cases

## PowerShell Abuse

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
Process Access

↓

lsass.exe
```

---

## Malware Download

Sequence

```
powershell.exe

↓

Network Connection

↓

File Created
```

---

## Suspicious Parent Process

Example

```
winword.exe

↓

cmd.exe

↓

powershell.exe
```

May indicate:

- Malicious Office Document
- Macro Execution

---

# Sysmon vs Windows Event Logs

| Feature | Windows Logs | Sysmon |
|----------|-------------|---------|
| Process Creation | Limited | Detailed |
| Network Connections | Limited | Yes |
| DNS Queries | No | Yes |
| Registry Monitoring | Limited | Yes |
| Process Injection | No | Yes |
| Parent Process | Limited | Detailed |

---

# Best Practices

- Deploy a Trusted Sysmon Configuration
- Collect Logs in SIEM
- Monitor PowerShell Activity
- Detect Process Injection
- Monitor Registry Changes
- Track Network Connections
- Keep Sysmon Updated
- Tune Rules to Reduce Noise

---

# Common SOC Investigation Example

Alert:

```
Suspicious PowerShell Activity
```

Investigation

```
Event ID 1

↓

powershell.exe

↓

EncodedCommand

↓

Event ID 3

↓

Connection to Unknown IP

↓

Event ID 11

↓

Suspicious File Created
```

Result

The analyst confirms malware execution, isolates the endpoint, blocks the malicious IP address, and escalates the incident.

---

# Popular Sysmon Configuration Projects

- SwiftOnSecurity Sysmon Config
- Olaf Hartong Sysmon Modular Config

These community configurations improve detection quality while reducing unnecessary log noise.

---

# Interview Questions

1. What is Sysmon?
2. Why is Sysmon better than standard Windows logs?
3. What is Event ID 1?
4. What does Event ID 3 record?
5. Which Sysmon Event ID detects DNS queries?
6. What is Event ID 10 used for?
7. How does Sysmon help detect malware?
8. What is Process Injection?
9. Why is parent-child process analysis important?
10. How are Sysmon logs used in a SIEM?

---

# Summary

Topics Covered

- Sysmon
- Installation
- Event IDs
- Process Creation
- Network Connections
- DNS Queries
- Registry Monitoring
- Process Injection
- Detection Use Cases
- Sysmon vs Windows Logs
- Best Practices
- Interview Questions

Sysmon is one of the most valuable monitoring tools for SOC Analysts. It provides deep visibility into Windows activity, enabling analysts to detect malware, investigate attacks, and understand attacker behavior far beyond standard Windows Event Logs.

**End of File**
