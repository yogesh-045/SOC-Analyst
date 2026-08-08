# ☁️ Azure Basics

Microsoft Azure is Microsoft's cloud computing platform that provides services such as virtual machines, storage, networking, identity management, monitoring, and security.

As a SOC Analyst, it is important to understand the basic Azure services used in cloud environments.

---

# What is Microsoft Azure?

## Definition

Microsoft Azure is a cloud computing platform developed by Microsoft that provides cloud services for computing, storage, networking, databases, security, and monitoring.

## Simple Definition

Azure allows organizations to build, deploy, and manage applications and infrastructure in the cloud without maintaining physical hardware.

### Example

A company hosts its website, databases, and applications on Microsoft Azure instead of using on-premises servers.

---

# 1. Azure Virtual Machines (Azure VM)

## Definition

Azure Virtual Machines are virtual servers that run Windows or Linux operating systems in Microsoft Azure.

## Simple Definition

Azure VM allows users to create and run virtual computers in the cloud.

## Purpose

- Host websites
- Run applications
- Deploy Windows/Linux servers
- Testing and development
- Database hosting

### Example

A company deploys a Windows Server VM in Azure to host an internal application.

### SOC Analyst Perspective

Monitor for:

- Unauthorized logins
- Failed login attempts
- Suspicious processes
- Malware activity
- High CPU or memory usage

---

# 2. Azure Storage

## Definition

Azure Storage is a cloud storage service used to securely store files, blobs, disks, queues, and tables.

## Simple Definition

Azure Storage stores data in the cloud for applications, backups, and file sharing.

## Purpose

- File storage
- Backup storage
- Application data
- Log storage
- Disaster recovery

### Example

A company stores application logs and backups in Azure Storage.

### SOC Analyst Perspective

Monitor for:

- Public storage containers
- Unauthorized file access
- Data downloads
- Storage permission changes
- Suspicious uploads

---

# 3. Microsoft Entra ID (Azure Active Directory)

## Definition

Microsoft Entra ID (formerly Azure Active Directory) is Microsoft's cloud-based Identity and Access Management (IAM) service.

## Simple Definition

Microsoft Entra ID manages user identities, authentication, and access to cloud resources.

## Purpose

- User authentication
- Single Sign-On (SSO)
- Multi-Factor Authentication (MFA)
- User and group management
- Access control

### Example

An employee signs in once using Microsoft Entra ID and gains access to Outlook, Teams, and SharePoint.

### SOC Analyst Perspective

Monitor for:

- Failed login attempts
- Impossible travel logins
- MFA failures
- New user creation
- Privilege escalation
- Risky sign-ins

---

# 4. Microsoft Defender for Cloud

## Definition

Microsoft Defender for Cloud is a cloud security service that provides security posture management and threat protection for Azure resources.

## Simple Definition

Microsoft Defender for Cloud helps identify security risks and protect Azure resources from cyber threats.

## Purpose

- Threat detection
- Security recommendations
- Vulnerability assessment
- Compliance monitoring
- Security alerts

### Example

Defender for Cloud detects an exposed virtual machine with an open RDP port and recommends remediation.

### SOC Analyst Perspective

Monitor for:

- Security alerts
- Vulnerabilities
- Misconfigured resources
- Malware detection
- Compliance issues

---

# 5. Azure Monitor

## Definition

Azure Monitor is a monitoring service that collects metrics, logs, and performance data from Azure resources.

## Simple Definition

Azure Monitor helps monitor cloud resources and generate alerts based on system activity.

## Purpose

- Performance monitoring
- Log collection
- Resource health monitoring
- Alert generation
- Incident investigation

### Example

Azure Monitor sends an alert when CPU usage on a virtual machine exceeds 90%.

### SOC Analyst Perspective

Monitor for:

- Performance issues
- Authentication logs
- Security alerts
- Resource health
- Suspicious activity

---

# Azure Services Comparison

| Service | Purpose |
|----------|---------|
| Azure Virtual Machines | Virtual Servers |
| Azure Storage | Cloud Storage |
| Microsoft Entra ID | Identity & Access Management |
| Microsoft Defender for Cloud | Cloud Security & Threat Protection |
| Azure Monitor | Monitoring, Logs & Alerts |

---

# Azure Services Used by SOC Analysts

| Azure Service | SOC Analyst Use Case |
|---------------|----------------------|
| Azure Virtual Machines | Investigate compromised virtual machines |
| Azure Storage | Detect exposed storage accounts and unauthorized access |
| Microsoft Entra ID | Monitor user authentication and permissions |
| Microsoft Defender for Cloud | Detect cloud threats and security misconfigurations |
| Azure Monitor | Analyze logs, monitor resources, and investigate incidents |

---

# AWS vs Azure Services

| AWS | Microsoft Azure |
|-----|-----------------|
| EC2 | Azure Virtual Machines |
| S3 | Azure Storage |
| IAM | Microsoft Entra ID |
| CloudTrail | Activity Logs |
| CloudWatch | Azure Monitor |
| GuardDuty | Microsoft Defender for Cloud |

---

# Key Points to Remember

- Azure Virtual Machines provide cloud-based virtual servers.
- Azure Storage stores files, backups, and application data.
- Microsoft Entra ID manages identities and access.
- Microsoft Defender for Cloud protects cloud resources.
- Azure Monitor collects logs, metrics, and generates alerts.

---

# Interview Questions

## 1. What is Microsoft Azure?

### Answer

Microsoft Azure is a cloud computing platform that provides services such as virtual machines, storage, networking, security, and monitoring over the Internet.

---

## 2. What are Azure Virtual Machines?

### Answer

Azure Virtual Machines are cloud-based virtual servers that run Windows or Linux operating systems.

---

## 3. What is Azure Storage?

### Answer

Azure Storage is a cloud storage service used to securely store files, backups, logs, and application data.

---

## 4. What is Microsoft Entra ID?

### Answer

Microsoft Entra ID is Microsoft's cloud-based Identity and Access Management (IAM) service that manages authentication, authorization, and access to cloud resources.

---

## 5. What is Microsoft Defender for Cloud?

### Answer

Microsoft Defender for Cloud is a cloud security solution that helps identify threats, security misconfigurations, vulnerabilities, and compliance issues in Azure environments.

---

## 6. What is Azure Monitor?

### Answer

Azure Monitor collects logs, metrics, and performance data from Azure resources and generates alerts for monitoring and incident response.

---

# Summary

- Microsoft Azure is Microsoft's cloud platform.
- Azure Virtual Machines provide virtual servers.
- Azure Storage securely stores cloud data.
- Microsoft Entra ID manages user identities and access.
- Microsoft Defender for Cloud provides cloud threat protection.
- Azure Monitor collects logs, monitors resources, and generates alerts.
- SOC Analysts use these services to detect threats, investigate incidents, and monitor cloud environments.
