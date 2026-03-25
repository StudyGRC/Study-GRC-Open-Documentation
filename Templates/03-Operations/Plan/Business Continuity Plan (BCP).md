### Business Continuity Plan (BCP)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PLN-054 |
| **Document Type** | Plan |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Business Continuity Plan (BCP) is to establish a framework for Study GRC Inc. ("the Organization") to maintain or quickly resume mission-critical functions in the event of a significant disruption. Aligned with **ISO 22301:2019**, this plan prioritizes the safety of personnel, the protection of the Organization’s reputation, and the continuity of its charitable and educational mission as defined in **Article I, Section 1.3** of the Bylaws.

### 2. Scope
This plan applies to all operations, personnel (employees, volunteers, and contractors), and information systems of Study GRC Inc.

**Inclusions:**
*   **Remote Workforce:** Protocols for distributed teams.
*   **Technology Infrastructure:** Cloud services (SaaS), learning platforms, and financial systems.
*   **Governance:** Leadership succession and decision-making authority.

**Exclusions:**
*   **Third-Party Internal Operations:** This plan covers the Organization's *response* to a vendor failure (e.g., AWS outage) but does not govern the internal recovery procedures of third-party vendors themselves.
*   **Minor Operational Glitches:** Routine IT issues resolved within standard Service Level Agreements (SLAs) are not considered "Disruptions" under this plan.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **RTO (Recovery Time Objective)** | The targeted duration of time and a service level within which a business process must be restored after a disaster (or disruption) in order to avoid unacceptable consequences. |
| **RPO (Recovery Point Objective)** | The maximum targeted period in which data might be lost from an IT service due to a major incident (e.g., "we can lose up to 4 hours of data"). |
| **MTPD (Maximum Tolerable Period of Disruption)** | The time it would take for adverse impacts, which might arise as a result of not providing a product/service or performing an activity, to become unacceptable. |
| **Crisis Management Team (CMT)** | The designated group of individuals responsible for declaring a disaster and executing this BCP. |
| **Invocation** | The formal act of declaring that a disruption has occurred and activating the BCP. |
| **Fundamental Action** | Significant events (merger, dissolution, asset sale) as defined in **Bylaws Article X**, which may trigger specific continuity or winding-up procedures. |

### 4. Plan Statements

#### 4.1 Crisis Management Team (CMT) Structure
The CMT is responsible for the invocation of this plan.

*   **CMT Leader:** Executive Director (CEO).
*   **CMT Alternate Leader:** President of the Board.
*   **Members:** CISO, CFO, VP of Education.

**4.1.1 Activation Criteria**
The CMT Leader is authorized to activate this plan upon the occurrence of:
*   Loss of critical infrastructure (e.g., Learning Management System) exceeding 4 hours.
*   Cybersecurity breach (Ransomware/Data Exfiltration).
*   Incapacitation of key leadership.
*   Reputational crisis requiring immediate public response.

#### 4.2 Business Impact Analysis (BIA) & Recovery Objectives
The Organization classifies assets and processes based on criticality to the mission.

| Tier | Criticality | Description | RTO | RPO |
| :--- | :--- | :--- | :--- | :--- |
| **Tier 1** | **Mission Critical** | Learning Management System (LMS), Website, Donor Payment Gateways. | 4 Hours | 1 Hour |
| **Tier 2** | **Essential** | Email, Financial Reporting, Slack/Discord Community. | 24 Hours | 24 Hours |
| **Tier 3** | **Non-Essential** | Social Media Posting, Routine Admin, Historical Archives. | 72 Hours | 1 Week |

#### 4.3 Continuity Strategies

**4.3.1 Technology & SaaS Resilience (Remote-First Context)**
As a remote-first entity, the Organization relies heavily on cloud providers.
*   **Redundancy:** Critical data must be backed up to an immutable, geographically distinct location (e.g., separate cloud bucket or offline storage) per the **Backup Policy**.
*   **Vendor Failure:** In the event of a primary SaaS provider failure (e.g., GitHub or LMS provider outage), the Organization shall switch to "Read-Only" mode using cached backups or alternative communication channels to inform the community.

