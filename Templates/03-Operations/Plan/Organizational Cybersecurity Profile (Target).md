### Organizational Cybersecurity Profile (Target)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PLN-005 |
| **Document Type** | Plan |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this **Organizational Cybersecurity Profile (Target)** is to define the desired state of cybersecurity outcomes for Study GRC Inc. ("the Organization"). Utilizing the NIST Cybersecurity Framework (CSF) 2.0, this plan establishes the specific security controls, risk management capabilities, and governance structures the Organization aims to achieve within the next 12 to 24 months.

This document serves as the strategic roadmap to bridge the gap between the Organization's *Current Profile* and its risk tolerance objectives, ensuring the protection of member data, the integrity of open-source educational resources, and compliance with federal grant requirements (2 CFR 200) and youth protection laws (COPPA).

### 2. Scope
This plan applies to the entire Organization, including:
*   **Personnel:** All employees, Board Directors, Operational Officers, and volunteers.
*   **Assets:** All hardware, software, cloud services (SaaS/IaaS), and intellectual property owned or leased by the Organization.
*   **Data:** All classes of data as defined in the *Data Classification Standard*, with specific emphasis on Personally Identifiable Information (PII) of minors and donors.

**Exclusions:**
*   Personal devices of volunteers are excluded from direct management but are subject to the *Bring Your Own Device (BYOD) Policy* and access control restrictions defined herein.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **NIST CSF 2.0** | The National Institute of Standards and Technology Cybersecurity Framework, organized into six functions: Govern, Identify, Protect, Detect, Respond, and Recover. |
| **Target Profile** | The desired state of the Organization's cybersecurity posture based on business objectives and risk appetite. |
| **Implementation Tier** | A qualitative measure of organizational cybersecurity risk management practices (Tier 1: Partial to Tier 4: Adaptive). |
| **Zero Trust** | A security model that assumes no user or device is trustworthy by default, regardless of location, requiring strict identity verification. |
| **Critical Services** | Systems essential to the Organization's mission, including the Learning Management System (LMS), financial systems, and member databases. |

### 4. Plan Statements (Target State Objectives)

The Organization targets an overall **NIST Implementation Tier 3 (Repeatable)**. The following subsections detail the specific target outcomes for each CSF Function.

#### 4.1 GOVERN (GV) - Target State
*   **GV.OC-01 (Organizational Context):** The Board of Directors shall integrate cybersecurity risk into the Organization’s enterprise risk management strategy. Cybersecurity is a standing agenda item for the Audit & Risk Committee.
*   **GV.RM-01 (Risk Management Strategy):** A formal risk appetite statement is approved by the Board. Risk assessments are conducted annually and prior to any *Fundamental Action* (as defined in Bylaws Article X) or major system acquisition.
*   **GV.SC-01 (Supply Chain):** All third-party vendors handling PII or financial data must undergo a *Vendor Security Risk Assessment (VSRA)* prior to contract execution. Contracts must include the Organization’s standard Data Protection Addendum (DPA).

#### 4.2 IDENTIFY (ID) - Target State
*   **ID.AM-01 (Asset Management):** An automated inventory of 100% of Organization-owned devices and authorized SaaS applications is maintained in real-time. Shadow IT is identified and remediated quarterly.
*   **ID.RA-01 (Risk Assessment):** Vulnerability scans are automated and run weekly on all web-facing assets. Penetration testing is conducted annually by an independent third party.
*   **ID.IM-01 (Improvement):** A "Lessons Learned" register is maintained. Post-incident reviews are mandatory for all incidents classified as "Medium" severity or higher.

#### 4.3 PROTECT (PR) - Target State
*   **PR.AA-01 (Identity Management):** Multi-Factor Authentication (MFA) is enforced on **100%** of accounts (staff, volunteers, and Board members) accessing Organization systems. No exceptions.
*   **PR.DS-01 (Data Security):**
    *   **At Rest:** All endpoints (laptops/mobiles) and databases are encrypted (AES-256).
    *   **In Transit:** TLS 1.2 or higher is enforced for all web traffic.
    *   **Minors:** Data belonging to users under 13 is segregated and subject to strict access controls compliant with COPPA and the *Child and Youth Safeguarding Policy*.
