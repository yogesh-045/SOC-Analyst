# What is Incident Response?
Incident Response (IR) is a structured process used to identify, analyze, contain, eradicate, recover from, and learn from cybersecurity incidents such as malware infections, phishing attacks, ransomware, unauthorized access, or data breaches.

Incident Response is the process of detecting, investigating, stopping, and recovering from a cyberattack while minimizing damage.

# Why is Incident Response Important?
Minimizes business impact

Reduces downtime

Protects sensitive data

Prevents attackers from spreading

Helps organizations recover quickly

Improves future security

# What is a Security Incident?
A security incident is any event that compromises or has the potential to compromise the confidentiality, integrity, or availability (CIA) of systems or data.

# Examples
Malware infection

Ransomware attack

Phishing email

Brute-force attack

Data breach

Insider threat

Unauthorized login

DDoS attack

# Incident Response Lifecycle (NIST)
1. Preparation
        ↓
2. Detection & Analysis
        ↓
3. Containment
        ↓
4. Eradication
        ↓
5. Recovery
        ↓
6. Lessons Learned

# 1. Preparation
Preparation involves getting people, tools, and processes ready before an incident occurs.

# Activities
Create Incident Response Plan

Define team roles

Deploy SIEM (Splunk, Sentinel)

Install EDR/XDR

Configure backups

Enable logging

Conduct security awareness training

Prepare communication plans

# Example
A company installs Microsoft Defender and Splunk before any attack occurs.

# 2. Detection & Analysis
Identify whether an alert is a real security incident and determine its scope and impact.

# Activities
Monitor SIEM alerts

Review Windows Event Logs

Analyze EDR alerts

Check firewall logs

Investigate suspicious IPs

Collect Indicators of Compromise (IOCs)

# Example
Splunk detects:

100 Failed Login Attempts

Event ID: 4625

Source IP: 192.168.1.50

SOC analysts investigate to determine if it's a brute-force attack.

# 3. Containment
Containment limits the attack to prevent further damage.

# Activities
Isolate infected computers

Disable compromised accounts

Block malicious IP addresses

Disconnect affected systems

Stop malicious processes

# Example
An employee's laptop is infected with ransomware.

The SOC team isolates the laptop from the network immediately.

# 4. Eradication
Remove the root cause of the incident.

# Activities
Delete malware

Remove malicious files

Close vulnerabilities

Patch systems

Reset compromised passwords

Remove persistence mechanisms

# Example
The malware is removed, and the vulnerable software is updated.

# 5. Recovery
Restore systems to normal operations safely.

# Activities
Restore data from backups

Reconnect systems

Verify systems are clean

Monitor for suspicious activity

Resume business operations

# Example
The cleaned laptop is reconnected after verification.

# 6. Lessons Learned
Review the incident to improve future defenses.

# Activities
Document what happened

Identify the root cause

Update security controls

Improve detection rules

Train employees

Update the Incident Response Plan

# Example
The company introduces Multi-Factor Authentication (MFA) after a credential compromise.

# Real-World Example
Scenario

An employee receives a phishing email.

## Step 1 – Detection

The employee clicks the link.

The SIEM detects suspicious login activity.

## Step 2 – Analysis

SOC Analyst checks:

Email logs -> Windows logs -> IP address -> User activity

The account is confirmed as compromised.

## Step 3 – Containment

Disable the account

Block the attacker's IP

Isolate the affected system

## Step 4 – Eradication

Remove malware

Reset the user's password

Delete malicious files

## Step 5 – Recovery

Restore any affected files

Re-enable the user account

Verify normal operations

## Step 6 – Lessons Learned

Update phishing detection rules

Train employees

Implement MFA

# SOC Analyst Responsibilities During Incident Response
Monitor SIEM alerts

Investigate suspicious activity

Analyze logs

Validate alerts (True Positive / False Positive)

Escalate incidents when needed

Document findings

Coordinate with Incident Response teams

Recommend containment actions

# Common Tools

| Tool | Category |
|------|----------|
| **Splunk** | SIEM |
| **Microsoft Sentinel** | Cloud SIEM / SOAR |
| **Microsoft Defender XDR** | XDR / EDR |
| **CrowdStrike Falcon** | EDR |
| **Sysmon** | Windows Monitoring |
| **Wireshark** | Network Analysis |
| **Volatility** | Memory Forensics |
| **FTK Imager** | Digital Forensics |
| **VirusTotal** | Threat Intelligence |
| **Nmap** | Network Scanning |

# Purpose & Example Use Case

| Tool | Purpose | Example Use Case |
|------|---------|------------------|
| **Splunk** | Collects, searches, analyzes, and visualizes logs from multiple sources. | Investigate failed logins (Event ID 4625), detect brute-force attacks, and create security dashboards. |
| **Microsoft Sentinel** | Cloud-native SIEM that collects, analyzes, and automates security incident response. | Detect suspicious Azure AD logins and automate incident response using playbooks. |
| **Microsoft Defender XDR** | Detects, investigates, and responds to threats across endpoints, identities, email, and cloud applications. | Identify malware execution, ransomware activity, and suspicious user behavior. |
| **CrowdStrike Falcon** | Provides real-time endpoint protection, threat detection, and incident response. | Detect malicious PowerShell execution, isolate compromised endpoints, and investigate attacks. |
| **Sysmon** | Records detailed Windows system events such as process creation, network connections, and file modifications. | Monitor process creation and network connection events for threat hunting. |
| **Wireshark** | Captures and analyzes network packets for troubleshooting and security investigations. | Analyze suspicious traffic, detect malware communication, or inspect DNS and HTTP requests. |
| **Volatility** | Analyzes RAM dumps to identify malware, hidden processes, injected code, and credentials. | Investigate a compromised system by extracting running processes and memory artifacts. |
| **FTK Imager** | Creates forensic images of disks and acquires digital evidence without modifying the original data. | Acquire a hard drive image during a forensic investigation for evidence preservation. |
| **VirusTotal** | Scans files, URLs, domains, IPs, and hashes using multiple antivirus engines and threat intelligence sources. | Check whether a suspicious file hash or URL is malicious before further investigation. |
| **Nmap** | Discovers hosts, open ports, running services, and operating systems on a network. | Identify active devices, open ports, and exposed services during network assessment or incident response. |

# Incident Response Interview Questions
What is Incident Response?
What are the six phases of Incident Response?
What is the difference between containment and eradication?
What should you do after detecting ransomware?
How would you investigate a phishing incident?
What tools are commonly used in Incident Response?
Why is documentation important during an incident?
What is the role of a SOC Analyst during Incident Response?
What is an Indicator of Compromise (IOC)?
What is the difference between an incident and an event?

# Key Points to Remember
Preparation → Be ready before an attack.

Detection & Analysis → Identify and investigate the incident.

Containment → Stop the attack from spreading.

Eradication → Remove the attacker or malware.

Recovery → Restore systems safely.

Lessons Learned → Improve security and prevent future incidents.