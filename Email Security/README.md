# 📧  Email Security

## What is Email Security?
### Definition

**Email Security** is the process of protecting email accounts, messages, and users from cyber threats such as phishing, malware, spam, spoofing, and Business Email Compromise (BEC).

### Simple Definition

> **Email Security protects email communication from unauthorized access and cyberattacks.**

---

## Why is Email Security Important?

Email is one of the most common attack vectors used by cybercriminals.

### Importance

- Prevents phishing attacks
- Blocks malware
- Protects sensitive information
- Prevents account compromise
- Reduces spam
- Prevents Business Email Compromise (BEC)

---

## Common Email-Based Attacks

- Phishing
- Spear Phishing
- Whaling
- Business Email Compromise (BEC)
- Email Spoofing
- Malicious Attachments
- Malicious Links
- Spam

---

# 2. Email Protocols

Email protocols define how emails are **sent**, **received**, and **stored** between email clients and mail servers.

---

## SMTP (Simple Mail Transfer Protocol)

### Definition

SMTP is used to **send emails** from a client to a mail server or between mail servers.

### Example

```text
You Send an Email
        │
        ▼
SMTP Transfers the Email
        │
        ▼
Mail Server
```

### Uses

- Sending emails
- Server-to-server email transfer

---

## POP3 (Post Office Protocol Version 3)

### Definition

POP3 is used to **download emails** from the mail server to the user's device.

### Features

- Downloads emails locally
- Emails are often removed from the server after download
- Best for using a single device

### Example

```text
Mail Server
     │
     ▼
Download Email
     │
     ▼
Laptop
```

---

## IMAP (Internet Message Access Protocol)

### Definition

IMAP allows users to **access and synchronize emails** across multiple devices.

### Features

- Emails remain on the server
- Syncs across multiple devices
- Supports folders and read/unread status

### Example

```text
          Mail Server
          /    |     \
         /     |      \
        ▼      ▼       ▼
    Laptop   Mobile   Tablet
```

---

## SMTP vs POP3 vs IMAP

| Protocol | Purpose | Emails Stored | Best For |
|----------|---------|---------------|----------|
| **SMTP** | Sending emails | Mail Server | Sending emails |
| **POP3** | Receiving emails | Local Device | Single device access |
| **IMAP** | Receiving & Syncing emails | Mail Server | Multiple device access |

---

## Quick Comparison

| Feature | SMTP | POP3 | IMAP |
|---------|------|------|------|
| Send Emails | ✅ | ❌ | ❌ |
| Receive Emails | ❌ | ✅ | ✅ |
| Sync Across Devices | ❌ | ❌ | ✅ |
| Stores Emails on Server | ✅ | ❌ | ✅ |
| Best For | Sending Emails | Single Device | Multiple Devices |

# 3. Email Authentication

Email authentication helps verify that an email is sent from a legitimate sender and has not been modified during transmission. It protects organizations from phishing and email spoofing attacks.

---

## SPF (Sender Policy Framework)

### Definition

**SPF (Sender Policy Framework)** verifies whether the sending mail server is authorized to send emails for a domain.

### Purpose

- Prevents sender spoofing
- Verifies authorized mail servers

### Example

```text
company.com
      │
      ▼
Authorized Mail Server
      │
      ▼
Email Accepted
```

---

## DKIM (DomainKeys Identified Mail)

### Definition

**DKIM (DomainKeys Identified Mail)** adds a **digital signature** to outgoing emails.

The receiving mail server verifies the signature to ensure the email has not been modified during transmission.

### Purpose

- Verifies email integrity
- Detects email tampering

### Example

```text
Email Sent
      │
      ▼
Digital Signature Added
      │
      ▼
Receiving Server Verifies Signature
      │
      ▼
Email Accepted
```

---

## DMARC (Domain-based Message Authentication, Reporting & Conformance)

### Definition

**DMARC** tells receiving mail servers what action to take if an email fails SPF or DKIM authentication.

### Policies

- **None** – Monitor only
- **Quarantine** – Send the email to Spam/Junk
- **Reject** – Reject the email completely

### Purpose

- Prevents phishing
- Prevents email spoofing
- Improves email security

### Example

```text
Email Received
       │
       ▼
SPF & DKIM Check
       │
       ▼
Pass ✔
   │
Email Delivered

OR

Fail ✖
   │
DMARC Policy Applied
(None / Quarantine / Reject)
```

---

## SPF vs DKIM vs DMARC

| Protocol | Purpose |
|----------|---------|
| **SPF** | Verifies the sending mail server. |
| **DKIM** | Verifies the email has not been modified using a digital signature. |
| **DMARC** | Defines how to handle emails that fail SPF or DKIM checks. |

---

# 4. Email Attacks

---

## Phishing

A fake email designed to steal credentials or sensitive information by pretending to come from a trusted source.

---

## Spear Phishing

A targeted phishing attack aimed at a **specific individual or organization** using personalized information.

---

## Whaling

A phishing attack targeting **high-profile executives** such as CEOs, CFOs, or senior management.

---

## Business Email Compromise (BEC)

