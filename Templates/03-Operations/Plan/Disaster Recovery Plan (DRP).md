### Disaster Recovery Plan (DRP)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PLN-002 |
| **Document Type** | Plan |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Disaster Recovery Plan (DRP) is to establish a defined protocol for the restoration of Study GRC Inc.’s (the "Organization") Information Technology (IT) systems, applications, and data following a major disruption.

This plan ensures the Organization can recover its technical capabilities within defined timeframes to minimize impact on operations, member services, and compliance obligations. This plan aligns with **NIST SP 800-34 Rev. 1** (Contingency Planning Guide for Federal Information Systems) and supports the data protection mandates outlined in **Article IX** of the Organization’s Bylaws.

### 2. Scope
This plan applies to all critical information systems, cloud-based infrastructure, software-as-a-service (SaaS) platforms, and data repositories utilized by Study GRC Inc.

**Inclusions:**
*   Core Identity & Access Management systems (e.g., Google Workspace, Azure AD).
*   Public-facing platforms (Website, Learning Management System).
*   Financial and operational data repositories.
*   Source code repositories and intellectual property.

**Exclusions:**
*   **Physical Safety:** Physical emergency response is covered under the Emergency Action Plan (EAP).
*   **Business Continuity:** Non-technical operational continuity (e.g., leadership succession) is covered in the Business Continuity Plan (BCP), though this DRP supports the BCP.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Disaster** | An event that renders critical IT systems inoperable or inaccessible for a duration exceeding the Maximum Tolerable Downtime (MTD), requiring external intervention or backup restoration to resolve. |
| **RTO (Recovery Time Objective)** | The maximum targeted duration of time and a service level within which a business process must be restored after a disaster. |
| **RPO (Recovery Point Objective)** | The maximum targeted period in which data might be lost from an IT service due to a major incident (i.e., the frequency of backups). |
| **MTD (Maximum Tolerable Downtime)** | The maximum amount of time a system can be unavailable before the Organization suffers irreparable harm. |
| **Cloud Service Provider (CSP)** | Third-party vendors (e.g., AWS, Google, GitHub) hosting the Organization's infrastructure. |

### 4. Plan Structure and Procedures

This plan is structured into three phases in accordance with NIST SP 800-34: **Activation**, **Recovery**, and **Reconstitution**.

#### 4.1 Phase 1: Activation and Notification
This phase defines the criteria for declaring a disaster and the process for notifying the Disaster Recovery Team (DRT).

**4.1.1 Disaster Declaration Criteria**
The DRP may be activated if any of the following occur:
*   Total loss of access to the primary Learning Management System (LMS) or Website for > 4 hours.
*   Confirmed ransomware infection affecting > 25% of organizational data or critical financial records.
*   Permanent loss of data requiring restoration from "Cold Storage" or off-site backups.
*   Major outage of a primary CSP (e.g., Google Workspace, AWS) expected to last > 24 hours.

**4.1.2 Notification Procedure**
1.  **Detection:** Any employee or volunteer identifying a potential disaster must immediately notify the Help Desk or CISO via the designated emergency channel (e.g., Signal, secondary email).
2.  **Assessment:** The CISO (or designate) assesses the situation to determine if it meets Disaster Declaration Criteria.
3.  **Declaration:** The Executive Director (CEO), upon recommendation from the CISO, formally declares a disaster.
4.  **Alerting:** The CISO activates the Call Tree to notify the DRT and the Board of Directors.

#### 4.2 Phase 2: Recovery
This phase focuses on the restoration of temporary or permanent IT operations. As a remote-first organization, this primarily involves Cloud and SaaS restoration.

**4.2.1 System Prioritization (Tiers)**
Systems are recovered in the following order of priority:

| Tier | Description | RTO | RPO | Examples |
| :--- | :--- | :--- | :--- | :--- |
| **Tier 1** | **Critical Infrastructure** | 4 Hours | 1 Hour | Identity Provider (IdP), Email, DNS, MFA. |
| **Tier 2** | **Core Operations** | 24 Hours | 4 Hours | LMS, Website, Financial Systems, Source Code. |
| **Tier 3** | **Support Systems** | 72 Hours | 24 Hours | Analytics, Marketing Tools, Non-critical archives. |

**4.2.2 Data Restoration Procedure**
1.  **Isolate:** Ensure the compromised environment is isolated to prevent reinfection (if cyber-attack related).
2.  **Select Snapshot:** Identify the last known "clean" backup point based on the RPO.
3.  **Restore:**
    *   **SaaS Data:** Utilize provider-specific restoration tools (e.g., Google Vault, GitHub Rewind) or third-party backup connectors.
    *   **Infrastructure:** Re-deploy infrastructure using Infrastructure-as-Code (IaC) scripts from the secure repository.
4.  **Verify:** The CISO must verify data integrity before opening access to users.

**4.2.3 Alternative Processing (Workarounds)**
If the primary CSP is unavailable for an extended period:
*   **Communication:** Operations shift to the secondary communication platform (e.g., from Slack to Discord/Signal).
*   **File Access:** Critical documents are accessed via the offline "Emergency Drive" maintained by the Secretary and Treasurer.

#### 4.3 Phase 3: Reconstitution
This phase outlines the steps to return to normal operations and terminate the disaster state.

**4.3.1 Validation and Testing**
1.  **Functional Testing:** System owners must verify that restored applications are fully functional.
2.  **Security Audit:** The CISO must perform a vulnerability scan on restored systems to ensure no security gaps were introduced during recovery.
3.  **Data Synchronization:** Ensure any data generated during "Alternative Processing" is merged back into the primary system.

**4.3.2 Deactivation**
1.  The Executive Director formally declares the disaster "Resolved."
2.  Notifications are sent to all Members and Stakeholders regarding the restoration of services.
3.  **After-Action Report (AAR):** Within 14 days, the DRT must conduct a retrospective to document lessons learned and update this DRP.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Executive Director (CEO)** | Authority to declare a disaster; authorizes emergency spending; manages external stakeholder communication. |
| **Chief Information Security Officer (CISO)** | Serves as the Disaster Recovery Coordinator (DRC); manages technical recovery efforts; verifies data integrity. |
| **VP of Education & Training** | Validates restoration of LMS and curriculum content; communicates with learners/instructors. |
| **Chief Financial Officer (CFO)** | Validates restoration of financial data; tracks emergency expenditures for insurance/audit purposes. |
| **Board of Directors** | Provides oversight; approves policy changes resulting from the AAR; supports funding for recovery. |
| **All Staff/Volunteers** | Follow emergency communication protocols; assist with validation testing as requested. |

### 6. Compliance and Enforcement

**6.1 Testing and Maintenance**
Pursuant to NIST SP 800-34, this plan must be tested at least **annually**. Testing methods may include:
*   **Tabletop Exercises:** Discussion-based scenarios.
*   **Functional Drills:** Restoring a non-production environment from backups.

**6.2 Enforcement**
Failure to adhere to the procedures in this plan during a declared disaster, or failure to maintain the readiness of this plan (e.g., neglecting backup verifications), may result in disciplinary action up to and including termination of employment or volunteer assignment.

### 7. References
*   **NIST SP 800-34 Rev. 1:** Contingency Planning Guide for Federal Information Systems.
*   **Study GRC Bylaws:** Article VIII (Records) and Article IX (Data Protection).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-015:** Backup Policy and Procedures.
*   **IS-PLN-001:** Incident Response Plan (IRP).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Draft aligned with NIST 800-34 and Bylaws. |