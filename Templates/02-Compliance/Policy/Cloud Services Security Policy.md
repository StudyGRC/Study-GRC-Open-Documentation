### Cloud Services Security Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-085 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2025-10-25 (Bi-Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
As a remote-first organization, Study GRC Inc. ("the Organization") relies heavily on cloud computing services to fulfill its charitable and educational mission. The purpose of this policy is to establish a framework for the secure selection, implementation, and use of Cloud Service Providers (CSPs). This policy ensures that data confidentiality, integrity, and availability are maintained across all cloud environments in alignment with the Cloud Security Alliance (CSA) Cloud Controls Matrix (CCM) and NIST standards.

### 2. Scope
This policy applies to:
*   **Personnel:** All employees, Board members, volunteers, and contractors utilizing Organization resources.
*   **Assets:** All data, applications, and infrastructure owned or leased by the Organization that are hosted, processed, or stored by third-party cloud providers.
*   **Service Models:** Software as a Service (SaaS), Platform as a Service (PaaS), and Infrastructure as a Service (IaaS).

**Exclusions:**
*   Personal cloud accounts (e.g., personal Gmail, Dropbox) used strictly for non-Organization business. However, the storage of Organization data on personal cloud accounts is strictly prohibited.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Cloud Service Provider (CSP)** | A third-party company offering a cloud-based platform, infrastructure, application, or storage service (e.g., AWS, Google Workspace, Slack, GitHub). |
| **SaaS (Software as a Service)** | Applications delivered over the internet (e.g., Zoom, Salesforce). |
| **IaaS (Infrastructure as a Service)** | Virtualized computing resources over the internet (e.g., AWS EC2, Azure VMs). |
| **Shadow IT** | Information technology systems, devices, software, applications, and services managed without explicit Organization approval. |
| **Shared Responsibility Model** | A security framework that dictates which security controls are the responsibility of the CSP and which are the responsibility of the customer (Study GRC Inc.). |
| **CASB** | Cloud Access Security Broker; software that sits between cloud service users and cloud applications to monitor activity and enforce security policies. |

### 4. Policy Statements

#### 4.1 Cloud Governance and Strategy (CSA Domain: GRC)
The Organization adopts a "Cloud-First" strategy but mandates that security is a prerequisite for adoption.
*   **4.1.1 Inventory:** The CISO must maintain a centralized inventory of all authorized CSPs, including the data classification level permitted for each platform.
*   **4.1.2 Risk Appetite:** The Organization shall not utilize CSPs that cannot demonstrate compliance with recognized security frameworks (e.g., SOC 2 Type II, ISO 27001, or FedRAMP) for handling Confidential or Restricted data.

#### 4.2 Acquisition and Vendor Assessment (CSA Domain: SCRM)
No personnel may enter into an agreement (free or paid) with a CSP without prior security review.
*   **4.2.1 Security Assessment:** All potential CSPs must undergo a Vendor Security Risk Assessment (VSRA) prior to onboarding. This assessment evaluates the provider's ability to protect data in accordance with the Organization's *Master Information Security Policy*.
*   **4.2.2 Youth Protection Compliance:** Any CSP that may process data of minors (under 18) must be evaluated for compliance with COPPA and the Organization's *Child and Youth Safeguarding Policy*.
*   **4.2.3 Terms of Service:** Personnel are prohibited from clicking "I Agree" on standard Terms of Service for enterprise-critical functions without review by the Legal or Compliance function to ensure IP rights are preserved per Bylaws Article IX.

#### 4.3 Identity and Access Management (CSA Domain: IAM)
Access to cloud services must be strictly controlled to prevent unauthorized entry.
*   **4.3.1 SSO Integration:** Where technically feasible, all CSPs must be integrated with the Organization’s centralized Single Sign-On (SSO) identity provider.
*   **4.3.2 Multi-Factor Authentication (MFA):** MFA is mandatory for all cloud services. If a CSP does not support MFA, it may not be used for any data classified higher than "Public."
*   **4.3.3 Least Privilege:** Access rights within cloud platforms must be granted based on the principle of least privilege and reviewed quarterly.

#### 4.4 Data Protection and Encryption (CSA Domain: DSI)
*   **4.4.1 Encryption at Rest:** All Organization data stored in the cloud must be encrypted at rest using industry-standard algorithms (e.g., AES-256).
*   **4.4.2 Encryption in Transit:** All data transmission to and from CSPs must be encrypted using TLS 1.2 or higher.
*   **4.4.3 Data Residency:** CSPs must allow the Organization to designate the geographic regions where data is stored to ensure compliance with applicable privacy laws (e.g., GDPR, CCPA).

#### 4.5 Prohibition of Shadow IT
*   **4.5.1 Unauthorized Use:** The use of unauthorized cloud services ("Shadow IT") for storing or processing Organization data is strictly prohibited.
*   **4.5.2 Discovery:** The CISO is authorized to use technical controls (e.g., CASB, firewall logs) to detect and block access to unauthorized cloud applications.

#### 4.6 Infrastructure and Configuration Management (CSA Domain: IVS)
For IaaS and PaaS environments (e.g., AWS, Azure):
*   **4.6.1 Hardening:** Default configurations must be changed. All cloud infrastructure must be hardened according to CIS Benchmarks.
*   **4.6.2 Public Access:** Cloud storage buckets (e.g., S3) and databases must be configured to block public access by default unless explicitly authorized for public web hosting.

#### 4.7 Incident Management (CSA Domain: SEF)
*   **4.7.1 Reporting:** CSPs must be contractually obligated to report security breaches affecting the Organization’s data within a timeframe that allows the Organization to meet its regulatory reporting obligations (e.g., 72 hours for GDPR).
*   **4.7.2 Response:** Cloud-related security incidents shall be managed in accordance with the *Incident Response Plan*.

#### 4.8 Intellectual Property and Data Ownership
Pursuant to **Bylaws Article IX, Section 9.3**, the Organization retains exclusive ownership of all Work Product created or stored within cloud services.
*   **4.8.1 Portability:** The Organization must ensure that data stored in a CSP can be retrieved in a standard, usable format to prevent vendor lock-in.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Board of Directors** | Approves the acceptable risk level regarding cloud adoption and reviews major vendor contracts involving critical data. |
| **Executive Director** | Ensures budget allocation for enterprise-grade security features (e.g., SSO) in cloud contracts. |
| **CISO** | Conducts vendor security assessments, maintains the authorized cloud inventory, and monitors for Shadow IT. |
| **IT/System Administrators** | Configures cloud environments (IaaS/PaaS) securely and manages IAM/SSO integration. |
| **Employees/Volunteers** | Uses only authorized cloud services; protects credentials; reports suspected Shadow IT or breaches. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

Unauthorized use of cloud services that results in a data breach or loss of Intellectual Property may be considered a violation of the **Board of Directors Code of Ethics** and **Bylaws Article IX**.

### 7. References
*   **CSA Cloud Controls Matrix (CCM) v4**
*   **NIST SP 800-144:** Guidelines on Security and Privacy in Public Cloud Computing
*   **Study GRC Bylaws:** Article IX (Intellectual Property)
*   **IS-POL-020:** Master Information Security Policy
*   **IS-FRM-005:** Vendor Security Risk Assessment (VSRA)
*   **HR-POL-001:** Employee Handbook (Acceptable Use)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Legal Officer | Initial Policy Release aligned with CSA CCM. |