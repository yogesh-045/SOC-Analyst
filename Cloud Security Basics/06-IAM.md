# 🔐 Identity and Access Management (IAM)

Identity and Access Management (IAM) is a security framework that controls **who can access resources** and **what actions they are allowed to perform**.

IAM is one of the most important security concepts in cloud environments such as **AWS** and **Microsoft Azure**.

---

# What is IAM?

## Definition

Identity and Access Management (IAM) is a security service that manages user identities, authentication, authorization, and permissions for accessing cloud resources.



### Example

A developer needs access only to EC2 instances.

Using IAM, the administrator grants permission to manage EC2 but denies access to S3 buckets and IAM settings.

---

# Why is IAM Important?

IAM helps organizations:

- Control access to cloud resources.
- Prevent unauthorized access.
- Protect sensitive data.
- Enforce security policies.
- Implement the Principle of Least Privilege.
- Track user activities.

---

# IAM Components

## 1. Users

### Definition

A User is an individual identity created to access cloud resources.


### Example

- Alice (Cloud Administrator)
- Bob (Developer)
- Charlie (SOC Analyst)

---

## 2. Groups

### Definition

A Group is a collection of users with the same permissions.



### Example

Developers Group

- Alice
- Bob
- John

All members automatically receive the same permissions.

---

## 3. Roles

### Definition

A Role is a set of permissions that can be temporarily assigned to users, services, or applications.



### Example

An EC2 instance needs access to an S3 bucket.

Instead of storing AWS credentials on the server, an IAM Role is attached to the EC2 instance.

---

## 4. Policies

### Definition

A Policy is a document that defines what actions are allowed or denied.

### Simple Definition

Policies specify permissions.

### Example

Allow

- Read S3 bucket

Deny

- Delete S3 bucket

---

# Principle of Least Privilege (PoLP)

## Definition

The Principle of Least Privilege means users should receive only the minimum permissions required to perform their job.



### Example

A Help Desk employee should be able to reset user passwords but should not be allowed to delete user accounts.

---

# AWS IAM Example

| Component | Example |
|-----------|---------|
| User | Alice |
| Group | Developers |
| Role | EC2-to-S3 Access |
| Policy | Read-Only S3 Access |

---

# Microsoft Entra ID Example

| Component | Example |
|-----------|---------|
| User | John |
| Group | SOC Team |
| Role | Security Reader |
| Policy | MFA Required |

---

# IAM Best Practices

- Enable Multi-Factor Authentication (MFA)
- Follow the Principle of Least Privilege
- Use strong passwords
- Regularly review user permissions
- Remove unused accounts
- Avoid using the root/administrator account for daily tasks
- Monitor login activity
- Rotate access keys regularly

---

# Common IAM Security Risks

| Risk | Description |
|------|-------------|
| Weak Passwords | Easy-to-guess passwords increase the risk of compromise. |
| Over-Permissioned Users | Users have more permissions than required. |
| Shared Accounts | Multiple users share the same account. |
| Unused Accounts | Inactive accounts remain enabled. |
| Disabled MFA | Accounts are protected only by passwords. |
| Exposed Access Keys | Credentials are leaked or stored insecurely. |

---

# SOC Analyst Perspective

As a SOC Analyst, monitor for:

- Multiple failed login attempts
- Successful login after repeated failures
- New user creation
- New administrator accounts
- Privilege escalation
- IAM policy changes
- MFA disabled
- Root account usage
- Login from unusual locations
- Suspicious API activity

---

# IAM in AWS vs Microsoft Azure

| AWS IAM | Microsoft Entra ID |
|----------|--------------------|
| IAM Users | Users |
| IAM Groups | Groups |
| IAM Roles | Roles |
| IAM Policies | Conditional Access / Permissions |
| MFA | MFA |

---

# Key Points to Remember

- IAM controls authentication and authorization.
- Users represent identities.
- Groups simplify permission management.
- Roles provide temporary access.
- Policies define permissions.
- Follow the Principle of Least Privilege.
- Enable MFA for all privileged accounts.

---

# Interview Questions

## 1. What is IAM?

### Answer

Identity and Access Management (IAM) is a security framework that controls who can access cloud resources and what actions they are allowed to perform.

---

## 2. What is an IAM User?

### Answer

An IAM User is an individual identity that can authenticate and access cloud resources.

---

## 3. What is an IAM Group?

### Answer

An IAM Group is a collection of users that share the same permissions.

---

## 4. What is an IAM Role?

### Answer

An IAM Role is a set of permissions that can be temporarily assigned to users, services, or applications.

---

## 5. What is an IAM Policy?

### Answer

An IAM Policy is a document that defines which actions are allowed or denied on cloud resources.

---

## 6. What is the Principle of Least Privilege?

### Answer

The Principle of Least Privilege states that users should be granted only the minimum permissions required to perform their job responsibilities.

---

## 7. Why is IAM important?

### Answer

IAM helps secure cloud environments by controlling access, preventing unauthorized activities, protecting sensitive data, and enforcing security policies.

---

# Summary

- IAM manages identities and permissions.
- Users, Groups, Roles, and Policies are the core IAM components.
- The Principle of Least Privilege reduces security risks.
- IAM is essential for protecting cloud resources in AWS and Azure.
- SOC Analysts monitor IAM logs and activities to detect unauthorized access, privilege escalation, and suspicious behavior.
