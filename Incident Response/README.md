# 🚨 Incident Response (IR)

## 📌 What is Incident Response?

**Incident Response (IR)** is a structured process used to identify, analyze, contain, eradicate, recover from, and learn from cybersecurity incidents such as malware infections, phishing attacks, ransomware, unauthorized access, or data breaches.

> **Simple Definition:**  
> Incident Response is the process of **detecting, investigating, stopping, and recovering from a cyberattack while minimizing damage.**

---

# 🎯 Why is Incident Response Important?

- ✅ Minimizes business impact
- ✅ Reduces downtime
- ✅ Protects sensitive data
- ✅ Prevents attackers from spreading
- ✅ Helps organizations recover quickly
- ✅ Improves future security

---

# 🔐 What is a Security Incident?

A **Security Incident** is any event that compromises or has the potential to compromise the **Confidentiality, Integrity, or Availability (CIA)** of systems or data.

## Examples

- Malware Infection
- Ransomware Attack
- Phishing Email
- Brute-Force Attack
- Data Breach
- Insider Threat
- Unauthorized Login
- DDoS Attack

---

# 🔄 Incident Response Lifecycle (NIST)

```text
Preparation
      │
      ▼
Detection & Analysis
      │
      ▼
Containment
      │
      ▼
Eradication
      │
      ▼
Recovery
      │
      ▼
Lessons Learned
```

---

# 1️⃣ Preparation

Preparation involves getting people, tools, and processes ready before an incident occurs.

## Activities

- Create Incident Response Plan
- Define Team Roles
- Deploy SIEM (Splunk, Sentinel)
- Install EDR/XDR
- Configure Backups
- Enable Logging
- Conduct Security Awareness Training
- Prepare Communication Plans

### Example

A company installs **Microsoft Defender** and **Splunk** before any cyberattack occurs.

---

# 2️⃣ Detection & Analysis

Identify whether an alert is a real security incident and determine its scope and impact.

## Activities

- Monitor SIEM Alerts
- Review Windows Event Logs
- Analyze EDR Alerts
- Check Firewall Logs
- Investigate Suspicious IPs
- Collect Indicators of Compromise (IOCs)

### Example

```text
Splunk Alert

100 Failed Login Attempts

Event ID : 4625

Source IP : 192.168.1.50
```

SOC Analysts investigate whether it is a brute-force attack.

---

# 3️⃣ Containment

Containment limits the attack to prevent further damage.

## Activities

- Isolate Infected Computers
- Disable Compromised Accounts
- Block Malicious IP Addresses
- Disconnect Affected Systems
- Stop Malicious Processes

### Example

```text
Ransomware Detected

↓

Isolate Employee Laptop

↓

Malware Cannot Spread
```

---

# 4️⃣ Eradication

Remove the root cause of the incident.

## Activities

- Delete Malware
- Remove Malicious Files
- Close Vulnerabilities
- Patch Systems
- Reset Compromised Passwords
- Remove Persistence Mechanisms

### Example

The malware is removed and the vulnerable application is patched.

---

# 5️⃣ Recovery

Restore systems to normal operations safely.

## Activities

- Restore Data from Backups
- Reconnect Systems
- Verify Systems are Clean
- Monitor Suspicious Activity
- Resume Business Operations

### Example

The cleaned laptop is verified and safely reconnected to the network.

---

# 6️⃣ Lessons Learned

Review the incident to improve future defenses.

## Activities

- Document the Incident
- Identify Root Cause
- Update Security Controls
- Improve Detection Rules
- Train Employees
- Update the Incident Response Plan

### Example

The organization enables **Multi-Factor Authentication (MFA)** after a credential compromise.

---

# 🌍 Real-World Incident Response Example

## Scenario

An employee receives a phishing email.

### Step 1 — Detection

- Employee clicks the phishing link.
- SIEM detects suspicious login activity.

---

### Step 2 — Analysis

SOC Analyst investigates:

```text
Email Logs
      │
      ▼
Windows Logs
      │
      ▼
IP Address
      │
      ▼
User Activity
```

The account is confirmed to be compromised.

---

### Step 3 — Containment

- Disable User Account
- Block Attacker IP
- Isolate Affected Endpoint

---

### Step 4 — Eradication

- Remove Malware
- Reset User Password
- Delete Malicious Files

---

### Step 5 — Recovery

- Restore Files
- Re-enable User Account
- Verify Normal Operations

---

### Step 6 — Lessons Learned

- Update Phishing Detection Rules
- Conduct Employee Awareness Training
- Enable Multi-Factor Authentication (MFA)

---

# 👨‍💻 SOC Analyst Responsibilities During Incident Response

