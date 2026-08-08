# ☁️ Cloud Service Models

Cloud Service Models define **how cloud services are delivered** to users. They determine **who is responsible for managing different parts of the IT infrastructure**.

The three main cloud service models are:

- IaaS (Infrastructure as a Service)
- PaaS (Platform as a Service)
- SaaS (Software as a Service)

---

# 1. Infrastructure as a Service (IaaS)

## Definition

Infrastructure as a Service (IaaS) provides virtualized computing resources such as servers, storage, networking, and virtual machines over the Internet.

The cloud provider manages the physical infrastructure, while the customer manages the operating system, applications, and data.

### Simple Definition

IaaS provides virtual servers and networking resources. You are responsible for installing and managing the operating system and applications.

### Responsibilities

### Cloud Provider Manages

- Physical Servers
- Networking
- Storage
- Virtualization

### Customer Manages

- Operating System
- Applications
- Data
- Security Configurations

### Examples

- Amazon EC2
- Microsoft Azure Virtual Machines
- Google Compute Engine

### Real-World Example

A company wants to host its own web application.

Instead of purchasing physical servers, it launches an **AWS EC2 instance**, installs **Windows/Linux**, configures the web server, and deploys the application.

---

# 2. Platform as a Service (PaaS)

## Definition

Platform as a Service (PaaS) provides a platform where developers can build, test, and deploy applications without managing the underlying infrastructure.

The cloud provider manages the servers, operating system, runtime environment, and platform services.

### Simple Definition

PaaS allows developers to focus only on writing application code while the cloud provider manages the infrastructure.

### Cloud Provider Manages

- Servers
- Networking
- Storage
- Operating System
- Runtime Environment

### Customer Manages

- Application Code
- Application Data

### Examples

- Azure App Service
- Google App Engine
- AWS Elastic Beanstalk

### Real-World Example

A developer uploads a Python web application to **Azure App Service**. Azure automatically manages the servers, updates, and operating system.

---

# 3. Software as a Service (SaaS)

## Definition

Software as a Service (SaaS) delivers fully managed software applications over the Internet.

Users simply access the application through a web browser without installing or maintaining the software.

### Simple Definition

SaaS allows users to use software directly through the Internet.

### Cloud Provider Manages

- Infrastructure
- Operating System
- Application
- Security Updates
- Maintenance

### Customer Manages

- User Accounts
- Data
- Application Settings

### Examples

- Microsoft 365
- Gmail
- Google Drive
- Dropbox
- Salesforce

### Real-World Example

Employees use **Microsoft 365** to send emails and create documents without installing or maintaining email servers.

---

# IaaS vs PaaS vs SaaS

| Feature | IaaS | PaaS | SaaS |
|----------|------|------|------|
| Infrastructure Managed By | Cloud Provider | Cloud Provider | Cloud Provider |
| Operating System | Customer | Cloud Provider | Cloud Provider |
| Applications | Customer | Customer | Cloud Provider |
| Best For | System Administrators | Developers | End Users |
| User Control | High | Medium | Low |

---

# Responsibility Comparison

| Component | IaaS | PaaS | SaaS |
|------------|------|------|------|
| Networking | Cloud Provider | Cloud Provider | Cloud Provider |
| Storage | Cloud Provider | Cloud Provider | Cloud Provider |
| Servers | Cloud Provider | Cloud Provider | Cloud Provider |
| Virtualization | Cloud Provider | Cloud Provider | Cloud Provider |
| Operating System | Customer | Cloud Provider | Cloud Provider |
| Runtime | Customer | Cloud Provider | Cloud Provider |
| Applications | Customer | Customer | Cloud Provider |
| Data | Customer | Customer | Customer |

---

# SOC Analyst Perspective

As a SOC Analyst:

### In IaaS

Monitor:

- Virtual Machines
- Firewall Rules
- IAM Permissions
- Network Logs

---

### In PaaS

Monitor:

- Application Logs
- User Activity
- Authentication Logs
- API Activity

---

### In SaaS

Monitor:

- Login Attempts
- User Accounts
- MFA Events
- Suspicious Access
- File Sharing Activities

---

# Key Points to Remember

- **IaaS** provides virtual infrastructure.
- **PaaS** provides a development platform.
- **SaaS** provides ready-to-use software.
- Customer responsibility decreases from **IaaS → PaaS → SaaS**.
- Cloud provider responsibility increases from **IaaS → PaaS → SaaS**.

---

# Interview Questions

## 1. What is IaaS?

### Answer

Infrastructure as a Service (IaaS) provides virtualized infrastructure such as servers, storage, and networking. The customer manages the operating system, applications, and data.

---

## 2. What is PaaS?

### Answer

Platform as a Service (PaaS) provides a platform for developing, testing, and deploying applications. The cloud provider manages the infrastructure and operating system.

---

## 3. What is SaaS?

### Answer

Software as a Service (SaaS) provides fully managed software applications over the Internet that users can access through a web browser.

---

## 4. Difference between IaaS, PaaS, and SaaS

| IaaS | PaaS | SaaS |
|------|------|------|
| Provides infrastructure | Provides development platform | Provides ready-to-use software |
| Customer manages OS and applications | Customer manages application code | Cloud provider manages everything except user data and settings |
| High user control | Medium user control | Low user control |

---

# 📚 Summary

- **IaaS** = Virtual Infrastructure
- **PaaS** = Development Platform
- **SaaS** = Ready-to-use Software
- Cloud provider manages more components as you move from **IaaS → PaaS → SaaS**.
- SOC Analysts monitor cloud resources, authentication, logs, and suspicious activities based on the service model being used.
