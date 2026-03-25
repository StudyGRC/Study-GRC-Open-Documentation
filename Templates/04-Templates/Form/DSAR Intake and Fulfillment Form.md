### DSAR Intake and Fulfillment Form

| Document Control | |
| :--- | :--- |
| **Document ID** | GOV-FRM-005 |
| **Document Type** | Form / Standard Operating Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Board of Directors / Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | **Internal Use** (Completed Forms are **Confidential**) |

### 1. Purpose
The purpose of this document is to standardize the intake, verification, processing, and fulfillment of **Data Subject Access Requests (DSARs)**. This form ensures Study GRC Inc. complies with the **Texas Data Privacy and Security Act (TDPSA)**, the **General Data Protection Regulation (GDPR)**, and **COPPA** regarding an individual's right to access, correct, delete, or port their personal data.

This document serves as both the **template for the public-facing request form** and the **internal log** used by the Privacy Team to track compliance with statutory response timelines (typically 30 to 45 days).

### 2. Scope
*   **Applies to:** All personal data collected, processed, or stored by Study GRC Inc., including data regarding members, donors, volunteers, employees, and program participants (including minors).
*   **Users:** This form is to be used by Data Subjects (external) to initiate requests and by the Privacy Officer/CISO (internal) to document fulfillment.
*   **Exclusions:** This form does not apply to law enforcement requests (refer to *Law Enforcement Data Request Procedure*) or internal discovery for litigation (refer to *Litigation Hold Procedure*).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **DSAR** | Data Subject Access Request. A written request from an individual asking how their personal data is being processed, or requesting action on that data. |
| **Data Subject** | The individual to whom the personal data relates (e.g., the member, donor, or student). |
| **Verifiable Request** | A request where the organization has successfully confirmed that the requester is the actual owner of the data or an authorized agent. |
| **Authorized Agent** | A person or entity registered with the Secretary of State that a consumer has authorized to act on their behalf. |
| **TDPSA** | Texas Data Privacy and Security Act. |

### 4. Form Specifications (Intake & Fulfillment)

This section outlines the mandatory data fields required for the intake mechanism (e.g., web form or email template) and the internal processing log.

#### 4.1 Part A: Requester Intake (Public Facing)
*To be completed by the Data Subject or Authorized Agent.*

**A.1 Requester Information**
*   **Full Name:** ________________________________________________________
*   **Email Address (Primary):** ____________________________________________
    *   *Note: This email must match our records to facilitate verification.*
*   **Relationship to Study GRC:**
    *   [ ] Member (Voting/Community)
    *   [ ] Donor
    *   [ ] Volunteer/Employee
    *   [ ] Parent/Guardian of a Minor Participant
    *   [ ] Other: __________________

**A.2 Request Type (Check all that apply)**
*   **[ ] Right to Know / Access:** Request a copy of specific personal data we hold about you.
*   **[ ] Right to Delete (Erasure):** Request deletion of your personal data (subject to retention laws).
*   **[ ] Right to Correct:** Request correction of inaccurate information.
*   **[ ] Right to Portability:** Request data in a machine-readable format.
*   **[ ] Right to Opt-Out:** Opt-out of targeted advertising or sale of data.

**A.3 Request Details**
*   **Date Range of Data:** ________________ to ________________
*   **Specific Context (Optional):** (e.g., "I am looking for my donation history" or "I want to delete my Slack account data.")
    *   _________________________________________________________________________

**A.4 Requests Regarding Minors (If applicable)**
*   *Pursuant to the Child and Youth Safeguarding Policy and COPPA:*
*   **Is this request regarding a person under the age of 18?** [ ] Yes [ ] No
*   **Name of Minor:** ____________________________________________________
*   **Parent/Guardian Verification:** I attest strictly under penalty of perjury that I am the legal guardian of the minor listed above.
    *   **Signature:** __________________________________ **Date:** ____________

