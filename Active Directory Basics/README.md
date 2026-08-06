# 📖 Active Directory (AD)

## What is Active Directory?

**Active Directory (AD)** is Microsoft's centralized directory service used to manage **users, computers, groups, and security policies** in an organization. It provides **authentication** and **authorization**, making it easier for administrators to manage the entire network from one place.

---

# 🎯 Why Do Organizations Use Active Directory?

Organizations use Active Directory because it:

- Simplifies administration
- Provides centralized management of users and computers
- Manages security policies from one location
- Improves overall security
- Supports **Single Sign-On (SSO)**
- Makes managing large networks easier

---

# ✅ Benefits of Active Directory

- 👤 Centralized User Management
- 🔐 Centralized Authentication
- ✅ Centralized Authorization
- ⚙️ Group Policy Management
- 🛡️ Better Security
- 🔑 Single Sign-On (SSO)
- 📋 Easy Auditing
- 📈 Scalability

---

# 🏗️ Active Directory Components

Active Directory consists of several components that help organize and manage a network.

| Component | Description |
|-----------|-------------|
| **Domain** | A logical group of users, computers, and resources sharing the same security database. |
| **Domain Controller (DC)** | A Windows Server that runs Active Directory and authenticates users. |
| **Forest** | The highest-level AD container containing one or more domains. |
| **Tree** | A group of domains sharing the same namespace. |
| **Organizational Unit (OU)** | A container used to organize users, computers, and groups. |
| **Objects** | Resources stored in AD such as Users, Computers, Groups, Printers, and Contacts. |

---

# ⭐ What Are the Benefits of Active Directory?

The major benefits of Active Directory include:

- 🏢 Centralized Administration
- 🔑 Single Sign-On (SSO)
- 🛡️ Better Security
- ⚙️ Group Policy Management
- 👥 Easy User Management
- 📂 Resource Sharing
- 🔒 Password Management
- 📈 Scalability
- 📊 Auditing and Logging

---
# 🖥️ Domain Controller (DC)

## What is a Domain Controller (DC)?

A **Domain Controller (DC)** is a **Windows Server** running **Active Directory Domain Services (AD DS)**. It authenticates users, authorizes access, stores the Active Directory database, applies **Group Policies**, and manages all domain resources.

---

## 🎯 Responsibilities of a Domain Controller

- 🔐 Authentication
- ✅ Authorization
- 🌐 DNS Integration
- ⚙️ Group Policy Management
- 🔄 Replication
- 👤 User Management

---

# 📂 Organizational Unit (OU)

## What is an Organizational Unit (OU)?

An **Organizational Unit (OU)** is a logical container inside a domain used to organize **Active Directory objects**. It simplifies administration and allows different **Group Policies (GPOs)** to be applied to different departments.

### 📌 Example

```text
Company
│
├── HR
├── IT
├── Finance
└── Sales
```

---

# 👥 Security Group vs Distribution Group

| Security Group | Distribution Group |
|----------------|--------------------|
| Used for assigning permissions | Used only for email distribution |
| Can assign access rights | Cannot assign access rights |
| Used for file and folder permissions | Used for mailing lists only |
| Supports access control | Does not support access control |

---

# 🌍 Global Catalog (GC)

## What is the Purpose of the Global Catalog?

The **Global Catalog (GC)** is a special **Domain Controller role** that stores a **searchable partial copy** of all objects in the forest. It improves search performance and supports cross-domain authentication.

### ✅ Global Catalog Enables

- 🔍 Fast object searches
- 👤 User logons across domains
- 👥 Universal Group membership lookups

---

# 🔐 Authentication vs Authorization

| Authentication | Authorization |
|---------------|---------------|
| Verifies a user's identity | Determines what resources the user can access |
| **Question:** Who are you? | **Question:** What are you allowed to access? |
| Uses username and password | Uses permissions and group memberships |

### Authentication Example

```
Username + Password
        │
        ▼
Identity Verified
```

