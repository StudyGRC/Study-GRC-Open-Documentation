### Document Classification and Labeling Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | GOV-STD-005 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | **Public** |

### 1. Purpose
The purpose of this Standard is to establish a mandatory framework for classifying and labeling all information assets generated, processed, or stored by Study GRC Inc. This ensures that data is protected according to its sensitivity and value, mitigating risks associated with unauthorized disclosure, modification, or destruction.

This Standard directly supports **Bylaws Article IX (Policies & Data Protection)**, specifically Section 9.2 (Confidentiality & NDA) and Section 9.3 (Intellectual Property), by defining the practical application of confidentiality requirements. Furthermore, it ensures compliance with federal regulations regarding youth protection (COPPA) and donor privacy (IRS).

### 2. Scope
This Standard applies to:
*   **Personnel:** All Directors, Officers, employees, volunteers, and contractors.
*   **Assets:** All physical documents, electronic files, databases, email communications, and software code repositories owned by the Organization.
*   **Third Parties:** Vendors and partners accessing Organization data must adhere to these standards via contract.

**Exclusions:** Publicly available third-party data not under the Organization's control.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Information Asset** | Any data, device, or other component of the environment that supports information-related activities. |
| **Data Owner** | The individual or role (e.g., Department Head) accountable for the classification, protection, and use of a specific data set. |
| **PII** | Personally Identifiable Information (e.g., names, addresses, SSNs). |
| **Sanitization** | The process of removing sensitive information from a document or media so that it can be declassified to a lower level. |
| **TLP** | Traffic Light Protocol (used for threat intelligence sharing). |

### 4. Standard Statements

#### 4.1 Classification Levels
All Study GRC Inc. information assets must be categorized into one of the following four levels. If data falls into multiple categories, the highest (most restrictive) classification applies.

**Level 1: PUBLIC (Green)**
*   **Definition:** Information intended for public release or which, if disclosed, would cause no harm to the Organization or individuals.
*   **Examples:**
    *   Open-source educational curriculum (Bylaws Art. 1.3).
    *   Published website content and blog posts.
    *   IRS Form 990 (Public Copy) and Annual Reports (Bylaws Art. 8.2).
    *   Job postings and volunteer opportunities.

**Level 2: INTERNAL (Amber)**
*   **Definition:** Information intended for internal operations. Unauthorized disclosure could cause minor operational disruption or embarrassment but no significant legal or financial damage.
*   **Examples:**
    *   Internal policies and procedures (unless marked Public).
    *   All-staff memos and non-sensitive meeting minutes.
    *   Draft educational materials not yet released.
    *   Internal slack conversations regarding day-to-day operations.

**Level 3: CONFIDENTIAL (Red)**
*   **Definition:** Sensitive information where unauthorized disclosure could result in legal liability, financial loss, or reputational damage. Access is restricted to specific roles on a "need-to-know" basis.
*   **Examples:**
    *   Donor records and donation history (non-public).
    *   Vendor contracts and negotiated rates.
    *   Employee/Volunteer personnel files (excluding medical).
    *   Board Meeting Minutes (Executive Session).
    *   Unpublished intellectual property or exam questions.

**Level 4: RESTRICTED (Black)**
*   **Definition:** Highly sensitive information requiring the strictest controls. Disclosure would cause severe harm to individuals (safety risks) or the Organization (existential threat).
*   **Examples:**
    *   **Youth Data:** Any PII regarding participants under age 18 (COPPA compliance).
    *   Background check results (Criminal history).
    *   Whistleblower identity and investigation files.
    *   Encryption keys, master passwords, and admin credentials.
    *   Employee medical records (HIPAA/ADA).

#### 4.2 Labeling Requirements
Visual labeling ensures users immediately recognize the sensitivity of a document.

**4.2.1 Documents (Word, PDF, Slides)**
*   **Public:** Labeling is optional but recommended: "Public Distribution".
*   **Internal:** Must include "INTERNAL USE ONLY" in the footer.
*   **Confidential:** Must include "CONFIDENTIAL" in the header (Red text preferred).
*   **Restricted:** Must include "RESTRICTED - [ROLE] EYES ONLY" in the header and footer.

**4.2.2 Email Communications**
*   **Confidential/Restricted:** Subject lines must begin with a tag to alert the recipient and trigger Data Loss Prevention (DLP) rules if applicable.
    *   Format: `[SEC=CONFIDENTIAL] Subject Line Here`
    *   Format: `[SEC=RESTRICTED] Subject Line Here`

**4.2.3 File Naming Conventions**
*   Files containing Level 3 or 4 data should append the classification to the filename.
    *   Example: `2023_Budget_Draft_CONFIDENTIAL.xlsx`

**4.2.4 Code Repositories (GitHub/GitLab)**
*   **Public Repos:** Must contain a `LICENSE` file (e.g., MIT, CC-BY) and a `README.md` stating it is open source.
*   **Private Repos:** Must include a `SECURITY.md` file defining the repository as Internal or Confidential.

#### 4.3 Handling and Protection Matrix
Users must adhere to the following handling requirements based on classification:

| Control | Level 1: Public | Level 2: Internal | Level 3: Confidential | Level 4: Restricted |
| :--- | :--- | :--- | :--- | :--- |
| **Access** | Anonymous / Everyone | All Staff & Volunteers | Role-Based (Need-to-Know) | Named Individuals Only |
| **Encryption (At Rest)** | Optional | Recommended | **Mandatory** | **Mandatory** |
| **Encryption (In Transit)** | TLS (HTTPS) | TLS (HTTPS) | **End-to-End Encrypted** | **End-to-End Encrypted** |
| **External Sharing** | Permitted | Manager Approval Required | Director Approval + NDA | **Prohibited** (Exceptions by Board) |
| **Storage Location** | Public Website, GitHub | Google Drive (Shared Drives) | Secure Drive (Restricted Folder) | Encrypted Vault / Secure Server |
| **Hard Copy Disposal** | Recycle | Shred | Cross-Cut Shred | Cross-Cut Shred / Incinerate |

#### 4.4 Re-Classification (Sanitization)
*   **Downgrading:** Information may be moved from a higher level to a lower level (e.g., Confidential to Public) only by the Data Owner.
*   **Sanitization:** Before downgrading, all sensitive data (PII, secrets) must be redacted or removed.
*   **Open Source Release:** Code or content developed internally (Level 2) intended for release (Level 1) must undergo a review to ensure no hardcoded credentials or PII are present.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Data Owner** | Assigns the initial classification level to data they create or manage. Reviews classification annually. |
| **All Users** | Apply appropriate labels to documents and emails. Adhere to the Handling Matrix (Section 4.3). |
| **CISO** | Maintains this Standard. Configures IT systems (DLP, Email Gateways) to enforce labeling rules where technically feasible. |
| **Department Heads** | Ensure their teams are trained on this Standard and that department-specific assets are correctly labeled. |

### 6. Compliance and Enforcement
Failure to comply with this Standard may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

*   **Unauthorized disclosure of Level 4 (Restricted) Youth Data** will result in immediate suspension pending investigation and mandatory reporting to relevant authorities if required by law.
*   **Mislabeling:** Intentionally mislabeling Public data as Restricted to avoid scrutiny (transparency avoidance) is a violation of the Organization's Code of Ethics.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article IX: Policies & Data Protection)
*   **GOV-POL-007:** Master Data Privacy Policy
*   **HR-POL-024:** Background Check Policy (Handling of Criminal History)
*   **IS-POL-001:** Master Information Security Policy
*   **NIST SP 800-53 Rev. 5:** Security and Privacy Controls (Family: System and Information Integrity)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial Release |