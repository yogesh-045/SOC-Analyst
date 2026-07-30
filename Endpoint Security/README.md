# What is an Endpoint?
An endpoint is any device connected to a network that can send or receive data.

These devices are potential entry points for attackers.

# Examples
Desktop Computer, Laptop, Mobile Phone, Tablet, Server, Virtual Machine (VM), IoT Devices, POS (Point of Sale) Systems

# Example
Internet
      │
───────────────
│      │      │
Laptop PC    Server
│      │      │
Endpoints

# Types of Endpoints
| Endpoint Type | Example | Description |
|---------------|---------|-------------|
| **Desktop** | Office PC | A workstation used by employees in offices for daily tasks. |
| **Laptop** | Employee Laptop | A portable computer used by employees for office or remote work. |
| **Server** | Windows Server, Linux Server | A system that provides services, applications, or data to other devices on the network. |
| **Mobile** | Android Phone, iPhone | Smartphones used to access company email, applications, and business data. |
| **Tablet** | iPad, Android Tablet | Portable touch-screen devices used for business operations and mobile productivity. |
| **Virtual Machine (VM)** | VMware VM, Hyper-V VM | A software-based computer running on a virtualization platform. |
| **IoT Device** | Smart Camera, Smart Printer, IP Camera | Internet-connected devices that collect, send, or receive data. |
| **POS Device** | Payment Machine, Billing Terminal | Point-of-Sale devices used in retail stores to process customer payments. |


# Why Endpoint Security is Important?
Endpoints are the most common targets for cyberattacks.

## Without endpoint protection:
Malware can infect systems

Ransomware can encrypt files

Credentials can be stolen

Attackers can move laterally

# Example
Employee opens a phishing email.
↓
Downloads malware.
↓
Laptop gets infected.
↓
Malware spreads across the company.

Endpoint Security stops this attack.

# Endpoint Security vs Network Security
| Feature | Endpoint Security | Network Security |
|---------|-------------------|------------------|
| **Protection Scope** | Protects individual devices (endpoints) | Protects the entire network infrastructure |
| **Focus** | Secures endpoints such as laptops, desktops, servers, and mobile devices | Secures network traffic and communication between devices |
| **Primary Technologies** | EDR, Antivirus, EPP, XDR | Firewall, IDS, IPS, VPN, NAC |
| **Threat Detection** | Detects malware, ransomware, malicious processes, and suspicious activities on endpoints | Detects network attacks, unauthorized access, DDoS attacks, and malicious traffic |
| **Monitoring** | Monitors endpoint behavior, files, processes, registry, and local activities | Monitors packets, network traffic, ports, protocols, and connections |
| **Response** | Isolates infected endpoints, kills malicious processes, quarantines files | Blocks malicious IPs, filters traffic, prevents unauthorized network access |
| **Example Tools** | Microsoft Defender for Endpoint, CrowdStrike Falcon, SentinelOne | Palo Alto Firewall, Cisco ASA, Fortinet Firewall, Snort, Suricata |
| **Example** | Microsoft Defender for Endpoint | Palo Alto Next-Generation Firewall |

# Antivirus (AV)
Antivirus scans files using known malware signatures.

# Features
Signature-based detection

File scanning

Virus removal

Limitation

Cannot detect many unknown or fileless attacks.

# Endpoint Protection Platform (EPP)
EPP combines antivirus with additional preventive security features.

# Features
Antivirus

Firewall

Device Control

USB Protection

Web Protection

Policy Management

Purpose: Prevent attacks before they happen.

# Endpoint Detection and Response (EDR)
EDR continuously monitors endpoint activity, detects suspicious behavior, investigates threats, and enables rapid response.

# Features
Process monitoring

Behavioral analysis

Threat hunting

Endpoint isolation

Incident investigation

Timeline analysis

Purpose: Detect, investigate, and respond to threats.

# Extended Detection and Response (XDR)
XDR extends detection and response beyond endpoints by combining data from multiple security products.

# Data Sources
Endpoint

