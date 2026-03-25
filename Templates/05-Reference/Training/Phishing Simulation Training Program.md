### Phishing Simulation Training Program

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-TRN-002 |
| **Document Type** | Training / Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of the Phishing Simulation Training Program is to strengthen the human firewall of Study GRC Inc. by assessing and improving the organization's resilience against social engineering attacks. This program establishes a controlled environment to test user awareness, identify high-risk user groups, and provide immediate "teachable moments" to reduce the likelihood of a successful data breach, ransomware infection, or credential theft. This program supports the data protection mandates outlined in **Bylaws Article IX**.

### 2. Scope
This program applies to all individuals with an active Study GRC Inc. email account (`@studygrc.org`) or access to the Organization’s internal communication systems.
*   **In Scope:** Board of Directors, Officers, Employees, Contractors, and Volunteers.
*   **Exclusions:** External vendors without internal email accounts, unless specifically integrated into the Organization's tenant.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Phishing** | A cybercrime in which a target is contacted by email, telephone, or text message by someone posing as a legitimate institution to lure individuals into providing sensitive data. |
| **Spear Phishing** | A highly targeted phishing attempt customized for a specific individual or role (e.g., targeting the CFO with a fake invoice). |
| **Teachable Moment** | A landing page displayed immediately after a user clicks a simulated phishing link, explaining that it was a test and highlighting the "red flags" they missed. |
| **Click Rate** | The percentage of users who clicked on a link or opened an attachment within a simulated phishing email. |
| **Report Rate** | The percentage of users who correctly identified and reported the simulated phishing email using the approved reporting tool. |

### 4. Program Standards and Procedures

#### 4.1 Simulation Frequency and Randomization
To ensure continuous vigilance in our remote-first environment:
1.  **Frequency:** The CISO must execute phishing simulations at least **monthly**.
2.  **Randomization:** Campaigns must be randomized to prevent users from warning one another ("The prairie dog effect"). Not all users will receive the same email at the same time.
3.  **Campaign Variety:** Simulations must vary in difficulty (Levels 1-5) and attack vector (e.g., credential harvesting, attachment opening, link clicking, CEO fraud).

#### 4.2 The "Teachable Moment" Protocol
The primary goal of this program is education, not punishment.
1.  **Immediate Feedback:** Users who fail a simulation (click a link or enter credentials) must be immediately redirected to a "Teachable Moment" landing page.
2.  **Content:** This page must display:
    *   A notification that this was a simulation.
    *   A screenshot of the email they received.
    *   Annotated "Red Flags" (e.g., mismatched URL, urgency, spelling errors) that the user missed.
3.  **Non-Punitive Tone:** The messaging must be constructive, encouraging the user to be more vigilant next time.

#### 4.3 Remedial Training Requirements
Users who repeatedly fail simulations require additional support.
1.  **First Failure:** User receives the immediate Teachable Moment. No further action required.
2.  **Second Failure (within 6 months):** User is automatically enrolled in a mandatory 15-minute "Phishing Awareness Refresher" course via the Learning Management System (LMS).
3.  **Chronic Failure (3+ failures within 6 months):**
    *   User accounts may be subject to enhanced security restrictions (e.g., removal of administrative privileges).
    *   A mandatory 1:1 review session with the CISO or IT Security designee is required.
    *   The user's manager is notified to discuss performance regarding information security responsibilities.

#### 4.4 Reporting Suspicious Emails
1.  **Phish Alert Button (PAB):** All organizational email clients must be equipped with a "Report Phishing" button.
2.  **Positive Reinforcement:** Users who correctly report a simulated phishing email shall receive an immediate "Congratulations" notification confirming the simulation.
3.  **Real Threats:** Users who report non-simulated (real) suspicious emails must receive confirmation from the Security Team regarding the outcome of the analysis when feasible.

#### 4.5 Prohibited Simulation Content
To maintain ethical standards and a healthy workplace culture, simulations **must not** utilize the following themes:
1.  **Personal Tragedies:** Notices of death, illness, or accidents regarding family members.
2.  **HR/Legal Threats:** Fake termination notices or sexual harassment allegations.
3.  **Political/Religious Content:** Content that could be construed as harassment or discrimination under the **Anti-Harassment and Non-Discrimination Policy**.

#### 4.6 Technical Configuration
1.  **Whitelisting:** The IT Department must whitelist the simulation vendor's IP addresses and domains to ensure delivery and prevent the simulations from being blocked by the spam filter.
2.  **Data Privacy:** The simulation platform must not store user passwords if a "credential harvesting" test is used. Data entered into fake forms must be immediately discarded.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Designs campaigns, analyzes metrics, and reports trends to the Executive Director. Ensures content is ethical and educational. |
| **IT Department** | Configures email gateways to whitelist simulation traffic and deploys the "Report Phishing" button to all endpoints. |
| **Managers** | Discusses chronic failure rates with employees as a performance and risk issue; supports remedial training time. |
| **Employees / Volunteers** | Actively inspects emails for red flags; reports suspicious emails using the designated tool; completes remedial training if assigned. |
| **Board of Directors** | Participates in simulations; reviews high-level aggregate risk data regarding organizational resilience. |

### 6. Compliance and Enforcement
Participation in the Phishing Simulation Training Program is mandatory.
*   **Metric Tracking:** Click rates and reporting rates are tracked key performance indicators (KPIs) for the Organization's security posture.
*   **Disciplinary Action:** While failing a simulation is a training opportunity, **willful refusal** to complete assigned remedial training or attempts to technically circumvent the testing platform may result in disciplinary action, up to and including termination of employment or volunteer assignment.

### 7. References
*   **Bylaws Article IX:** Policies & Data Protection.
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-005:** Acceptable Use Policy (AUP).
*   **NIST CSF 2.0 (PR.AT-01):** Personnel are provided with awareness and training so that they can perform their information security-related duties and responsibilities.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial release of Phishing Simulation Program. |