### CASB Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-088 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director / CISO |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish the governance framework for the use of a Cloud Access Security Broker (CASB) within Study GRC Inc. As a remote-first organization relying heavily on cloud services, this policy aims to mitigate the risks associated with "Shadow IT," prevent data leakage, and ensure visibility into cloud application usage. This policy supports the Organization’s commitment to data protection as outlined in **Article IX (Policies & Data Protection)** of the Bylaws and aligns with NIST Cybersecurity Framework (CSF) functions regarding protection and detection.

### 2. Scope
This policy applies to:
*   **Personnel:** All employees, volunteers, contractors, and Board members accessing Organization data.
*   **Assets:** All Organization-owned devices and any personal devices (BYOD) used to access Organization resources.
*   **Applications:** All cloud-based applications (SaaS), platforms (PaaS), and infrastructure (IaaS), whether officially sanctioned by the IT Department or unsanctioned.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **CASB (Cloud Access Security Broker)** | A software tool or service that sits between an organization's on-premises infrastructure and a cloud provider's infrastructure to enforce security, compliance, and governance policies. |
| **Shadow IT** | The use of information technology systems, devices, software, applications, and services without explicit IT department approval. |
| **Sanctioned Application** | A cloud application that has been vetted for security, compliance, and legal terms, and is officially approved for use by the Organization. |
| **Unsanctioned Application** | A cloud application that has not been approved for use. These may be blocked or monitored depending on risk level. |
| **DLP (Data Loss Prevention)** | Strategies and tools used to ensure that sensitive data is not lost, misused, or accessed by unauthorized users. |
| **API (Application Programming Interface)** | A set of protocols for building and integrating application software; CASBs often use APIs to scan data at rest in cloud apps. |

### 4. Policy Statements

#### 4.1. Mandatory CASB Deployment
To maintain visibility and control over the Organization’s distributed data environment, Study GRC Inc. must deploy and maintain a CASB solution. This solution serves as the primary enforcement point for cloud security policies.
*   All traffic destined for cloud applications from managed devices must be routed through or monitored by the CASB where technically feasible.
*   API integration must be configured for all major Sanctioned Applications (e.g., Google Workspace, Slack, GitHub) to scan data at rest.

#### 4.2. Cloud Application Classification
The CISO or their designee must utilize the CASB to maintain a dynamic inventory of all cloud applications in use. Applications must be classified into one of the following categories:
1.  **Sanctioned:** Fully vetted, enterprise license procured, SSO integrated.
2.  **Tolerated:** Low risk, no sensitive data allowed, but not officially supported (e.g., a specific music streaming site for personal use).
3.  **Unsanctioned/Blocked:** High risk, redundant functionality, or known malicious reputation. Access to these applications must be technically blocked.

#### 4.3. Management of Shadow IT
The Organization acknowledges that Shadow IT poses significant security, financial, and compliance risks.
*   **Discovery:** The CASB must be configured to continuously discover new cloud applications being accessed by personnel.
*   **Review:** The IT Department must review the "Shadow IT Report" monthly to identify high-volume or high-risk unsanctioned apps.
*   **Remediation:** If a legitimate business need is identified for a Shadow IT application, it must undergo the formal **Vendor Security Risk Assessment (VSRA)** process to become a Sanctioned Application. If no need exists or the risk is too high, the application must be blocked.

#### 4.4. Data Loss Prevention (DLP) Enforcement
Pursuant to **Bylaws Article IX, Section 9.2 (Confidentiality)**, the CASB must enforce DLP policies to prevent the unauthorized exfiltration of sensitive data.
*   **Pattern Matching:** The CASB must be configured to block or quarantine files containing PII (Personally Identifiable Information), Youth Data, or Financial Data from being uploaded to Unsanctioned Applications (e.g., personal Dropbox, unvetted PDF converters).
*   **External Sharing:** The CASB must monitor and, where necessary, revoke public sharing links created within Sanctioned Applications that violate the **Data Classification Standard**.

#### 4.5. Context-Aware Access Control
Access to Sanctioned Applications is not binary; it is context-dependent. The CASB must enforce policies based on:
*   **User Group:** (e.g., Volunteers may have restricted access compared to Staff).
*   **Device Status:** (e.g., Managed devices may download files; Unmanaged/BYOD devices may be restricted to "View Only" via browser isolation).
*   **Location:** Access from high-risk geolocations or anonymizing proxies (TOR nodes) must be blocked or require stepped-up Multi-Factor Authentication (MFA).

#### 4.6. Threat Protection
The CASB must be configured to detect and block:
*   **Compromised Accounts:** Anomalous behavior indicative of account takeover (e.g., impossible travel, massive data download).
*   **Malware:** Malicious files attempting to be uploaded to or downloaded from cloud storage.
*   **OAuth Abuse:** Malicious third-party apps attempting to connect to Sanctioned Application accounts (e.g., a fake calendar app requesting full email read access).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns the CASB strategy; defines high-level blocking and DLP policies; reviews monthly Shadow IT reports. |
| **IT Systems Administrator** | Configures CASB policies, alerts, and API connectors; manages the daily operation of the CASB dashboard. |
| **Department Heads** | Responsible for submitting formal requests for new software tools rather than utilizing Shadow IT; ensures team compliance. |
| **Employees & Volunteers** | Must utilize only Sanctioned Applications for processing Organization data; must not attempt to bypass CASB controls (e.g., via VPNs). |

### 6. Compliance and Enforcement
Failure to comply with this policy—specifically the intentional circumvention of CASB controls or the storage of Sensitive Data in Unsanctioned Applications—constitutes a violation of the Organization's security protocols.

Violations may result in disciplinary action, up to and including termination of employment or volunteer assignment. In cases where Shadow IT usage results in a data breach, legal action may be pursued in accordance with **Bylaws Article VII (Indemnification)** and applicable state/federal laws.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-STD-005:** Data Classification Standard
*   **IS-POL-020:** Acceptable Use Policy (AUP)
*   **IS-FRM-010:** Vendor Security Risk Assessment (VSRA)
*   **NIST SP 800-53 (Rev. 5):** AC-4 (Information Flow Enforcement), SC-7 (Boundary Protection)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Compliance Architect | Initial Policy Drafting and Approval |