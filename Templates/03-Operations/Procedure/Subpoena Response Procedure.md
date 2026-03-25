### Subpoena Response Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | LGL-PRC-003 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2025-10-27 (Bi-Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Executive Director / Legal Counsel |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized, legally compliant, and privacy-focused protocol for Study GRC Inc. (the "Organization") when responding to subpoenas, court orders, search warrants, and other legal demands for data. This procedure ensures the Organization fulfills its legal obligations under Texas and Federal law while vigorously protecting the privacy rights of its members, particularly regarding the Organization's commitment to minimizing data exposure as outlined in the Privacy Policy and Bylaws.

### 2. Scope
This procedure applies to all Employees, Directors, Officers, Volunteers, and Contractors of Study GRC Inc. It covers the receipt and processing of any legal request for:
*   Member or donor data (PII).
*   Internal communications (Slack, Email, Discord).
*   Financial records.
*   Proprietary educational content or code.

**Exclusions:** This procedure does not cover routine regulatory filings (e.g., IRS Form 990) or voluntary data sharing explicitly authorized by the Data Subject.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Subpoena** | A writ ordering a person to attend a court or produce documents. (e.g., *Subpoena Duces Tecum*). |
| **Preservation Order** | A legal instruction to retain data that might otherwise be deleted under standard retention schedules. |
| **Registered Agent** | The entity designated in Bylaws Article I, Section 1.2 to receive service of process in Texas. |
| **Gag Order** | A court order prohibiting the Organization from notifying the target of the subpoena that their data has been requested. |
| **Quash** | A legal motion to reject or void a subpoena or court order. |
| **ECPA** | Electronic Communications Privacy Act (18 U.S.C. § 2510 et seq.), governing the disclosure of electronic communications. |

### 4. Procedures

#### 4.1 Receipt and Intake
**4.1.1 Service of Process**
Legal demands are typically served via the Organization’s Registered Agent (per Bylaws Section 1.2) or via certified mail to the principal office.
*   **Action:** If any staff member or volunteer receives a subpoena directly (e.g., via email or in person), they must **immediately** forward the document to the Executive Director and the Board President.
*   **Prohibition:** Do not reply to the sender, acknowledge receipt, or provide any data until authorized by Legal Counsel.

**4.1.2 Validation**
The Executive Director, in consultation with Legal Counsel, must verify:
1.  **Authenticity:** Is the document issued by a valid court or agency?
2.  **Jurisdiction:** Does the issuing court have jurisdiction over a Texas Non-Profit Corporation? (e.g., Out-of-state civil subpoenas often require "domestication" in Texas courts to be enforceable).
3.  **Service:** Was it served correctly according to the Texas Rules of Civil Procedure?

#### 4.2 Preservation (Legal Hold)
**4.2.1 Immediate Freeze**
Upon receipt of a valid (or potentially valid) legal demand, the Executive Director must issue a **Legal Hold Notice** to the Chief Information Security Officer (CISO) and relevant data custodians.
*   **Action:** Suspend all auto-deletion or rotation policies for the specific data requested.
*   **Scope:** This includes backups, logs, and active databases.
*   **Silence:** Do not discuss the existence of the subpoena on public channels (Slack/Discord) to avoid "tipping off" unrelated parties or violating potential seal orders.

#### 4.3 Member Notification Policy
**4.3.1 Default Stance: Transparency**
Consistent with the Organization's mission to empower practitioners, Study GRC Inc. will notify the affected member(s) regarding the subpoena **before** disclosing their information, unless:
1.  Prohibited by a specific statute or court order (e.g., a sealed warrant or Gag Order).
2.  There is a clear and imminent danger of death or serious physical injury (Emergency Disclosure).

**4.3.2 Notification Process**
If notification is legally creating, the Executive Director will send a formal notice to the member's email address on file, stating:
*   A legal demand for their information has been received.
*   The Organization intends to comply within [Number] days (typically 10 days) unless the member provides proof that they have filed a Motion to Quash in the relevant court.

#### 4.4 Legal Review and Objections
**4.4.1 Grounds for Objection**
Legal Counsel shall review the demand to determine if the Organization should file objections or a Motion to Quash based on:
*   **Overbreadth:** The request asks for "all data" rather than specific, relevant information.
*   **Undue Burden:** Compliance would be technically impossible or financially crippling.
*   **Privacy Rights:** The request violates First Amendment rights (anonymous speech) or privacy laws (GDPR/CCPA).
*   **Privilege:** The data is protected by attorney-client privilege.

**4.4.2 Youth Data (COPPA)**
If the data pertains to a known minor (under 18), the Organization must exercise heightened scrutiny.
*   **Action:** Ensure strict compliance with the Children's Online Privacy Protection Act (COPPA). Notification must be directed to the parent/guardian on file.

#### 4.5 Data Minimization and Production
**4.5.1 Strict Scope**
If the Organization is compelled to produce data, it will produce **only** the specific data points requested and nothing more.
*   *Example:* If a subpoena asks for "Login Logs," do not provide "Chat History."

**4.5.2 Secure Transfer**
*   **Encryption:** Data must never be sent via plain text email.
*   **Method:** Use a secure, encrypted file transfer method (e.g., password-protected zip file via secure link, with the password sent via a separate channel).
*   **Logging:** The CISO must log exactly what data was produced, to whom, and when.

#### 4.6 Cost Reimbursement
**4.6.1 Fee Recovery**
To the extent permitted by law (e.g., ECPA or Texas Rules of Civil Procedure), the Organization shall invoice the requesting party for the reasonable costs incurred in searching for, assembling, and reproducing the requested records.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Recipient (Any Staff/Volunteer)** | Immediately forwards legal documents to Leadership; does not respond directly. |
| **Executive Director** | Primary point of contact; authorizes Legal Hold; coordinates with Counsel. |
| **Legal Counsel** | Reviews validity; drafts objections/Motions to Quash; advises on notification. |
| **CISO** | Executes technical preservation (Legal Hold); extracts data securely; ensures data minimization. |
| **Board of Directors** | Informed of high-risk subpoenas (e.g., those involving government investigations or significant financial liability). |

### 6. Compliance and Enforcement
**6.1 Unauthorized Disclosure**
Any employee or volunteer who discloses member data to law enforcement or third parties without following this procedure (i.e., without a valid warrant/subpoena and Executive Director approval) is subject to immediate termination and potential legal action for breach of the Organization's Confidentiality Policy (Bylaws Article IX, Section 9.2).

**6.2 Failure to Preserve**
Failure to adhere to a Legal Hold notice (destroying evidence) may result in criminal liability for the individual and the Organization (Obstruction of Justice).

### 7. References
*   **Study GRC Inc. Bylaws:** Article I, Section 1.2 (Registered Agent); Article IX (Confidentiality).
*   **Privacy Policy:** Section regarding "Disclosure to Law Enforcement."
*   **Document Retention and Destruction Policy:** (Suspension protocols).
*   **Texas Business Organizations Code:** Chapter 22.
*   **Electronic Communications Privacy Act (ECPA):** 18 U.S.C. § 2701-2712.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial Release |