### Post-Incident Review/Lessons Learned

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-052 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Incident Response Team Lead |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to formalize the Post-Incident Review (PIR) process, also known as "Lessons Learned." This procedure ensures that Study GRC Inc. systematically analyzes security incidents and significant near-misses to identify root causes, evaluate the effectiveness of the Incident Response Plan (IRP), and implement corrective actions. This process satisfies the "Recover" function of the NIST Cybersecurity Framework (CSF) and ensures continuous improvement of the Organization’s security posture.

### 2. Scope
This procedure applies to all confirmed Information Security Incidents classified as **Medium (Severity 3)**, **High (Severity 2)**, or **Critical (Severity 1)**, as defined in the *Incident Classification/Severity Matrix*.

*   **Inclusions:** All members of the Incident Response Team (IRT), IT staff, Executive Leadership, and relevant stakeholders (e.g., Legal, HR, Communications) involved in the incident.
*   **Exclusions:** Low-severity automated alerts (e.g., failed login attempts blocked by MFA) that do not result in compromise, unless a trend is identified.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **PIR (Post-Incident Review)** | A meeting and analysis phase conducted after an incident has been contained and eradicated to determine what happened, why it happened, and how to prevent recurrence. |
| **Root Cause Analysis (RCA)** | A systematic process for identifying the fundamental cause of an event, rather than just addressing its symptoms. |
| **Hot Wash** | An immediate, informal debrief conducted by the IRT immediately following incident containment while details are fresh. |
| **Cold Wash** | A formal, scheduled meeting and documented report occurring within a set timeframe after the incident closure. |
| **Artifacts** | Digital evidence, logs, chat transcripts, and screenshots collected during the incident. |

### 4. Procedures

#### 4.1 Timing and Initiation
4.1.1 **Trigger:** The Incident Commander (IC) must initiate the PIR process upon moving the incident ticket status to "Resolved" or "Monitoring."
4.1.2 **Timeframe:**
*   **Hot Wash:** Must occur within **24 hours** of incident containment.
*   **Cold Wash (Formal PIR):** Must be scheduled and conducted within **five (5) business days** of incident closure.
4.1.3 **Attendance:** Attendance is mandatory for all primary responders. Legal Counsel must be invited to PIRs for Severity 1 and 2 incidents to establish Attorney-Client Privilege over the resulting report.

#### 4.2 Data Collection and Preparation
Prior to the formal PIR meeting, the Incident Commander or designee must aggregate the following:
4.2.1 **Timeline Construction:** A precise, UTC-timestamped chronology of the attack lifecycle, including:
*   First evidence of compromise.
*   Time of detection/alert generation.
*   Time of IRT mobilization.
*   Time of containment.
*   Time of restoration.
4.2.2 **Communication Logs:** Exports of relevant Slack/Discord channels (e.g., `#incident-war-room`), email threads, and ticketing system notes.
4.2.3 **Technical Evidence:** Summary of logs (SIEM, Firewall, EDR) and forensic findings.

#### 4.3 Conducting the PIR Meeting
The meeting must follow a "Blameless Post-Mortem" approach. The focus is on process and technology failure, not human error.

**Agenda Items:**
1.  **Executive Summary:** Brief overview of the incident.
2.  **Timeline Review:** Walkthrough of the "Time to Detect" (TTD) and "Time to Remediate" (TTR).
3.  **What Went Well?** Identify successful controls, effective alerts, and team coordination.
4.  **What Went Wrong?** Identify control failures, missing logs, communication breakdowns, or delays.
5.  **Root Cause Analysis (RCA):** Apply the "5 Whys" technique to determine the core issue (e.g., "Server was patched late" -> "Why?" -> "Change management process is unclear").
6.  **Corrective Actions:** Define specific tasks to prevent recurrence.

#### 4.4 Root Cause Analysis (RCA) Requirements
For all Severity 1 and 2 incidents, a formal RCA is required. The RCA must categorize the failure into one of the following:
*   **People:** Training gaps, social engineering susceptibility, resource shortages.
*   **Process:** Policy gaps, failure to follow procedure, inadequate change management.
*   **Technology:** Software bugs, misconfiguration, unpatched vulnerabilities, hardware failure.
*   **External:** Vendor failure, zero-day exploit, force majeure.

#### 4.5 The Lessons Learned Report (LLR)
4.5.1 **Drafting:** The Incident Commander must draft the LLR using the *Incident Report Template* within **three (3) business days** of the PIR meeting.
4.5.2 **Content:** The report must include:
*   Incident Summary and Classification.
*   Final Timeline.
*   Root Cause Statement.
*   Impact Assessment (Financial, Reputational, Legal, Data Loss).
*   List of Corrective Actions (Action Items).

#### 4.6 Corrective Action Tracking
4.6.1 **Assignment:** Every Corrective Action must be assigned a specific **Owner** and a **Due Date**.
4.6.2 **Ticket Generation:** Action items must be entered into the Organization’s project management system (e.g., Jira/Asana) as specific tasks (e.g., "Update Firewall Rules," "Revise Phishing Training").
4.6.3 **Monitoring:** The CISO or Audit Committee will review open Corrective Actions monthly until closure.

#### 4.7 Record Retention
In accordance with **Bylaws Article VIII (Records, Transparency & Finance)** and the *Document Retention Policy*:
4.7.1 The final LLR must be stored securely in the designated "Compliance/Incidents" repository.
4.7.2 Reports involving Youth Data (COPPA) or PII must be encrypted at rest.
4.7.3 Retention period is **seven (7) years** from the date of incident closure.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Incident Commander (IC)** | Facilitates the PIR meeting, drafts the LLR, and assigns corrective actions. |
| **CISO** | Reviews and approves the final LLR; ensures resources are allocated for corrective actions. |
| **IRT Members** | Provide accurate testimony, logs, and evidence during the review; implement technical fixes. |
| **Legal Counsel** | Reviews LLRs for high-severity incidents to ensure language does not create unnecessary liability; advises on regulatory notification obligations. |
| **Human Resources** | Participates if the incident involved internal misconduct or requires employee disciplinary action. |

### 6. Compliance and Enforcement
Failure to participate honestly in a Post-Incident Review, including the intentional concealment of errors or evidence, is a violation of the **Board of Directors Code of Ethics and Conduct** and the **Employee Handbook**.

*   **Non-Retaliation:** The Organization strictly prohibits retaliation against employees who report security gaps or admit to unintentional errors during the PIR process, provided no malicious intent existed.
*   **Enforcement:** Failure to implement assigned Corrective Actions by the due date may result in performance improvement plans for the responsible document owners.

### 7. References
*   **NIST SP 800-61 Rev. 2:** Computer Security Incident Handling Guide (Section 3.4 - Post-Incident Activity).
*   **ISO/IEC 27001:2013:** Control A.16.1.6 (Learning from information security incidents).
*   **Study GRC Inc. Bylaws:** Article VIII (Records).
*   **IS-POL-045:** Incident Response Plan (IRP).
*   **IS-STD-046:** Incident Classification/Severity Matrix.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Incident Response Lead | Initial release of PIR procedure. |