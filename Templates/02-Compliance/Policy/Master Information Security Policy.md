### Master Information Security Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-001 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this Master Information Security Policy (MISP) is to establish the high-level governance framework for protecting the confidentiality, integrity, and availability (CIA) of Study GRC Inc.’s information assets. As a remote-first, 501(c)(3) non-profit organization handling sensitive data—including youth participant information and federal grant data—this policy mandates a risk-based security program aligned with **NIST Cybersecurity Framework (CSF) 2.0** and **ISO/IEC 27001:2022**. This policy serves as the foundation for all subordinate security standards, procedures, and guidelines.

### 2. Scope
This policy applies to:
*   **People:** All employees, Board Directors, officers, volunteers, contractors, and third-party vendors accessing Study GRC Inc. systems or data.
*   **Assets:** All information systems, networks, software, intellectual property, and data (electronic and physical) owned, leased, or operated by the Organization.
*   **Environments:** The Organization’s cloud infrastructure, SaaS applications, and remote work environments (including BYOD endpoints used for organizational business).

**Exclusions:** Publicly available open-source educational resources provided by the Organization are excluded from *confidentiality* controls but remain subject to *integrity* and *availability* controls.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **CIA Triad** | The three pillars of information security: **Confidentiality** (only authorized access), **Integrity** (accuracy and completeness), and **Availability** (accessible when needed). |
| **Information Asset** | Any data, device, or other component of the environment that supports information-related activities. |
| **Incident** | An occurrence that actually or potentially jeopardizes the CIA of information or an information system. |
| **Least Privilege** | The principle that users and systems should have only the minimum access necessary to perform their stated duties. |
| **P.I.I.** | Personally Identifiable Information. Any representation of information that permits the identity of an individual to whom the information applies to be reasonably inferred by either direct or indirect means. |
| **Remote-First** | An operational model where the primary work environment is decentralized, relying on cloud services and residential/public networks rather than a central physical office. |

### 4. Policy Statements

#### 4.1 Governance and Oversight (NIST CSF: GOVERN)
4.1.1 **Board Responsibility:** Pursuant to **Bylaws Article III**, the Board of Directors retains ultimate fiduciary responsibility for information security risk. The Board must approve this Master Policy and review the Organization’s risk profile annually.
4.1.2 **Operational Leadership:** Pursuant to **Bylaws Article V**, the Chief Information Security Officer (CISO) is delegated the authority to design, implement, and enforce the Information Security Program. The CISO reports material risks directly to the Board.
4.1.3 **Policy Hierarchy:** In the event of a conflict between this policy and a subordinate standard or procedure, this policy prevails. In the event of a conflict between this policy and applicable law (e.g., Texas Business & Commerce Code), the law prevails.

#### 4.2 Asset Management and Classification (NIST CSF: IDENTIFY)
4.2.1 **Inventory:** The Organization must maintain an accurate, up-to-date inventory of all physical devices, software, and cloud assets.
4.2.2 **Data Classification:** All data must be classified into one of three categories to determine appropriate controls:
*   **Public:** Information intended for public release (e.g., Open Source curriculum, website content).
*   **Internal:** Business operations data not intended for public disclosure (e.g., internal memos, slack history).
*   **Confidential/Restricted:** Sensitive data requiring strict protection (e.g., Youth/Minor PII, donor financial data, employee HR records, passwords).
4.2.3 **Youth Protection:** Data pertaining to minors (under 18) is automatically classified as **Confidential/Restricted** and requires the highest level of access control and encryption.

#### 4.3 Protection Mechanisms (NIST CSF: PROTECT)
4.3.1 **Access Control:** Access to systems and data must be granted on a "Need-to-Know" and "Least Privilege" basis.
*   **MFA:** Multi-Factor Authentication (MFA) is mandatory for all remote access, administrative accounts, and access to Confidential data.
*   **Review:** User access rights must be reviewed at least semi-annually.
4.3.2 **Cryptography:**
*   **Data at Rest:** All Confidential data stored on laptops, mobile devices, or cloud databases must be encrypted.
*   **Data in Transit:** All data transmission over public networks (Internet) must use strong encryption protocols (e.g., TLS 1.2+).
4.3.3 **Remote Work & BYOD:**
*   Personnel using personal devices (BYOD) for organizational business must adhere to the *Remote Work Security Standard*, including the installation of required security agents or MDM profiles where applicable.
*   Use of public Wi-Fi for accessing Confidential data is prohibited unless a secure VPN is utilized.
4.3.4 **Awareness Training:** All personnel must complete security awareness training upon hire and annually thereafter. Phishing simulations must be conducted periodically.

#### 4.4 Detection and Monitoring (NIST CSF: DETECT)
4.4.1 **Continuous Monitoring:** The Organization must employ automated tools (e.g., Endpoint Detection and Response, Cloud Security Posture Management) to detect anomalous activity across its decentralized network.
4.4.2 **Logging:** Audit logs recording privileged user access, failed login attempts, and changes to security configurations must be generated, protected from tampering, and retained for a minimum of one (1) year.

#### 4.5 Incident Response (NIST CSF: RESPOND)
4.5.1 **Incident Response Plan (IRP):** The CISO must maintain a tested Incident Response Plan.
4.5.2 **Reporting:** All personnel are required to report suspected security incidents to the Security Team immediately.
4.5.3 **Notification:** In the event of a confirmed data breach, the Organization must comply with notification requirements defined in **Texas Business & Commerce Code § 521.053** and applicable federal grant regulations (2 CFR 200).

#### 4.6 Business Continuity and Recovery (NIST CSF: RECOVER)
4.6.1 **Backups:** Critical data must be backed up regularly. Backups must be encrypted, immutable (where feasible to prevent ransomware destruction), and tested for restorability at least annually.
4.6.2 **Disaster Recovery:** The Organization must maintain a Disaster Recovery Plan (DRP) capable of restoring critical operations within the Recovery Time Objective (RTO) defined by the Board.

#### 4.7 Third-Party Risk Management
4.7.1 **Vendor Assessment:** Third-party vendors with access to Confidential data must undergo a security risk assessment prior to contract execution.
4.7.2 **Contracts:** Contracts with service providers must include specific provisions regarding data protection, breach notification, and the right to audit.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Board of Directors** | Approves the Master Information Security Policy; provides budget and resources; oversees high-level risk management. |
| **Executive Director (CEO)** | Ensures organizational alignment with security policies; champions a culture of security; enforces disciplinary actions for non-compliance. |
| **Chief Information Security Officer (CISO)** | Develops and maintains security policies; manages the security team; oversees incident response; reports compliance status to the Board. |
| **Data Owners** | Classify data assets; authorize access requests based on business need; review access privileges. |
| **All Personnel** | Adhere to all security policies; protect credentials; report suspected incidents immediately. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment, volunteer assignment, or contract. Legal action may be pursued for severe violations involving theft, fraud, or intentional sabotage.

**Exceptions:** Any exception to this policy must be documented in writing, detailing the specific risk acceptance, and approved by the CISO. Exceptions involving Confidential data require Executive Director approval.

### 7. References
*   **Study GRC Inc. Bylaws:** Article III (Governance), Article V (Operational Leadership), Article IX (Data Protection).
*   **NIST Cybersecurity Framework (CSF) 2.0**
*   **ISO/IEC 27001:2022:** Clause 5 (Organizational Controls).
*   **Texas Business & Commerce Code:** Chapter 521 (Identity Theft Enforcement and Protection).
*   **2 CFR 200.303:** Internal Controls (Federal Grants).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Policy Draft aligned with Bylaws and NIST CSF 2.0. |