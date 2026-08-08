# 🕵️ Threat Hunting

## 📌 What is Threat Hunting?

**Threat Hunting** is a proactive cybersecurity process where security analysts actively search for hidden threats, attackers, or malicious activities that have bypassed traditional security tools.

> **Simple Definition:**  
> Threat Hunting is the proactive process of searching for hidden cyber threats inside an organization's network before they cause damage.

---

# 🎯 Why is Threat Hunting Important?

- ✅ Detects hidden attackers
- ✅ Finds threats missed by Antivirus or EDR
- ✅ Reduces attacker dwell time
- ✅ Improves overall security posture
- ✅ Prevents data breaches
- ✅ Improves detection rules

---

# 🔄 How Threat Hunting Works

```text
Collect Logs
      │
      ▼
Analyze Data
      │
      ▼
Look for Suspicious Activity
      │
      ▼
Identify IOC / IOA
      │
      ▼
Investigate
      │
      ▼
Contain Threat
      │
      ▼
Report Findings
```

---

# 🏢 Why Organizations Perform Threat Hunting

Traditional security tools cannot detect every attack.

Threat Hunting helps security teams proactively identify hidden attackers before they can cause serious damage.

## Benefits

- Detect hidden threats
- Reduce attacker dwell time
- Find malware missed by Antivirus
- Improve security posture
- Prevent data breaches
- Improve detection rules

### Example

```text
Attacker steals employee credentials

↓

No Antivirus Alert

↓

Threat Hunter notices:

• Login at 3:00 AM
• Impossible Travel
• PowerShell Execution

↓

Attack Detected Before Data Theft
```

---

# 📊 Common Data Sources

Threat Hunters collect data from multiple sources, including:

- Windows Event Logs
- Sysmon Logs
- EDR Alerts
- Firewall Logs
- DNS Logs
- Proxy Logs
- Authentication Logs
- Network Traffic

---

# 🔍 Threat Hunting Examples

## Example 1 — PowerShell Abuse

Threat Hunter searches for:

```text
powershell.exe
```

Finds PowerShell downloading a file from an unknown website.

### Result

Malware is discovered.

---

## Example 2 — Multiple Failed Logins

SIEM shows:

```text
Event ID : 4625

100 Failed Login Attempts

Same Source IP
```

### Possible Threat

Brute-force attack.

---

## Example 3 — Suspicious Network Connection

```text
Employee Laptop

↓

Unknown Foreign IP

↓

Possible C2 Communication
```

SOC Analyst investigates the suspicious connection.

---

# 🛡️ Types of Threat Hunting

## 1️⃣ Structured Hunting

Starts with a known attacker technique (usually from MITRE ATT&CK).

### Examples

- PowerShell Abuse
- Credential Dumping
- Lateral Movement

---

## 2️⃣ Unstructured Hunting

Triggered by suspicious alerts or unusual activity.

### Example

```text
EDR Alert

↓

Suspicious PowerShell Activity

↓

SOC Investigation
```

---

## 3️⃣ Intelligence-Driven Hunting

Uses Threat Intelligence such as IOCs, threat feeds, malware reports, or known attacker infrastructure.

### Example

```text
Threat Intelligence

↓

Malicious IP

185.220.101.45

↓

Search Firewall & Proxy Logs
```

---

# 🚩 IOC vs IOA

| IOC (Indicator of Compromise) | IOA (Indicator of Attack) |
|--------------------------------|----------------------------|
| Malicious IP Address | PowerShell Downloading Malware |
| Malicious File Hash | Office Spawning cmd.exe |
| Malicious Domain | LSASS Memory Access |
| Suspicious URL | Multiple Failed Logins |

---

# 🛠️ Common Threat Hunting Tools

| Tool | Purpose |
|------|---------|
| Splunk | Log Analysis & SIEM |
| Microsoft Sentinel | Cloud SIEM |
| Microsoft Defender for Endpoint | EDR |
| CrowdStrike Falcon | EDR |
| Sysmon | Windows Event Logging |
| Wireshark | Network Traffic Analysis |
| VirusTotal | Threat Intelligence |
| Nmap | Network Discovery & Port Scanning |

---

# 🔄 Threat Hunting Process

```text
Define Hypothesis
      │
      ▼
Collect Logs
      │
      ▼
Search Suspicious Activity
      │
      ▼
Analyze IOC & IOA
      │
      ▼
Investigate Systems
      │
      ▼
Contain Threat
      │
      ▼
Document Findings
```