**4.3.2 Workforce Continuity**
*   **Distributed Risk:** Since staff is remote, a regional disaster (e.g., hurricane in Florida) affects only a portion of the team. Workload redistribution must be handled by the VP of Education or appropriate department head.
*   **Communication Failure:** If the primary communication tool (e.g., Slack) is unavailable, the CMT will activate the **Secondary Communication Channel** (e.g., Signal Group or Email Tree).

#### 4.4 Leadership Succession & Governance Continuity

**4.4.1 Operational Leadership Succession**
If the Executive Director is incapacitated or unavailable during a crisis:
1.  Authority transfers immediately to the **President of the Board**.
2.  If the President is unavailable, authority transfers to the **Treasurer**.
3.  This temporary authority remains until the Board meets to appoint an Interim Executive Director per **Bylaws Article V**.

**4.4.2 Board Continuity ("Doomsday Clause")**
In the event of a catastrophic loss of Directors, the Organization shall strictly adhere to **Bylaws Article III, Section 3.10**:
*   If zero (0) Directors remain, *any* Voting Member may call a **Special Emergency Meeting** with 10 days' notice.
*   The sole purpose of this meeting is to elect a new interim Board to restore governance.

**4.4.3 Financial Continuity**
*   **Access:** At least two (2) individuals (e.g., Treasurer and Executive Director) must have administrative access to bank accounts to ensure vendor payments and payroll can continue if one person is incapacitated.
*   **Emergency Spending:** The CMT is authorized to approve emergency expenditures up to $10,000 to restore operations, to be ratified by the Board at the next meeting.

#### 4.5 Plan Testing and Maintenance
To ensure ISO 22301 compliance:
*   **Annual Exercise:** The CMT must conduct a tabletop exercise (TTX) at least once per fiscal year to simulate a disruption (e.g., ransomware attack or key person loss).
*   **Post-Incident Review:** After any activation of the BCP (real or test), a "Lessons Learned" report must be generated within 14 days.
*   **Plan Update:** This plan must be reviewed and updated annually or following any significant change to the Organization's structure or technology stack.

#### 4.6 Communication Strategy
*   **Internal:** The CMT will provide status updates to staff/volunteers every 4 hours during a Tier 1 crisis.
*   **External:** The **Director of Kindness and Generosity (DKG)** is responsible for drafting community-facing communications.
*   **Transparency:** In the event of a data breach, the Organization shall comply with the **Data Breach Notification Procedure** and **Bylaws Article VIII (Transparency)** regarding disclosure.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Board of Directors** | Approves the BCP policy; provides fiduciary oversight; assumes leadership in "Doomsday" scenarios. |
| **Executive Director (CMT Leader)** | Declares disaster; directs recovery operations; authorizes emergency spending. |
| **CISO** | Manages technical recovery (DRP); secures data during disruption; leads BIA updates. |
| **VP of Education** | Ensures curriculum and community resources are communicated/restored; manages volunteer workforce redistribution. |
| **All Staff/Volunteers** | Maintain personal contact information; participate in BCP testing; follow CMT directives during a crisis. |

### 6. Compliance and Enforcement
Failure to comply with this plan, particularly regarding the maintenance of redundancy/backups or participation in mandatory testing, may result in disciplinary action up to and including termination of employment or volunteer assignment.

Failure by the Board to adhere to succession protocols defined in the Bylaws may result in legal liability or loss of non-profit status.

### 7. References
*   **ISO 22301:2019** - Security and resilience — Business continuity management systems.
*   **Bylaws of Study GRC Inc.** (Specifically Articles III, V, and X).
*   **IS-PLN-055** Disaster Recovery Plan (DRP).
*   **IS-POL-030** Master Information Security Policy.
*   **IS-PRC-045** Incident Response Plan (IRP).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Release aligned with ISO 22301 and Bylaws. |