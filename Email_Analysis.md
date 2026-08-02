# Email Analysis

## About

Email Analysis is the process of examining email messages, headers, attachments, links, and sender information to identify phishing attempts, malware, spoofing, and other email-based attacks.

SOC Analysts perform email analysis to determine whether an email is legitimate or malicious and to prevent cyber attacks before they spread across the organization.

---

# What is Email Analysis?

Email Analysis involves inspecting every component of an email to verify its authenticity and identify suspicious indicators.

Analysts examine:

- Sender Information
- Email Headers
- Attachments
- Embedded URLs
- Email Content
- Authentication Records

---

# Why Email Analysis is Important

Email Analysis helps organizations:

- Detect Phishing Attacks
- Prevent Malware Infections
- Stop Business Email Compromise (BEC)
- Protect User Credentials
- Reduce Financial Fraud
- Improve Incident Response

---

# Components of an Email

```
Sender

↓

Recipient

↓

Subject

↓

Date & Time

↓

Email Headers

↓

Body

↓

Attachments

↓

Links
```

---

# Common Email Attacks

## 1. Phishing

Fake emails designed to steal sensitive information.

Examples

- Banking Login Pages
- Office 365 Login
- Password Reset Emails

---

## 2. Spear Phishing

Targeted phishing aimed at a specific individual or organization.

Characteristics

- Personalized
- Higher Success Rate
- Difficult to Detect

---

## 3. Business Email Compromise (BEC)

Attackers impersonate executives or trusted employees.

Purpose

- Financial Fraud
- Credential Theft
- Data Theft

---

## 4. Malware Attachments

Examples

- PDF
- DOCX
- XLSX
- ZIP
- ISO
- EXE

Purpose

- Install Malware
- Deploy Ransomware
- Download Payloads

---

## 5. Email Spoofing

The attacker forges the sender's email address to appear legitimate.

---

# Email Header Analysis

Important Header Fields

| Header | Purpose |
|---------|----------|
| From | Sender Address |
| To | Recipient |
| Subject | Email Subject |
| Date | Delivery Time |
| Message-ID | Unique Email Identifier |
| Return-Path | Original Sending Address |
| Received | Mail Server Path |
| Reply-To | Reply Address |

---

# Email Authentication

## SPF

Sender Policy Framework verifies whether the sending server is authorized.

---

## DKIM

DomainKeys Identified Mail digitally signs outgoing emails.

---

## DMARC

Domain-based Message Authentication, Reporting and Conformance combines SPF and DKIM to reduce spoofing.

---

# Suspicious Indicators

- Unknown Sender
- Misspelled Domain Name
- Urgent Language
- Fake Login Page
- Shortened URLs
- Unexpected Attachments
- Password-Protected ZIP Files
- Executable Files
- Mismatched Reply-To Address

---

# Attachment Analysis

Check:

- File Extension
- File Size
- Digital Signature
- File Hash
- VirusTotal Results
- Sandbox Analysis

High-Risk Extensions

- .exe
- .bat
- .cmd
- .js
- .vbs
- .scr

---

# URL Analysis

Before opening a link, verify:

- Domain Name
- HTTPS Usage
- URL Reputation
- Redirects
- Typosquatting
- IP Address Instead of Domain

Example Suspicious URL

```
https://micr0soft-login.example
```

---

# Email Analysis Workflow

```
Receive Email

↓

Analyze Header

↓

Check Sender

↓

Inspect URLs

↓

Analyze Attachments

↓

Verify SPF/DKIM/DMARC

↓

Threat Intelligence Check

↓

Determine Verdict

↓

Report Incident
```

---

# Common Email Analysis Tools

- Microsoft Defender for Office 365
- VirusTotal
- Any.Run
- Hybrid Analysis
- MXToolbox
- AbuseIPDB
- URLScan.io
- Joe Sandbox

---

# SOC Investigation Steps

1. Collect the Email
2. Review Headers
3. Verify Sender
4. Check Authentication Results
5. Scan Attachments
6. Inspect URLs
7. Search Threat Intelligence
8. Determine Impact
9. Block Indicators
10. Document Findings

---

# Best Practices

- Never Open Suspicious Attachments
- Verify Unexpected Emails
- Check Email Headers
- Validate SPF, DKIM, and DMARC
- Scan Attachments Before Opening
- Use Sandboxes for Analysis
- Report Phishing Immediately
- Block Confirmed Malicious Indicators

---

# Real-Life Example

A finance employee receives an email appearing to come from the company's CEO requesting an urgent wire transfer.

The SOC Analyst investigates and finds:

- The **Reply-To** address differs from the **From** address.
- SPF validation fails.
- The embedded URL points to a fake Microsoft 365 login page.
- The sender domain closely resembles the legitimate company domain (typosquatting).

The analyst classifies the email as a **Business Email Compromise (BEC)** attempt, blocks the sender, updates email security filters, and warns employees about the phishing campaign.

---

# Interview Questions

1. What is Email Analysis?
2. Why are email headers important?
3. What is SPF?
4. What is DKIM?
5. What is DMARC?
6. What is Business Email Compromise (BEC)?
7. How can you identify a phishing email?
8. What are common malicious attachment types?
9. Which tools are used for email analysis?
10. What should a SOC Analyst do after identifying a malicious email?

---

# Summary

Topics Covered

- Email Analysis
- Email Headers
- Phishing
- Spear Phishing
- Business Email Compromise
- Email Spoofing
- SPF
- DKIM
- DMARC
- Attachment Analysis
- URL Analysis
- Email Analysis Workflow
- Best Practices
- Interview Questions

Email Analysis is one of the most important responsibilities of a SOC Analyst. Careful examination of headers, authentication records, URLs, attachments, and threat intelligence enables analysts to detect phishing attacks, prevent malware infections, and protect organizational assets from email-based threats.

**End of File**
