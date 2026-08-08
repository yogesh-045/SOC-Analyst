# ☁️ Cloud Security Threats

Cloud environments provide flexibility and scalability, but they also introduce security risks if they are not configured and monitored properly.

As a SOC Analyst, understanding common cloud security threats helps detect, investigate, and respond to security incidents.

---

# What are Cloud Security Threats?

## Definition

Cloud Security Threats are risks or attacks that can compromise the confidentiality, integrity, or availability of cloud resources and data.

## Simple Definition

Cloud Security Threats are attacks or mistakes that can expose cloud resources or sensitive information.

---

# 1. Misconfigured S3 Bucket

## Definition

A misconfigured S3 bucket is an Amazon S3 storage bucket with incorrect permissions that allow unauthorized users to access its contents.

## Simple Definition

An S3 bucket is accidentally made public, allowing anyone on the Internet to access stored files.

### Example

A company stores customer records in an S3 bucket.

The bucket is configured as **Public**, allowing anyone to download sensitive files.

### Risks

- Data leakage
- Financial loss
- Compliance violations

### SOC Analyst Perspective

Monitor for:

- Public bucket permissions
- Bucket policy changes
- Large data downloads
- Unauthorized access attempts

---

# 2. Exposed Credentials

## Definition

Exposed credentials occur when usernames, passwords, API keys, or access keys are accidentally disclosed.

## Simple Definition

Cloud credentials become visible to unauthorized users.

### Example

A developer uploads AWS Access Keys to a public GitHub repository.

### Risks

- Unauthorized cloud access
- Resource deletion
- Data theft
- Privilege abuse

### SOC Analyst Perspective

Monitor for:

- New logins using exposed accounts
- API key usage from unusual locations
- Unexpected IAM activity
- Root account access

---

# 3. Public Storage

## Definition

Public Storage refers to cloud storage resources that are accessible from the Internet without proper restrictions.

## Simple Definition

Cloud files are publicly accessible when they should be private.

### Example

An Azure Storage Account containing employee documents is configured for public access.

### Risks

- Sensitive data exposure
- Information leakage
- Privacy violations

### SOC Analyst Perspective

Monitor for:

- Public storage containers
- Anonymous access
- Large downloads
- Permission changes

---

# 4. Weak IAM Policies

## Definition

Weak IAM policies grant users more permissions than required.

## Simple Definition

Users receive excessive access rights.

### Example

A developer is granted **Administrator** permissions instead of **Read-Only** access.

### Risks

- Privilege escalation
- Insider abuse
- Unauthorized resource modification

### SOC Analyst Perspective

Monitor for:

- IAM policy changes
- Administrator role assignments
- Privilege escalation events
- New IAM users

---

# 5. Data Breach

## Definition

A Data Breach occurs when sensitive information is accessed, stolen, or exposed without authorization.

## Simple Definition

Confidential data is leaked or stolen.

### Example

An attacker gains access to a cloud database and steals customer information.

### Risks

- Financial loss
- Legal penalties
- Reputation damage

### SOC Analyst Perspective

Monitor for:

- Large data transfers
- Unusual download activity
- Unauthorized database access
- Suspicious API calls

---

# 6. Insider Threat

## Definition

An Insider Threat occurs when an employee, contractor, or trusted user intentionally or unintentionally compromises cloud security.



### Example

An employee copies confidential company files to a personal cloud storage account.

### Risks

- Data theft
- Intellectual property loss
- Compliance violations

### SOC Analyst Perspective

Monitor for:

- Unusual file downloads
- Access outside business hours
- Privilege misuse
- Data uploads to external services

---

# Cloud Security Threats Comparison

| Threat | Description | Example |
|----------|-------------|---------|
| Misconfigured S3 Bucket | Incorrect bucket permissions | Public customer data |
| Exposed Credentials | Leaked passwords or API keys | AWS keys on GitHub |
| Public Storage | Publicly accessible cloud storage | Public Azure Storage |
| Weak IAM Policies | Excessive permissions | Developer with Admin access |
| Data Breach | Unauthorized access to sensitive data | Customer database leaked |
| Insider Threat | Misuse by trusted users | Employee copying company data |

---

# Common Detection Methods

| Threat | Detection Method |
|----------|-----------------|
| Misconfigured S3 Bucket | AWS Config, Security Hub, CloudTrail |
| Exposed Credentials | GitHub Secret Scanning, IAM Logs |
| Public Storage | Azure Security Center, Defender for Cloud |
| Weak IAM Policies | IAM Access Analyzer, Permission Reviews |
| Data Breach | SIEM Alerts, DLP Solutions |
| Insider Threat | UEBA, EDR, SIEM Monitoring |

---

# SOC Analyst Responsibilities

A SOC Analyst should:

- Monitor cloud logs
- Detect suspicious logins
- Investigate IAM changes
- Identify exposed storage
- Review CloudTrail logs
- Review Azure Monitor logs
- Validate alerts
- Escalate confirmed incidents
- Document findings

---

# Key Points to Remember

- Misconfigured cloud storage is a common cause of data breaches.
- Never expose cloud credentials.
- Apply the Principle of Least Privilege.
- Monitor cloud logs regularly.
- Enable MFA for privileged accounts.
- Investigate unusual user activity.

---

# Interview Questions

## 1. What are common cloud security threats?

### Answer

Common cloud security threats include:

- Misconfigured S3 Buckets
- Exposed Credentials
- Public Storage
- Weak IAM Policies
- Data Breaches
- Insider Threats

---

## 2. What is a Misconfigured S3 Bucket?

### Answer

A Misconfigured S3 Bucket is an Amazon S3 bucket with incorrect permissions that allows unauthorized users to access stored data.

---

## 3. What are Exposed Credentials?

### Answer

Exposed Credentials are usernames, passwords, API keys, or access keys that are accidentally disclosed, allowing attackers to access cloud resources.

---

## 4. Why are Weak IAM Policies dangerous?

### Answer

Weak IAM policies grant excessive permissions, increasing the risk of privilege escalation, unauthorized access, and insider threats.

---

## 5. What is an Insider Threat?

### Answer

An Insider Threat occurs when a trusted user intentionally or unintentionally compromises cloud security by misusing authorized access.

---

## 6. How can cloud security threats be detected?

### Answer

Cloud security threats can be detected using:

- AWS CloudTrail
- Azure Monitor
- Microsoft Defender for Cloud
- SIEM solutions
- EDR/XDR
- IAM activity monitoring

---

# Summary

- Cloud Security Threats can expose sensitive data and cloud resources.
- Common threats include Misconfigured S3 Buckets, Exposed Credentials, Public Storage, Weak IAM Policies, Data Breaches, and Insider Threats.
- SOC Analysts detect these threats by monitoring cloud logs, IAM activities, storage permissions, and security alerts.
- Following security best practices and continuous monitoring helps reduce cloud security risks.