### Authorization Example

```
Identity Verified
        │
        ▼
Access Granted Based on Permissions
```

---

# 🎫 Kerberos Authentication

## What is Kerberos?

**Kerberos** is the default authentication protocol used in **Active Directory**. After a user logs in, the **Key Distribution Center (KDC)** on the Domain Controller issues a **Ticket Granting Ticket (TGT)**. The client then uses the **TGT** to request **Service Tickets** for accessing network resources without repeatedly sending the user's password.

---

## 🔄 Kerberos Authentication Steps

1. User enters **username and password**.
2. Client requests a **Ticket Granting Ticket (TGT)** from the **KDC**.
3. KDC verifies the user's credentials.
4. Client receives the **TGT**.
5. Client requests a **Service Ticket** using the TGT.
6. KDC issues the **Service Ticket**.
7. Client presents the Service Ticket to the target server.
8. Access is granted if the ticket is valid.

---

## 📊 Kerberos Authentication Flow

```text
User
 │
 ▼
Login
 │
 ▼
Domain Controller (KDC)
 │
 ▼
Ticket Granting Ticket (TGT)
 │
 ▼
Request Service Ticket
 │
 ▼
Service Ticket Issued
 │
 ▼
File Server
 │
 ▼
✅ Access Granted
```

---

# 🔑 NTLM Authentication

## When is NTLM Used?

**NTLM (NT LAN Manager)** is Microsoft's older authentication protocol. It is mainly used when **Kerberos authentication** is unavailable or unsupported. Although NTLM is still supported for compatibility, **Kerberos is preferred** because it is more secure.

---

## 📌 NTLM is Used When

- 🖥️ Legacy systems
- 💻 Workgroup computers
- 📦 Applications that do not support Kerberos
- ⚠️ Situations where Kerberos requirements are not met

> **Note:** In modern Active Directory environments, **Kerberos** is the default authentication protocol, while **NTLM** is mainly used for backward compatibility.

---

# ⚙️ Group Policy Object (GPO)

## What is a Group Policy Object (GPO)?

A **Group Policy Object (GPO)** is a collection of settings that allows administrators to configure and enforce rules on users and computers in an **Active Directory** domain.

---

## 🎯 Common Uses of GPO

- 🔒 Disable USB Devices
- 🔑 Enforce Password Policies
- 📦 Install Software
- 🛡️ Configure Windows Firewall
- 🚫 Disable Control Panel
- 🖼️ Set Desktop Wallpaper

---

## 📌 Example

```text
Administrator creates a GPO

        │
        ▼
Disable USB Storage

        │
        ▼
Applied automatically to all
computers in the IT Department
```

---

# 🌐 DNS Basics

## What is DNS?

**DNS (Domain Name System)** translates **domain names** into **IP addresses**.

Active Directory depends on **DNS** to locate **Domain Controllers** and other network services.

---

## 📌 Example

Instead of remembering:

```text
192.168.1.10
```

Users simply type:

```text
server.company.local
```

---

## ✅ Why DNS is Important in Active Directory

- 🌍 Finds Domain Controllers
- 👤 Supports User Logins
- 🔐 Enables Authentication
- 📡 Helps Computers Locate Network Resources

> **Without DNS, Active Directory will not function properly.**

---

# 👥 Active Directory Users and Computers (ADUC)

## What is ADUC?

**Active Directory Users and Computers (ADUC)** is the **Microsoft Management Console (MMC)** used to manage Active Directory objects.

---

## Using ADUC, Administrators Can

- ➕ Create Users
- ❌ Delete Users
- 🔒 Disable or Enable Accounts
- 👥 Create Groups
- 💻 Join Computers to the Domain
- 🔑 Reset Passwords
- 📂 Move Objects Between Organizational Units (OUs)

---

## 📌 Example

```text
User Name   : Rahul
Department  : IT
Password    : ********

↓

Rahul can now log in
to any domain-joined computer.
```

