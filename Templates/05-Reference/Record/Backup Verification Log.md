### Backup Verification Log

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-REG-001 |
| **Document Type** | Record / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-04-25 (Bi-Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Systems Administrator |
| **Classification** | Internal |

### 1. Purpose
The purpose of the **Backup Verification Log** is to provide an immutable, auditable record of data backup activities and their subsequent verification. This document serves as the primary evidence that Study GRC Inc. is adhering to its *Backup Policy and Procedures* and *Disaster Recovery Plan (DRP)*.

This log ensures compliance with **Bylaws Article VIII (Records, Transparency & Finance)** regarding the maintenance of correct and complete books and records, and supports the organization's ability to recover from ransomware, data corruption, or system failure.

### 2. Scope
This standard applies to all critical systems and data repositories managed by Study GRC Inc., including but not limited to:
*   **Financial Systems:** (e.g., QuickBooks Online, Expense Management).
*   **Donor & Member Databases:** (e.g., CRM, Membership Rolls).
*   **Educational Content Repositories:** (e.g., LMS, GitHub repositories).
*   **Operational Documents:** (e.g., Google Workspace/Microsoft 365 Shared Drives).

**Exclusions:** Transient data on local end-user devices is excluded, as all critical work product must be stored on sanctioned cloud platforms per the *Remote Work Policy*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Integrity Check** | An automated process (e.g., checksum verification) confirming the backup file is not corrupted. |
| **Restoration Test** | A manual or automated process where data is retrieved from the backup media and opened/executed to verify usability. |
| **RPO (Recovery Point Objective)** | The maximum acceptable amount of data loss measured in time (e.g., 24 hours). |
| **Immutable Backup** | A backup file that cannot be altered or deleted for a specific period, protecting against ransomware encryption. |
| **3-2-1 Rule** | Strategy requiring three copies of data, on two different media types, with one off-site (cloud). |

### 4. Logging Requirements and Procedures

#### 4.1 Frequency of Verification
While backup jobs may run daily via automation, the **verification** of these jobs must be logged according to the following schedule:
*   **Daily:** Automated review of job success/failure notifications.
*   **Weekly:** Manual entry into this log confirming the integrity of the previous week's backups.
*   **Monthly:** A random sample Restoration Test must be performed and recorded in this log.

#### 4.2 Log Entry Standards
Every entry in the Backup Verification Log must contain, at minimum, the data points defined in Section 5. Entries must be made within 24 hours of the verification activity.

#### 4.3 Handling Failures
If a backup job is recorded as "FAILED" or "CORRUPT" in this log:
1.  An Incident Ticket must be generated immediately.
2.  The Ticket ID must be referenced in the "Notes/Ticket Reference" column.
3.  A follow-up entry must be made once a successful ad-hoc backup is completed to resolve the gap.

#### 4.4 Record Retention
In accordance with the *Document Retention and Destruction Policy*, Backup Verification Logs must be retained for a minimum of **three (3) years** for audit purposes.

### 5. Backup Verification Log Schema
*Note: The actual log is maintained in the organization's secure ticketing system or a protected spreadsheet. The table below defines the mandatory schema for that record.*

| Date of Check | Time (CST) | System/Asset ID | Backup Type | Verification Method | Status | Restored File Sample (If Restore Test) | Auditor/Admin | Notes / Ticket Ref |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| [YYYY-MM-DD] | [HH:MM] | [e.g., FIN-QBO-01] | [Full / Incr / Diff] | [Log Review / Checksum / Full Restore] | [PASS / FAIL] | [Filename.ext] | [Username] | [Ticket #] |

**Example Entries:**

| Date | Time | System | Type | Method | Status | Sample | Admin | Notes |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 2023-10-01 | 09:00 | CRM-Prod | Incr | Log Review | PASS | N/A | j.doe | Auto-success email received. |
| 2023-10-01 | 09:15 | Website-DB | Full | Checksum | FAIL | N/A | j.doe | **INC-2039**: Checksum mismatch. |
| 2023-10-05 | 14:00 | Fin-Drive | Full | Restore | PASS | *2023_Budget.xlsx* | a.smith | Monthly random restore test. |

### 6. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **System Administrator** | Performs daily/weekly checks and enters data into the log. Initiates incident response for failures. |
| **CISO** | Reviews the Backup Verification Log monthly to ensure consistency and adherence to the 3-2-1 rule. Signs off on quarterly audits. |
| **Audit Committee** | May request access to these logs during the annual financial audit to verify internal controls over financial reporting. |

### 7. Compliance and Enforcement
Failure to maintain accurate backup logs constitutes a violation of the organization's *Internal Controls Framework*.
*   **Falsification of Logs:** Intentionally marking a failed or unchecked backup as "PASS" is considered gross misconduct and may result in immediate termination of employment or contract.
*   **Negligence:** Repeated failure to update the log will result in progressive disciplinary action.

### 8. References
*   **Bylaws of Study GRC Inc.** (Article VIII - Records, Transparency & Finance)
*   **NIST SP 800-34 Rev. 1** (Contingency Planning Guide for Federal Information Systems)
*   **IS-POL-010:** Master Information Security Policy
*   **IS-POL-055:** Backup Policy and Procedures
*   **IS-PLAN-002:** Disaster Recovery Plan (DRP)

### 9. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | CISO | Initial release of log standard and schema. |