### IR Playbook: Insider Threat

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PLY-004 |
| **Document Type** | Playbook (Standard Operating Procedure) |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) & Legal Counsel |
| **Document Owner** | Incident Response Team Lead |
| **Classification** | **Confidential / Internal Use Only** |

### 1. Purpose
The purpose of this Playbook is to establish a standardized, legally defensible response to Information Security incidents originating from internal actors (Insider Threats). This document defines the procedures for detecting, containing, investigating, and remediating threats posed by individuals with authorized access to Study GRC Inc. systems, while balancing organizational security with privacy rights and employment/volunteer laws.

This playbook specifically addresses the **Legal Coordination** requirement, ensuring that evidence is preserved for potential disciplinary action, civil litigation, or criminal prosecution.

### 2. Scope
This playbook applies to all "Insiders," defined as any individual with past or present authorized access to Study GRC Inc. assets, data, or facilities.
*   **In Scope:** Employees, Board Directors, Officers, Volunteers, Contractors, Third-Party Vendors with systems access, and Interns.
*   **Out of Scope:** External attackers with no internal credentials (refer to *IS-PLY-001 Phishing* or *IS-PLY-005 Unauthorized Access*).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Insider Threat** | A security risk that originates from within the organization, typically involving a current or former employee, volunteer, or business associate who has inside information concerning the organization's security practices, data, and computer systems. |
| **Malicious Insider** | An insider who intentionally abuses their access for personal gain, revenge, or sabotage (e.g., data theft, logic bombs). |
| **Negligent Insider** | An insider who exposes the organization to risk through carelessness or failure to follow policy (e.g., ignoring update prompts, bypassing security controls for convenience). |
| **Compromised Insider** | An insider whose credentials have been stolen or hijacked by an external actor (often treated initially as an Insider Threat until attribution is confirmed). |
| **Legal Hold** | A process used to preserve all forms of relevant information when litigation is reasonably anticipated. |
| **Chain of Custody** | The chronological documentation or paper trail that records the sequence of custody, control, transfer, analysis, and disposition of physical or electronic evidence. |

### 4. Procedures

#### 4.1 Phase 1: Detection and Triage
*Warning: Do not confront the suspect immediately. Premature confrontation may lead to destruction of evidence.*

1.  **Trigger Identification:** The Incident Response Team (IRT) receives an alert via:
    *   **Technical Indicators:** DLP (Data Loss Prevention) alerts, massive file downloads, access at unusual times, unauthorized privilege escalation, or disablement of logging.
    *   **Behavioral Indicators:** Reports via the *Whistleblower Complaint Intake Form*, disgruntled behavior, resignation notice followed by high data activity.
2.  **Initial Triage (Silent Mode):**
    *   The Incident Commander (IC) must verify the validity of the alert without tipping off the user.
    *   **Verify Authorization:** Check if the activity was part of an approved Change Request or assigned task.
    *   **Classification:** Determine if the threat is **Negligent** (training issue) or **Malicious** (legal issue).

#### 4.2 Phase 2: Containment and Preservation
*Objective: Stop the data loss or damage immediately while preserving evidence for legal action.*

1.  **Legal Hold Initiation:**
    *   The IC must notify Legal Counsel immediately.
    *   Legal Counsel issues a **Preservation Order** to IT to snapshot relevant mailboxes, logs, and endpoints.
    *   **Strict Confidentiality:** Only the IC, CISO, Legal Counsel, and HR/Volunteer Coordinator should be aware of the investigation.
2.  **Access Suspension (The "Kill Switch"):**
    *   **Timing:** Execute immediately upon confirmation of malicious intent.
    *   **Actions:**
        *   Disable SSO/Identity Provider account (Okta/Azure AD).
        *   Revoke VPN and Remote Desktop access.
        *   Revoke API keys and GitHub/GitLab tokens.
        *   Reset passwords for any shared accounts the user had access to.
        *   If the user is physically present (rare in remote-first), escort them from the premises/Zoom meeting.
3.  **Device Isolation:**
    *   If a corporate-managed device is involved, issue a remote lock or quarantine command via MDM (Mobile Device Management). **Do not remote wipe** at this stage (destroys evidence).

