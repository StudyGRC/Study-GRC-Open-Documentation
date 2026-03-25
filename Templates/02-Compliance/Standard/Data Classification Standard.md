### Data Classification Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-028 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to establish a framework for classifying data based on its sensitivity, value, and criticality to Study GRC Inc. (the "Organization"). This classification drives the application of appropriate security controls to protect data from unauthorized access, modification, or destruction.

This Standard satisfies **NIST CSF ID.AM-2**, ensuring that data is managed consistent with the Organization’s risk strategy and mission to provide open-source resources while rigorously protecting community and youth data.

### 2. Scope
This Standard applies to:
*   **All Data:** Electronic and physical information assets created, processed, stored, or transmitted by the Organization.
*   **All Personnel:** Employees, Board Directors, Officers, Volunteers, and Contractors.
*   **All Systems:** Organization-owned devices, authorized BYOD endpoints, and third-party cloud services (SaaS/IaaS).

**Exclusions:** Personal data stored on BYOD devices that is wholly unrelated to the Organization’s business or community operations.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Data Owner** | The individual or role (usually a Department Head) with the authority to decide the classification level of a specific data set and grant access rights. |
| **Data Custodian** | The IT or Security personnel responsible for implementing the technical controls (encryption, access lists) defined by the Data Owner. |
| **PII (Personally Identifiable Information)** | Information that can be used to distinguish or trace an individual's identity, either alone or when combined with other information (e.g., name, email, IP address). |
| **Youth Data** | Any data pertaining to a natural person under the age of 18. Due to COPPA and Texas Family Code requirements, this data requires elevated protection. |
| **TLP (Traffic Light Protocol)** | A system for classifying sensitive information created by CISA/FIRST, used here to align with the cybersecurity community standards. |

### 4. Standards

#### 4.1 Classification Levels
All Organization data must be categorized into one of the following four levels. If the classification of a data set is unclear, it must be treated as **Confidential** until formally classified by the Data Owner.

| Level | Classification Name | Description | Examples |
| :--- | :--- | :--- | :--- |
| **Level 1** | **Public** (TLP:CLEAR) | Information intended for public release or open-source distribution. Disclosure causes no harm. | • Open-source curriculum<br>• Published Bylaws<br>• IRS Form 990s (Public Copy)<br>• Press Releases<br>• Website Content |
| **Level 2** | **Internal** (TLP:GREEN) | Information for internal operations. Disclosure would cause minimal harm or embarrassment but is not intended for the public. | • Internal memos<br>• Draft policies<br>• Employee/Volunteer handbooks<br>• Slack #general discussions<br>• Vendor lists |
| **Level 3** | **Confidential** (TLP:AMBER) | Sensitive information where unauthorized disclosure could cause reputational damage, financial loss, or privacy violations. | • Donor giving history<br>• Volunteer contact lists (Adult)<br>• Unpublished financial budgets<br>• Vendor contracts<br>• Board Meeting Minutes (Drafts) |
| **Level 4** | **Restricted** (TLP:RED) | Highly sensitive data where disclosure could result in severe legal action, safety risks, or regulatory fines. **Strict Need-to-Know.** | • **All Youth Data** (Names, ages, images)<br>• Background Check Reports<br>• Social Security Numbers<br>• Passwords/Private Keys<br>• Whistleblower identities |

#### 4.2 Labeling Requirements
Data Owners must ensure data is labeled to indicate its classification level.

*   **Documents:** Header or Footer must state the classification (e.g., "CONFIDENTIAL - STUDY GRC INTERNAL USE ONLY").
*   **Emails:** Subject lines for Level 3 and 4 data must begin with `[SECURE]` or `[CONFIDENTIAL]`.
*   **File Systems:** Folder names in cloud storage (e.g., Google Drive, SharePoint) must include the classification level (e.g., `HR - Restricted - Employee Files`).
*   **Code Repositories:** Public repositories (GitHub) must contain a `LICENSE` file. Private repositories containing proprietary tools must be marked in the `README.md`.

#### 4.3 Handling and Protection Requirements
The following minimum security controls must be applied based on classification:

| Control | Level 1: Public | Level 2: Internal | Level 3: Confidential | Level 4: Restricted |
| :--- | :--- | :--- | :--- | :--- |
| **Access Control** | Open to World | All Staff/Volunteers | Role-Based (Group) | Individual Need-to-Know |
| **Encryption (Transit)** | TLS 1.2+ (HTTPS) | TLS 1.2+ | TLS 1.2+ | TLS 1.2+ / End-to-End |
| **Encryption (Rest)** | Optional | Recommended | **Required** | **Required** |
| **External Sharing** | Permitted | Approval Required | NDA Required | **Strictly Prohibited** without CISO & Legal Approval |
| **Storage Location** | Public Website / GitHub | Intranet / Drive | Secure Cloud Drive | Secure Enclave / Encrypted Vault |
| **MFA Requirement** | N/A | Required for Access | Required for Access | Required (Phishing-Resistant Preferred) |
| **Hard Copy Disposal** | Recycle | Shred | Cross-Cut Shred | Cross-Cut Shred / Incinerate |

#### 4.4 Data Aggregation
If Level 2 (Internal) data is aggregated to a point where it reveals sensitive patterns (e.g., a full database of all volunteers), the aggregate dataset must be reclassified to **Level 3 (Confidential)**.

#### 4.5 Reclassification
Data classification may change over time (e.g., an embargoed press release becomes Public).
*   Only the **Data Owner** may downgrade a classification level.
*   Any user may upgrade a classification level if they believe the data is under-protected, pending review by the Data Owner.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Data Owner** | Determines the classification of data created within their department. Reviews classification annually. Authorizes access to Level 3 and Level 4 data. |
| **CISO** | Defines the security controls for each level. Audits compliance with this Standard. Manages the DLP (Data Loss Prevention) tools. |
| **All Personnel** | Responsible for applying the correct labels and handling data according to this Standard. Must report misclassified or exposed data immediately. |
| **Board of Directors** | Pursuant to **Bylaws Article IX**, Directors must adhere to these standards regarding Board materials and Conflict of Interest disclosures. |

### 6. Compliance and Enforcement
Failure to comply with this Standard may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action.

*   **Youth Data:** Mishandling Level 4 Youth Data may trigger mandatory reporting requirements under the **Texas Family Code** and **COPPA**.
*   **Intellectual Property:** Unauthorized release of Level 3 or 4 data may violate the **Intellectual Property** provisions in **Bylaws Article IX (9.3)**.

### 7. References
*   **Bylaws of Study GRC Inc.** (Specifically Article IX: Policies & Data Protection)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-020:** Data Privacy Policy (GDPR/TDPSA)
*   **HR-POL-015:** Child and Youth Safeguarding Policy
*   **NIST CSF 2.0:** ID.AM-2, PR.DS-5

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Compliance Architect | Initial Release aligned with NIST ID.AM-2 |