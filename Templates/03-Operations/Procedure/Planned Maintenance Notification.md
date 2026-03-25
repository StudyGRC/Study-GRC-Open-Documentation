### Planned Maintenance Notification Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IT-PRC-005 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Systems Administrator |
| **Classification** | Public |

### 1. Purpose
The purpose of this procedure is to standardize the communication process regarding scheduled downtime or service degradation of Study GRC Inc. information systems. This procedure ensures that internal staff, volunteers, and the external community receive timely, accurate, and transparent information regarding maintenance activities. This aligns with the Organization’s mission to provide reliable, open-source resources and minimizes disruption to the learner ecosystem.

### 2. Scope
This procedure applies to all **Production Systems** owned or managed by Study GRC Inc., including but not limited to the public website, Learning Management System (LMS), community forums (e.g., Discord/Slack integrations), and internal collaboration tools.

**Exclusions:**
*   **Emergency Maintenance:** Unscheduled outages required to mitigate immediate security threats or critical system failures (governed by *IT-POL-009 Incident Response Plan*).
*   **Transparent Updates:** Backend updates that result in zero downtime or user-perceptible latency.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Planned Maintenance** | Any scheduled work on IT infrastructure or software that is expected to result in downtime, reduced performance, or loss of functionality. |
| **Maintenance Window** | The specific timeframe during which the maintenance activity is authorized to occur. |
| **Stakeholders** | Any individual or group affected by the system availability, including Board Directors, Staff, Volunteers, and Community Members. |
| **Status Page** | The designated public-facing webpage where real-time system health is displayed. |
| **CAB** | Change Advisory Board; a group responsible for assessing and approving changes to the IT environment. |

### 4. Procedures

#### 4.1 Maintenance Scheduling and Approval
Before a notification can be issued, the maintenance window must be established in accordance with the *IT-PRC-040 Change Control and Management Procedure*.

1.  **Window Selection:** Maintenance must be scheduled during off-peak hours based on user analytics (typically 02:00 UTC to 06:00 UTC) to minimize community impact.
2.  **Approval:** The **System Administrator** must submit a Change Request to the CISO or CAB.
3.  **Classification:** The change must be classified to determine the notification timeline:
    *   **Major Maintenance:** Expected downtime > 15 minutes or significant UI/UX changes.
    *   **Minor Maintenance:** Expected downtime < 15 minutes or minimal user impact.

#### 4.2 Notification Timelines
The Organization must provide advance notice to allow stakeholders to plan accordingly.

| Impact Level | Minimum Notice Period | Target Audience |
| :--- | :--- | :--- |
| **Major Maintenance** | 7 Calendar Days | All Users (Email + Banner + Social) |
| **Minor Maintenance** | 48 Hours | Active Users (Banner + Status Page) |
| **Internal-Only Tools** | 24 Hours | Staff/Volunteers (Slack/Email) |

#### 4.3 Notification Channels
Notifications must be distributed across multiple channels to ensure visibility.

1.  **System Status Page:** The primary source of truth. An entry must be created in "Scheduled" status immediately upon approval.
2.  **In-App Banners:** A dismissible banner must be activated on the affected platform (e.g., LMS dashboard).
3.  **Community Platforms:** An automated or manual announcement must be posted in the `#announcements` channel of the community Discord/Slack.
4.  **Email:** For Major Maintenance affecting the LMS, a dedicated email blast must be sent to all registered learners.

#### 4.4 Notification Content Requirements
All notifications must be written in plain English, avoiding excessive technical jargon, and must include:

1.  **Systems Affected:** Clearly list which services will be unavailable.
2.  **Window:** Start and End time in UTC (and local time if applicable).
3.  **Impact:** What the user will experience (e.g., "The site will be offline," "Login will be disabled," "Slow performance").
4.  **Reason:** A brief, transparent explanation (e.g., "Database upgrade for faster performance," "Security patching").
5.  **Action Required:** Instructions for the user (e.g., "Save your work before [Time]").

#### 4.5 Execution and Updates
During the maintenance window:

1.  **Start Notification:** The System Administrator updates the Status Page to "In Progress" at the start of the window.
2.  **Delay Notification:** If the maintenance exceeds the scheduled window by more than 30 minutes, an update must be posted to the Status Page and Community Channels estimating the new completion time.
3.  **Completion Notification:** Upon successful verification of system stability, the System Administrator must update the Status Page to "Operational" and post an "All Clear" message to Community Channels.

#### 4.6 Post-Maintenance Review
If the maintenance resulted in unexpected extended downtime or user issues, a **Post-Implementation Review (PIR)** must be conducted within 3 business days, and a transparent retrospective may be published to the community if deemed necessary by the Director of Kindness and Generosity (DKG) to maintain trust.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO** | Approves the maintenance window and validates the risk assessment. |
| **System Administrator** | Schedules the window, drafts the technical content, executes the maintenance, and updates the Status Page. |
| **Director of Kindness & Generosity (DKG)** | Reviews notification language for tone; manages community sentiment during outages. |
| **Change Advisory Board (CAB)** | Reviews Major Maintenance requests to ensure minimal conflict with organizational events. |
| **Users/Members** | Responsible for reading notifications and saving work prior to the maintenance window. |

### 6. Compliance and Enforcement
Failure to adhere to this procedure—specifically performing maintenance without notification—is a violation of the *IT-PRC-040 Change Control and Management Procedure*. Violations may result in disciplinary action, up to and including termination of employment or volunteer assignment.

Repeated failure to notify the community undermines the Organization's reputation and may trigger a review by the Board of Directors under Bylaws Article V (Operational Leadership).

### 7. References
*   **IT-POL-001:** Master Information Security Policy
*   **IT-PRC-040:** Change Control and Management Procedure
*   **IT-POL-009:** Incident Response Plan
*   **Bylaws Article V:** Operational Leadership (CISO Duties)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | IT Systems Admin | Initial Release aligned with ITIL Change Management standards. |