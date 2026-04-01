# 🔐 IAM Project – Microsoft Entra ID (Azure AD)

![Azure](https://img.shields.io/badge/Azure-Entra%20ID-blue?style=for-the-badge&logo=microsoftazure)
![IAM](https://img.shields.io/badge/IAM-Identity%20Management-orange?style=for-the-badge)
![Security](https://img.shields.io/badge/Security-Zero%20Trust-green?style=for-the-badge)
![MFA](https://img.shields.io/badge/MFA-Enabled-red?style=for-the-badge)
![SSO](https://img.shields.io/badge/SSO-SAML-blueviolet?style=for-the-badge)

---

# Identity and Access Management (IAM) Lab using Microsoft Entra ID

## Overview

This repository showcases a hands-on implementation of core Identity and Access Management (IAM) concepts using **Microsoft Entra ID (Azure Active Directory)**.

The project simulates a real-world enterprise IAM environment, covering:

* Identity Lifecycle Management (Joiner, Mover, Leaver)
* Role-Based Access Control (RBAC)
* Multi-Factor Authentication (MFA)
* Single Sign-On (SSO) with Federation

All implementations are validated using logs, testing scenarios, and security best practices.

---

## Project Modules

### Identity Lifecycle Management (JML)

**Objective:** Simulate real-world user lifecycle operations.

**Key Implementations:**

* User provisioning (Joiner)
* Role transition (Mover)
* User deprovisioning (Leaver)
* MFA enforcement using Security Defaults
* Audit log validation

**Scenarios Covered:**

* Jane (HR) → moved to Finance
* Chris (Finance) → offboarded (account disabled & access revoked)

Report: `IAM User Lifecycle Management using Microsoft Entra ID Report.docx`

---

## IAM Architecture Diagram

![IAM Architecture](images/iam-architecture.png)

### 2️⃣ Role-Based Access Control (RBAC)

**Objective:** Enforce least privilege using role-based access design.

**Key Implementations:**

* Defined roles: HR, Finance, IT
* Application-based access control:

  * HR App
  * Finance App
  * IT Tool
* Direct user-to-application assignment (free-tier limitation workaround)

**Access Validation:**

* Users only access assigned applications
* Unauthorized access blocked
* Edge case testing performed

Report: `RBAC assignment in EntraID and Implementation Report.docx`

---

### 3️⃣ Multi-Factor Authentication (MFA)

**Objective:** Strengthen authentication using additional verification factors.

**Key Implementations:**

* Enabled **Security Defaults** (tenant-wide MFA)
* Configured **Microsoft Authenticator App**
* Simulated real-world login scenarios:

  * Successful authentication
  * Failed login attempts
  * MFA denial
  * Session-based authentication behavior

**Security Concepts:**

* Zero Trust Model
* Strong Identity Verification
* Continuous Monitoring via logs

Report: `Multi-Factor Authentication (MFA) Deployment using Microsoft Entra ID.docx`

---

### 4️⃣ Single Sign-On (SSO) & Federation

**Objective:** Implement centralized authentication using SAML-based SSO.

**Key Implementations:**

* Configured **SAML-based SSO**
* Established **federation trust**
* Created enterprise application (SSO-Lab-App)
* Assigned users and validated access

**Authentication Flow:**
User → Entra ID → SAML Token → Application Access

**Validation:**

* Successful login via SSO
* Verified using Sign-in Logs
* Access denied when user removed (authorization check)

Report: `Single Sign_on and Federation Setup using Microsoft Entra ID.docx`

---

## Tools & Technologies

* Microsoft Entra ID (Azure Active Directory)
* Azure Portal
* Microsoft Authenticator App
* Microsoft Graph PowerShell
* SAML (Security Assertion Markup Language)
* MyApps Portal

---

## Architecture Overview

This lab simulates an enterprise IAM environment:

* **Identity Provider (IdP):** Microsoft Entra ID
* **Users:** HR, Finance, IT roles
* **Applications:** HR App, Finance App, IT Tool, SSO App
* **Authentication:** Password + MFA
* **Authorization:** RBAC

---

## Security Principles Implemented

* Least Privilege Access
* Zero Trust Security Model
* Strong Authentication (MFA)
* Centralized Identity Management
* Access Governance & Audit Logging

---

## Key Learnings

* End-to-end IAM lifecycle management (JML)
* RBAC design and enforcement
* MFA deployment and behavior analysis
* SAML-based SSO and federation setup
* Log-based validation and troubleshooting

---

## Repository Structure

```
IAM-Project/
│
├── IAM User Lifecycle Management using Microsoft Entra ID Report.docx
├── RBAC assignment in EntraID and Implementation Report.docx
├── Multi-Factor Authentication (MFA) Deployment using Microsoft Entra ID.docx
├── Single Sign_on and Federation Setup using Microsoft Entra ID.docx
└── README.md
```

---

## Future Enhancements

* Implement Conditional Access Policies
* Integrate with HR systems for automation
* Use group-based RBAC (Premium features)
* Implement passwordless authentication (FIDO2)
* Automate provisioning using APIs / PowerShell

---

## Author

**Suvarna Rekha V**
Aspiring IAM & Cybersecurity Professional