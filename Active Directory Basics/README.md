#  What is Active Directory?
"Active Directory is Microsoft's centralized directory service used to manage users, computers, groups, and security policies in an organization. It provides authentication and authorization, making it easier for administrators to manage the entire network from one place."

#  Why do organizations use Active Directory?
Organizations use Active Directory because it simplifies administration by providing centralized management of users, computers, and security policies. It also improves security, supports Single Sign-On, and makes it easier to manage large networks.
# Benefits
Centralized user management

Centralized authentication

Centralized authorization

Group Policy management

Better security

Single Sign-On

Easy auditing

Scalability

# Active Directory Components
Active Directory consists of several components that help organize and manage the network.
# Main Components
Domain – A logical group of users, computers, and resources sharing the same security database.

Domain Controller (DC) – A Windows Server that runs Active Directory and authenticates users.

Forest – The highest-level AD container containing one or more domains.

Tree – A group of domains sharing the same namespace.

Organizational Unit (OU) – A container used to organize users, computers, and groups.

Objects – Resources stored in AD such as Users, Computers, Groups, 
Printers, and Contacts.

#  What are the benefits of Active Directory?
The main benefits of Active Directory are centralized management, improved security, Single Sign-On, easier user administration, Group Policy management, and the ability to efficiently manage thousands of users and computers.

# Major benefits include:
Centralized administration

Single Sign-On

Better security

Group Policy management

Easy user management

Resource sharing

Password management

Scalability

Auditing and logging


#  What is a Domain Controller (DC)?
A Domain Controller is a Windows Server running Active Directory Domain Services. It authenticates users, authorizes access, stores the Active Directory database, applies Group Policies, and manages all domain resources.

# Responsibilities
Authentication

Authorization

DNS integration

Group Policy

Replication

User management



#  What is an Organizational Unit (OU)?
An Organizational Unit is a logical container inside a domain used to organize Active Directory objects. It simplifies administration and allows different Group Policies to be applied to different departments.

# Example
Company

HR

IT

Finance

Sales

#  What is the difference between a Security Group and a Distribution Group?
A Security Group is used to assign permissions to resources such as folders and printers, whereas a Distribution Group is only used for email distribution and cannot be used for access control

# Security Group
Used for permissions

Can assign access rights

Used for file and folder permissions


#  What is the purpose of the Global Catalog?
The Global Catalog is a special Domain Controller role that stores a searchable partial copy of all objects in the forest. It improves search performance and supports cross-domain authentication.

# It enables:
Fast object searches

User logons across domains

Universal Group membership lookups

#  Explain Authentication and Authorization.
Authentication verifies the user's identity using credentials like a username and password. Authorization determines what resources the authenticated user is allowed to access based on permissions and group memberships.

Authentication

Authentication verifies identity.

# Question:
Who are you?

# Example
Username and password verification.

Authorization

Authorization determines permissions.

# Question

What are you allowed to access?


#  How does Kerberos authentication work?
Kerberos is the default authentication protocol in Active Directory. After a user logs in, the Domain Controller's KDC issues a Ticket Granting Ticket. The client then uses this TGT to obtain Service Tickets for resources, allowing secure authentication without repeatedly sending the user's password.

# Steps
User enters username and password.

The client requests a Ticket Granting Ticket (TGT) from the Domain 
Controller (specifically the Key Distribution Center, or KDC).

The KDC verifies the user's credentials.

The client receives a TGT.

When accessing a service, the client uses the TGT to request a Service 
Ticket.

The Service Ticket is presented to the target server.

Access is granted if the ticket is valid.

User

↓

Login

↓

Domain Controller (KDC)

↓

TGT

↓

Service Ticket

↓

File Server

↓

Access Granted


# When is NTLM used?
NTLM is Microsoft's older authentication protocol. It is mainly used when Kerberos authentication is unavailable or unsupported. Although still supported for compatibility, Kerberos is preferred because it is more secure.

NTLM is used when Kerberos cannot be used.

# Examples
Legacy systems

Workgroup computers

Some applications that do not support Kerberos

Certain scenarios where Kerberos requirements are not met

# Group Policy (GPO)
A Group Policy Object (GPO) is a collection of settings that allows administrators to configure and enforce rules on users and computers in an Active Directory domain.

# Uses
Disable USB devices

Enforce password policies

Install software

Configure Windows Firewall

Disable Control Panel

Set desktop wallpaper

# Example
Admin creates a policy:

Disable USB Storage

The policy is automatically applied to every computer in the IT department.

#  DNS Basics
DNS (Domain Name System) translates domain names into IP addresses.

Active Directory depends on DNS to locate Domain Controllers and other services.

# Example
Instead of remembering:

192.168.1.10