**A.5 Authorized Agent (If applicable)**
*   If submitting on behalf of another, attach **Proof of Authorization** (Power of Attorney or written permission).

---

#### 4.2 Part B: Internal Processing Log (Internal Use Only)
*To be completed by the Privacy Officer or CISO.*

**B.1 Intake & Verification**
*   **DSAR Case ID:** `DSAR-[YYYY]-[###]`
*   **Date Received:** [YYYY-MM-DD]
*   **Statutory Deadline:** [YYYY-MM-DD] (45 Days for TDPSA / 30 Days for GDPR)
*   **Identity Verification Method:**
    *   [ ] Email Verification Loop (Standard)
    *   [ ] Government ID Check (High Sensitivity Data)
    *   [ ] Parent/Guardian Verification (COPPA/Youth)
    *   [ ] Rejected (Unable to Verify)

**B.2 Data Search & Collation**
*   **Systems Queried:**
    *   [ ] CRM / Membership Database
    *   [ ] Financial/Donation System (Stripe/QuickBooks)
    *   [ ] Email Marketing (Mailchimp/HubSpot)
    *   [ ] Collaboration Tools (Slack/Discord/Google Workspace)
    *   [ ] HR/Payroll Systems
*   **Data Found?** [ ] Yes [ ] No

**B.3 Review & Redaction**
*   **Third-Party Data Removed?** [ ] Yes [ ] N/A (Ensuring no other person's data is included).
*   **Confidential Business Info Redacted?** [ ] Yes [ ] N/A
*   **Legal Hold Check:** Is this data subject under a Legal Hold?
    *   [ ] Yes (STOP: Do not delete data. Consult Legal Counsel).
    *   [ ] No (Proceed).

**B.4 Disposition & Response**
*   **Action Taken:**
    *   [ ] Request Fulfilled (Data Sent / Deleted).
    *   [ ] Request Denied (See B.5).
    *   [ ] Extension Requested (+45 days).
*   **Date Response Sent:** [YYYY-MM-DD]
*   **Transmission Method:** [ ] Secure Portal [ ] Encrypted Email

**B.5 Exception/Denial Rationale (If applicable)**
*   [ ] Unverifiable Identity
*   [ ] Manifestly Unfounded or Excessive (GDPR Art. 12)
*   [ ] Conflict with Record Retention Laws (e.g., IRS 7-year requirement)
*   [ ] Data is De-identified/Anonymized
*   **Notes:** __________________________________________________________________

**B.6 Approval**
*   **Processed By:** __________________________ (Name/Title)
*   **Final Approval:** __________________________ (CISO/Privacy Officer)

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Data Subject** | Provide accurate information and respond to verification requests (e.g., clicking a confirmation email) within 7 days. |
| **Privacy Officer / CISO** | Oversee the DSAR inbox, verify identities, coordinate with system owners to retrieve data, and approve final redactions. |
| **System Administrators** | Execute technical searches and deletions (e.g., "Run SQL query for User ID X") upon instruction from the Privacy Officer. |
| **Legal Counsel** | Review denials of requests or requests involving complex legal holds or minors. |

### 6. Compliance and Enforcement
Failure to process a DSAR within the statutory timeframe (45 days under TDPSA, 30 days under GDPR) constitutes a regulatory violation that may result in fines against the Organization.

Internal staff who willfully ignore, delete, or tamper with data subject to an active DSAR or Legal Hold will face disciplinary action, up to and including termination, in accordance with the **Sanctions Policy**.

### 7. References
*   **Bylaws Article IX (Policies & Data Protection)**
*   **GOV-POL-030:** Master Data Privacy Policy
*   **GOV-PRC-010:** Data Subject Access Request (DSAR) Procedure
*   **Texas Business & Commerce Code § 541 (TDPSA)**
*   **GDPR Articles 15-22** (Rights of the Data Subject)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Legal Officer | Initial Release |