# 2. Threat Intelligence Types ⭐

Threat Intelligence is mainly divided into four types:

1. Strategic Threat Intelligence
2. Tactical Threat Intelligence
3. Operational Threat Intelligence
4. Technical Threat Intelligence

---

## 1. Strategic Threat Intelligence

### Definition

Strategic Threat Intelligence provides **high-level information about cyber threats, risks, trends, and their potential business impact**.

### Focus

- Cybersecurity trends
- Threat landscape
- Business risks
- Industry-specific threats
- Long-term security planning

### Used By

- CISO
- Security Managers
- Senior Management
- Business Leaders

### Example

If ransomware attacks against a particular industry are increasing, management can use this intelligence to improve:

- Security budget
- Backup strategy
- Endpoint security
- Security policies

### Key Point

> **Strategic Intelligence = Business Risk + Long-Term Decision Making**

---

## 2. Tactical Threat Intelligence

### Definition

Tactical Threat Intelligence focuses on the **Tactics, Techniques, and Procedures (TTPs)** used by threat actors.

It helps security teams understand **how attackers operate**.

### Focus

- Attacker Tactics
- Techniques
- Procedures
- Attack methods
- MITRE ATT&CK techniques

### Examples

- Phishing
- PowerShell
- Credential Dumping
- Brute Force
- Lateral Movement
- Command and Control
- Persistence

### SOC Use

SOC teams can use tactical intelligence to:

- Create detection rules
- Improve security controls
- Perform threat hunting
- Detect attacker behavior

### Key Point

> **Tactical Intelligence = How the Attacker Operates**

---

## 3. Operational Threat Intelligence

### Definition

Operational Threat Intelligence provides information about **specific threat actors, campaigns, and ongoing or upcoming attacks**.

It helps security teams understand:

- Who is attacking
- What they are targeting
- Why they are attacking
- How the campaign is being conducted

### Focus

- Threat Actors
- Attack Campaigns
- Targeted Organizations
- Attack Methods
- Current Threat Activity

### Example

A threat intelligence report identifies an active ransomware campaign targeting financial organizations.

The SOC can use this information to:

- Increase monitoring
- Perform threat hunting
- Check relevant IOCs
- Improve detection coverage
- Prepare incident response procedures

### Key Point

> **Operational Intelligence = Specific Threat Campaigns + Threat Actors**

---

## 4. Technical Threat Intelligence

### Definition

Technical Threat Intelligence focuses on **technical indicators associated with malicious activity**, commonly known as **Indicators of Compromise (IOCs)**.

### Common IOCs

| Indicator | Example |
|---|---|
| IP Address | `185.XX.XX.XX` |
| Domain | `malicious-example.com` |
| URL | `http://malicious-example.com/payload` |
| File Hash | `SHA256: abc123...` |
| Email Address | `attacker@example.com` |
| File Name | `invoice.exe` |
| Malware Signature | Known malicious pattern |

### Used In

- SIEM
- EDR
- Firewall
- IDS/IPS
- Email Security
- DNS Security
- Threat Intelligence Platforms

### SOC Example

A threat intelligence feed reports:

```text

Malicious IP: 185.XX.XX.XX
```
