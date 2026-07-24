# Incident Report

## Incident Summary

A Windows failed logon event (Event ID 4625) was detected during the investigation.

The failed logon event was generated in a controlled lab environment for SOC Analyst training and investigation purposes.

## Alert Information

| *Field* | *Value* |
|--------|-------|
|** Event ID** | 4625 |
|** Severity** | Low |
| **Host** | DESKTOP-LDBFHIM |
| **Target User** | Yogeshh~ |
| **Source IP** | 127.0.0.1 |
| **Logon Type** | 2 |
| **Authentication Package** | Negotiate |


## Investigation Steps

### Step 1

Reviewed Event ID 4625.

### Step 2

Verified the target account.

Target Account: Yogeshh~

### Step 3

Reviewed the failure reason.

Failure Reason: Unknown user name or bad password.

### Step 4

Verified Status Code.

Status: xC000006D

Sub Status: 0xC000006A

This indicates an incorrect password.

### Step 5

Reviewed Source IP.

Source IP: 127.0.0.1

This confirms the login attempt originated from the local machine.

### Step 6

Reviewed Logon Type.

Logon Type:2

Interactive Logon.

### Step 7

Reviewed Process Information.

Process: C:\Windows\System32\svchost.exe

Legitimate Windows process.


## Findings

 Event ID 4625 identified.

 Authentication failed because of an incorrect password.

 Target account was **Yogeshh~**.

 Source IP was localhost (127.0.0.1).

 Login type was Interactive (Type 2).

 The event was generated in a controlled lab environment.


## Conclusion

The investigation determined that the failed authentication was caused by an incorrect password entered for the local Windows account.

No indicators of malicious activity were observed.

The activity was performed intentionally for SOC Analyst training.



## Recommendations

- Monitor repeated failed login attempts.
- Alert when multiple Event ID 4625 events occur within a short period.
- Correlate Event ID 4625 with Event ID 4624 to detect successful logins after repeated failures.