- Monitor SIEM Alerts
- Investigate Suspicious Activity
- Analyze Logs
- Validate Alerts (True Positive / False Positive)
- Escalate Incidents
- Document Findings
- Coordinate with Incident Response Team
- Recommend Containment Actions

---

# 🛠️ Common Incident Response Tools

| Tool | Category |
|------|----------|
| Splunk | SIEM |
| Microsoft Sentinel | Cloud SIEM / SOAR |
| Microsoft Defender XDR | XDR / EDR |
| CrowdStrike Falcon | EDR |
| Sysmon | Windows Monitoring |
| Wireshark | Network Analysis |
| Volatility | Memory Forensics |
| FTK Imager | Digital Forensics |
| VirusTotal | Threat Intelligence |
| Nmap | Network Scanning |

---

# 📖 Purpose & Example Use Cases

| Tool | Purpose | Example Use Case |
|------|---------|------------------|
| Splunk | Log Collection & Analysis | Detect brute-force attacks (Event ID 4625) |
| Microsoft Sentinel | Cloud SIEM & SOAR | Detect suspicious Azure AD logins |
| Microsoft Defender XDR | Endpoint, Identity & Email Protection | Detect ransomware & malware |
| CrowdStrike Falcon | Endpoint Detection & Response | Isolate compromised endpoints |
| Sysmon | Windows Event Logging | Monitor process creation |
| Wireshark | Packet Analysis | Analyze suspicious network traffic |
| Volatility | Memory Forensics | Investigate malware from RAM |
| FTK Imager | Disk Forensics | Acquire forensic disk images |
| VirusTotal | Threat Intelligence | Check malicious file hashes & URLs |
| Nmap | Network Discovery | Discover open ports & services |

---

# 📋 Incident Response Workflow

```text
Security Alert
      │
      ▼
Validate Alert
      │
      ▼
Investigate Logs
      │
      ▼
Collect IOCs
      │
      ▼
Contain Threat
      │
      ▼
Remove Malware
      │
      ▼
Recover Systems
      │
      ▼
Document Findings
      │
      ▼
Lessons Learned
```

---

# 🎤 Interview Questions

## Q1. What is Incident Response?

**Answer:**

Incident Response is a structured process used to detect, investigate, contain, eradicate, recover from, and learn from cybersecurity incidents while minimizing business impact.

---

## Q2. What are the six phases of Incident Response?

- Preparation
- Detection & Analysis
- Containment
- Eradication
- Recovery
- Lessons Learned

---

## Q3. What is the difference between Containment and Eradication?

| Containment | Eradication |
|-------------|-------------|
| Stops the attack from spreading | Removes the root cause of the attack |
| Temporary action | Permanent cleanup |

---

## Q4. What should you do if ransomware is detected?

1. Validate the alert
2. Isolate the infected endpoint
3. Stop malicious processes
4. Collect evidence
5. Remove malware
6. Restore data from backups
7. Monitor the environment
8. Document the incident

---

## Q5. How would you investigate a phishing incident?

- Analyze Email Headers
- Review Sender Domain
- Check URLs & Attachments
- Review SIEM Logs
- Investigate User Activity
- Collect IOCs
- Contain the Incident
- Document Findings

---

## Q6. What tools are commonly used in Incident Response?

- Splunk
- Microsoft Sentinel
- Microsoft Defender XDR
- CrowdStrike Falcon
- Sysmon
- Wireshark
- Volatility
- FTK Imager
- VirusTotal
- Nmap

---

## Q7. Why is documentation important during an incident?

Documentation helps with:

- Evidence Collection
- Compliance
- Root Cause Analysis
- Future Improvements
- Incident Reporting

---

## Q8. What is the role of a SOC Analyst during Incident Response?

- Monitor Alerts
- Investigate Logs
- Validate Alerts
- Analyze IOCs
- Contain Threats
- Escalate Incidents
- Document Findings

---

## Q9. What is an Indicator of Compromise (IOC)?

An IOC is evidence that a system has already been compromised.

**Examples:**

- Malicious IP
- File Hash
- Domain
- URL
- Registry Key

---

## Q10. What is the difference between an Event and an Incident?

| Event | Incident |
|--------|----------|
| Any system activity | Security event that threatens CIA |
| May be normal | Requires investigation and response |

---

# 📝 Key Points to Remember

- ✅ Preparation → Be ready before an attack.
- ✅ Detection & Analysis → Identify and investigate the incident.
- ✅ Containment → Stop the attack from spreading.
- ✅ Eradication → Remove malware and eliminate the root cause.
- ✅ Recovery → Restore systems safely.
- ✅ Lessons Learned → Improve defenses to prevent future attacks.
