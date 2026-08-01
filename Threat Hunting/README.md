# What is Threat Hunting?
Threat Hunting is a proactive cybersecurity process where security analysts actively search for hidden threats, attackers, or malicious activities that have bypassed traditional security tools.
Unlike waiting for alerts, threat hunters look for suspicious behavior before it becomes a major incident.

Threat Hunting is the proactive process of searching for hidden cyber threats inside an organization's network before they cause damage.

# Why is Threat Hunting Important?
Detects hidden attackers

Finds threats missed by antivirus or EDR

Reduces attacker dwell time

Improves overall security

Helps prevent data breaches

# How Threat Hunting Works
Collect Logs

      ↓
Analyze Data

      ↓
Look for Suspicious Activity
      
      ↓
Identify IOC/IOA
      
      ↓
Investigate
      
      ↓
Contain Threat
      
      ↓
Report Findings

# Why Organizations Perform Threat Hunting?
Organizations perform Threat Hunting because not every cyberattack is detected by security tools like Antivirus, EDR, or SIEM.
Threat Hunting helps security teams proactively search for hidden attackers before they cause damage.

## Benefits
Detect hidden threats

Reduce attacker dwell time

Find malware missed by antivirus

Improve security posture

Prevent data breaches

Improve detection rules

# Example
A hacker gains access using stolen credentials.

No antivirus alert is generated.

A Threat Hunter notices:

Login at 3:00 AM

Impossible travel
    
PowerShell execution

The attacker is detected before stealing data.

# Common Data Sources
Windows Event Logs

Sysmon Logs

EDR Alerts

Firewall Logs

DNS Logs

Proxy Logs

Authentication Logs

Network Traffic

# Example 1: PowerShell Abuse

A threat hunter searches for:

powershell.exe

They find PowerShell downloading a file from an unknown website.

Investigation reveals malware.

# Example 2: **Multiple Failed Logins**

SIEM shows:

Event ID 4625
100 failed logins from the same IP

This may indicate a brute-force attack.

# Example 3: Suspicious Network Connection

An employee's laptop connects to an unknown foreign IP address.

The SOC analyst investigates and finds Command-and-Control (C2) communication.

#  Types of Threat Hunting
1. Structured Hunting

Structured hunting starts from a known attack technique or framework, usually MITRE ATT&CK.
Hunters search for evidence of specific attacker behaviors.

# Example 

Search for:
PowerShell abuse

Credential dumping

Lateral movement

2. Unstructured Hunting

Triggered by an alert or suspicious event.
Analysts investigate without a predefined hypothesis.

# Example

EDR reports:

Suspicious PowerShell Activity

The SOC Analyst investigates to determine whether it's malicious.

3. Intelligence-Driven Hunting

Uses Threat Intelligence (IOCs, malware reports, threat feeds) to search for known attacker activity.

# Example 
Threat Intelligence reports:

Malicious IP

185.220.101.45

The SOC team searches firewall and proxy logs to see whether any internal systems communicated with that IP.

# IOC and IOA
| IOC (Indicator of Compromise) | IOA (Indicator of Attack) |
|-------------------------------|---------------------------|
| **Malicious IP Address** | PowerShell downloading malware |
| **Malicious File Hash** | Microsoft Office spawning `cmd.exe` |
| **Malicious Domain** | LSASS memory access (Credential Dumping) |
| **Suspicious URL** | Multiple failed login attempts |


# Common Threat Hunting Tools
| Tool | Purpose |
|------|---------|
| **Splunk** | Log Analysis & SIEM |
| **Microsoft Sentinel** | Cloud SIEM |
| **Microsoft Defender for Endpoint** | Endpoint Detection & Response (EDR) |
| **CrowdStrike Falcon** | Endpoint Detection & Response (EDR) |
| **Sysmon** | Windows Event Logging |
| **Wireshark** | Network Traffic Analysis |
| **VirusTotal** | Threat Intelligence |
| **Nmap** | Network Discovery & Port Scanning |

