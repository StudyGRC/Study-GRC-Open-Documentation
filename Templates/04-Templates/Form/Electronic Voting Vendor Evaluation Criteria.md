### Electronic Voting Vendor Evaluation Criteria

| Document Control | |
| :--- | :--- |
| **Document ID** | GOV-FRM-018 |
| **Document Type** | Form / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2025-10-27 (Bi-Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Secretary of the Board |
| **Classification** | Internal |

### 1. Purpose
The purpose of this document is to establish a standardized, rigorous framework for evaluating and selecting third-party electronic voting systems. This ensures Study GRC Inc. complies with **Bylaws Article II, Section 2.3** (prohibition of proxy voting) and **Section 2.5** (electronic voting window), while adhering to **NIST Cybersecurity Framework** standards for election integrity. This form mitigates risks associated with election fraud, data breaches, and lack of auditability.

### 2. Scope
This evaluation criteria applies to any Software-as-a-Service (SaaS) or platform vendor considered for facilitating:
*   Annual Meetings of the Membership.
*   Board of Directors Elections.
*   Fundamental Actions (Mergers, Dissolution, Bylaw Amendments).
*   Special Emergency Meetings.

**Exclusions:** Informal polling or non-binding surveys (e.g., Slack polls) used for community engagement do not require this level of scrutiny.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **End-to-End Verifiability** | A property of a voting system that allows voters to verify their vote was cast as intended, recorded as cast, and tallied as recorded. |
| **Voter-Verified Audit Trail (VVAT)** | A software-independent verification method (digital or physical) that allows for a post-election audit. |
| **TBOC** | Texas Business Organizations Code. |
| **TLS 1.2+** | Transport Layer Security; a cryptographic protocol designed to provide communications security over a computer network. |
| **SAML/SSO** | Security Assertion Markup Language / Single Sign-On; allows members to use existing credentials to authenticate. |

### 4. Evaluation Criteria Checklist

The Evaluation Team (Secretary, CISO, and Governance Committee) must utilize this checklist when vetting vendors.

#### 4.1 Mandatory Security & Integrity Requirements (NIST Alignment)
*Vendors receiving a "Fail" on any item in this section are automatically disqualified.*

| Requirement | Description | Pass/Fail | Notes |
| :--- | :--- | :--- | :--- |
| **Encryption in Transit** | System must use TLS 1.2 or higher for all data transmission. | | |
| **Encryption at Rest** | Voter data and ballot data must be encrypted in the database (AES-256 preferred). | | |
| **Authentication Integrity** | System must support unique, one-time-use credentials or tokenized links for each Voting Member to prevent double-voting. | | |
| **Audit Logs** | System must maintain immutable logs of all administrator actions and voting events (timestamps, IP addresses). | | |
| **No Proxy Capability** | System must **not** allow a user to delegate their vote to another user, in strict compliance with **Bylaws Section 2.3**. | | |
| **Data Sovereignty** | Data must be hosted in jurisdictions compliant with Study GRC’s privacy policy (e.g., US-based or GDPR compliant). | | |
| **SOC 2 Type II** | Vendor must provide a current SOC 2 Type II report or equivalent security certification. | | |

#### 4.2 Functional & Bylaws Compliance
| Requirement | Description | Score (1-5) | Notes |
| :--- | :--- | :--- | :--- |
| **Extended Voting Window** | Ability to keep polls open for exactly seven (7) days as required by **Bylaws Section 2.5**. | | |
| **Voter List Export** | Ability to generate an alphabetical list of members who voted (to satisfy **Bylaws Section 2.6** inspection rights) without revealing *how* they voted (if secret ballot). | | |
| **Candidate Profiles** | Capability to display "Nomination Statements" and conflict disclosures directly on the ballot or linked clearly (**Bylaws Section 2.5**). | | |
| **Quorum Calculation** | Automated calculation of quorum based on total eligible voters vs. votes cast (**Bylaws Section 2.4**). | | |
| **Weighted/Class Voting** | Ability to segregate "Supporting Members" (Voting) from "Community Participants" (Non-Voting) via segmentation. | | |
| **Write-In Candidates** | Ability to enable or disable write-in candidates based on specific election rules. | | |

#### 4.3 Usability & Accessibility (Inclusion)
| Requirement | Description | Score (1-5) | Notes |
| :--- | :--- | :--- | :--- |
| **WCAG 2.1 AA Compliance** | Platform must be accessible to users with disabilities (screen reader compatibility, contrast). | | |
| **Mobile Responsiveness** | Interface must be fully functional on mobile devices (iOS/Android) without loss of features. | | |
| **User Experience (UX)** | Voting process should require no more than 3 clicks to access the ballot from the invitation email. | | |
| **Confirmation Receipt** | System must send an email receipt to the voter confirming their vote was cast (Integrity check). | | |

#### 4.4 Vendor Reliability & Support
| Requirement | Description | Score (1-5) | Notes |
| :--- | :--- | :--- | :--- |
| **Uptime SLA** | Service Level Agreement guaranteeing 99.9% uptime during the 7-day election window. | | |
| **Support Availability** | Technical support available within 4 hours during the election window. | | |
| **Reference Checks** | Positive references from other 501(c)(3) non-profits or governance bodies. | | |

### 5. Scoring Summary

| Section | Weight | Score |
| :--- | :--- | :--- |
| 4.1 Security (Mandatory) | Pass/Fail | [Pass/Fail] |
| 4.2 Functional | 40% | [ ] / 25 |
| 4.3 Usability | 30% | [ ] / 20 |
| 4.4 Reliability | 30% | [ ] / 15 |
| **TOTAL SCORE** | **100%** | **[ ] / 100** |

**Recommendation:**
[ ] Approve Vendor
[ ] Reject Vendor
[ ] Approve with Conditions: ___________________

### 6. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Secretary** | Leads the evaluation process; ensures functional alignment with Bylaws Article II. |
| **Chief Information Security Officer (CISO)** | Conducts the technical security review (Section 4.1); validates SOC 2 reports and encryption standards. |
| **Governance Committee** | Reviews the final recommendation to ensure the vendor supports fair and transparent elections. |
| **Executive Director** | Executes the contract and Data Processing Agreement (DPA) upon Board approval. |

### 7. Compliance and Enforcement
Failure to utilize this evaluation criteria when selecting a voting vendor may result in the invalidation of election results by the Membership or the Board. Selection of a vendor that does not meet the Mandatory Security Requirements (Section 4.1) constitutes a violation of the **Board Code of Ethics** (Duty of Care) and the **Master Information Security Policy**.

### 8. References
*   **Bylaws of Study GRC Inc.** (Articles II & III)
*   **Texas Business Organizations Code (TBOC)** § 22.160 (Voting of Members)
*   **NIST SP 800-53 r5** (Security and Privacy Controls for Information Systems)
*   **NIST SP 1500-100** (Internet Voting System Standards - Principles)
*   **GOV-POL-005** Master Information Security Policy