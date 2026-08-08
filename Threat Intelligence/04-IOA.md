# 4. IOA — Indicators of Attack ⭐⭐

## What is IOA?

**IOA (Indicator of Attack)** is a behavior or activity that indicates an attacker may be attempting to compromise a system or network.

---

## Suspicious Behavior

Examples of suspicious behavior:

- PowerShell executing encoded commands
- Multiple failed login attempts
- Credential dumping
- Unexpected admin account creation
- Disabling security tools
- Unusual lateral movement
- Suspicious process execution

---

## Attack Patterns

Attack patterns are sequences of activities that indicate an ongoing or attempted attack.

**Example:**

```text
Phishing
   ↓
Malicious Attachment
   ↓
PowerShell Execution
   ↓
Credential Theft
   ↓
Lateral Movement