*   **PR.AT-01 (Awareness & Training):**
    *   All new personnel (including volunteers) complete security awareness training within 7 days of onboarding.
    *   Phishing simulations are conducted monthly; users who fail must retake training.
*   **PR.PS-01 (Platform Security):** A "Cloud-First, Zero-Trust" architecture is fully implemented. Access is granted based on the Principle of Least Privilege (PoLP) and Just-in-Time (JIT) provisioning where feasible.

#### 4.4 DETECT (DE) - Target State
*   **DE.CM-01 (Continuous Monitoring):** A centralized logging solution (SIEM) aggregates logs from the Identity Provider (IdP), Endpoint Detection & Response (EDR), and cloud infrastructure.
*   **DE.AE-01 (Anomalies & Events):** Automated alerts are configured for high-risk indicators, including:
    *   Impossible travel logins.
    *   Mass data export/download.
    *   Privilege escalation attempts.
*   **DE.DP-01 (Detection Processes):** The detection capability is tested quarterly via Tabletop Exercises (TTX).

#### 4.5 RESPOND (RS) - Target State
*   **RS.MA-01 (Incident Management):** An *Incident Response Plan (IRP)* is fully operational. The Incident Response Team (IRT) has defined roles, including Legal Counsel for breach notification analysis (TX Bus. & Com. Code § 521.053).
*   **RS.CO-01 (Communications):** Pre-approved communication templates for stakeholders (members, donors, regulators) are drafted and reviewed by Legal.
*   **RS.AN-01 (Analysis):** Forensic readiness is established. Logs are retained for a minimum of 365 days to support investigation.

#### 4.6 RECOVER (RC) - Target State
*   **RC.RP-01 (Recovery Planning):** A *Business Continuity Plan (BCP)* and *Disaster Recovery Plan (DRP)* are documented and tested annually.
*   **RC.BR-01 (Backup & Restore):**
    *   Critical data is backed up daily.
    *   Backups are immutable (WORM storage) to prevent ransomware encryption.
    *   Restoration tests are performed quarterly to verify Recovery Time Objectives (RTO).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Board of Directors** | Approves the Target Profile and allocates budget/resources to achieve these objectives. Reviews progress quarterly. |
| **Executive Director (CEO)** | Ensures operational alignment between business goals and security targets. Champions the security culture. |
| **Chief Info Security Officer (CISO)** | Owns this Plan. Directs the technical implementation, monitors progress, and reports gaps to the Board. |
| **VP of Education & Training** | Ensures educational platforms (LMS) meet the *Protect* and *Recover* targets to maintain service availability. |
| **IT/Security Team** | Executes technical controls (MFA, Encryption, SIEM configuration) required to meet the Target Profile. |
| **Volunteers & Staff** | Adhere to implemented controls (e.g., using MFA, reporting incidents) to support the target state. |

### 6. Compliance and Enforcement
Achievement of this Target Profile is a strategic priority for the Organization.
*   **Gap Analysis:** The CISO must perform a gap analysis against this Target Profile every six (6) months.
*   **Reporting:** Material deviations or failure to progress toward the Target Profile must be reported to the Audit & Risk Committee.
*   **Enforcement:** Failure to adhere to the policies supporting this profile (e.g., bypassing MFA) may result in disciplinary action, up to and including termination of employment or volunteer assignment.

### 7. References
*   **Bylaws of Study GRC Inc.** (Specifically Art. III §3.1, Art. V §5.2, Art. IX §9.3)
*   **NIST Cybersecurity Framework (CSF) 2.0**
*   **IS-POL-001:** Master Information Security Policy
*   **IS-PLN-004:** Organizational Cybersecurity Profile (Current)
*   **2 CFR 200.303:** Internal Controls (Federal Grants)
*   **COPPA:** Children's Online Privacy Protection Act

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial release of Target Profile aligned with NIST CSF 2.0. |