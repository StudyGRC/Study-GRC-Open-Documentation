### Service Request Ticketing and Escalation Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-003 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized framework for the submission, triage, management, and escalation of service requests and technical incidents within Study GRC Inc. This procedure ensures **Accountability** by creating an immutable audit trail of all operational support activities, ensuring that resources are allocated efficiently, and guaranteeing that member and staff issues are resolved within defined service levels. This aligns with the operational management duties defined in **Article V** of the Bylaws.

### 2. Scope
This procedure applies to all "Requesters" (Employees, Board Directors, Volunteers, and Contractors) and "Fulfillers" (IT Staff, System Administrators, and Operational Officers).

**In Scope:**
*   Technical support requests (hardware/software).
*   Access provisioning and de-provisioning (Identity Management).
*   Bug reports regarding the Organization’s open-source repositories or website.
*   General operational inquiries requiring tracked resolution.

**Out of Scope:**
*   **Whistleblower Complaints:** Must be submitted via the *Whistleblower Complaint Intake Form* per the *Whistleblower Protection Policy*.
*   **Emergency Life Safety Issues:** Immediate threats to physical safety must be reported to local emergency services (911) first.
*   **Cybersecurity Incidents:** Confirmed security breaches must be reported immediately via the *Incident Response Plan (IRP)*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Service Request** | A formal request from a user for something to be provided (e.g., a password reset, access to a folder, or a software license). |
| **Incident** | An unplanned interruption to an IT service or reduction in the quality of an IT service (e.g., "The website is down"). |
| **Ticket** | A digital record within the Organization’s designated Ticketing System (e.g., Jira Service Management, Freshservice) containing all details of a request. |
| **SLA (Service Level Agreement)** | The agreed-upon time period within which a ticket must be responded to or resolved. |
| **Tier 1 Support** | First line of support; handles basic troubleshooting and routing. |
| **Tier 2/3 Support** | Specialized technical staff (e.g., DevOps, Security Engineers) for complex issues. |
| **Escalation** | The process of moving a ticket to a higher level of expertise (Functional) or management authority (Hierarchical). |

### 4. Procedures

#### 4.1. Request Submission (Intake)
To ensure accountability and tracking, "drive-by" requests (e.g., direct messages via Slack/Teams or verbal requests) are prohibited for formal service actions.

1.  **Submission Channels:** Requesters must submit requests via one of the following approved channels:
    *   **Service Portal:** [Insert URL] (Preferred)
    *   **Email:** support@[organization-domain].org
    *   **Slack/Teams Integration:** Using the `/ticket` command in the `#helpdesk` channel.
2.  **Mandatory Information:** All requests must include:
    *   Requester Name and Role.
    *   Category (e.g., Access, Hardware, Software, Bug).
    *   Priority Assessment (Low, Medium, High, Critical).
    *   Detailed Description of the need or issue.

#### 4.2. Triage and Prioritization
Upon receipt, the Ticketing System automatically assigns a unique ID. The Service Desk Agent must validate the priority within **two (2) business hours**.

| Priority Level | Definition | Target Response Time | Target Resolution Time |
| :--- | :--- | :--- | :--- |
| **P1 - Critical** | System-wide outage; Blockage of core mission delivery; Data breach risk. | 30 Minutes | 4 Hours |
| **P2 - High** | Critical function unavailable for a single user; Significant workaround required. | 2 Hours | 1 Business Day |
| **P3 - Medium** | Non-critical error; Standard access request; System glitch with workaround. | 4 Hours | 3 Business Days |
| **P4 - Low** | Cosmetic issue; "Nice to have" feature request; Information inquiry. | 1 Business Day | 5 Business Days |

#### 4.3. Ticket Assignment and Fulfillment
1.  **Assignment:** The Ticket is assigned to a specific Fulfiller. The Fulfiller must update the status to "In Progress."
2.  **Communication:** All communication regarding the ticket must occur within the Ticketing System comments to maintain the audit trail.
3.  **Remote Access:** If remote control of a user's device is required, the Fulfiller must obtain explicit consent in the ticket notes prior to initiating the session, in accordance with the *Remote Access Policy*.

#### 4.4. Escalation Protocol
Escalation ensures that stalled tickets or complex issues receive appropriate attention.

**4.4.1 Functional Escalation (Skill-Based)**
*   **Trigger:** Tier 1 cannot resolve the issue within 60 minutes of active work.
*   **Action:** Ticket is reassigned to Tier 2 (e.g., System Admin or CISO).
*   **Documentation:** Tier 1 must document all troubleshooting steps attempted before reassignment.

**4.4.2 Hierarchical Escalation (Management-Based)**
*   **Trigger:**
    *   SLA Breach (Target Resolution Time exceeded by 50%).
    *   Requester dissatisfaction with the proposed solution.
    *   P1 (Critical) incidents not resolved within 2 hours.
*   **Action:**
    *   **Level 1:** Notify the **VP of Education & Training** (for LMS issues) or **CISO** (for IT issues).
    *   **Level 2:** If unresolved after Level 1 intervention, the issue is escalated to the **Executive Director**.

#### 4.5. Resolution and Closure
1.  **Verification:** The Fulfiller marks the ticket as "Resolved" and provides a resolution summary.
2.  **User Acceptance:** The Ticketing System sends a notification to the Requester. The Requester has **three (3) business days** to reopen the ticket if the issue persists.
3.  **Auto-Closure:** If no action is taken by the Requester after three days, the system automatically moves the ticket to "Closed." Closed tickets cannot be reopened; a new ticket must be generated.

#### 4.6. Reporting and Accountability
1.  **Monthly Review:** The CISO shall generate a "Ticket Metrics Report" reviewing:
    *   Total volume.
    *   SLA breach percentage.
    *   Customer Satisfaction (CSAT) scores.
2.  **Board Oversight:** Significant trends or systemic failures identified in the metrics report must be summarized and presented to the Board of Directors quarterly, ensuring alignment with **Bylaws Article VIII (Records, Transparency & Finance)**.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Requester** | Submits tickets via approved channels; provides necessary information; tests resolution promptly. |
| **Service Desk Agent (Tier 1)** | Performs initial triage; resolves routine requests; documents all activities in the ticket. |
| **System Administrators (Tier 2)** | Handles complex technical issues; accepts functional escalations; maintains system documentation. |
| **CISO** | Owns the Ticketing System; monitors SLA compliance; handles hierarchical escalations regarding security or infrastructure. |
| **Executive Director** | Final escalation point for disputes; approves resource allocation for P1/Critical incidents. |

### 6. Compliance and Enforcement
Strict adherence to this procedure is required to maintain the Organization's accountability standards.

*   **Bypassing the System:** Repeated failure to submit tickets for service requests (e.g., "shoulder tapping") may result in performance counseling.
*   **Data Integrity:** Falsifying ticket timestamps, priority levels, or resolution notes is considered a violation of the *Code of Ethics* and may result in disciplinary action, up to and including termination.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article V - Operational Leadership)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-005:** Access Control Policy
*   **IS-POL-024:** Remote Access Policy
*   **IS-PLN-001:** Incident Response Plan (IRP)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial Release |