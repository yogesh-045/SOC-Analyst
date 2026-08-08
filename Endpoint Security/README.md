# 🛡️ Endpoint Security

## 📌 What is an Endpoint?

An **endpoint** is any device connected to a network that can send or receive data.

These devices are common entry points for attackers, making endpoint security a critical part of cybersecurity.

### Examples of Endpoints

- 🖥️ Desktop Computer
- 💻 Laptop
- 📱 Mobile Phone
- 📟 Tablet
- 🖧 Server
- ☁️ Virtual Machine (VM)
- 📹 IoT Devices
- 💳 POS (Point of Sale) Systems

---

# Types of Endpoints

| Endpoint | Example | Description |
|----------|---------|-------------|
| Desktop | Office PC | Workstation used by employees |
| Laptop | Employee Laptop | Portable device for office/remote work |
| Server | Windows/Linux Server | Provides services and applications |
| Mobile | Android, iPhone | Access business applications |
| Tablet | iPad, Android Tablet | Mobile productivity device |
| Virtual Machine | VMware, Hyper-V | Software-based computer |
| IoT Device | Smart Camera, Printer | Internet-connected smart devices |
| POS Device | Billing Machine | Retail payment processing |

---

# Why Endpoint Security is Important

Without endpoint protection:

- Malware infection
- Ransomware attacks
- Credential theft
- Lateral movement
- Data breaches

### Example Attack

```text
Phishing Email
      │
      ▼
Employee Downloads Malware
      │
      ▼
Laptop Infected
      │
      ▼
Malware Spreads Across Company
```

Endpoint Security helps stop this attack before it spreads.

---

# Endpoint Security vs Network Security

| Feature | Endpoint Security | Network Security |
|----------|------------------|------------------|
| Scope | Individual Devices | Entire Network |
| Focus | Endpoints | Network Traffic |
| Technologies | AV, EPP, EDR, XDR | Firewall, IDS, IPS, VPN |
| Monitoring | Files, Registry, Processes | Packets, Ports, Protocols |
| Response | Isolate Device | Block Traffic |

---

# Antivirus (AV)

## What is Antivirus?

Antivirus detects malware using known malware signatures.

### Features

- Signature-based detection
- File scanning
- Virus removal

### Limitation

- Cannot detect many unknown attacks
- Weak against fileless malware

---

# Endpoint Protection Platform (EPP)

## What is EPP?

EPP combines Antivirus with additional preventive security controls.

### Features

- Antivirus
- Firewall
- Device Control
- USB Protection
- Web Protection
- Policy Management

### Purpose

Prevent attacks before they execute.

---

# Endpoint Detection & Response (EDR)

## What is EDR?

EDR continuously monitors endpoint activity, detects suspicious behavior, investigates threats, and responds automatically.

### Features

- Process Monitoring
- Behavioral Analysis
- Threat Hunting
- Endpoint Isolation
- Incident Investigation
- Timeline Analysis

### Purpose

Detect, investigate and respond to attacks.

---

# Extended Detection & Response (XDR)

## What is XDR?

XDR extends EDR by collecting telemetry from multiple security products.

### Data Sources

- Endpoint
- Email
- Identity
- Cloud
- Firewall
- Network
- Servers

### Purpose

Provide organization-wide visibility.

---

# AV vs EPP vs EDR vs XDR

| Feature | AV | EPP | EDR | XDR |
|----------|:--:|:--:|:--:|:--:|
| Malware Detection | ✅ | ✅ | ✅ | ✅ |
| Signature Detection | ✅ | ✅ | ✅ | ✅ |
| Behavioral Detection | ❌ | ⚠️ | ✅ | ✅ |
| Continuous Monitoring | ❌ | ⚠️ | ✅ | ✅ |
| Threat Hunting | ❌ | ❌ | ✅ | ✅ |
| Endpoint Isolation | ❌ | ❌ | ✅ | ✅ |
| Automated Response | ❌ | ⚠️ | ✅ | ✅ |
| Multi-Source Visibility | ❌ | ❌ | ❌ | ✅ |

---

# How EDR Works

## 1. Process Monitoring

Tracks every running process.

Examples:

- cmd.exe
- powershell.exe
- chrome.exe

---

## 2. File Monitoring

Monitors:

- File Creation
- File Modification
- File Deletion

Detects ransomware encryption.

---

## 3. Registry Monitoring

Detects registry modifications used for persistence.

---

## 4. Network Monitoring

Monitors

- Source IP
- Destination IP
- Ports
- Protocols

Detects suspicious outbound communication.

---

## 5. Behavioral Analysis

Example

