### Right to Rectification Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | DP-PRC-007 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Data Protection Officer (DPO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized workflow for handling requests from Data Subjects to correct, update, or complete their Personal Data held by Study GRC Inc. This procedure ensures compliance with the General Data Protection Regulation (GDPR) Article 16 ("Right to Rectification") and maintains the integrity and accuracy of the Organization's records.

### 2. Scope
This procedure applies to all Personal Data processed by Study GRC Inc. in its capacity as a Data Controller.
*   **In Scope:** Active databases (CRM, HRIS, LMS), membership rolls, volunteer registries, and marketing lists.
*   **Exclusions:**
    *   Data contained in immutable system logs or audit trails where modification would compromise security integrity.
    *   Historical legal documents (e.g., signed contracts) where the document itself cannot be altered, though a supplementary note may be appended.
    *   Backups (until they are restored to a live environment).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Data Subject** | An identified or identifiable natural person (e.g., member, donor, employee, volunteer) whose personal data is processed by the Organization. |
| **Rectification** | The act of correcting inaccurate Personal Data. |
| **Incomplete Data** | Data that is factually correct but lacks necessary context or detail to be a true representation of the Data Subject. |
| **Supplementary Statement** | A written statement provided by the Data Subject to be attached to their record to complete incomplete data. |
| **System of Record** | The authoritative data source for a given data element (e.g., the HRIS is the system of record for employee addresses). |

### 4. Procedures

#### 4.1 Request Intake
4.1.1 **Submission Channels:** Data Subjects may submit a request for rectification via:
*   The dedicated Privacy Portal on the Study GRC website.
*   Email to `privacy@[studygrc.org]`.
*   Direct update via self-service portals (e.g., Member Profile Dashboard), which is the preferred method for contact details.

4.1.2 **Logging:** Upon receipt, the Privacy Team must log the request in the **Data Subject Access Request (DSAR) Register** (DP-REG-001) within 24 hours.

#### 4.2 Identity Verification
4.2.1 **Verification Standard:** Before disclosing or altering any data, the Privacy Team must verify the identity of the requester to prevent unauthorized account takeovers.
*   **Standard Request:** Verification via email confirmation from the address on file.
*   **Sensitive Request:** For sensitive data (e.g., financial info, medical data), the requester may be asked to provide additional proof of identity (e.g., government ID) via a secure upload channel.

#### 4.3 Assessment of Accuracy
4.3.1 **Review:** The Data Protection Officer (DPO) or designee must review the request to determine if the data in question is actually inaccurate or incomplete.
4.3.2 **Evidence:**
*   For objective facts (e.g., spelling of name, address change), the Organization generally accepts the Data Subject's assertion unless there is a compelling reason to doubt it.
*   For disputed facts (e.g., performance review scores, disciplinary records), the Data Subject must provide evidence supporting the claim that the data is factually incorrect, rather than simply an opinion they disagree with.
4.3.3 **Timeline:** The assessment must be completed without undue delay and no later than **30 calendar days** from receipt of the request.

#### 4.4 Execution of Rectification
4.4.1 **Updating Systems:** If the request is valid:
*   The System Administrator for the relevant **System of Record** must update the data.
*   If the data is "Incomplete" rather than "Inaccurate," the Administrator must append the **Supplementary Statement** provided by the Data Subject to the record.

4.4.2 **Downstream Propagation:** The Privacy Team must identify if this data has been replicated to other systems (e.g., from CRM to Marketing Automation) and ensure the correction is propagated to all secondary systems.

4.4.3 **Third-Party Notification (GDPR Art. 19):** If the inaccurate data was disclosed to third parties (e.g., payroll processors, insurance providers), the Privacy Team must notify those recipients of the rectification, unless this proves impossible or involves disproportionate effort.

#### 4.5 Rejection of Request
4.5.1 **Grounds for Rejection:** A request may be rejected if:
*   The data is accurate and the Organization has evidence to prove it.
*   The request is manifestly unfounded or excessive.
*   The request seeks to alter a legal record that must remain historically accurate (e.g., a past invoice cannot be changed, but a credit memo can be issued).

4.5.2 **Notification of Rejection:** If rejected, the DPO must inform the Data Subject in writing within 30 days, explaining:
*   The reasons for not taking action.
*   Their right to lodge a complaint with a supervisory authority.

#### 4.6 Completion and Closure
4.6.1 **Confirmation:** Once the data is updated, the Privacy Team must send a confirmation notice to the Data Subject.
4.6.2 **Record Keeping:** The DSAR Register must be updated to "Closed," retaining a record of the request, the verification method, and the action taken (but not the old inaccurate data itself).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Data Subject** | Provides accurate information and evidence to support claims of inaccuracy. |
| **Data Protection Officer (DPO)** | Oversees the rectification process, validates requests, and determines if a request should be rejected. |
| **Privacy Team** | Logs requests, performs identity verification, and communicates with the Data Subject. |
| **System Administrators** | Executes the technical updates in the IT systems (HRIS, CRM, LMS) upon instruction from the DPO. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in inaccurate records, leading to operational errors and violations of GDPR Article 16. Non-compliance by employees may result in disciplinary action, up to and including termination.

**Regulatory Note:** Failure to rectify data upon request can result in regulatory fines under GDPR of up to €20 million or 4% of global turnover.

### 7. References
*   **GDPR Article 16:** Right to Rectification.
*   **GDPR Article 12:** Transparent information, communication, and modalities for the exercise of the rights of the data subject.
*   **GDPR Article 19:** Notification obligation regarding rectification or erasure of personal data or restriction of processing.
*   **Bylaws of Study GRC Inc.:** Article IX (Policies & Data Protection).
*   **DP-POL-001:** Master Data Privacy Policy.
*   **DP-REG-001:** Data Subject Access Request (DSAR) Register.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial Draft created for GDPR compliance. |