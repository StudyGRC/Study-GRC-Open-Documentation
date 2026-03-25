### Right to Erasure (Forgotten) Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | PRIV-PRC-004 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to operationalize the "Right to Erasure" (also known as the "Right to be Forgotten") as mandated by Article 17 of the General Data Protection Regulation (GDPR) and aligned with the Texas Data Privacy and Security Act (TDPSA). This document defines the specific steps Study GRC Inc. (the "Organization") must take to securely and permanently remove Personal Data upon a verified request from a Data Subject, ensuring compliance while preserving records required by law for 501(c)(3) auditability and youth protection.

### 2. Scope
This procedure applies to all Personal Data processed by the Organization, regardless of format (digital or physical).

*   **In Scope:**
    *   Member records (Supporting, Community, Honorary).
    *   Learner data within the Learning Management System (LMS).
    *   Volunteer records.
    *   Donor records (subject to retention overrides).
    *   Marketing and newsletter lists.
*   **Exclusions:**
    *   Data required to be retained by US Federal or State law (e.g., IRS tax records, employment records).
    *   Data related to active legal claims or investigations.
    *   Records of individuals permanently banned for violations of the *Child and Youth Safeguarding Policy* (retained for safety purposes under "Legitimate Interest").

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Data Subject** | The individual to whom the Personal Data relates (e.g., member, donor, student). |
| **Erasure** | The irreversible destruction or anonymization of data so that it can no longer be attributed to a specific data subject. |
| **Legal Hold** | A process used to preserve all forms of relevant information when litigation is reasonably anticipated. |
| **Put Beyond Use** | A state where data in backups is not immediately overwritten but is technically restricted from processing until the backup cycle expires. |
| **Controller** | Study GRC Inc., the entity determining the purposes and means of processing personal data. |

### 4. Procedures

#### 4.1 Intake and Identity Verification
**4.1.1** All requests for erasure must be submitted via the designated Privacy Portal or emailed to `privacy@studygrc.org`.
**4.1.2** Upon receipt, the Privacy Team must log the request in the *Data Subject Access Request (DSAR) Register* (PRIV-REG-001) within 24 hours.
**4.1.3** The Privacy Team must verify the identity of the requester.
*   **Standard Verification:** Email confirmation via the address on file.
*   **Enhanced Verification:** If the request involves sensitive data or historical donor records, the Organization may request additional proof of ID (e.g., government ID redacted to show only name/address).
**4.1.4** If the requester is a minor (under 18), the request must be verified against the *Verifiable Parental Consent* records, unless the minor is exercising their specific right to erase data collected while they were a child (GDPR Art. 17(1)(f)).

#### 4.2 Request Evaluation and Exemption Analysis
**4.2.1** The CISO or designated Privacy Officer must review the request against GDPR Article 17 grounds. Erasure is required if:
*   The data is no longer necessary for the original purpose.
*   The Data Subject withdraws consent (and no other legal ground exists).
*   The data was unlawfully processed.
**4.2.2** **Mandatory Retention Check:** Before approving erasure, the Officer must check for overriding retention obligations:
*   **Financial/Donor Records:** Per **Bylaws Article VIII (Records, Transparency & Finance)** and IRS regulations, donor contribution records must be retained for seven (7) years. These cannot be erased but must be minimized (restricted).
*   **Youth Protection:** If the individual has been flagged for safety violations, their basic identity data must be retained on the *Internal Exclusion List* to prevent re-entry, citing "Public Interest" and "Legitimate Interest" for child safeguarding.
**4.2.3** If an exemption applies, the request is **Denied in Part**. The Data Subject must be informed which data will be erased and which must be kept, citing the specific legal basis.

#### 4.3 Technical Execution of Erasure
If the request is approved, the following steps must be executed within 30 days of the initial request.

**4.3.1 Primary Systems (Live Data)**
*   **CRM/Membership Database:** Execute the "Hard Delete" or "Anonymize" function. Anonymization is preferred if it preserves aggregate statistical data (e.g., "Unknown User" completed "Course 101").
*   **LMS (Learning Management System):** Remove learner profile and progress data. Ensure forum posts are anonymized or deleted based on the platform's capability.
*   **Email Marketing:** Remove the email address from all active subscriber lists and suppression lists (unless the user requests to be added to a "Do Not Contact" list, which requires retaining the email).
*   **Collaboration Tools (Slack/Discord):** Deactivate the account and scrub PII from profile fields. Note: Public messages may remain unless specifically requested for removal, provided they do not contain PII.

**4.3.2 Third-Party Processors**
*   The Privacy Officer must send a *Notification of Erasure* to all downstream processors (e.g., payment gateways, cloud storage providers) identified in the *Records of Processing Activities (ROPA)*.
*   Confirmation of receipt from vendors must be logged.

**4.3.3 Backups and Archives**
*   It is recognized that immediate deletion from immutable backups is technically impossible.
*   **Procedure:** The Data Subject's ID is added to a "Suppression List."
*   If a backup is ever restored, the Suppression List must be run immediately to re-erase the data before the system goes live.
*   Data in backups is considered "Put Beyond Use" until the retention cycle overwrites the tape/snapshot (typically 90 days per *IT-STD-015 Backup Policy*).

#### 4.4 Notification and Closure
**4.4.1** Once technical execution is complete, the Privacy Officer must draft a *Certificate of Erasure*.
**4.4.2** Send the final notification to the Data Subject confirming:
*   The date the erasure was completed.
*   Any data retained due to legal exemptions (e.g., "We have deleted your profile, but retained donation records #12345 as required by IRS tax law").
**4.4.3** Close the ticket in the DSAR Register.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Data Subject** | Submits a clear request for erasure and provides necessary identity verification. |
| **Privacy Officer / CISO** | Evaluates requests, determines exemptions, coordinates execution, and communicates with the Data Subject. |
| **System Administrators** | Executes technical deletion scripts or manual removal in IT systems (LMS, CRM, IDP). |
| **Executive Director** | Final escalation point for disputes regarding retention vs. erasure (e.g., donor disputes). |
| **Third-Party Vendors** | Processors must comply with erasure instructions sent by Study GRC Inc. within their contractual timelines. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in severe regulatory penalties under GDPR (up to 4% of global turnover) and reputational damage.
*   **Internal:** Employees who intentionally delay or obstruct a valid erasure request are subject to disciplinary action, up to and including termination.
*   **External:** Failure to execute erasure within the statutory timeframe (30 days, extendable by 60 days for complexity) constitutes a compliance breach and must be reported to the Board of Directors.

### 7. References
*   **GDPR Article 17:** Right to Erasure ('Right to be Forgotten').
*   **Bylaws Article VIII:** Records, Transparency & Finance.
*   **PRIV-POL-001:** Master Data Privacy Policy.
*   **IT-STD-015:** Backup and Retention Standard.
*   **IRS Publication 557:** Tax-Exempt Status for Your Organization (Record Retention).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial release aligned with GDPR Art 17 and Bylaws. |