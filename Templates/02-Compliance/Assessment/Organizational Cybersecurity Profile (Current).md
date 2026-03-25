### Organizational Cybersecurity Profile (Current)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-ASM-004 |
| **Document Type** | Assessment / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | CISO |
| **Classification** | **Confidential** (Internal Use Only) |

### 1. Purpose
The purpose of this document is to establish the **Current Profile** of Study GRC Inc.'s cybersecurity posture. This assessment maps the Organization’s existing cybersecurity activities, controls, and processes against the **NIST Cybersecurity Framework (CSF) 2.0**.

This profile serves as the baseline for:
1.  Identifying the gap between our current state and our desired **Target Profile** (IS-PLN-005).
2.  Prioritizing budget and resources for the Executive Director and Board of Directors.
3.  Demonstrating due diligence in protecting Member data and Intellectual Property pursuant to **Bylaws Article IX (Policies & Data Protection)** and **Article VIII (Records, Transparency & Finance)**.
4.  Ensuring compliance with federal grant requirements (2 CFR 200) and youth protection laws (COPPA).

### 2. Scope
This profile encompasses all information systems, data, and assets owned, leased, or utilized by Study GRC Inc.

*   **In Scope:**
    *   Cloud infrastructure (SaaS, PaaS, IaaS).
    *   Organization-issued devices.
    *   Volunteer and contractor devices (BYOD) accessing organizational data (limited to the data/access layer).
    *   Third-party vendor relationships and supply chain.
    *   Data related to Voting Members, Community Participants (including minors), and donors.
*   **Exclusions:**
    *   Personal data on volunteer devices not related to Study GRC business.
    *   Home network security of remote volunteers (except where VPN/Zero Trust clients are enforced).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Current Profile** | A snapshot of the cybersecurity outcomes the Organization is currently achieving. |
| **Target Profile** | A definition of the cybersecurity outcomes the Organization aspires to achieve based on risk appetite. |
| **NIST CSF 2.0** | The National Institute of Standards and Technology Cybersecurity Framework, organized by Functions: Govern, Identify, Protect, Detect, Respond, and Recover. |
| **Implementation Tier** | A qualitative measure of organizational cybersecurity risk management practices (Tier 1: Partial to Tier 4: Adaptive). |
| **CISO** | Chief Information Security Officer, as defined in Bylaws Article V. |

### 4. Assessment of Current State (NIST CSF 2.0 Mapping)

The Organization currently operates at an aggregate **Tier 2 (Risk-Informed)** level. While policies are approved by the Board, automation and real-time integration are in development.

#### 4.1 Function: GOVERN (GV)
*The Organization’s cybersecurity risk management strategy, expectations, and policy are established, communicated, and monitored.*

*   **Current Status:** **Tier 2 (Risk-Informed)**
*   **Strengths:**
    *   **Organizational Context (GV.OC):** The Mission and Bylaws (Article I & III) clearly define the non-profit and educational nature.
    *   **Roles & Responsibilities (GV.RR):** The Board has appointed a CISO and established an Audit Committee (Bylaws Art. V & VI).
    *   **Policy (GV.PO):** A Master Information Security Policy and Data Privacy Policy exist and are reviewed bi-annually.
*   **Weaknesses/Gaps:**
    *   **Supply Chain Risk Management (GV.SC):** Vendor risk assessments are performed ad-hoc rather than systematically for all minor SaaS tools.
    *   **Oversight (GV.OV):** Cybersecurity reporting to the Board occurs, but specific KPIs are not yet standardized in the Board meeting minutes.

#### 4.2 Function: IDENTIFY (ID)
*The Organization’s current cybersecurity risks are understood.*

*   **Current Status:** **Tier 1 (Partial)**
*   **Strengths:**
    *   **Asset Management (ID.AM):** Critical cloud assets (GitHub, Finance Systems, Donor CRM) are inventoried.
    *   **Risk Assessment (ID.RA):** Risks regarding youth data (COPPA) are identified and documented.
*   **Weaknesses/Gaps:**
    *   **Asset Management (ID.AM):** Due to the remote-first, volunteer-heavy nature, a real-time inventory of BYOD endpoints accessing the network is incomplete.
    *   **Improvement (ID.IM):** No formal mechanism exists to capture "lessons learned" from near-misses outside of major incidents.