An attacker impersonates a trusted executive, employee, or vendor to trick someone into:

- Transferring money
- Sharing confidential information
- Approving fraudulent requests

---

## Email Spoofing

The attacker **forges the sender's email address** to make the email appear as if it came from a trusted source.

---

## Malicious Attachments

Attachments containing malware that infects the victim's system when opened.

### Common Examples

- PDF
- Word Document
- ZIP File
- Excel File

---

## Malicious Links

Links that redirect users to malicious websites.

### Examples

- Fake login pages
- Malware download sites
- Credential theft websites

# 5. Indicators of a Phishing Email

A phishing email often contains signs that indicate it is malicious. A SOC Analyst should look for these indicators during an investigation.

## Common Indicators

- Fake sender address
- Urgent language (e.g., **"Act Now!"**, **"Account will be suspended"**)
- Suspicious or shortened links
- Unexpected attachments
- Grammar or spelling mistakes
- Domain mismatch
- Requests for passwords or sensitive information

---

## Example

```text
From: support@micr0soft.com
Subject: Your Account Will Be Suspended!

⚠ Urgent Action Required!
Click here to verify your account immediately.

https://login-micr0soft.com
```

**Indicators Found:**

- Fake sender domain
- Urgent language
- Suspicious URL
- Credential harvesting attempt

---

# 6. Email Header Analysis

Email headers provide technical information about an email and help SOC Analysts identify phishing, spoofing, and the actual source of an email.

---

## From

Displays the sender's email address shown to the recipient.

**Example**

```text
From: support@microsoft.com
```

---

## To

Displays the recipient's email address.

**Example**

```text
To: user@company.com
```

---

## Return-Path

Shows the email address used for handling bounced emails.

**Purpose**

- Detect email spoofing
- Verify the actual sending address

---

## Received

Shows the path the email traveled through different mail servers before reaching the recipient.

**Purpose**

- Identify the originating mail server
- Trace the email route
- Detect suspicious servers

---

## Message-ID

A unique identifier assigned to every email.

**Purpose**

- Track emails
- Correlate investigations
- Identify duplicate emails

---

## Reply-To

Specifies the email address where replies should be sent.

Attackers often change this field to redirect responses.

**Example**

```text
From: ceo@company.com

Reply-To: attacker@gmail.com
```

This is a common phishing indicator.

---

# 7. Email Security Tools

| Tool | Purpose |
|------|---------|
| **Microsoft Defender for Office 365** | Protects against phishing, malware, and malicious attachments. |
| **Proofpoint** | Email security, phishing protection, and threat detection. |
| **Mimecast** | Email filtering, spam protection, and email security. |
| **Cisco Secure Email** | Email gateway that blocks spam, phishing, and malware. |

---

# Email Security Tool Summary

| Tool | Category |
|------|----------|
| Microsoft Defender for Office 365 | Email Security |
| Proofpoint | Secure Email Gateway (SEG) |
| Mimecast | Secure Email Gateway (SEG) |
| Cisco Secure Email | Email Security Gateway |

# 8. Interview Questions & Answers

---

## 1. What is Email Security?

### Answer

> Email Security is the process of protecting email accounts, messages, and users from cyber threats such as phishing, malware, spam, spoofing, and Business Email Compromise (BEC).

---

## 2. Why is Email Security important?

### Answer

> Email Security is important because email is one of the most common attack vectors used by cybercriminals. It helps prevent phishing attacks, blocks malware, protects sensitive information, prevents account compromise, and reduces spam.

---

## 3. What is SMTP?

### Answer

> SMTP (Simple Mail Transfer Protocol) is used to send emails from a client to a mail server or between mail servers.

---

## 4. What is POP3?

### Answer

> POP3 (Post Office Protocol Version 3) is used to download emails from the mail server to a user's device. Emails are typically stored locally and may be removed from the server after download.

---

## 5. What is IMAP?

### Answer

> IMAP (Internet Message Access Protocol) allows users to access and synchronize emails across multiple devices while keeping emails stored on the mail server.

---

## 6. Difference between POP3 and IMAP

| POP3 | IMAP |
|------|------|
| Downloads emails to the local device | Keeps emails on the mail server |
| Best for a single device | Best for multiple devices |
| Limited synchronization | Synchronizes across all devices |

---

## 7. What is Phishing?

### Answer

> Phishing is a cyberattack where attackers send fraudulent emails pretending to be from trusted sources to steal credentials, financial information, or other sensitive data.

---

## 8. Difference between Phishing and Spear Phishing

| Phishing | Spear Phishing |
|----------|----------------|
| Targets many users | Targets a specific person or organization |
| Generic email | Personalized email |
| Lower success rate | Higher success rate |

---

## 9. What is Whaling?

### Answer

> Whaling is a phishing attack that specifically targets high-profile executives such as CEOs, CFOs, or other senior management personnel.

---

## 10. What is Business Email Compromise (BEC)?

### Answer

> Business Email Compromise (BEC) is an attack where a cybercriminal impersonates a trusted executive, employee, or vendor to trick someone into transferring money or sharing sensitive information.

