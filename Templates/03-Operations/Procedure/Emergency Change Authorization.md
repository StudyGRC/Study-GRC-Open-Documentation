### Emergency Change Authorization

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-065 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Director of IT Operations |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to define the authorized process for implementing **Emergency Changes** to Study GRC Inc.'s production systems, infrastructure, and applications. While standard change management procedures ensure stability through rigorous review, specific scenarios (e.g., active cyberattacks, critical service outages) require an expedited process to mitigate **Urgency Risk**. This procedure balances the need for rapid remediation with the requirement for accountability, auditability, and system integrity.

### 2. Scope
This procedure applies to all technical personnel, contractors, and volunteers with administrative access to Study GRC Inc.'s production environments.

*   **In Scope:**
    *   Production servers, databases, and network infrastructure.
    *   Customer-facing learning management systems (LMS).
    *   Security appliances (firewalls, IDPS) requiring immediate configuration changes to block threats.
    *   Third-party integrations critical to business operations.
*   **Exclusions:**
    *   Changes to non-production environments (Dev/Test/Staging), unless those changes are required to validate the emergency fix.
    *   Routine maintenance or "urgent" changes that do not meet the strict criteria for "Emergency" defined in Section 3.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Emergency Change** | A change that must be implemented immediately to correct a Service Interruption or a Security Incident. |
| **Service Interruption** | A condition where a critical business function is unavailable or severely degraded, impacting the Organization's ability to deliver its mission. |
| **Security Incident** | An active threat or breach compromising the confidentiality, integrity, or availability of data (e.g., active ransomware, zero-day exploit). |
| **ECAB** | **Emergency Change Advisory Board**. A subset of the standard CAB authorized to make rapid decisions on emergency changes. |
| **Retrospective Change Record** | A change request ticket created or finalized *after* the implementation of the fix to ensure audit trails are maintained. |

### 4. Procedures

#### 4.1 Criteria for Invocation
An Emergency Change may **only** be requested if one or more of the following criteria are met:
1.  **Critical Outage:** A production system is down, preventing users from accessing educational resources.
2.  **Security Threat:** Immediate action is required to patch a vulnerability, block malicious traffic, or isolate a compromised host.
3.  **Data Integrity:** A system error is actively corrupting data.
4.  **Legal/Compliance:** Immediate action is required to comply with a sudden legal directive or regulatory requirement.

*Note: Poor planning does not constitute an emergency. Missed deadlines for standard changes do not qualify for this procedure.*

#### 4.2 Emergency Change Advisory Board (ECAB) Formation
Due to the remote-first nature of Study GRC Inc., the ECAB is a dynamic group convened via the designated secure communication channel (e.g., Slack `#incidents` channel or Zoom).

The ECAB must consist of a minimum of **two (2)** approvers from the following list:
1.  Chief Information Security Officer (CISO) (Primary Approver)
2.  Executive Director (CEO)
3.  VP of Education & Training (if LMS is affected)
4.  Lead DevOps Engineer (cannot approve their own change)

#### 4.3 Process Workflow

**4.3.1 Identification and Declaration**
1.  The **Requester** identifies a critical issue meeting the criteria in Section 4.1.
2.  The Requester declares an incident in the ticketing system (or via the emergency communication channel if the ticketing system is down).

**4.3.2 Request Formulation**
1.  The Requester proposes a specific technical fix.
2.  The Requester must verbally or textually communicate:
    *   **What** is broken.
    *   **What** the fix is.
    *   **Risk** of applying the fix (e.g., "This might restart the database").
    *   **Back-out Plan** (e.g., "We can revert the commit" or "We have a snapshot").

**4.3.3 ECAB Approval (Expedited)**
1.  ECAB members review the proposed fix immediately.
2.  Approval may be granted verbally or via chat to ensure speed.
3.  **Mandatory:** If approval is verbal, the CISO or Incident Commander must log a timestamped note in the incident channel: *"Emergency Change [Description] approved by [Name] at [Time]."*

**4.3.4 Implementation**
1.  The Requester (or designated Engineer) implements the change.
2.  Where possible, peer review (e.g., "over-the-shoulder" via screen share) should be utilized during execution.

**4.3.5 Verification**
1.  The Requester verifies that the fix resolved the issue.
2.  The Requester verifies that no new critical issues were introduced.

#### 4.4 Post-Implementation Documentation (The "Retro")
To satisfy **NIST** and **2 CFR 200** audit requirements, the following must occur within **24 hours** of the incident resolution:

1.  **Retrospective Ticket:** A Change Request ticket must be created (or updated) tagged as "Emergency."
2.  **Documentation:** The ticket must include:
    *   The nature of the emergency.
    *   The specific changes made (code diffs, config snapshots).
    *   Who approved it and when.
    *   Verification results.
3.  **Post-Incident Review (PIR):** If the change caused collateral damage or failed, a PIR meeting is required to analyze the root cause.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Requester** | Identifies the emergency, proposes the technical fix, and implements the change after approval. Responsible for creating the Retrospective Change Record. |
| **ECAB Member** | Evaluates the risk of the emergency change vs. the risk of the outage. Grants or denies approval. |
| **Incident Commander** | Coordinates the response, ensures the ECAB is convened, and logs verbal approvals in the incident chat. |
| **CISO** | Ultimate authority for security-related emergency changes. Reviews all Emergency Change records monthly for compliance. |
| **Executive Director** | Informed of all emergency changes affecting the Organization's public availability or reputation. |

### 6. Compliance and Enforcement
Failure to follow this procedure poses a significant risk to the Organization's stability and security.

*   **Unauthorized Changes:** Implementing changes to production systems without ECAB approval (even during an emergency) is a violation of the **Master Information Security Policy**.
*   **Documentation Failure:** Failing to submit the Retrospective Change Record within 24 hours will result in a formal performance review.
*   **Disciplinary Action:** Violations may result in disciplinary action, up to and including termination of employment or contract, in accordance with the **Employee Handbook**.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-040:** Patch Management Policy
*   **IS-PLN-001:** Incident Response Plan
*   **NIST SP 800-53 (Rev. 5):** Control CM-3 (Configuration Change Control)
*   **ISO/IEC 27001:2013:** Annex A.12.1.2 (Change Management)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial release of Emergency Change Authorization procedure. |