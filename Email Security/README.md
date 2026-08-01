1. Email Security Basics
What is Email Security?
Definition

Email Security is the process of protecting email accounts, messages, and users from cyber threats such as phishing, malware, spam, spoofing, and Business Email Compromise (BEC).

Simple Definition

Email Security protects email communication from unauthorized access and cyberattacks.

Why is Email Security Important?

Email is one of the most common attack vectors used by cybercriminals.

Importance
Prevents phishing attacks
Blocks malware
Protects sensitive information
Prevents account compromise
Reduces spam
Prevents Business Email Compromise (BEC)
Common Email-Based Attacks
Phishing
Spear Phishing
Whaling
Business Email Compromise (BEC)
Email Spoofing
Malicious Attachments
Malicious Links
Spam
2. Email Protocols
SMTP (Simple Mail Transfer Protocol)
Definition

SMTP is used to send emails from a client to a mail server or between mail servers.

Example
You send an email

↓

SMTP sends it

↓

Mail Server
Uses
Sending emails
Server-to-server email transfer
POP3 (Post Office Protocol Version 3)
Definition

POP3 is used to download emails from the mail server to the user's device.

Features
Downloads emails locally
Emails are often removed from the server after download
Best for using a single device
Example
Mail Server

↓

Download Email

↓

Laptop
IMAP (Internet Message Access Protocol)
Definition

IMAP allows users to access and synchronize emails across multiple devices.

Features
Emails remain on the server
Syncs across devices
Supports folders and read/unread status
Example
Mail Server

↓

Laptop

↓

Mobile

↓

Tablet
SMTP vs POP3 vs IMAP
| Protocol | Purpose | Emails Stored | Best For |
|----------|---------|---------------|----------|
| SMTP | Sending emails | Mail Server | Sending emails |
| POP3 | Receiving emails | Local Device | Single device access |
| IMAP | Receiving & Syncing emails | Mail Server | Multiple devices |
3. Email Authentication
SPF (Sender Policy Framework)
Definition

SPF verifies whether the sending mail server is authorized to send emails for a domain.

Purpose

Prevents sender spoofing.

Example
company.com

↓

Authorized Mail Server

↓

Email Accepted
DKIM (DomainKeys Identified Mail)
Definition

DKIM adds a digital signature to outgoing emails.

The receiving server verifies the signature to ensure the email was not modified.

Purpose

Maintains email integrity.

DMARC (Domain-based Message Authentication, Reporting & Conformance)
Definition

DMARC tells receiving mail servers what to do if SPF or DKIM validation fails.

Policies
None
Quarantine
Reject
Purpose

Prevents phishing and email spoofing.

Difference
| Protocol | Purpose |
|----------|---------|
| SPF | Verifies the sending mail server. |
| DKIM | Verifies the email has not been modified using a digital signature. |
| DMARC | Defines how to handle emails that fail SPF or DKIM checks. |
4. Email Attacks
Phishing

A fake email designed to steal credentials or sensitive information.

Spear Phishing

A targeted phishing attack aimed at a specific individual or organization.

Whaling

A phishing attack targeting high-profile executives such as CEOs or CFOs.

Business Email Compromise (BEC)

An attacker impersonates a trusted business executive or vendor to trick employees into transferring money or sharing confidential data.

Email Spoofing

The attacker forges the sender's email address to appear as a trusted source.

Malicious Attachments

Attachments containing malware.

Examples:

PDF
Word Document
ZIP File
Excel File
Malicious Links

Links that redirect users to:

Fake login pages
Malware download sites
Credential theft websites
5. Indicators of a Phishing Email
Fake sender address
Urgent language ("Act Now!", "Account will be suspended")
Suspicious or shortened links
Unexpected attachments
Grammar or spelling mistakes
Domain mismatch
Requests for passwords or sensitive information
6. Email Header Analysis
From

Shows the displayed sender email address.

To

Shows the recipient.

Return-Path

Shows the address used for handling bounced emails.

Useful for identifying spoofed emails.

Received

Shows the path the email took through mail servers.

Helps determine the true origin.

Message-ID

A unique identifier assigned to each email.

Useful for tracking and investigations.

Reply-To

Specifies where replies should be sent.

Attackers often change this to redirect responses.

7. Email Security Tools
Tool	Purpose
Microsoft Defender for Office 365	Protects against phishing, malware, and malicious attachments.
Proofpoint	Email security, phishing protection, and threat detection.
Mimecast	Email filtering, spam protection, and email security.
Cisco Secure Email	Email gateway that blocks spam, phishing, and malware.
Remaining Interview Questions
1. What is phishing?

Answer:

Phishing is a cyberattack where attackers send fraudulent emails pretending to be from trusted sources to steal credentials, financial information, or other sensitive data.

2. Difference between phishing and spear phishing?
| Phishing | Spear Phishing |
|----------|----------------|
| Targets many users | Targets a specific person or organization |
| Generic email | Personalized email |
| Lower success rate | Higher success rate |
3. What is BEC?

Answer:

Business Email Compromise (BEC) is an attack in which a cybercriminal impersonates a trusted executive, employee, or vendor to trick someone into transferring money or disclosing sensitive information.

4. What is SPF?

Answer:

SPF (Sender Policy Framework) is an email authentication method that verifies whether the sending mail server is authorized to send emails for a domain.

5. What is DKIM?

Answer:

DKIM (DomainKeys Identified Mail) uses a digital signature to verify that an email has not been modified during transmission.

6. What is DMARC?

Answer:

DMARC (Domain-based Message Authentication, Reporting & Conformance) works with SPF and DKIM to define how receiving mail servers should handle emails that fail authentication checks, helping prevent spoofing and phishing.

7. What indicators make an email suspicious?

Answer:

Common indicators include a fake sender address, urgent language, suspicious links, unexpected attachments, grammar or spelling mistakes, domain mismatches, and requests for sensitive information such as passwords or banking details.