#### 4.3 Phase 3: Investigation and Forensics
*Objective: Determine the scope of the breach and gather admissible evidence.*

1.  **Forensic Analysis:**
    *   Analyze logs to determine:
        *   **What** data was accessed/exfiltrated?
        *   **When** did the activity begin?
        *   **How** was the data moved (USB, Cloud Storage, Email)?
    *   Maintain a strict **Chain of Custody** log for all digital evidence.
2.  **Intellectual Property Assessment:**
    *   Review *Bylaws Article IX (Intellectual Property)* and the user's *Work Made for Hire Assignment*.
    *   Identify if proprietary code, donor lists (PII), or financial data were targeted.
3.  **Human Resources / Legal Interview:**
    *   **Interview:** Conducted by HR/Legal (not IT).
    *   **Goal:** Obtain an explanation or confession.
    *   **Documentation:** All interactions must be documented.
    *   *Note:* If the suspect is a Board Director, refer to *Bylaws Section 3.6 (Removal of Directors)* regarding "Cause."

#### 4.4 Phase 4: Eradication and Recovery
1.  **Sanitization:**
    *   Remove any backdoors, logic bombs, or unauthorized accounts created by the insider.
    *   Delete exfiltrated data from unauthorized locations (if accessible/negotiated).
2.  **Credential Rotation:**
    *   Force password resets for all team members if the insider had admin access or access to password vaults.
    *   Rotate all shared secrets (API keys, service account credentials).
3.  **Restoration:**
    *   Restore corrupted data from clean backups created prior to the incident.

#### 4.5 Phase 5: Post-Incident Activity and Legal Action
1.  **Disciplinary Action:**
    *   **Employees:** Termination for cause per the *Employee Handbook*.
    *   **Volunteers:** Revocation of volunteer status per *Volunteer Service Agreement*.
    *   **Directors/Officers:** Initiation of removal proceedings per *Bylaws Article III*.
2.  **Legal Prosecution:**
    *   Consult with Legal Counsel regarding referral to law enforcement (FBI/local authorities) under:
        *   **CFAA (Computer Fraud and Abuse Act):** For unauthorized access.
        *   **DTSA (Defend Trade Secrets Act):** For IP theft.
        *   **Texas Penal Code:** For computer crimes.
3.  **Notification:**
    *   Determine if the breach triggers notification requirements under *TX Bus. & Com. Code § 521.053* (Data Breach Notification) or GDPR (if EU data subjects involved).
4.  **Lessons Learned:**
    *   Update the *Risk Register*.
    *   Refine *Access Control Policies* (Least Privilege).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Incident Commander (IC)** | Coordinates the overall response; primary liaison between IT and Legal. |
| **Legal Counsel** | Advises on legality of surveillance/containment; manages Legal Hold; interfaces with Law Enforcement; determines regulatory notification requirements. |
| **HR / Volunteer Coordinator** | Manages personnel aspects; conducts interviews; executes termination/suspension; handles internal communications. |
| **IT Security / Forensics** | Performs technical containment; gathers evidence; maintains chain of custody; performs system restoration. |
| **Board of Directors** | Informed only if the incident involves an Officer, significant financial loss, or triggers a "Fundamental Action" threshold. |

### 6. Compliance and Enforcement
Failure to follow this playbook during an investigation may result in the inadmissibility of evidence in court or wrongful termination lawsuits.

**Prohibited Conduct during Investigation:**
*   **"Hacking Back":** IT staff must not access the suspect’s *personal* home network or personal devices without a court order, even if company data is present.
*   **tipping Off:** Discussing the investigation with non-authorized personnel is strictly prohibited.

Any individual found to be an Insider Threat (Malicious) will be subject to immediate termination of employment or volunteer service and referral to law enforcement.

### 7. References
*   **Bylaws of Study GRC Inc.** (Specifically Art. III, VII, IX)
*   **IS-POL-001:** Master Information Security Policy
*   **HR-POL-005:** Acceptable Use Policy (AUP)
*   **HR-POL-012:** Whistleblower Protection Policy
*   **IS-STD-008:** Data Classification Standard
*   **Legal:** Computer Fraud and Abuse Act (18 U.S.C. § 1030)

### 8. Revision History
| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial Draft |