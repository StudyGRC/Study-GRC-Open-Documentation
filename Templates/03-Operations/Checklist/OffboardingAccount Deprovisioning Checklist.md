### Offboarding and Account Deprovisioning Checklist

| Document Control | |
| :--- | :--- |
| **Document ID** | HR-CHK-005 |
| **Document Type** | Checklist / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director & CISO |
| **Document Owner** | Director of Human Resources |
| **Classification** | Internal |

### 1. Purpose
The purpose of this checklist is to ensure the secure, consistent, and compliant separation of individuals from Study GRC Inc. This process mitigates cybersecurity risks associated with unauthorized access, ensures the retention of organizational knowledge and Intellectual Property in accordance with **Bylaws Article IX**, and facilitates the recovery of organizational assets. This document satisfies security controls regarding access revocation (NIST PR.AC-4) and asset management.

### 2. Scope
This checklist applies to all individuals separating from the Organization, regardless of the reason for separation (voluntary or involuntary).
*   **Applies to:** Employees, Contractors, Board Directors, Officers, and Volunteers with system access.
*   **Exclusions:** Community Participants (Non-Voting) with no internal system access beyond public-facing forums.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Deprovisioning** | The technical process of revoking digital identities and removing access rights to software, networks, and data. |
| **Involuntary Separation** | Termination initiated by the Organization (e.g., for cause, layoff). Requires immediate access revocation. |
| **Privileged Account** | An account with elevated permissions (e.g., System Administrator, Financial Approver, Social Media Manager). |
| **Work Product** | As defined in **Bylaws Article IX (9.3)**, all content, code, and materials created during service, which are the sole property of the Organization. |

### 4. Procedures and Checklist

#### 4.1 Phase I: Notification and Planning (1-2 Weeks Prior)
*Applicable for Voluntary Resignation. For Involuntary Termination, skip to Phase III.*

*   [ ] **Resignation Acceptance:** HR/Board receives written resignation.
*   [ ] **Separation Date Confirmation:** Establish the final date of employment/service.
*   [ ] **Stakeholder Notification:** Notify IT/Security, Finance, and the direct manager of the upcoming departure.
*   [ ] **Public Communication Plan:** Determine if/when to notify the community or partners (Required for **Board Officers** per Bylaws Article IV).

#### 4.2 Phase II: Knowledge Transfer & IP Preservation (Final Week)
*   [ ] **Work Product Audit:** Verify all "Work Product" (Bylaws Art. IX) is stored on Organization-controlled drives (Google Drive/SharePoint), not personal devices.
*   [ ] **Code Repository Commit:** Ensure all code is committed to the Organization’s GitHub/GitLab repositories.
*   [ ] **Credential Handover:** Retrieve passwords for any shared accounts (e.g., social media) not managed via SSO.
*   [ ] **Project Status Handoff:** Manager reviews outstanding tasks and reassigns them in the Project Management tool (e.g., Jira/Asana).
*   [ ] **Conflict of Interest Update:** Ensure the departing individual has no lingering commitments that bind the Organization.

#### 4.3 Phase III: Access Revocation (The "Kill Switch")
*Timing: Effective immediately upon termination (Involuntary) or at close of business on the final day (Voluntary).*

**Identity & Access Management (IAM)**
*   [ ] **Disable SSO/IdP Account:** Suspend the user in the primary Identity Provider (e.g., Google Workspace, Azure AD, Okta). *Do not delete immediately—suspend to preserve data.*
*   [ ] **Force Session Logout:** Trigger a "sign out of all sessions" to kill active web tokens on personal/remote devices.
*   [ ] **MFA Token Revocation:** Revoke/delete registered MFA tokens or YubiKeys associated with the user.
*   [ ] **Reset Shared Passwords:** If the user knew shared passwords (e.g., "admin@" accounts), rotate those credentials immediately.

**Specific Application Access**
*   [ ] **Remove from Communication Platforms:** Deactivate account in Slack/Discord/Teams.
*   [ ] **Revoke Code Repository Access:** Remove user from GitHub/GitLab organizations.
*   [ ] **Revoke Financial Access:** Remove access to banking portals, expense management (Expensify/Brex), and payroll systems.
*   [ ] **Revoke Cloud Infrastructure:** Remove IAM users/roles from AWS/Azure/GCP.
*   [ ] **Revoke Social Media:** Remove Admin/Editor rights from LinkedIn, Twitter/X, and Facebook pages.
*   [ ] **VPN/Remote Access:** Revoke VPN certificates and remove from the allowed remote access group.

#### 4.4 Phase IV: Asset Recovery & Financial Closure
*   [ ] **Hardware Return:** Issue a pre-paid shipping label to the remote employee/volunteer for the return of laptops, monitors, and hardware tokens (YubiKeys).
*   [ ] **Remote Wipe (If applicable):** If the device cannot be returned immediately or is lost, initiate a remote wipe via MDM (Mobile Device Management).
*   [ ] **Corporate Card Cancellation:** Cancel physical and virtual corporate credit cards immediately.
*   [ ] **Expense Reconciliation:** Process final expense reports; deduct outstanding personal expenses from final pay (if compliant with TX Labor Code).
*   [ ] **Final Payroll:** Process final paycheck, including payout of accrued PTO (if required by policy).

#### 4.5 Phase V: Data Retention & Legal Hold
*   [ ] **Email Forwarding/Archiving:** Configure email forwarding to the manager or convert the account to a "Shared Mailbox" for monitoring.
*   [ ] **Drive Transfer:** Transfer ownership of Google Drive/OneDrive files to a service account or the manager.
*   [ ] **Legal Hold Check:** Verify if the individual is involved in active litigation or investigations. If yes, **freeze** all data deletion policies for their accounts.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **HR / Operations** | Initiates the offboarding request; conducts exit interview; manages asset recovery logistics. |
| **Manager** | Ensures knowledge transfer; verifies IP handover; identifies specific app access to be revoked. |
| **IT / CISO** | Executes technical deprovisioning (Phase III); manages data retention/archiving; performs remote wipes. |
| **Finance** | Cancels credit cards; processes final payments; removes banking access. |

### 6. Compliance and Enforcement
Failure to execute this checklist may result in data breaches, loss of Intellectual Property, or regulatory non-compliance.
*   **Negligence:** Managers or IT staff who fail to timely deprovision access resulting in a security incident may face disciplinary action.
*   **Unauthorized Access:** Departing personnel who attempt to access systems after their termination date will be subject to legal action under the **Computer Fraud and Abuse Act (CFAA)** and **Texas Penal Code § 33.02**.
*   **IP Theft:** Retention of Organization data or code after separation is a violation of **Bylaws Article IX** and will be pursued legally.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article IX - Intellectual Property; Article V - Operational Leadership)
*   **NIST CSF 2.0:** PR.AC-4 (Access permissions are managed, incorporating the principles of least privilege and separation of duties).
*   **ISO/IEC 27001:2022:** Annex A 5.8 (Information security in project management) and A 8.1.4 (Return of assets).
*   **HR-POL-001:** Employee Handbook (Separation Policy).
*   **IS-POL-001:** Master Information Security Policy (Access Control).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial creation of standard checklist. |