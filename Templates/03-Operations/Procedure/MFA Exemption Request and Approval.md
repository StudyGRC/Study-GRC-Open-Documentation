### MFA Exemption Request and Approval

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-015 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Security Operations Manager |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to define the strict, risk-based process for requesting, reviewing, and approving exemptions to the Organization’s Multi-Factor Authentication (MFA) Mandate. While MFA is a non-negotiable standard for protecting Study GRC Inc.’s remote-first infrastructure, the Organization recognizes that rare technical limitations (e.g., legacy systems, specific accessibility needs, or non-interactive service accounts) may require temporary or permanent deviations.

This procedure ensures that any deviation is formally documented, risk-assessed, subjected to compensating controls, and time-bound, ensuring alignment with **NIST SP 800-63B** and **CISA Cybersecurity Performance Goals (CPGs)**.

### 2. Scope
This procedure applies to:
*   **Users:** All employees, volunteers, Board Directors, and contractors.
*   **Assets:** All Organization-owned or managed systems, applications, cloud tenants (e.g., Google Workspace, Azure, AWS), and VPNs.
*   **Accounts:** Human user accounts and non-human service accounts.

**Exclusions:**
*   Public-facing resources intended for anonymous access (e.g., public website read-only pages) do not require MFA and are outside the scope of this exemption process.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **MFA (Multi-Factor Authentication)** | A security system that requires more than one method of authentication from independent categories of credentials to verify the user's identity for a login or other transaction. |
| **Compensating Control** | An alternative security measure put in place to mitigate the risk that arises when a primary security control (MFA) cannot be implemented. |
| **Service Account** | A non-human account used by an application or service to interact with the operating system or other applications. |
| **Risk Acceptance** | A formal decision by leadership to acknowledge a residual risk and continue operations without applying a specific control, typically for a defined period. |
| **CISO** | Chief Information Security Officer, as defined in **Bylaws Article V, Section 5.2**. |

### 4. Procedures

#### 4.1 Valid Justification Criteria
Requests for MFA exemptions will **only** be considered for the following reasons. Convenience is **never** a valid justification.

1.  **Technical Incompatibility:** The legacy application or system does not support modern authentication protocols (SAML, OIDC) or TOTP/FIDO2 integration.
2.  **Non-Interactive Service Accounts:** Automated scripts or backend services where human interaction for MFA challenges is technically impossible.
3.  **Accessibility/Disability:** A documented medical or physical condition prevents the user from utilizing standard MFA hardware/software, and no accessible MFA alternative (e.g., YubiKey) is viable.
4.  **Emergency "Break Glass" Accounts:** Specific administrative accounts designated for catastrophic recovery where MFA infrastructure might be unavailable.

#### 4.2 Request Initiation
1.  The Requestor must submit a ticket via the IT Service Management (ITSM) portal using the "Security Exception Request" form.
2.  The request must include:
    *   **Asset/Account Name:** Specific target of the exemption.
    *   **Business Justification:** Detailed explanation of why MFA cannot be applied.
    *   **Duration:** Start date and requested end date (Maximum 12 months).
    *   **Data Classification:** The sensitivity of data accessible by this account (Public, Internal, Confidential, Restricted).

#### 4.3 Risk Assessment and Compensating Controls
Upon receipt, the Security Team must perform a risk assessment within three (3) business days.

1.  **Verify Justification:** Confirm technical limitations or accessibility needs.
2.  **Determine Risk Level:**
    *   *High:* Account has administrative privileges or access to Confidential/Restricted data (e.g., Donor PII, Student Records).
    *   *Medium:* Account has internal access but limited privileges.
    *   *Low:* Account has isolated access to non-sensitive data.
3.  **Assign Compensating Controls:** The Security Team must mandate at least one of the following controls to replace MFA:
    *   **IP Allow-listing:** Restrict access to a static, known IP address (e.g., the office VPN gateway).
    *   **Password Complexity:** Increase password length requirement to 25+ characters.
    *   **Rotation Frequency:** Force password rotation every 30 days (for service accounts).
    *   **Alerting:** Configure immediate SIEM alerts for *any* login activity on this account.

#### 4.4 Approval Authority Matrix
Approval is based on the residual risk level after compensating controls are applied.

| Risk Level | Required Approver(s) |
| :--- | :--- |
| **Low** | IT Manager |
| **Medium** | CISO |
| **High** | CISO **AND** Executive Director (CEO) |

*Note: Per **Bylaws Article V**, the CISO holds authority over data privacy and security. However, High-Risk acceptances involving potential impact to the Organization's reputation or liability require Executive Director sign-off.*

#### 4.5 Implementation and Configuration
1.  **Configuration:** IT Administrators configure the exemption in the Identity Provider (IdP) or system settings.
2.  **Documentation:** The ticket is updated with:
    *   The specific configuration change made.
    *   The implemented compensating controls.
    *   The expiration date set in the system.
3.  **Verification:** The Requestor verifies access. The Security Team verifies that compensating controls (e.g., IP restriction) are active.

#### 4.6 Monitoring and Review
1.  **Continuous Monitoring:** All accounts with MFA exemptions are tagged in the SIEM. Any anomaly (e.g., login from a new country, failed attempts) triggers a Sev-1 Security Incident.
2.  **Quarterly Audit:** The Security Team reviews all active exemptions quarterly.
3.  **Expiration:**
    *   Exemptions expire automatically on the defined end date.
    *   Seven (7) days prior to expiration, the Requestor receives a notification.
    *   **Renewal:** Requires a new request and re-assessment. Renewals are not automatic.

#### 4.7 Revocation
The CISO reserves the right to revoke any exemption immediately and without notice if:
1.  Threat intelligence indicates active targeting of the specific system.
2.  The account is compromised.
3.  The user/system violates the compensating controls (e.g., accessing from a non-allow-listed IP).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Requestor** | Submit accurate justification; adhere strictly to assigned compensating controls. |
| **Security Analyst** | Review technical feasibility; assign risk level; define compensating controls. |
| **IT Administrator** | Implement the technical configuration for the exemption and controls. |
| **CISO** | Final authority on Medium/High risk exemptions; ensures alignment with risk appetite. |
| **Executive Director** | Co-approver for High-Risk exemptions that may impact organizational liability. |

### 6. Compliance and Enforcement
**Strict Enforcement:** Bypassing MFA mechanisms without a formally approved exemption ticket is a violation of the **Master Information Security Policy**.

Failure to comply with this procedure—including falsifying justification for an exemption or disabling MFA without authorization—may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-005:** Access Control Policy
*   **NIST SP 800-63B:** Digital Identity Guidelines (Authentication and Lifecycle Management)
*   **CISA CPG 2.1:** Multifactor Authentication

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Release aligned with Bylaws and NIST standards. |