Email

Identity

Cloud

Firewall

Network

Servers

Purpose: Provide complete visibility across the environment.

# Difference
| Feature | Antivirus (AV) | EPP (Endpoint Protection Platform) | EDR (Endpoint Detection & Response) | XDR (Extended Detection & Response) |
|---------|----------------|-------------------------------------|--------------------------------------|--------------------------------------|
| **Malware Detection** | ✅ Yes | ✅ Yes | ✅ Yes | ✅ Yes |
| **Signature-Based Detection** | ✅ Yes | ✅ Yes | ✅ Yes | ✅ Yes |
| **Behavioral Detection** | ❌ No | ⚠️ Limited | ✅ Yes | ✅ Yes |
| **Continuous Monitoring** | ❌ No | ⚠️ Limited | ✅ Yes | ✅ Yes |
| **Threat Hunting** | ❌ No | ❌ No | ✅ Yes | ✅ Yes |
| **Endpoint Isolation** | ❌ No | ❌ No | ✅ Yes | ✅ Yes |
| **Automated Response** | ❌ No | ⚠️ Limited | ✅ Yes | ✅ Yes |
| **Multi-Source Visibility** | ❌ No | ❌ No | ❌ No | ✅ Yes (Endpoint, Network, Email, Identity, Cloud) |
| **Primary Focus** | Detect and remove known malware | Prevent endpoint threats | Detect, investigate, and respond to endpoint attacks | Detect and respond across the entire security ecosystem |
| **Best For** | Home users and basic protection | Endpoint prevention | SOC monitoring and Incident Response | Enterprise-wide threat detection and response |
| **Example Tools** | Windows Defender Antivirus, Avast, Kaspersky | Symantec Endpoint Protection, Trend Micro Apex One | Microsoft Defender for Endpoint, CrowdStrike Falcon, SentinelOne | Microsoft Defender XDR, Cortex XDR, Trend Vision One |

# How EDR Works
EDR continuously collects telemetry from endpoints.

1. Process Monitoring

Tracks every process.

Example

cmd.exe

powershell.exe

chrome.exe

2. File Monitoring

Monitors:

File creation

File deletion

File modification

Detects ransomware encryption.

3. Registry Monitoring

Detects registry changes.

Useful for finding persistence mechanisms.

4. Network Connection Monitoring

Monitors:

Source IP

Destination IP

Ports

Protocols

Detects suspicious outbound connections.

5. Behavioral Analysis

Instead of relying only on signatures,

EDR analyzes behavior.

# Example

Word
↓
Starts PowerShell
↓
Downloads Malware
↓
Alert

This behavior is suspicious.

6. Alert Generation

If malicious behavior is detected,

EDR creates an alert.

# Example
High Severity

PowerShell Download Attempt

7. Endpoint Isolation

EDR can isolate the infected computer.

Company Network
↓
PC-01
↓
Disconnected
↓
Malware Cannot Spread

#  Common Threats
Malware--
Malicious software designed to damage or compromise systems.

# Example:
Virus, Worm, Trojan

Ransomware--
Encrypts files and demands payment.

#  Example:
WannaCry, LockBit

Trojan--
Malware disguised as legitimate software.

# Example:
Fake PDF Reader

Fileless Malware

Runs in memory using legitimate tools.

# Examples:
PowerShell

WMI

No malicious file is written to disk.

PowerShell Attacks--
Attackers misuse PowerShell to:

Download malware,
Execute scripts,
Move laterally,
Create persistence,
Credential Dumping,

Steals usernames and password hashes.

Common target:

LSASS.exe

Common tool:

Mimikatz

# IOC (Indicator of Compromise)
Evidence that a system has already been compromised.

# Examples
Malicious IP,
File Hash,
Domain,
URL,
Registry Key

# IOA (Indicator of Attack)
Suspicious attacker behavior that may indicate an attack is in progress.

# Examples
PowerShell downloading files

Office spawning cmd.exe

LSASS memory access

Multiple failed logins