#### 4.3 Function: PROTECT (PR)
*Safeguards to ensure delivery of critical infrastructure services are implemented.*

*   **Current Status:** **Tier 2 (Risk-Informed)**
*   **Strengths:**
    *   **Identity Management (PR.AA):** MFA is mandated for all staff and Board members on core systems (Google Workspace, GitHub, Financials).
    *   **Data Security (PR.DS):** Encryption at rest and in transit is standard for all managed cloud services.
    *   **Awareness & Training (PR.AT):** Board members and Officers receive onboarding training regarding fiduciary duties and data privacy.
*   **Weaknesses/Gaps:**
    *   **Access Control (PR.AC):** "Least Privilege" is policy, but technical enforcement on shared volunteer folders requires manual review.
    *   **Platform Security (PR.PS):** Endpoint Detection and Response (EDR) is not universally deployed on volunteer BYOD equipment.

#### 4.4 Function: DETECT (DE)
*The Organization defines how it identifies the occurrence of a cybersecurity event.*

*   **Current Status:** **Tier 1 (Partial)**
*   **Strengths:**
    *   **Adverse Event Analysis (DE.AE):** Alerts from major SaaS providers (e.g., "Suspicious Login" from Google) are routed to the IT/Security team.
*   **Weaknesses/Gaps:**
    *   **Continuous Monitoring (DE.CM):** There is no 24/7 Security Operations Center (SOC) or centralized SIEM (Security Information and Event Management) aggregating logs from all sources.
    *   **Detection Processes:** Reliance is primarily on manual review of logs post-event rather than automated real-time alerting.

#### 4.5 Function: RESPOND (RS)
*The Organization defines how it responds to a detected cybersecurity incident.*

*   **Current Status:** **Tier 2 (Risk-Informed)**
*   **Strengths:**
    *   **Incident Management (RS.MA):** An Incident Response Plan (IRP) exists.
    *   **Communications (RS.CO):** Bylaws Article III (Emergency Meetings) and Article X (Fundamental Actions) provide a governance framework for crisis decision-making.
*   **Weaknesses/Gaps:**
    *   **Analysis (RS.AN):** Forensic capabilities are limited; the organization relies on external counsel/vendors for deep analysis, which may delay response times due to budget constraints.
    *   **Mitigation (RS.MI):** Automated containment (e.g., isolating a volunteer's laptop remotely) is not technically feasible with current tooling.

#### 4.6 Function: RECOVER (RC)
*The Organization defines how it restores capabilities or services impaired due to a cybersecurity incident.*

*   **Current Status:** **Tier 2 (Risk-Informed)**
*   **Strengths:**
    *   **Backup Recovery (RC.RP):** Cloud-native backups (SaaS) provide high durability for core data.
    *   **Governance (RC.GO):** The "Doomsday Clause" in Bylaws Section 3.10 ensures organizational continuity of leadership.
*   **Weaknesses/Gaps:**
    *   **Testing:** Full-scale disaster recovery drills are not conducted annually. Recovery time objectives (RTOs) are estimated but not empirically validated.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO** | Owns the Current Profile; conducts annual assessments; reports gaps to the Board. |
| **Board of Directors** | Reviews the Current Profile summary; approves budget for moving toward the Target Profile (Bylaws Art. III). |
| **Executive Director (CEO)** | Ensures operational teams (Education, DKG) cooperate with assessment data collection. |
| **Audit Committee** | Validates that the Current Profile accurately reflects reality and is not overly optimistic. |

### 6. Compliance and Enforcement
This document is a descriptive assessment, not a prescriptive policy. However, falsification of data contributing to this profile by any Officer or Director constitutes a breach of the **Professional Ethics and Community Guidelines** and may result in removal for cause under **Bylaws Section 3.6**.

The gaps identified in Section 4 must be addressed in the **Gap Analysis and Action Plan (IS-PLN-006)**.

### 7. References
*   **Bylaws of Study GRC Inc.** (Specifically Articles III, V, VIII, IX).
*   **NIST Cybersecurity Framework (CSF) 2.0**.
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-PLN-005:** Organizational Cybersecurity Profile (Target).
*   **2 CFR 200.303:** Internal Controls (Federal Grant Compliance).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial baseline assessment creation. |