---

# 🚨 Common Active Directory Attacks

## 1️⃣ Pass-the-Hash (PtH)

Uses **stolen NTLM password hashes** to authenticate without knowing the actual password.

---

## 2️⃣ Pass-the-Ticket (PtT)

Uses **stolen Kerberos tickets** to access resources without re-entering credentials.

---

## 3️⃣ Kerberoasting

An attacker requests **Kerberos Service Tickets** and attempts to crack them offline to recover **service account passwords**.

---

## 4️⃣ Password Spraying

Attempts **one common password** against **many different user accounts** to avoid account lockouts.

### Example

```text
Password

Welcome@123

        │
        ▼

Tried Against

Rahul
Amit
John
Sneha
```

---

## 5️⃣ Brute Force Attack

Attempts **many passwords** against **one account** until the correct password is found.

---

## 6️⃣ Golden Ticket Attack

An attacker forges a **Kerberos Ticket Granting Ticket (TGT)** after compromising the **KRBTGT** account to gain long-term access to the domain.

---

## 7️⃣ DCSync Attack

An attacker impersonates a **Domain Controller** and requests password hashes from Active Directory.

---

# 🔍 Detection & Monitoring

Detection and Monitoring involve continuously observing **Active Directory logs** and **security events** to identify suspicious or malicious activities.

---

## 👨‍💻 What SOC Analysts Monitor

- ❌ Failed Logins
- 🌍 Successful Logins from Unusual Locations
- 👑 Privileged Account Logins
- 👤 User Account Creation
- 👥 Group Membership Changes
- 🔑 Password Resets
- 🔒 Account Lockouts
- 🎫 Kerberos Ticket Requests
- ⚙️ New Process Creation
- 💙 PowerShell Execution

---

# 📊 Common SIEM Detection Rules

- 🚨 More than **10 failed logins within 5 minutes**
- 👑 New **Domain Admin** account created
- 🚫 Disabled account successfully logged in
- ➕ User added to **Domain Admins**
- 🔒 Multiple account lockouts
- 🎫 Unusual Kerberos ticket activity

---

# 🛠️ Common Monitoring Tools

- Splunk
- Microsoft Sentinel
- IBM QRadar
- Microsoft Defender XDR
- CrowdStrike Falcon
- Sysmon
- Windows Event Viewer

---

# 📑 Important Windows Event IDs for SOC Analysts

| Event ID | Event Name | Description | SOC Use Case |
|----------|------------|-------------|--------------|
| **4624** | Successful Logon | User successfully logged in | Detect unusual login times or locations |
| **4625** | Failed Logon | Login attempt failed | Detect brute-force and password spraying |
| **4634** | User Logoff | User logged off | Track session duration |
| **4648** | Logon Using Explicit Credentials | Login using alternate credentials | Detect credential misuse and lateral movement |
| **4672** | Special Privileges Assigned | Administrative account login | Monitor privileged account activity |
| **4688** | New Process Created | New process started | Detect malware execution and PowerShell abuse |
| **4720** | User Account Created | New AD user account created | Detect unauthorized account creation |
| **4726** | User Account Deleted | User account deleted | Investigate suspicious account removal |
| **4728** | User Added to Security Group | User added to security group | Detect privilege escalation |
| **4732** | Member Added to Local Security Group | User added to local security group | Monitor local administrator changes |
| **4740** | User Account Locked Out | Account locked after failed logins | Detect brute-force attacks |
| **4768** | Kerberos TGT Requested | Ticket Granting Ticket requested | Monitor Kerberos authentication |
| **4769** | Kerberos Service Ticket Requested | Service ticket requested | Detect Kerberoasting attacks |
| **4771** | Kerberos Authentication Failed | Kerberos login failed | Detect password guessing or expired passwords |
| **4776** | NTLM Authentication | NTLM credential validation | Detect Pass-the-Hash attacks and legacy authentication |