---

# ⚖️ Threat Hunting vs Incident Response

| Threat Hunting | Incident Response |
|----------------|-------------------|
| Proactive | Reactive |
| Searches for hidden threats | Responds to confirmed incidents |
| Focuses on suspicious behavior | Focuses on investigation & recovery |
| Goal is early detection | Goal is containment & recovery |

---

# 👨‍💻 SOC Analyst Responsibilities

- Monitor SIEM & EDR Logs
- Search for Suspicious Activities
- Analyze Windows Event Logs
- Investigate IOCs & IOAs
- Validate Alerts
- Escalate Confirmed Threats
- Document Findings

---

# 🗺️ MITRE ATT&CK Framework

## What is MITRE ATT&CK?

MITRE ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge) is a knowledge base of real-world attacker behavior.

It helps defenders understand how attackers operate and improve threat detection.

---

# 🎯 Tactics

A **Tactic** represents the attacker's objective.

Examples:

- Initial Access
- Execution
- Persistence
- Privilege Escalation
- Defense Evasion
- Credential Access
- Discovery
- Lateral Movement
- Collection
- Exfiltration
- Impact

---

# 🔧 Techniques

A **Technique** describes how an attacker achieves a tactic.

### Example

```text
Credential Dumping
```

---

# ⚙️ Procedures

A **Procedure** describes the exact tools or commands attackers use.

### Example

```text
Mimikatz

or

Dump LSASS Memory
```

---

# 📌 TTP

| Component | Meaning |
|-----------|---------|
| Tactics | Why the attacker performs an action |
| Techniques | How the attacker performs the action |
| Procedures | Exact tools or commands used |

---

# 🎤 Interview Questions

## Q1. What is Threat Hunting?

**Answer:**

Threat Hunting is the proactive process of searching for hidden cyber threats inside an organization's environment before they are detected by automated security tools.

---

## Q2. Why is Threat Hunting important?

- Detects hidden attackers
- Reduces attacker dwell time
- Finds threats missed by security tools
- Improves overall security posture

---

## Q3. Threat Hunting vs Incident Response

| Threat Hunting | Incident Response |
|----------------|-------------------|
| Proactive | Reactive |
| Finds hidden threats | Responds to incidents |

---

## Q4. Which tools are commonly used?

- Splunk
- Microsoft Sentinel
- Microsoft Defender for Endpoint
- CrowdStrike Falcon
- Sysmon
- Wireshark
- VirusTotal
- Nmap

---

## Q5. What is the goal of Threat Hunting?

To proactively identify, investigate, and eliminate hidden threats before they impact the organization.

---

## Q6. What are IOCs?

Indicators of Compromise are pieces of evidence suggesting a system has already been compromised.

### Examples

- Malicious IP
- Domain
- URL
- File Hash
- Registry Key

---

## Q7. What are TTPs?

| Term | Meaning |
|------|---------|
| Tactics | Why |
| Techniques | How |
| Procedures | Exact Tool/Method |

---

## Q8. What is MITRE ATT&CK?

MITRE ATT&CK is a publicly available knowledge base of attacker tactics and techniques used by security teams for detection, investigation, and threat hunting.

---

## Q9. Which logs are useful for Threat Hunting?

- Windows Event Logs
- Sysmon Logs
- EDR Logs
- Firewall Logs
- DNS Logs
- Proxy Logs
- SIEM Logs
- Authentication Logs

---

## Q10. How do you investigate a brute-force attack?

1. Review Event ID **4625** (Failed Logins)
2. Identify Source IP
3. Identify Target User
4. Check Timestamps
5. Look for Event ID **4624** (Successful Login)
6. Correlate SIEM & EDR Logs
7. Determine if the attack succeeded
8. Block Malicious IP (if required)
9. Escalate the Incident
10. Document Findings

---

# 📝 Key Points to Remember

- ✅ Threat Hunting is **Proactive**.
- ✅ Uses logs, telemetry, and threat intelligence.
- ✅ Searches for hidden attackers before alerts are generated.
- ✅ Relies heavily on IOC, IOA, and MITRE ATT&CK.
- ✅ Helps reduce attacker dwell time.
- ✅ Improves an organization's overall detection capability.
