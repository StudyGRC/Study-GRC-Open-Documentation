### Backup Testing and Restoration Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-055 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Systems Administrator |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to mandate and standardize the validation of Study GRC Inc.'s data backup capabilities. Backups are only effective if they can be successfully restored. This procedure ensures that the Organization can recover from data loss events—including ransomware attacks, accidental deletion, or system failures—within established Recovery Time Objectives (RTO) and Recovery Point Objectives (RPO), thereby satisfying internal control requirements under 2 CFR 200 and NIST Cybersecurity Framework (Recover Function).

### 2. Scope
This procedure applies to all critical data repositories and systems managed by Study GRC Inc., including but not limited to:
*   **Cloud Infrastructure:** Production environments (e.g., AWS, Azure).
*   **SaaS Applications:** Google Workspace, Microsoft 365, Financial Systems (e.g., QuickBooks Online), and Donor Management Systems.
*   **Code Repositories:** GitHub/GitLab (Source code and documentation).
*   **Youth Protection Data:** Any databases containing sensitive information regarding minors.

**Exclusions:** Transient data stored on local employee devices that has not been synced to sanctioned cloud storage is excluded, as local storage is not a designated backup target per the *Remote Work Policy*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **RTO (Recovery Time Objective)** | The maximum acceptable length of time that a computer, system, network, or application can be down after a failure or disaster occurs. |
| **RPO (Recovery Point Objective)** | The maximum acceptable amount of data loss measured in time (e.g., 1 hour of data loss). |
| **Sandbox Environment** | An isolated computing environment used for testing that does not impact the live production network or data. |
| **Integrity Check** | A process (often using checksums) to verify that restored data is identical to the original source data and has not been corrupted. |
| **Tabletop Exercise** | A discussion-based session where team members meet in an informal, classroom setting to discuss their roles during an emergency and their responses to a specific emergency situation. |

### 4. Procedures

#### 4.1 Testing Schedule and Frequency
Restoration tests must be performed according to the criticality of the data classification:

1.  **Mission Critical (Financial, Youth Data, Identity Services):** Quarterly full restoration tests.
2.  **Business Operational (Email, Code Repositories):** Semi-annual sampling tests.
3.  **Archival/Compliance Data:** Annual spot-check.

#### 4.2 Test Selection and Planning
Prior to initiating a test, the IT Systems Administrator must:
1.  **Select the Scenario:** Choose a specific scenario (e.g., "Single file deletion," "Database corruption," "Full ransomware encryption").
2.  **Select the Target:** Identify specific files, databases, or virtual machines to restore. To ensure validity, the target should be selected randomly rather than using the same test file repeatedly.
3.  **Define Success Criteria:** Confirm the RTO and RPO for the selected target (e.g., "Must be restored within 4 hours with no more than 1 hour of data loss").

#### 4.3 Execution of Restoration (Technical Steps)
**WARNING:** Never restore test data over live production data. All testing must occur in a designated Sandbox Environment or to a non-production file path.

**4.3.1 File-Level Restoration (Granular)**
1.  Log in to the backup management console.
2.  Locate the specific file or folder version from a backup point at least 24 hours old.
3.  Initiate a "Restore to New Location" command.
4.  Download/Access the restored file.
5.  **Validation:** Open the file to ensure it is readable and verify the "Last Modified" timestamp matches the backup point.

**4.3.2 Database/Application Restoration**
1.  Provision a Sandbox instance of the database server or application.
2.  Retrieve the encrypted backup volume or SQL dump.
3.  Import the data into the Sandbox instance.
4.  **Validation:** Run a `COUNT(*)` query on key tables to verify record counts match the source system at the time of backup. Perform a checksum verification if available.

**4.3.3 Full System/Disaster Recovery (DR) Simulation**
1.  Once annually, the CISO must coordinate a full DR simulation.
2.  Simulate a total loss of the primary cloud region or service.
3.  Trigger the failover or restoration process to the secondary region/provider.
4.  **Validation:** Verify that the application loads, users can authenticate, and data is accessible in the secondary environment.

#### 4.4 Data Integrity and Security Verification
During the restoration test, the following security checks must be performed:
1.  **Decryption:** Verify that encrypted backups can be successfully decrypted using the stored keys.
2.  **Access Control:** Verify that the restored data retains the appropriate Access Control Lists (ACLs) (e.g., ensuring Youth Data is not accessible to unauthorized staff after restoration).
3.  **Malware Scan:** Scan the restored data in the Sandbox environment to ensure the backup itself was not infected (crucial for ransomware loops).

#### 4.5 Documentation and Reporting (The Validation Log)
Every test must be documented in the **Backup Testing Register**. The entry must include:
1.  Date and Time of Test.
2.  Tester Name.
3.  System/Data Tested.
4.  Time to Restore (Actual vs. RTO).
5.  Data Point Restored (Actual vs. RPO).
6.  Pass/Fail Status.
7.  **Sign-off:** Signature (digital) of the CISO or designated reviewer.

If a test fails, a **Corrective Action Plan (CAP)** ticket must be opened immediately, and a re-test must be scheduled within 7 days of the fix.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Approves the testing schedule; reviews validation logs; declares pass/fail for annual DR simulations. |
| **IT Systems Administrator** | Executes the technical restoration procedures; maintains the Sandbox environment; documents results in the Backup Testing Register. |
| **Data Owners (e.g., CFO, VP Education)** | Verifies the accuracy of restored data (e.g., confirming that the restored financial report matches the general ledger). |
| **Audit Committee** | Reviews the Backup Testing Register annually to ensure compliance with 2 CFR 200 internal control standards. |

### 6. Compliance and Enforcement
Failure to adhere to this procedure compromises the Organization's ability to recover from disasters and violates federal grant compliance requirements regarding internal controls.

*   **Non-Compliance:** Employees found falsifying testing logs or neglecting scheduled tests may be subject to disciplinary action, up to and including termination.
*   **Audit Evidence:** The Backup Testing Register serves as primary evidence for external audits (Single Audit) and cyber liability insurance renewals.

### 7. References
*   **NIST Cybersecurity Framework (CSF) 2.0:** Function: RECOVER (RC); Category: RC.RP (Recovery Planning).
*   **2 CFR 200.303:** Internal Controls.
*   **IS-POL-020:** Master Information Security Policy.
*   **IS-POL-054:** Backup Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial release of Backup Testing/Restoration Procedure. |