# Difference

| Feature | IOC (Indicator of Compromise) | IOA (Indicator of Attack) |
|---------|-------------------------------|---------------------------|
| **Definition** | Evidence that a system has already been compromised. | Suspicious behavior indicating an attack is occurring or about to occur. |
| **Purpose** | Identifies signs of a completed or ongoing compromise. | Detects attacker behavior before or during an attack. |
| **Detection Type** | Reactive | Proactive |
| **Timing** | After compromise | Before or during compromise |
| **Focus** | Evidence left by attackers | Attacker techniques and behavior |
| **Examples** | Malicious IP address, File Hash, Domain, URL, Registry Key | PowerShell downloading malware, Office spawning `cmd.exe`, LSASS access, Multiple failed logins |
| **SOC Use Case** | Investigate confirmed compromise and identify affected systems. | Detect suspicious activity early and stop the attack before damage occurs. |

# EDR Investigation Workflow
Alert
↓
Validate Alert
↓
Investigate Process
↓
Check Parent Process
↓
Check Command Line
↓
Hash Analysis
↓
Network Connections
↓
Identify IOC/IOA
↓
Contain Endpoint
↓
Escalate
↓
Document Findings

#  Popular EDR Tools
Tool	Vendor
Microsoft Defender--- for Endpoint	Microsoft
CrowdStrike Falcon--	CrowdStrike
SentinelOne	--SentinelOne
Cortex XDR --	Palo Alto Networks
VMware Carbon Black	VMware
Trellix	Trellix

#  SOC Analyst Responsibilities
A SOC Analyst using EDR is responsible for:

Monitor EDR alerts

Validate True Positive vs False Positive

Investigate suspicious processes

Check parent-child process relationships

Analyze file hashes

Review network connections

Collect IOCs and IOAs

Isolate infected endpoints

Escalate high-severity incidents

Document findings

Recommend remediation

# Interview Questions & Answers
1. What is EDR?
EDR (Endpoint Detection and Response) is a security solution that continuously monitors endpoint activity, detects suspicious behavior, investigates threats, and enables rapid response such as endpoint isolation and threat remediation.

2. Difference between Antivirus and EDR?
| Antivirus | EDR |
|-----------|-----|
| **Signature-based** | Behavior-based + Signatures |
| **Detects known malware** | Detects known and unknown threats |
| **Limited visibility** | Full endpoint visibility |
| **No threat hunting **| Supports threat hunting |
| **Basic protection** | Detection, investigation, and response |

3. Difference between EDR and XDR?
| EDR | XDR |
|-----|-----|
| **Protects endpoints** | Protects endpoints, email, cloud, identity, and network |
| **Endpoint telemetry** | Multi-source telemetry |
| **Endpoint-focused** | Organization-wide visibility |


4. What is Endpoint Security?

Endpoint Security is the practice of protecting endpoint devices such as laptops, desktops, servers, and mobile devices from cyber threats using tools like Antivirus, EPP, EDR, and XDR.

5. What is IOC?

An Indicator of Compromise (IOC) is evidence that suggests a system has already been compromised, such as a malicious IP address, file hash, domain, or registry key.

6. What is IOA?

An Indicator of Attack (IOA) is suspicious behavior that indicates an attack may be occurring, such as PowerShell launching from Microsoft Word or attempts to dump LSASS memory.

7. How does EDR detect malware?

EDR detects malware by continuously monitoring endpoint activity, analyzing process behavior, monitoring files and registry changes, inspecting network connections, using behavioral analytics, correlating events, and generating alerts when suspicious activity is detected.

8. What would you do if EDR detects ransomware?
If EDR detects ransomware, I would:

Validate the alert.

Isolate the affected endpoint.

Stop malicious processes if possible.

Identify affected users and systems.

Collect IOCs and logs.

Investigate the attack's origin and spread.

Escalate the incident to the Incident Response team.

Assist with malware removal and recovery.

Monitor the environment for additional malicious activity.

Document the investigation and lessons learned.