# 3. IOC — Indicators of Compromise ⭐⭐⭐

## What is IOC?

**IOC (Indicator of Compromise)** is a piece of evidence that indicates a system or network may be compromised or involved in malicious activity.

Common IOCs include:

- IP Address
- Domain
- URL
- File Hash
- Email Address
- Malicious Files

---

## 1. IP Address

A malicious IP address can indicate communication with an attacker-controlled server or malicious infrastructure.

**Example:**

`185.XX.XX.XX`

**SOC Use:**

- Search SIEM, firewall, proxy, and network logs
- Identify suspicious connections
- Block the IP if confirmed malicious
- Investigate affected systems

---

## 2. Domain

A malicious domain may be used for phishing, malware delivery, or Command and Control (C2).

**Example:**

`malicious-example.com`

**SOC Use:**

- Search DNS and proxy logs
- Check domain reputation
- Identify users/systems accessing the domain
- Block the domain if confirmed malicious

---

## 3. URL

A malicious URL can redirect users to phishing pages, malware downloads, or exploit pages.

**Example:**

`http://malicious-example.com/payload.exe`

**SOC Use:**

- Investigate web activity
- Identify users who accessed the URL
- Check for downloaded files
- Block the URL if confirmed malicious

---

## 4. File Hash

A file hash is a unique value generated from a file. It can be used to identify known malicious files.

**Common Hash Types:**

- MD5
- SHA-1
- SHA-256

**Example:**

`SHA256: abc123...`

**SOC Use:**

- Search EDR/SIEM for the hash
- Identify affected endpoints
- Verify whether the file is malicious
- Quarantine or remove the file

---

## 5. Email

Email-related information can be used as an IOC during phishing investigations.

**Examples:**

- Malicious sender address
- Suspicious sender domain
- Malicious attachment
- Phishing URL
- Suspicious email headers

**Example:**

`attacker@malicious-example.com`

**SOC Use:**

- Analyze email headers
- Check sender reputation
- Investigate attachments and URLs
- Search for similar emails
- Remove malicious emails from mailboxes

---

## 6. Malicious Files

Malicious files are files designed to perform unauthorized or harmful actions.

**Examples:**

- `invoice.exe`
- `payload.dll`
- `update.bat`
- `script.ps1`
- `document.docm`

**SOC Use:**

Analysts investigate:

- File name
- File path
- File hash
- Parent process
- Process execution
- User
- Network connections

---

## IOC Investigation Workflow

```text
IOC Identified
      ↓
Validate IOC
      ↓
Search SIEM / EDR
      ↓
Find Related Activity
      ↓
Identify Affected Systems
      ↓
Investigate
      ↓
Contain / Block
      ↓
Incident Response