# Threat Hunting Process
1. Define a hypothesis.
2. Collect logs and telemetry.
3. Search for suspicious activity.
4. Analyze IOCs and IOAs.
5. Investigate affected systems.
6. Contain the threat.
7. Document findings.

# Threat Hunting vs Incident Response
| Threat Hunting | Incident Response |
|----------------|-------------------|
| **Proactive** | Reactive |
| **Searches for hidden threats** | Responds to confirmed incidents |
| **Looks for suspicious behavior** | Investigates security incidents |
| **Goal is early detection** | Goal is containment and recovery |

# SOC Analyst Responsibilities
Analyze logs from SIEM and EDR

Search for suspicious activities

Investigate IOCs and IOAs

Validate alerts

Escalate confirmed threats

Document findings


# What is MITRE ATT&CK?
MITRE ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge) is a knowledge base that documents real-world attacker behaviors.
It helps defenders understand how attackers operate and improve detections.

# Tactics
A Tactic represents the attacker's objective or goal.

# Examples:
Initial Access

Execution

Persistence

Privilege Escalation

Defense Evasion

Credential Access

Discovery

Lateral Movement

Collection

Exfiltration

Impact

# Techniques
A Technique describes how an attacker achieves a tactic.

Technique: Credential Dumping

# Procedures
Procedures describe the specific steps or tools an attacker uses to perform a technique.

Procedure: Use Mimikatz or Dump LSASS Memory

TTP stands for:

Tactics → Why the attacker is performing an action.
Techniques → How the attacker performs it.
Procedures → The exact tools or commands used.

# Interview Questions
# 1. What is Threat Hunting?
Threat Hunting is the proactive process of searching for hidden threats and malicious activities within an organization's environment before they are detected by automated security tools.

# 2. Why is Threat Hunting important?
It helps detect hidden attackers, reduces attacker dwell time, identifies threats missed by traditional security tools, and improves an organization's overall security posture.

# 3. What is the difference between Threat Hunting and Incident Response?
| Threat Hunting | Incident Response |
|----------------|-------------------|
| **Proactive** | Reactive |
| **Finds hidden threats** | Responds to confirmed incidents |

# 4. What tools are used for Threat Hunting?
Common tools include Splunk, Microsoft Sentinel, Microsoft Defender for Endpoint, CrowdStrike Falcon, Sysmon, Wireshark, VirusTotal, and Nmap.

# 5. What is the goal of Threat Hunting?
The goal is to proactively identify, investigate, and eliminate hidden threats before they can cause significant damage to the organization.

# 6. What are IOCs?
Indicators of Compromise (IOCs) are pieces of evidence that indicate a system may have been compromised. Examples include malicious IP addresses, domains, URLs, file hashes, registry keys, and suspicious processes.

# 7. What are TTPs?
TTP stands for Tactics, Techniques, and Procedures. Tactics describe the attacker's goal, Techniques describe how the goal is achieved, and Procedures are the specific tools or methods used to carry out the technique.

# 8. What is MITRE ATT&CK?
MITRE ATT&CK is a publicly available knowledge base of real-world attacker behaviors. It organizes adversary actions into tactics and techniques, helping security teams detect, investigate, and defend against cyber threats.

# 9. Which logs are useful for Threat Hunting?
Common logs used for Threat Hunting include Windows Event Logs, Sysmon Logs, EDR Logs, Firewall Logs, DNS Logs, Proxy Logs, and SIEM Logs because they provide visibility into user activity, processes, network traffic, and authentication events.

# 10. How do you investigate brute-force activity?
I would first review failed login events (such as Event ID 4625), identify the source IP address, target account, timestamps, and the number of failed attempts. I would then check for any successful logins (Event ID 4624) from the same IP, correlate the activity with SIEM and EDR logs, determine whether the attack was successful, block the malicious IP if required, and escalate the incident according to the organization's procedures.