Users type:

server.company.local


# Why DNS is Important in AD
Finds Domain Controllers

Supports user logins

Enables authentication

Helps computers locate network resources

Without DNS, Active Directory will not function properly.

#  AD Users & Computers
Active Directory Users and Computers (ADUC) is the Microsoft Management Console (MMC) tool used to manage Active Directory objects.

# Using ADUC, administrators can:
Create users

Delete users

Disable or enable accounts

Create groups

Join computers to the domain

Reset passwords

Move objects between Organizational Units (OUs)

# Example

Administrator creates:

User

Rahul

Department

IT

Password

********

This user can now log in to any domain-joined computer.

# Common Active Directory Attacks
# Pass-the-Hash (PtH)
Uses stolen NTLM password hashes to authenticate without knowing the actual password.

# Pass-the-Ticket (PtT)
Uses stolen Kerberos tickets to access resources without re-entering credentials.

# Kerberoasting
An attacker requests Kerberos service tickets and attempts to crack them offline to recover service account passwords.

# Password Spraying
Attempts one common password against many different user accounts to avoid account lockouts.

# Example:

Password:

Welcome@123

↓

Tried on

Rahul
Amit
John
Sneha

# Brute Force Attack
Attempts many passwords against a single account until one works.

# Golden Ticket Attack
An attacker forges a Kerberos Ticket Granting Ticket (TGT), usually after compromising the KRBTGT account, to gain long-term access to the domain.

# DCSync Attack
An attacker impersonates a Domain Controller and requests password hashes from Active Directory.

#  Detection & Monitoring
Detection and Monitoring involve continuously observing Active Directory logs and events to identify suspicious or malicious activities.

# What SOC Analysts Monitor
Failed logins

Multiple successful logins from unusual locations

Privileged account logins

User account creation

Group membership changes

Password resets

Account lockouts

Kerberos ticket requests

New process creation

PowerShell execution

# Common SIEM Rules
More than 10 failed logins in 5 minutes

New Domain Admin account created

Disabled account successfully logs in

Account added to the Domain Admins group

Multiple account lockouts

Unusual Kerberos ticket activity

# Common Monitoring Tools
Splunk

Microsoft Sentinel

QRadar

Microsoft Defender XDR

CrowdStrike Falcon

Sysmon

Windows Event Viewer



| Event ID | Event Name | Description | SOC Use Case |
|----------|------------|-------------|--------------|
| **4624** | Successful Logon | Generated when a user successfully logs in to a system. | Monitor normal logins and detect unusual login times or locations. |
| **4625** | Failed Logon | Generated when a login attempt fails due to an incorrect username or password. | Detect brute-force attacks, password spraying, or unauthorized access attempts. |
| **4634** | User Logoff | Generated when a user logs off from a system. | Track user session duration and identify abnormal logoff behavior. |
| **4648** | Logon Using Explicit Credentials | Generated when a user logs in using different credentials (e.g., Run As). | Detect credential misuse, lateral movement, or privilege escalation attempts. |
| **4672** | Special Privileges Assigned | Generated when an account with administrative or special privileges logs in. | Monitor privileged account usage and detect suspicious admin logins. |
| **4688** | New Process Created | Generated whenever a new process starts on the system. | Detect malicious processes, PowerShell abuse, or malware execution. |
| **4720** | User Account Created | Generated when a new user account is created in Active Directory. | Detect unauthorized account creation or persistence mechanisms. |
| **4726** | User Account Deleted | Generated when a user account is deleted. | Monitor account removal and investigate suspicious deletions. |
| **4728** | User Added to Security Group | Generated when a user is added to a security-enabled global group. | Detect privilege escalation, especially additions to Domain Admins or other privileged groups. |
| **4732** | Member Added to Local Security Group | Generated when a member is added to a local security group. | Monitor changes to local administrator or privileged groups. |
| **4740** | User Account Locked Out | Generated when a user account is locked due to multiple failed login attempts. | Detect brute-force attacks or compromised accounts. |
| **4768** | Kerberos TGT Requested | Generated when a user requests a Kerberos Ticket Granting Ticket (TGT). | Monitor Kerberos authentication activity and identify abnormal login patterns. |
| **4769** | Kerberos Service Ticket Requested | Generated when a service ticket is requested from the Key Distribution Center (KDC). | Detect Kerberoasting attacks and unusual service ticket requests. |
| **4771** | Kerberos Authentication Failed | Generated when Kerberos authentication fails. | Detect password guessing, expired passwords, or authentication issues. |
| **4776** | NTLM Authentication | Generated when NTLM authentication is used to validate user credentials. | Detect legacy authentication usage, Pass-the-Hash attacks, or systems not using Kerberos. |