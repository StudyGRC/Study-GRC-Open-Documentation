### Role-Based Security Training Requirements

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-066 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to define the mandatory cybersecurity training requirements for specific roles within Study GRC Inc. While general security awareness is required for all personnel, individuals with access to sensitive data, financial systems, or critical infrastructure require specialized instruction to mitigate elevated risks.

This Standard satisfies **NIST CSF Control PR.AT-3**, ensuring that personnel are provided cybersecurity education relevant to their specific duties, and aligns with **2 CFR 200.303** regarding internal controls for federal grant compliance.

### 2. Scope
This Standard applies to all Directors, Officers, employees, contractors, and volunteers of Study GRC Inc. who hold "Privileged Roles" or "High-Risk Roles" as defined herein.

*   **Inclusions:** Board of Directors, Operational Officers (C-Suite), IT/Engineering staff, Finance/HR personnel, and Youth Program Coordinators.
*   **Exclusions:** General Community Participants and Supporting Members who do not hold volunteer leadership positions or access organizational systems.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Privileged User** | Any user with administrative rights (e.g., "root," "admin," "super-user") to systems, code repositories (GitHub), or cloud environments (AWS/Azure/GCP). |
| **Role-Based Training** | Targeted education modules designed to address the specific threats, vulnerabilities, and compliance obligations associated with a specific job function. |
| **COPPA** | Children's Online Privacy Protection Act; federal law regulating the collection of data from children under 13. |
| **BEC** | Business Email Compromise; a specific type of phishing attack targeting executives and finance staff to authorize fraudulent transfers. |
| **OWASP Top 10** | A standard awareness document for developers and web application security. |

### 4. Standards

#### 4.1 Training Matrix and Curricula
All personnel assigned to the roles listed below must complete the designated training modules in addition to the Annual General Security Awareness Training.

**4.1.1 Board of Directors & Executive Officers**
*   **Focus:** Strategic Risk, Fiduciary Responsibility, Whaling/Executive Phishing.
*   **Mandatory Modules:**
    *   Business Email Compromise (BEC) defense.
    *   Cybersecurity Governance and Oversight (NIST/NACD principles).
    *   Crisis Management and Incident Response decision-making.
    *   Mobile Device Security for traveling executives.

**4.1.2 IT Administrators, DevOps, and Engineering**
*   **Focus:** System Hardening, Secure Architecture, Supply Chain Risk.
*   **Mandatory Modules:**
    *   Secure Coding Practices (OWASP Top 10).
    *   Cloud Security Fundamentals (Shared Responsibility Model).
    *   Secrets Management (API keys, credentials in code).
    *   Open Source Software (OSS) vulnerability management and licensing.
    *   Incident Response technical execution.

**4.1.3 Finance and Procurement Staff**
*   **Focus:** Fraud Prevention, Federal Compliance.
*   **Mandatory Modules:**
    *   Wire Transfer Fraud and Social Engineering.
    *   Vendor verification and anti-kickback procedures.
    *   **2 CFR 200** Uniform Guidance (Grant financial compliance).
    *   PCI-DSS awareness (if handling credit card data directly).

**4.1.4 Human Resources and Legal**
*   **Focus:** Data Privacy, Insider Threat.
*   **Mandatory Modules:**
    *   Handling PII and Sensitive Personal Data (GDPR/CCPA/TDPSA).
    *   Insider Threat detection and personnel vetting.
    *   Secure onboarding and offboarding procedures.

**4.1.5 Youth Program Coordinators & Moderators**
*   **Focus:** Child Safety, Data Minimization.
*   **Mandatory Modules:**
    *   **COPPA** Compliance and Data Collection limits.
    *   Digital Grooming prevention and detection.
    *   Managing minors in online communities (Discord/Slack safety).
    *   Mandatory Reporting of suspected abuse (Texas Family Code).

#### 4.2 Timing and Frequency
*   **Initial Training:** Personnel assuming a Privileged or High-Risk role must complete the role-specific training within **14 days** of appointment or hire.
*   **Access Contingency:** Privileged access (e.g., Admin rights, bank access) shall not be granted until the initial role-based training is verified as complete.
*   **Refresher Training:** Role-based training must be repeated **annually**.
*   **Triggered Training:** Significant changes to the threat landscape or a material change in job duties will trigger an immediate requirement for updated training.

#### 4.3 Competency and Validation
*   **Testing:** All training modules must conclude with a competency assessment (quiz/exam).
*   **Passing Score:** A minimum score of **80%** is required to certify completion.
*   **Phishing Simulations:**
    *   **Finance/Execs:** Must undergo targeted "Spear Phishing" simulations quarterly.
    *   **IT/Devs:** Must undergo "Credential Harvesting" simulations quarterly.

#### 4.4 Remedial Training
Any individual who fails a competency assessment twice, or falls victim to a phishing simulation, must undergo:
1.  Immediate revocation of privileged access (if deemed necessary by the CISO).
2.  Mandatory 1-on-1 remedial coaching with the Security Team.
3.  Re-certification of the training module within **5 business days**.

#### 4.5 Content Maintenance
The CISO must review and update the training curriculum **bi-annually** to ensure alignment with:
*   Emerging threat vectors (e.g., AI-generated attacks).
*   Changes in regulatory requirements (e.g., updates to Texas Business Organizations Code or Federal Grant rules).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO** | Develops/selects training content; monitors compliance; reports metrics to the Board. |
| **Department Heads** | Ensure their staff complete assigned training; enforce remediation for failures. |
| **HR Department** | Assigns training tracks during onboarding based on job description. |
| **Employees/Volunteers** | Complete all assigned training within deadlines; report technical issues with training platforms. |
| **Board of Directors** | Allocates budget for training resources; completes Director-specific training. |

### 6. Compliance and Enforcement
Failure to comply with this Standard is a violation of the Organization's security protocols.
*   **First Offense:** Verbal warning and immediate suspension of privileged access until training is completed.
*   **Second Offense:** Written warning and potential removal from the specific role or project.
*   **Continued Non-Compliance:** Termination of employment or volunteer assignment for cause, as defined in **Bylaws Article III, Section 3.6** (for Directors) or the Employee Handbook.

### 7. References
*   **NIST CSF 2.0 (PR.AT-03):** Personnel are provided cybersecurity awareness education and are trained to perform their cybersecurity-related duties.
*   **2 CFR 200.303(e):** Internal controls for federal award compliance.
*   **Study GRC Bylaws Article IX:** Intellectual Property & Data Protection.
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-005:** Access Control Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Release aligned with NIST PR.AT-3 |