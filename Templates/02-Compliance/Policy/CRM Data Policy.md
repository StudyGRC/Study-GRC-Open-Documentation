### CRM Data Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-025 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish mandatory standards for the entry, maintenance, security, and integrity of data within the Study GRC Inc. Customer Relationship Management (CRM) system. As an organization dedicated to "advancing governance, risk, and compliance knowledge" (Bylaws Article I, Section 1.3), Study GRC Inc. must maintain a pristine database to ensure accurate reporting, effective donor stewardship, and compliance with global data privacy regulations (including TDPSA, GDPR, and CCPA). This policy specifically addresses the risk of "Dirty Data," which compromises decision-making and operational efficiency.

### 2. Scope
This policy applies to all employees, contractors, Board Directors, and volunteers ("Users") who have read or write access to the Organization’s CRM system.

*   **In Scope:** All constituent records (individuals and organizations), donation history, volunteer logs, case management data, and API integrations connected to the CRM.
*   **Exclusions:** Financial ledgers held strictly within the accounting software (e.g., QuickBooks), although synchronization data between the CRM and accounting software is in scope.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **CRM** | Customer Relationship Management system; the central repository for constituent data (e.g., Salesforce, HubSpot, NeonCRM). |
| **Constituent** | Any individual or organization with a record in the CRM (e.g., donors, members, volunteers, vendors). |
| **Dirty Data** | Data that is erroneous, incomplete, duplicate, outdated, or formatted inconsistently. |
| **PII** | Personally Identifiable Information; any representation of information that permits the identity of an individual to whom the information applies to be reasonably inferred by either direct or indirect means. |
| **Data Steward** | The designated staff member responsible for the daily hygiene and structural integrity of CRM data. |
| **Minor** | Any constituent under the age of 18. |

### 4. Policy Statements

#### 4.1 Data Governance and Ownership
In accordance with **Bylaws Article VIII, Section 8.1** regarding the maintenance of records, the CRM is a designated corporate record.
*   **4.1.1** The **Chief Information Security Officer (CISO)** owns the security architecture of the CRM.
*   **4.1.2** The **VP of Education & Training** and **Director of Kindness and Generosity** are the primary Data Owners for their respective domains (Learner data and Donor/Member data).
*   **4.1.3** Users must not utilize CRM data for personal benefit, commercial solicitation outside of Organization business, or any purpose conflicting with the **Conflict of Interest Policy (Bylaws Article IX, Section 9.1)**.

#### 4.2 Data Entry and Quality Standards
To prevent Dirty Data, all Users must adhere to the following entry standards. Failure to follow these standards may result in revocation of write access.

*   **4.2.1 Search Before Create:** Before creating a new record, Users **must** perform a search using at least two criteria (e.g., Email Address and Last Name) to ensure the constituent does not already exist.
*   **4.2.2 Case Sensitivity and Formatting:**
    *   **Names:** Must use Title Case (e.g., "Jane Doe," not "jane doe" or "JANE DOE").
    *   **Phone Numbers:** Must follow the E.164 standard or the format `(555) 555-5555`.
    *   **Addresses:** Must adhere to USPS standardization (e.g., use "St." instead of "Street" if validated by address tools).
*   **4.2.3 Required Fields:** Users must not bypass required fields using placeholder data (e.g., "N/A", "TBD", or "Test"). If data is unknown, the record should not be created until the data is verified.
*   **4.2.4 Email Verification:** Email addresses must be verified for syntax validity before entry.

#### 4.3 Duplicate Management
*   **4.3.1** The CRM Administrator must configure automated duplicate matching rules (e.g., Fuzzy Logic on Name + Exact Match on Email).
*   **4.3.2** Users presented with a "Possible Duplicate" warning during data entry must resolve the warning by reviewing the existing record before proceeding.
*   **4.3.3** A systematic de-duplication audit must be performed **quarterly** by the Data Steward.

#### 4.4 Data Privacy and Classification
*   **4.4.1 Minor Flags:** Given the Organization's K-12 focus, any record belonging to a Minor must be explicitly flagged. Contact information for Minors must be handled in strict accordance with the **COPPA Compliance Policy**.
*   **4.4.2 Opt-Out Compliance:** Users must respect "Do Not Email," "Do Not Call," and "Do Not Solicit" flags immediately. Manually overriding these flags is strictly prohibited and constitutes a violation of the **Master Data Privacy Policy**.
*   **4.4.3 Sensitive Data:** The storage of Prohibited Data (e.g., Full Credit Card Numbers, Social Security Numbers, Biometric Data) within standard CRM text fields is **strictly prohibited**.

#### 4.5 Access Control and Security
*   **4.5.1 Least Privilege:** Users shall be granted the minimum level of access required to perform their job functions.
*   **4.5.2 Authentication:** Access to the CRM must be protected by **Multi-Factor Authentication (MFA)** in accordance with the **Master Information Security Policy**.
*   **4.5.3 Export Restrictions:** Bulk export of data (more than 50 records) is restricted to the Executive Director, CISO, and designated Data Stewards. All exports must be logged.

#### 4.6 Data Retention and Archiving
*   **4.6.1** Inactive records (defined as no interaction for 5+ years) shall be archived or anonymized in accordance with the **Document Retention and Destruction Policy**, unless a financial transaction history requires longer retention under IRS regulations.
*   **4.6.2** Users must not delete records containing financial history. These records must be deactivated/archived rather than hard-deleted.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Executive Director** | Ultimate accountability for data integrity; authorizes bulk export requests. |
| **CISO** | Manages CRM security settings, MFA enforcement, and API integrations. |
| **CRM Administrator / Data Steward** | Configures validation rules, performs quarterly de-duplication, and trains staff on entry standards. |
| **All Users** | Adhere to data entry standards (Section 4.2); report data anomalies; protect credentials. |
| **Director of Kindness & Generosity** | Ensures donor and member data accuracy and compliance with donor intent. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

*   **Systematic Enforcement:** The Organization reserves the right to use technical controls (validation rules, field restrictions) to enforce this policy.
*   **Access Revocation:** Users who repeatedly create duplicate records or violate data quality standards will have their "Write" access revoked pending retraining.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article VIII - Records; Article IX - Data Protection)
*   **IS-POL-001:** Master Information Security Policy
*   **GOV-POL-012:** Document Retention and Destruction Policy
*   **PRIV-POL-001:** Master Data Privacy Policy
*   **Texas Business Organizations Code § 22.353** (Books and Records)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Draft |