---

## 11. What is Email Spoofing?

### Answer

> Email Spoofing is a technique where an attacker forges the sender's email address to make an email appear as though it came from a trusted source.

---

## 12. What is SPF?

### Answer

> SPF (Sender Policy Framework) is an email authentication method that verifies whether the sending mail server is authorized to send emails for a domain.

---

## 13. What is DKIM?

### Answer

> DKIM (DomainKeys Identified Mail) adds a digital signature to outgoing emails so the receiving server can verify that the email has not been modified during transmission.

---

## 14. What is DMARC?

### Answer

> DMARC (Domain-based Message Authentication, Reporting & Conformance) works with SPF and DKIM to define how receiving mail servers should handle emails that fail authentication checks, helping prevent spoofing and phishing.

---

## 15. Difference between SPF, DKIM, and DMARC

| Protocol | Purpose |
|----------|---------|
| **SPF** | Verifies the sending mail server. |
| **DKIM** | Verifies the email has not been modified using a digital signature. |
| **DMARC** | Defines how to handle emails that fail SPF or DKIM checks. |

---

## 16. What indicators make an email suspicious?

### Answer

Common indicators include:

- Fake sender address
- Urgent language
- Suspicious links
- Unexpected attachments
- Grammar or spelling mistakes
- Domain mismatch
- Requests for passwords or sensitive information

---

## 17. How do you investigate a phishing email?

### Answer

> First, I verify the sender's email address and domain. Then, I analyze the email header, including the **From**, **Reply-To**, **Return-Path**, and **Received** fields. Next, I inspect URLs by hovering over them without clicking and scan any attachments using approved security tools. I search the SIEM or email gateway to determine whether other users received the same email. If the email is confirmed as malicious, I block the sender, domain, and URLs, isolate any affected endpoints if necessary, reset compromised credentials, document the investigation, and escalate the incident according to the organization's Incident Response process.

---

## 18. Which tools are commonly used for Email Security?

### Answer

Common Email Security tools include:

- Microsoft Defender for Office 365
- Proofpoint
- Mimecast
- Cisco Secure Email



## SOC Analyst Workflow (Phishing Email Investigation)

```text
Phishing Email Received
        ↓
Verify Sender
        ↓
Analyze Email Header
        ↓
Check URLs
        ↓
Scan Attachments
        ↓
Search if Other Users Received It
        ↓
Block Sender / Domain / URL
        ↓
Contain the Threat
        ↓
Document & Report
```

### Step 1: Verify Sender

- Verify the sender's email address.
- Check the display name.
- Verify the sender's domain.
- Look for domain mismatches.

**Example**

**Legitimate**
```text
support@microsoft.com
```

**Fake**
```text
support@micr0soft.com
```

---

### Step 2: Analyze Email Header

Check the following fields:

- From
- Return-Path
- Reply-To
- Message-ID
- Received

**Purpose:** Identify the actual sender and detect email spoofing.

---

### Step 3: Check URLs

- Hover over links before clicking.
- Compare the displayed URL with the actual URL.
- Look for misspelled domains.

**Example**

**Legitimate**
```text
https://login.microsoft.com
```

**Fake**
```text
https://login-micr0soft.com
```

---

### Step 4: Scan Attachments

- Check the file type.
- Scan the attachment using VirusTotal (or approved security tools).
- Look for suspicious file extensions.

**Examples**

```text
invoice.pdf.exe
salary.zip
payment.xlsm
document.docm
```

---

### Step 5: Search if Other Users Received It

Search for:

- Same sender
- Same subject
- Same URL
- Same attachment hash

**Purpose:** Determine whether multiple users received the phishing email.

---

### Step 6: Block Sender / Domain / URL

If confirmed malicious, block:

- Sender email
- Domain
- URL
- IP Address (if applicable)
- File Hash (if applicable)

---

### Step 7: Contain the Threat

If a user interacted with the email:

- Disable the compromised account (if required).
- Isolate the affected endpoint.
- Reset the user's password.
- Remove malicious emails from mailboxes.
- Block identified IOCs.

---

### Step 8: Document & Report

Document:

- Timeline
- Sender
- Subject
- Impact
- IOCs
- Actions Taken
- Final Status

Escalate the incident if required.

## Interview Question

### Q. How do you investigate a phishing email?

**Answer:**

> First, I verify the sender's email address and domain. Then, I analyze the email header, including the **From**, **Reply-To**, **Return-Path**, and **Received** fields. Next, I inspect URLs by hovering over them without clicking and scan any attachments using approved security tools. I search the SIEM or email gateway to determine whether other users received the same email. If the email is confirmed as malicious, I block the sender, domain, and URLs, isolate any affected endpoints if necessary, reset compromised credentials, document the investigation, and escalate the incident according to the organization's Incident Response process.
>

## Phishing Investigation Workflow

```text
Verify Sender
      ↓
Analyze Header
      ↓
Check URLs
      ↓
Scan Attachments
      ↓
Search Other Recipients
      ↓
Block Malicious Indicators
      ↓
Contain
      ↓
Document & Escalate
```
