### Cybersecurity Risk Management Strategy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-003 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this **Cybersecurity Risk Management Strategy** is to define Study GRC Inc.'s approach to identifying, assessing, responding to, and monitoring cybersecurity risks. As a Texas non-profit corporation dedicated to open-source education and youth-inclusive communities, we must balance the need for open collaboration with the imperative to protect our members, intellectual property, and reputation.

This policy satisfies **NIST CSF 2.0 (GV.RM)** requirements by establishing the Organization’s risk appetite, tolerance levels, and integration of cybersecurity risk into the broader Enterprise Risk Management (ERM) framework.

### 2. Scope
This policy applies to:
*   **People:** All Directors, Officers, employees, volunteers, contractors, and third-party vendors.
*   **Assets:** All information systems, data (including member PII and youth data), intellectual property, financial assets, and brand reputation.
*   **Operations:** All business processes, including remote work environments, cloud infrastructure, and event management.

**Exclusions:** Risks associated with personal devices not used for Organizational business, provided they do not connect to the Organization’s secure networks or data repositories.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Risk Appetite** | The amount and type of risk the Organization is willing to pursue or retain in anticipation of achieving its strategic objectives. |
| **Risk Tolerance** | The specific maximum risk that the Organization is willing to accept regarding a specific category (e.g., zero tolerance for youth data compromise). |
| **Inherent Risk** | The level of risk before any controls or mitigations are applied. |
| **Residual Risk** | The level of risk remaining after controls have been implemented. |
| **Risk Treatment** | The process of selecting and implementing measures to modify risk (Mitigate, Transfer, Avoid, Accept). |
| **Asset Owner** | The individual responsible for the management and protection of a specific data set or system. |

### 4. Policy Statements

#### 4.1 Risk Management Philosophy
Study GRC Inc. adopts a **risk-aware** culture rather than a risk-averse one. We acknowledge that operating a digital-first, open-source community involves inherent risks. Our strategy is to identify these risks early and manage them to a level that aligns with our charitable mission and fiduciary duties under **Texas Business Organizations Code (TBOC) § 22.221**.

#### 4.2 Risk Appetite and Tolerance
The Board of Directors establishes the following risk appetite levels to guide decision-making:

*   **Low Appetite (Zero Tolerance):**
    *   **Youth Safety:** Any risk that could physically or emotionally harm a minor or expose their PII (COPPA compliance).
    *   **Legal & Compliance:** Non-compliance with laws (e.g., IRS 501(c)(3) status, 2 CFR 200 Federal Grant requirements, GDPR/CCPA).
    *   **Financial Fraud:** Theft, embezzlement, or misuse of donor funds.
*   **Moderate Appetite:**
    *   **Operational Uptime:** As a volunteer-driven community, we accept short-term service interruptions that do not result in data loss.
    *   **Vendor Reliance:** We accept reliance on major SaaS providers (e.g., GitHub, Discord) provided due diligence is performed.
*   **High Appetite:**
    *   **Innovation & Open Source:** We encourage the publication of educational tools and code. We accept the risk that open-source contributions may require rapid patching or iteration, provided no sensitive data is embedded in the code.

#### 4.3 Risk Assessment Methodology
The CISO must establish a formal Risk Assessment Program that includes:
1.  **Asset Inventory:** Maintaining a current inventory of all hardware, software, and data assets.
2.  **Threat Modeling:** Identifying potential threats (e.g., ransomware, phishing, insider threat) relevant to our remote-first operating model.
3.  **Vulnerability Analysis:** Regular scanning and testing of systems.
4.  **Impact Analysis:** Calculating risk based on **Likelihood × Impact**.

Risk assessments must be conducted **annually** or upon significant changes to the environment (e.g., new major software deployment, merger/acquisition).

#### 4.4 Risk Treatment Options
Once a risk is assessed, the Risk Owner (in consultation with the CISO) must select one of the following treatment options:

1.  **Mitigate (Treat):** Implement controls (technical, administrative, or physical) to reduce the risk to an acceptable level.
2.  **Transfer (Share):** Shift the liability to a third party (e.g., purchasing Cyber Liability Insurance or outsourcing to a compliant vendor).
3.  **Avoid (Terminate):** Discontinue the activity or technology causing the risk because it exceeds the Organization's risk appetite.
4.  **Accept (Retain):** Formally acknowledge the risk and choose not to take further action.
    *   *Requirement:* Risk Acceptance for "High" or "Critical" risks requires formal sign-off by the **Executive Director** and notification to the **Board of Directors**.

#### 4.5 Third-Party Risk Management (TPRM)
Pursuant to **2 CFR 200.318**, the Organization must maintain oversight of contractors and vendors.
*   All vendors handling Confidential or Restricted data must undergo a **Vendor Security Risk Assessment (VSRA)** prior to engagement.
*   Contracts must include the right to audit and requirements for breach notification.

#### 4.6 Integration with Enterprise Risk Management (ERM)
Cybersecurity risk shall not be managed in a silo. The CISO shall report cybersecurity risks to the **Audit and Risk Committee** quarterly. These risks must be aggregated with financial, legal, and operational risks to provide the Board with a holistic view of the Organization's health.

#### 4.7 Continuous Monitoring
Risk is dynamic. The Organization shall utilize automated tools and manual reviews to monitor the effectiveness of controls. Key Performance Indicators (KPIs) and Key Risk Indicators (KRIs) must be defined and reported to Operational Leadership.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Board of Directors** | Defines the Organization's Risk Appetite; reviews and approves this Policy; provides oversight via the Audit and Risk Committee (Bylaws Art. VI). |
| **Audit & Risk Committee** | Reviews high-level risk reports; ensures the CISO has adequate resources; monitors compliance with 2 CFR 200 and IRS regulations. |
| **Executive Director (CEO)** | Accountable for the overall implementation of the Risk Strategy; approves Risk Acceptance for high-level operational risks. |
| **Chief Info Security Officer (CISO)** | Develops the Risk Management Framework; facilitates risk assessments; maintains the Risk Register; reports status to the Board. |
| **Asset/System Owners** | Identifies risks within their specific domain (e.g., VP of Education for LMS risks); implements selected risk treatments. |
| **All Staff/Volunteers** | Reports identified risks or vulnerabilities to the security team; adheres to implemented controls. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

**Risk Acceptance Violation:** Accepting a risk on behalf of the Organization without proper authority (as defined in Section 4.4) constitutes a breach of fiduciary duty.

### 7. References
*   **NIST Cybersecurity Framework (CSF) 2.0:** Category GV.RM (Governance Risk Management).
*   **Bylaws of Study GRC Inc.:** Article III (Board Powers) and Article V (Operational Leadership).
*   **2 CFR 200 (Uniform Guidance):** § 200.303 (Internal Controls).
*   **Texas Business Organizations Code:** § 22.221 (General Standards for Directors).
*   **Study GRC Policy:** IS-POL-001 (Master Information Security Policy).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Draft aligned with NIST CSF 2.0 and Bylaws. |