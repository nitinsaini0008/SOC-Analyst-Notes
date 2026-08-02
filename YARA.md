# YARA

## About

YARA is a tool used to identify and classify malware based on patterns, strings, binary characteristics, and file attributes. It allows malware analysts, SOC Analysts, and Threat Hunters to create rules that detect malicious files and suspicious behavior.

YARA is often called the **"pattern matching language for malware."**

---

# What is YARA?

YARA is an open-source tool that scans files, processes, and memory using custom rules.

It helps security teams:

- Detect Malware
- Identify Malicious Files
- Search Memory
- Classify Malware Families
- Support Incident Response

---

# Why YARA is Important

YARA helps organizations:

- Detect Known Malware
- Identify New Malware Variants
- Perform Threat Hunting
- Analyze Malware Samples
- Improve Detection Rules
- Support Digital Forensics

---

# YARA Rule Structure

A YARA rule contains four main sections:

```yara
rule Rule_Name
{
    meta:
        author = "SOC Team"

    strings:
        $a = "powershell"

    condition:
        $a
}
```

---

# Main Sections

## Rule

Defines the rule name.

Example

```yara
rule Suspicious_PowerShell
```

---

## Meta

Stores descriptive information.

Example

```yara
meta:
    author = "Nitin Kumar Saini"
    description = "Detects suspicious PowerShell usage"
    date = "2026-08-02"
```

---

## Strings

Defines patterns to search for.

Example

```yara
strings:
    $cmd = "cmd.exe"
    $ps = "powershell.exe"
```

Types of Strings

- Text Strings
- Hex Strings
- Regular Expressions

---

## Condition

Defines when the rule matches.

Example

```yara
condition:
    any of them
```

Other Examples

```yara
condition:
    all of them
```

```yara
condition:
    $cmd and $ps
```

---

# Example YARA Rule

```yara
rule Detect_PowerShell
{
    meta:
        author = "SOC Analyst"
        severity = "High"

    strings:
        $a = "powershell.exe"

    condition:
        $a
}
```

---

# YARA Workflow

```
Malware Sample

↓

YARA Rule

↓

Pattern Matching

↓

Match Found

↓

SOC Investigation
```

---

# Common YARA Use Cases

- Malware Detection
- Threat Hunting
- Memory Analysis
- Digital Forensics
- File Classification
- IOC Detection
- Ransomware Identification

---

# YARA Scanning

Scan a File

```bash
yara rules.yar sample.exe
```

---

Scan an Entire Folder

```bash
yara -r rules.yar /home/user/files/
```

---

# String Types

## Text String

```yara
$a = "cmd.exe"
```

---

## Hex String

```yara
$a = { 50 45 00 00 }
```

---

## Regular Expression

```yara
$a = /powershell.*/
```

---

# YARA Modules

Common modules include:

- pe
- elf
- math
- hash
- dotnet
- magic

Example

```yara
import "pe"
```

---

# Best Practices

- Use Specific Detection Strings
- Avoid Generic Patterns
- Test Rules Before Deployment
- Reduce False Positives
- Document Rule Purpose
- Update Rules Regularly
- Share Rules with Security Teams

---

# YARA vs Sigma

| YARA | Sigma |
|------|-------|
| Detects Files and Memory | Detects Log Events |
| Malware Focus | SIEM Focus |
| Pattern Matching | Log Detection |
| Used by Malware Analysts | Used by SOC Analysts |

---

# Real-Life Example

A suspicious executable is found on an employee's computer.

The SOC team scans the file using YARA rules.

The file matches a ransomware detection rule because it contains known malicious strings and behavioral indicators.

The analyst quarantines the file, blocks related hashes, updates threat intelligence, and shares new detection rules with the SOC team.

---

# Interview Questions

1. What is YARA?
2. Why is YARA important?
3. What are the main sections of a YARA rule?
4. What is the purpose of the `strings` section?
5. What is the purpose of the `condition` section?
6. What are common YARA use cases?
7. What is the difference between YARA and Sigma?
8. What are YARA modules?
9. How does YARA help malware analysis?
10. Why should YARA rules be tested before deployment?

---

# Summary

Topics Covered

- YARA
- Rule Structure
- Meta
- Strings
- Conditions
- YARA Modules
- Malware Detection
- Threat Hunting
- YARA vs Sigma
- Best Practices
- Interview Questions

YARA is one of the most powerful tools for malware detection and classification. By creating well-designed rules, security professionals can quickly identify malicious files, support incident response, and improve threat detection across their environments.

**End of File**
