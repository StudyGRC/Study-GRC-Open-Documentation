### ROPA Maintenance/Update Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | DP-PRC-034 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Data Privacy Officer (DPO) / CISO |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized methodology for maintaining the **Record of Processing Activities (ROPA)** for Study GRC Inc. (the "Organization"). This procedure ensures the Organization maintains an accurate, up-to-date, and comprehensive inventory of how personal data is collected, processed, stored, and shared.

This procedure is designed to satisfy the documentation requirements of **GDPR Article 30**, the **Texas Data Privacy and Security Act (TDPSA)**, and the Organization’s commitment to data transparency as outlined in **Bylaws Article VIII (Records, Transparency & Finance)** and **Article IX (Policies & Data Protection)**.

### 2. Scope
This procedure applies to all Departments, Operational Officers, employees, volunteers, and contractors who define or execute processes involving **Personal Data**.

*   **In Scope:** All automated and manual processing of Personal Data (e.g., donor lists, member databases, employee records, youth participant logs).
*   **Exclusions:** Purely statistical, anonymized data where re-identification is impossible.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **ROPA** | Record of Processing Activities. A living document that maps the lifecycle of data within the Organization. |
| **Personal Data** | Any information relating to an identified or identifiable natural person (e.g., name, email, IP address, dietary restrictions). |
| **Data Steward** | The Department Head or Operational Officer (e.g., VP of Education, DKG) responsible for a specific business process that uses data. |
| **Processing** | Any operation performed on data, including collection, recording, organization, storage, adaptation, retrieval, consultation, use, disclosure, or destruction. |
| **Special Category Data** | Sensitive data requiring higher protection (e.g., health data, biometric data, data regarding minors). |

### 4. Procedures

#### 4.1 Trigger Events for ROPA Updates
The ROPA is not a static document. It **must** be updated upon the occurrence of any of the following triggers:
1.  **New Tool Acquisition:** Procurement of new software (SaaS) or hardware that stores Personal Data.
2.  **New Process Creation:** Launch of a new program, scholarship, or community initiative (e.g., a new mentorship program).
3.  **Change in Processing:** Significant changes to how existing data is used (e.g., sharing member data with a new sponsor).
4.  **Data Sharing:** Establishing a new API connection or data transfer to a third party.

#### 4.2 Initial Data Mapping (New Processes)
When a Data Steward initiates a new process involving Personal Data, they must complete the **Preliminary Data Intake Form** (DP-FRM-001) prior to implementation.

1.  **Identify the Purpose:** Clearly state *why* the data is needed (e.g., "To process membership dues").
2.  **Identify the Legal Basis:** Select the justification (e.g., Consent, Contractual Necessity, Legitimate Interest).
3.  **Categorize Data:** List specific data fields (e.g., Name, Credit Card Token).
4.  **Identify Subjects:** Who is the data about? (e.g., Minors, Employees, Donors).

#### 4.3 ROPA Entry Requirements
The Privacy Office/CISO will translate the Intake Form into the Master ROPA Registry. Every entry **must** contain the following fields to ensure **Accuracy**:

1.  **Process Name & ID:** Unique identifier for the workflow.
2.  **Controller/Processor Status:** Whether Study GRC determines the purpose (Controller) or acts on behalf of another (Processor).
3.  **Purpose of Processing:** Specific description.
4.  **Categories of Data Subjects:** (e.g., Voting Members, Students).
5.  **Categories of Personal Data:** (e.g., Financial, Contact, Health).
6.  **Recipients:** List of third parties/vendors receiving the data.
7.  **Transfers:** Identification of cross-border transfers (e.g., EU to US) and the transfer mechanism used (e.g., SCCs, Data Privacy Framework).
8.  **Retention Period:** Specific timeframe for deletion, aligned with the **Records Retention Schedule**.
9.  **Security Measures:** Technical and organizational controls applied (e.g., Encryption at rest, MFA).

#### 4.4 Quarterly Validation Reviews
To maintain accuracy, the Privacy Office shall conduct quarterly spot-checks.

1.  **Selection:** The Privacy Office selects 10% of ROPA entries for validation.
2.  **Interview:** The Privacy Office interviews the relevant Data Steward to verify:
    *   Is the tool still in use?
    *   Has the data volume changed?
    *   Are access controls still appropriate?
3.  **Correction:** Any discrepancies must be corrected in the Master ROPA Registry within **five (5) business days**.

#### 4.5 Annual Certification
In January of each fiscal year, coinciding with the preparation of the Annual Financial Report (Bylaws Section 8.2), a full ROPA certification is required.

1.  **Distribution:** The CISO sends the current ROPA extract to all Department Heads.
2.  **Review:** Department Heads must review all lines attributed to their department.
3.  **Attestation:** Department Heads must sign the **Annual Data Inventory Attestation**, confirming that the ROPA accurately reflects their department's data practices.
4.  **Gap Analysis:** The CISO identifies any "Shadow IT" or undocumented processes discovered during this review and initiates a **Privacy Impact Assessment (PIA)**.

#### 4.6 Version Control and Archiving
1.  The Master ROPA Registry must be stored in a secure, access-controlled repository (e.g., Secure SharePoint/GRC Platform).
2.  Previous versions of the ROPA must be retained for **five (5) years** to demonstrate historical compliance to regulators.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO / Privacy Officer** | Owns the Master ROPA Registry; conducts quality assurance; determines legal basis for processing; enforces this procedure. |
| **Data Stewards (Dept Heads)** | Responsible for the **accuracy** of ROPA entries related to their function; must report changes in processing immediately. |
| **IT Department** | Notifies the Privacy Office of any new software installation or vendor integration that may impact data processing. |
| **Board of Directors** | Reviews high-level privacy risks derived from the ROPA during the annual risk assessment. |

### 6. Compliance and Enforcement
Failure to maintain an accurate ROPA exposes the Organization to significant regulatory fines under GDPR (up to 4% of global revenue) and the TDPSA.

**Internal Enforcement:**
*   Employees or volunteers who knowingly bypass the ROPA process (e.g., implementing "Shadow IT" involving personal data) may be subject to disciplinary action, up to and including termination of employment or volunteer assignment.
*   Inaccurate reporting during the Annual Certification may result in a formal performance review citation.

### 7. References
*   **GDPR Article 30:** Records of processing activities.
*   **Texas Data Privacy and Security Act (TDPSA):** Controller duties.
*   **Bylaws Article IX:** Policies & Data Protection.
*   **DP-POL-001:** Master Data Privacy Policy.
*   **GOV-STD-005:** Records Retention Schedule.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial release of ROPA Maintenance Procedure. |