```text
Word
  │
  ▼
PowerShell
  │
  ▼
Downloads Malware
  │
  ▼
🚨 Alert Generated
```

Instead of relying only on signatures, EDR analyzes behavior.

---

## 6. Alert Generation

Example Alert

```
Severity : High

Alert : PowerShell Download Attempt
```

---

## 7. Endpoint Isolation

```text
Company Network

     │
     ▼

PC-01 (Isolated)

Malware cannot spread
```

---

# Common Endpoint Threats

## Malware

Examples

- Virus
- Worm
- Trojan

---

## Ransomware

Examples

- WannaCry
- LockBit

---

## Trojan

Example

- Fake PDF Reader

---

## Fileless Malware

Runs in memory using:

- PowerShell
- WMI

No malicious file is written to disk.

---

## PowerShell Attacks

Attackers use PowerShell to

- Download Malware
- Execute Scripts
- Lateral Movement
- Persistence
- Credential Dumping

---

## Credential Dumping

Target

```
LSASS.exe
```

Common Tool

```
Mimikatz
```

---

# IOC (Indicator of Compromise)

Evidence that a system has already been compromised.

### Examples

- Malicious IP
- File Hash
- Domain
- URL
- Registry Key

---

# IOA (Indicator of Attack)

Suspicious attacker behavior indicating an attack is occurring.

### Examples

- PowerShell downloading files
- Office spawning cmd.exe
- LSASS access
- Multiple failed logins

---

# IOC vs IOA

| Feature | IOC | IOA |
|----------|-----|-----|
| Detection | Reactive | Proactive |
| Timing | After Attack | Before/During Attack |
| Focus | Evidence | Attacker Behavior |
| SOC Goal | Confirm Compromise | Stop Attack Early |

---

# EDR Investigation Workflow

```text
Alert
   │
   ▼
Validate Alert
   │
   ▼
Investigate Process
   │
   ▼
Check Parent Process
   │
   ▼
Check Command Line
   │
   ▼
Hash Analysis
   │
   ▼
Network Connections
   │
   ▼
Identify IOC / IOA
   │
   ▼
Contain Endpoint
   │
   ▼
Escalate
   │
   ▼
Document Findings
```

---

# Popular EDR Tools

| Vendor | Product |
|---------|---------|
| Microsoft | Defender for Endpoint |
| CrowdStrike | Falcon |
| SentinelOne | SentinelOne |
| Palo Alto | Cortex XDR |
| VMware | Carbon Black |
| Trellix | Trellix EDR |

---

# SOC Analyst Responsibilities

- Monitor EDR Alerts
- Validate True Positive vs False Positive
- Investigate Suspicious Processes
- Analyze Parent-Child Process
- Review File Hashes
- Check Network Connections
- Collect IOCs & IOAs
- Isolate Infected Endpoint
- Escalate High Severity Incidents
- Document Findings
- Recommend Remediation

---

# Interview Questions

## Q1. What is EDR?

**Answer**

EDR (Endpoint Detection and Response) continuously monitors endpoint activity, detects suspicious behavior, investigates threats, and enables rapid response such as endpoint isolation.

---

## Q2. Antivirus vs EDR

| Antivirus | EDR |
|------------|-----|
| Signature Based | Behavior + Signature Based |
| Detects Known Malware | Detects Known & Unknown Threats |
| Limited Visibility | Full Endpoint Visibility |
| No Threat Hunting | Supports Threat Hunting |

---

## Q3. EDR vs XDR

| EDR | XDR |
|------|-----|
| Endpoint Protection | Organization-wide Protection |
| Endpoint Telemetry | Multi-source Telemetry |
| Endpoint Focused | Enterprise Visibility |

---

## Q4. What is Endpoint Security?

Protecting endpoint devices like laptops, desktops, servers, and mobiles using AV, EPP, EDR, and XDR.

---

## Q5. What is IOC?

Evidence that indicates a system has already been compromised.

Examples:

- Malicious IP
- File Hash
- Domain
- Registry Key

---

## Q6. What is IOA?

Suspicious attacker behavior indicating an attack may be occurring.

Examples:

- Word spawning PowerShell
- LSASS Memory Access

---

## Q7. How does EDR detect malware?

- Process Monitoring
- File Monitoring
- Registry Monitoring
- Network Monitoring
- Behavioral Analysis
- Event Correlation
- Alert Generation

---

## Q8. What would you do if EDR detects ransomware?

1. Validate the Alert
2. Isolate Endpoint
3. Stop Malicious Process
4. Identify Affected Systems
5. Collect IOCs & Logs
6. Investigate Root Cause
7. Escalate to IR Team
8. Assist Recovery
9. Monitor Environment
10. Document Lessons Learned
