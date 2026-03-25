### Change Control and Management Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-072 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-26 |
| **Next Review Date** | 2024-10-26 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized method for the efficient and prompt handling of all changes to Study GRC Inc.'s controlled IT and operational environments. This procedure aligns with **ITIL v4** best practices to minimize the impact of change-related incidents, improve day-to-day operations, and ensure that all changes are recorded, evaluated, authorized, prioritized, planned, tested, implemented, documented, and reviewed in a controlled manner.

This procedure supports the Organization's obligation to maintain "correct and complete books and records" as mandated by **Article VIII, Section 8.1 of the Bylaws**.

### 2. Scope
This procedure applies to all "Configuration Items" (CIs) within the Organization's production environment.
*   **In Scope:**
    *   Production servers, databases, and cloud infrastructure (AWS/Azure/GCP).
    *   Core applications (LMS, Financial Systems, Website).
    *   Network security configurations (Firewalls, VPNs, SSO).
    *   Policies and Standards (Governance Documents).
*   **Exclusions:**
    *   Development or Sandbox environments that do not connect to production data.
    *   Local desktop customization that does not affect security controls or network connectivity.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Change** | The addition, modification, or removal of anything that could have an effect on IT services or operational integrity. |
| **RFC (Request for Change)** | A formal proposal for a change to be made. It includes details of the proposed change, and may be recorded on paper or electronically. |
| **CAB (Change Advisory Board)** | A body that exists to support the authorization of changes and to assist Change Management in the assessment and prioritization of changes. |
| **Back-out Plan** | A documented procedure to restore the system to its pre-change state if the implementation fails. |
| **Configuration Item (CI)** | Any component or other service asset that needs to be managed in order to deliver an IT service. |

### 4. Procedures

#### 4.1 Change Classification
All changes must be categorized into one of the following types to determine the required approval workflow:

1.  **Standard Change:** A pre-authorized change that is low risk, relatively common, and follows a procedure or work instruction (e.g., patching a non-critical server, creating a new user account).
2.  **Normal Change:** A change that is not an Emergency or Standard Change. Normal changes follow the defined steps of the change process and require CAB approval (e.g., upgrading the LMS, changing firewall rules).
3.  **Emergency Change:** A change that must be introduced as soon as possible to resolve a major incident or implement a security patch.
4.  **Major Change:** A high-risk change with significant potential impact on the Organization's mission or financial standing (e.g., migrating cloud providers).

#### 4.2 The Request for Change (RFC) Process
Any personnel (Employee, Volunteer, or Contractor) wishing to initiate a change must submit an RFC via the Organization’s IT Service Management (ITSM) ticketing system.

**4.2.1 RFC Requirements**
The RFC must contain, at minimum:
*   Description of the change.
*   Reason for the change (Business Case).
*   Impact assessment (Risk/Benefit analysis).
*   Proposed schedule (Start/End time).
*   **Back-out Plan** (Mandatory for Normal/Major changes).
*   Testing/Validation plan.

#### 4.3 Assessment and Risk Evaluation
Upon receipt of an RFC, the Change Manager (or CISO) must review the request for completeness.

**4.3.1 Peer Review**
For code-based changes, a peer review must be conducted and documented prior to CAB submission, ensuring compliance with **Article IX, Section 9.3** regarding Intellectual Property and Open Source commitments.

**4.3.2 Risk Scoring**
The Change Manager assigns a risk score based on:
*   Number of users affected.
*   Potential for service downtime.
*   Complexity of the back-out plan.
*   Security implications (Data Privacy/Integrity).

#### 4.4 Change Authorization (The CAB)
**4.4.1 Standard Changes**
Approved automatically by the Change Manager or designated Department Head.

**4.4.2 Normal Changes**
Must be reviewed by the Change Advisory Board (CAB).
*   **CAB Composition:** CISO, VP of Education, and relevant Technical Leads.
*   **Quorum:** A simple majority of the CAB is required for approval.
*   **Criteria:** The CAB evaluates the technical feasibility, resource availability, and conflict with other scheduled changes.

**4.4.3 Major Changes**
Require CAB approval *plus* final sign-off from the Executive Director. If the change constitutes a "Fundamental Action" (e.g., selling assets/merging systems) as defined in **Bylaws Article X**, it must be escalated to the Board of Directors.

#### 4.5 Emergency Change Procedure
Used only when a critical service is down or a severe security vulnerability exists.

1.  **Verbal Approval:** The Change Manager or CISO may grant verbal approval to proceed immediately.
2.  **Execution:** The technical team implements the fix.
3.  **Retroactive Documentation:** An RFC must be filed within 24 hours of the incident resolution, categorized as "Emergency - Retroactive."

#### 4.6 Implementation and Testing
1.  **Scheduling:** Changes must be scheduled during maintenance windows (defined as 22:00 - 06:00 CT) unless otherwise authorized.
2.  **Communication:** Stakeholders must be notified at least 24 hours in advance via the `#announcements` channel or email.
3.  **Execution:** The implementer executes the change following the documented plan.
4.  **Validation:** Post-implementation testing is performed immediately.
    *   *Pass:* Close RFC as "Successful."
    *   *Fail:* Execute Back-out Plan immediately.

#### 4.7 Post-Implementation Review (PIR)
A PIR is mandatory for all **Major Changes** and **Failed Changes**.
The PIR meeting must answer:
*   Did the change meet the desired objectives?
*   Was the change implemented on time and within budget?
*   Did any unexpected incidents occur?
*   Are the records (CMDB) updated?

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Change Requester** | Identifies the need for change, submits the RFC, and assists with testing. |
| **Change Manager** | Filters requests, convenes the CAB, ensures the process is followed, and maintains the Change Schedule. |
| **Change Advisory Board (CAB)** | Assesses, prioritizes, and authorizes Normal and Major changes. |
| **Implementer** | Builds and deploys the change; executes the back-out plan if necessary. |
| **Chief Information Security Officer (CISO)** | Holds veto power over any change deemed to introduce unacceptable security risk (per **Bylaws Article V, Section 5.2**). |
| **Executive Director** | Approves Major Changes and resolves deadlocks within the CAB. |

### 6. Compliance and Enforcement
**6.1 Unauthorized Changes**
Any change made to the production environment without a corresponding approved RFC is considered an "Unauthorized Change." This is a violation of the Organization's internal controls.

**6.2 Disciplinary Action**
Failure to comply with this procedure, including bypassing the CAB or falsifying testing results, may result in disciplinary action, up to and including termination of employment or volunteer assignment.

**6.3 Audit Trail**
All RFCs, approvals, and PIR documents must be retained for a minimum of three (3) years in accordance with the **Document Retention and Destruction Policy**.

### 7. References
*   **Bylaws of Study GRC Inc.** (specifically Articles V, VIII, IX, and X)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-PRC-040:** Patch Management Policy
*   **ITIL v4:** Change Control Practice Guide
*   **NIST SP 800-53 (CM Family):** Configuration Management

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-26 | Chief Compliance Architect | Initial Release aligned with ITIL v4 and Bylaws. |