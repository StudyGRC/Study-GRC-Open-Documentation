### IT Help Desk Support Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IT-PRC-005 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | IT Operations Manager |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized, secure, and efficient method for receiving, prioritizing, and resolving technical support requests within Study GRC Inc. This procedure ensures that:
1.  Technical issues are resolved within established Service Level Agreements (SLAs) to minimize operational disruption.
2.  Identity verification protocols are strictly followed to prevent social engineering attacks during account recovery.
3.  Support interactions comply with the Organization’s data privacy and youth protection obligations.

### 2. Scope
This procedure applies to all "Users" of Study GRC Inc. information systems, including:
*   **Internal:** Board of Directors, Officers, Employees, and Volunteers.
*   **External:** Community Participants and Learners accessing Organization-managed platforms (e.g., LMS, Community Forum).

**In Scope:**
*   Access control (password resets, MFA issues).
*   Organization-managed software (SaaS platforms, collaboration tools).
*   Organization-owned hardware (if issued).

**Out of Scope:**
*   Repair or troubleshooting of personal devices (BYOD) beyond basic connectivity to Organization resources.
*   Home network debugging (ISP issues) for remote staff.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Incident** | An unplanned interruption to an IT service or reduction in the quality of an IT service (e.g., "I can't login"). |
| **Service Request** | A formal request from a user for something to be provided (e.g., "I need a license for software X"). |
| **Ticket** | The digital record of a support request tracked in the IT Service Management (ITSM) tool. |
| **SLA (Service Level Agreement)** | The agreed-upon time frame for responding to and resolving tickets based on priority. |
| **Tier 1 Support** | First line of support; handles basic issues (password resets, FAQs). |
| **Tier 2 Support** | Specialized support; handles complex technical issues requiring administrative access or system configuration. |

### 4. Procedures

#### 4.1 Request Submission (Intake)
Users must submit support requests through authorized channels to ensure tracking and security.
1.  **Primary Channel:** Submit a ticket via the [Link to IT Service Portal].
2.  **Secondary Channel:** Email `support@[studygrc.org]`.
3.  **Emergency Channel:** For "Critical" system-wide outages only, designated leadership may contact the IT On-Call via the emergency Slack channel `#ops-emergency`.

**Prohibited Channels:** Support requests sent via personal text message, personal social media, or direct messages (DMs) to IT staff personal accounts will not be processed.

#### 4.2 Triage and Prioritization
Upon receipt, the Help Desk Agent must categorize the ticket and assign a priority level based on the following matrix:

| Priority | Definition | Response SLA | Resolution SLA |
| :--- | :--- | :--- | :--- |
| **P1 - Critical** | System-wide outage; Data breach; Security incident; Blockage of revenue-generating activity. | 30 Minutes | 4 Hours |
| **P2 - High** | Critical function broken for a single user; VIP (Board/Officer) access issue; Time-sensitive deadline at risk. | 2 Hours | 8 Hours |
| **P3 - Medium** | Standard system errors; Non-critical access issues; Software installation requests. | 8 Hours | 2 Business Days |
| **P4 - Low** | Cosmetic issues; "How-to" questions; Feature requests. | 24 Hours | 5 Business Days |

#### 4.3 Identity Verification (Mandatory Security Step)
To prevent unauthorized access via social engineering, Help Desk Agents must verify the requester's identity **before** performing any account action (e.g., password reset, MFA disablement).

1.  **Standard Verification:** Verify the request originates from the user's registered organizational email address.
2.  **Enhanced Verification (Required for MFA/Password Resets):**
    *   If the user is locked out of email/Slack, the Agent must initiate a brief video call (Zoom/Teams) to visually verify the user against their file photo or government ID.
    *   Alternatively, a verification code may be sent to the user's secondary email or mobile number on file in the HR/Volunteer Information System (HRIS).
3.  **Failure to Verify:** If identity cannot be verified, the request must be denied and flagged as a potential security incident.

#### 4.4 Issue Resolution and Escalation
1.  **Tier 1 Resolution:** The Agent attempts to resolve the issue using the Knowledge Base.
2.  **Escalation:** If the issue cannot be resolved within 60 minutes or requires elevated privileges not held by Tier 1:
    *   Escalate to **Tier 2 (SysAdmin)**.
    *   Update the ticket notes with steps already taken.
3.  **Vendor Escalation:** If the issue is caused by a third-party provider (e.g., Microsoft, LMS Provider), Tier 2 will open a support case with the vendor and monitor for resolution.

#### 4.5 Youth Protection Protocols
Pursuant to the *Child and Youth Safeguarding Policy*, special care must be taken when providing support to minors (Community Participants under 18).
1.  **No 1-on-1 Private DMs:** Support for minors must be conducted via the public ticketing system or email where a copy is archived.
2.  **Video Support:** If a video call is required for a minor, a second adult (staff/volunteer) or the minor's parent/guardian must be present (Two-Deep Leadership).
3.  **Data Minimization:** Agents must not request more personal information from a minor than is strictly necessary to resolve the technical issue.

#### 4.6 Ticket Closure
1.  **Confirmation:** The Agent must confirm with the user that the issue is resolved before closing the ticket.
2.  **No Response:** If the user does not respond to requests for information after three (3) attempts over five (5) business days, the ticket may be closed as "Abandoned."
3.  **Documentation:** The resolution method must be documented in the ticket to aid future troubleshooting.

#### 4.7 Security Incident Identification
If a support request indicates a potential compromise (e.g., "I received a 2FA code I didn't request," "My files are encrypted"), the Help Desk Agent must:
1.  Immediately reclassify the ticket as a **Security Incident**.
2.  Escalate directly to the CISO or Incident Response Team.
3.  Follow the *Incident Response Plan (IRP)* rather than standard support procedures.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Requester (User)** | Provide accurate information; respond to IT inquiries promptly; verify identity when requested. |
| **Help Desk Agent (Tier 1)** | Triage tickets; perform identity verification; resolve routine issues; escalate complex issues. |
| **System Administrator (Tier 2)** | Resolve complex infrastructure issues; manage vendor support cases. |
| **CISO** | Monitor SLA compliance; review ticket trends for systemic risks; oversee identity verification standards pursuant to Bylaws Article V. |

### 6. Compliance and Enforcement
Failure to comply with this procedure—specifically the bypassing of Identity Verification steps—may result in disciplinary action, up to and including termination of employment or volunteer assignment.

Any attempt by a user to deceive Help Desk staff to gain unauthorized access (internal social engineering) will be treated as a severe violation of the *Code of Ethics and Conduct* and may result in immediate expulsion and legal action.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-003:** Access Control Policy
*   **IS-PLN-001:** Incident Response Plan
*   **HR-POL-020:** Child and Youth Safeguarding Policy
*   **Bylaws Article V:** Operational Leadership (CISO Duties)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name/Title] | Initial release of Help Desk Support Procedure. |