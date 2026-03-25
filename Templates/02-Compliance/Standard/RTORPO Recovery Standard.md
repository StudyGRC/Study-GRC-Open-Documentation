### RTO/RPO Recovery Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-058 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this standard is to define the mandatory **Recovery Time Objectives (RTO)** and **Recovery Point Objectives (RPO)** for all information systems, applications, and data repositories managed by Study GRC Inc.

This standard ensures that in the event of a disruption (e.g., cyberattack, system failure, or natural disaster), the Organization can restore critical operations within a timeframe that minimizes harm to our community-driven ecosystem, protects our 501(c)(3) status, and maintains compliance with federal grant requirements (2 CFR 200) and Texas Business Organizations Code.

### 2. Scope
This standard applies to:
*   All technological assets, software, and cloud-based services (SaaS/IaaS/PaaS) utilized by Study GRC Inc.
*   All data classified as Confidential or Restricted under the *Data Classification Standard*.
*   All employees, contractors, and volunteers responsible for system architecture, administration, or data management.

**Exclusions:**
*   Personal devices (BYOD) not holding unique organizational data.
*   Third-party platforms where Study GRC Inc. has no administrative control over data retention (e.g., public social media feeds), though content backup is encouraged.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Recovery Time Objective (RTO)** | The maximum acceptable length of time that a computer, system, network, or application can be down after a failure or disaster occurs. (i.e., "How long can we be offline?") |
| **Recovery Point Objective (RPO)** | The maximum acceptable amount of data loss measured in time. It determines the frequency of backups. (i.e., "How much data can we afford to lose?") |
| **Maximum Tolerable Period of Disruption (MTPD)** | The duration after which the organization's viability will be continuously compromised if a product or service cannot be resumed. |
| **Mission Critical (Tier 1)** | Systems essential for the immediate survival of the organization, financial integrity, or safety of youth participants. |
| **Business Important (Tier 2)** | Systems required for day-to-day operations where a short delay is manageable but inconvenient. |
| **Non-Essential (Tier 3)** | Systems used for archival, testing, or non-urgent tasks. |

### 4. Standards

#### 4.1 System Criticality Tiers
All systems must be categorized into one of the following tiers. The CISO, in consultation with the Executive Director, holds the final authority on tier designation.

| Tier | Classification | Description | Examples |
| :--- | :--- | :--- | :--- |
| **Tier 1** | **Mission Critical** | Failure causes immediate legal liability, financial loss, or safety risks. | Financial Systems (QuickBooks), Donor Database, Voting System (during elections), Youth Protection Data. |
| **Tier 2** | **Business Important** | Failure impedes operations but workarounds exist for a short duration. | Learning Management System (LMS), Email, Website (Content), Collaboration Tools (Slack/Teams). |
| **Tier 3** | **General / Support** | Failure causes minor inconvenience. | Archives, Test Environments, Marketing Analytics, Deprecated Systems. |

#### 4.2 Mandatory RTO and RPO Metrics
System Owners must architect their solutions (including backup strategies and high-availability configurations) to meet or exceed the following metrics:

| Tier | RTO (Max Downtime) | RPO (Max Data Loss) | Backup Frequency Requirement |
| :--- | :--- | :--- | :--- |
| **Tier 1** | **8 Hours** | **1 Hour** | Continuous Replication or Hourly Snapshots |
| **Tier 2** | **24 Hours** | **24 Hours** | Daily Backups |
| **Tier 3** | **72 Hours** | **Last Successful Backup** | Weekly Backups |

#### 4.3 Election Period Exception
Pursuant to **Bylaws Article II (Membership)**, the integrity of the voting process is paramount. During the active "Electronic Voting Window" (7 days post-Annual Meeting) and the preceding nomination period:
*   The **Electronic Voting System** is elevated to **Tier 1 Criticality**.
*   **RTO** is reduced to **4 Hours**.
*   **RPO** is reduced to **Zero (Real-time consistency)** to prevent disenfranchisement of Voting Members.

#### 4.4 Backup and Redundancy Requirements
To ensure RPO targets are met:
1.  **Redundancy:** Tier 1 systems must utilize geographically redundant storage (e.g., AWS S3 Cross-Region Replication) to protect against regional outages.
2.  **Immutability:** Backups for Tier 1 and Tier 2 systems must be immutable (Write Once, Read Many) for at least 30 days to protect against ransomware encryption.
3.  **Independence:** Backups must be stored on a separate infrastructure or account from the production environment (Segregation of Duties).

#### 4.5 Validation and Testing
Establishing a standard is insufficient without verification.
1.  **Annual Testing:** A full restoration test must be conducted annually for all Tier 1 systems to verify that actual recovery times meet the defined RTO.
2.  **Evidence:** Logs of successful backup completion and restoration tests must be retained for audit purposes in accordance with the *Document Retention and Destruction Policy*.
3.  **Failure to Meet Standard:** If a test reveals that a system cannot meet its RTO/RPO, a Corrective Action Plan (CAP) must be filed with the CISO within 5 business days.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this standard; approves Tier classifications; reviews annual restoration test results. |
| **System Owners / Administrators** | Configure systems to meet RTO/RPO requirements; ensure backups are running; perform restoration tests. |
| **Executive Director** | Accepts the residual risk for any system formally exempted from this standard; authorizes budget for necessary backup infrastructure. |
| **Audit & Risk Committee** | Reviews aggregate compliance with this standard as part of the annual risk assessment. |

### 6. Compliance and Enforcement
Failure to comply with this standard puts the Organization at existential risk.
*   **System Non-Compliance:** Systems found to be non-compliant with their assigned Tier metrics may be taken offline until remediation is complete.
*   **Personnel:** Failure to configure backups or falsification of restoration testing results may result in disciplinary action, up to and including termination of employment or volunteer assignment.

### 7. References
*   **NIST SP 800-34 Rev. 1:** Contingency Planning Guide for Federal Information Systems.
*   **ISO 22301:** Security and resilience — Business continuity management systems.
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-STD-028:** Data Classification Standard.
*   **IS-PLN-001:** Business Continuity Plan (BCP).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Compliance Architect | Initial Release aligned with Bylaws and NIST frameworks. |