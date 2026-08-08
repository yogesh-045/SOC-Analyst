# ☁️ AWS Basics

Amazon Web Services (AWS) is the world's most widely used cloud platform. It provides on-demand cloud services such as computing, storage, networking, databases, security, and monitoring.

As a SOC Analyst, you should know the purpose of common AWS services and where security logs come from.

---

# What is AWS?

## Definition

Amazon Web Services (AWS) is a cloud computing platform provided by Amazon that offers a wide range of cloud services over the Internet.

## Simple Definition

AWS allows organizations to use cloud resources like virtual servers, storage, networking, and security without owning physical hardware.

### Example

A company hosts its website on AWS instead of purchasing and maintaining its own servers.

---

# 1. Amazon EC2 (Elastic Compute Cloud)

## Definition

Amazon EC2 is a service that provides virtual servers in the cloud.

## Simple Definition

EC2 allows you to create and run virtual machines (VMs) on AWS.

## Purpose

- Host applications
- Run Windows or Linux servers
- Deploy websites
- Test software
- Run databases

### Example

A company launches a Linux EC2 instance to host its web application.

### SOC Analyst Perspective

Monitor for:

- Unauthorized logins
- Suspicious processes
- Malware activity
- High CPU usage
- Security group changes

---

# 2. Amazon S3 (Simple Storage Service)

## Definition

Amazon S3 is an object storage service used to store files and data in the cloud.

## Simple Definition

S3 is used to store files such as documents, images, videos, backups, and logs.

## Purpose

- File storage
- Backups
- Log storage
- Static website hosting
- Disaster recovery

### Example

A company stores daily backups in an S3 bucket.

### SOC Analyst Perspective

Monitor for:

- Public buckets
- Unauthorized downloads
- Bucket policy changes
- Data exfiltration
- Suspicious uploads

---

# 3. AWS IAM (Identity and Access Management)

## Definition

AWS IAM is a service used to securely manage access to AWS resources.

## Simple Definition

IAM controls **who can access AWS resources** and **what actions they can perform**.

## Purpose

- Create users
- Create groups
- Assign roles
- Manage permissions

### Example

An administrator creates an IAM user for a developer with access only to EC2 services.

### SOC Analyst Perspective

Monitor for:

- Failed login attempts
- Privilege escalation
- New IAM users
- Policy changes
- Root account usage

---

# 4. Amazon VPC (Virtual Private Cloud)

## Definition

Amazon VPC allows you to create an isolated virtual network within AWS.

## Simple Definition

A VPC is a private network where AWS resources communicate securely.

## Purpose

- Network isolation
- Secure communication
- Control IP addressing
- Configure routing
- Apply network security

### Example

A company deploys its EC2 instances inside a private VPC to prevent direct Internet access.

### SOC Analyst Perspective

Monitor for:

- Network traffic
- Security Group changes
- Network ACL changes
- Unauthorized connections
- Suspicious inbound or outbound traffic

---

# 5. AWS CloudTrail

## Definition

AWS CloudTrail records API calls and user activities performed in an AWS account.

## Simple Definition

CloudTrail tracks **who did what, when, and from where** in AWS.

## Purpose

- Audit AWS activity
- Track user actions
- Investigate incidents
- Detect unauthorized changes

### Example

An administrator deletes an S3 bucket.

CloudTrail records:

- User
- Time
- Source IP
- API action

### SOC Analyst Perspective

Monitor for:

- Failed logins
- IAM changes
- Deleted resources
- Suspicious API calls
- Root account activity

---

# 6. Amazon CloudWatch

## Definition

Amazon CloudWatch monitors AWS resources, applications, and system performance.

## Simple Definition

CloudWatch collects metrics, logs, and alerts from AWS services.

## Purpose

- Monitor servers
- Monitor applications
- Collect logs
- Generate alerts
- Track performance

### Example

CloudWatch sends an alert when CPU usage on an EC2 instance exceeds 90%.

### SOC Analyst Perspective

Monitor for:

- High CPU usage
- Memory usage
- Disk usage
- Application logs
- Security alerts

---

# AWS Services Comparison

| Service | Purpose |
|----------|---------|
| EC2 | Virtual Servers |
| S3 | Cloud Storage |
| IAM | Identity & Access Management |
| VPC | Private Network |
| CloudTrail | Audit Logs & API Activity |
| CloudWatch | Monitoring & Alerts |

---

# AWS Services Used by SOC Analysts

| AWS Service | SOC Analyst Use Case |
|-------------|----------------------|
| EC2 | Investigate compromised virtual machines |
| S3 | Detect exposed storage buckets |
| IAM | Monitor user permissions and suspicious logins |
| VPC | Investigate network traffic |
| CloudTrail | Investigate user actions and API calls |
| CloudWatch | Monitor alerts, logs, and system health |

---

# Key Points to Remember

- EC2 provides virtual servers.
- S3 stores files and data.
- IAM manages users and permissions.
- VPC provides network isolation.
- CloudTrail records AWS activities.
- CloudWatch monitors resources and generates alerts.

---

# Interview Questions

## 1. What is AWS?

### Answer

AWS (Amazon Web Services) is a cloud computing platform that provides services such as virtual servers, storage, networking, and security over the Internet.

---

## 2. What is EC2?

### Answer

Amazon EC2 (Elastic Compute Cloud) is a service that provides virtual servers for running applications in the cloud.

---

## 3. What is Amazon S3?

### Answer

Amazon S3 (Simple Storage Service) is an object storage service used to securely store and retrieve files and data.

---

## 4. What is AWS IAM?

### Answer

AWS IAM (Identity and Access Management) is a service that controls who can access AWS resources and what actions they can perform.

---

## 5. What is Amazon VPC?

### Answer

Amazon VPC (Virtual Private Cloud) is a private virtual network that securely hosts AWS resources.

---

## 6. What is AWS CloudTrail?

### Answer

AWS CloudTrail records API calls and user activities in an AWS account, helping with auditing and security investigations.

---

## 7. What is Amazon CloudWatch?

### Answer

Amazon CloudWatch monitors AWS resources, collects logs and metrics, and generates alerts based on predefined conditions.

---

# Summary

- AWS is Amazon's cloud computing platform.
- EC2 provides virtual servers.
- S3 stores files and backups.
- IAM manages identities and permissions.
- VPC provides secure networking.
- CloudTrail records user activities and API calls.
- CloudWatch monitors resources and generates alerts.
- SOC Analysts use these services to investigate incidents, monitor logs, detect suspicious activity, and improve cloud security.
