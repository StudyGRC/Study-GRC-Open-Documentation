### Penetration Testing Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-015 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this policy is to establish a mandate and framework for the rigorous validation of Study GRC Inc.'s security controls through simulated cyberattacks (penetration testing). This policy ensures that security weaknesses are identified, documented, and remediated before they can be exploited by malicious actors. This policy directly supports the Organization’s obligation to protect member data and maintains compliance with the "Validation" function of the NIST Cybersecurity Framework (CSF) and industry best practices.

### 2. Scope
This policy applies to all information systems, networks, applications, and cloud infrastructure owned, leased, or operated by Study GRC Inc.

*   **In-Scope:**
    *   External-facing web applications and APIs (including the community platform and learning management systems).
    *   Cloud infrastructure configurations (e.g., AWS, Azure, GCP).
    *   Internal networks and VPN endpoints.
    *   Mobile applications developed by the Organization.
*   **Out-of-Scope:**
    *   Denial of Service (DoS) or Distributed Denial of Service (DDoS) testing, unless explicitly authorized in a specific stress-test engagement.
    *   Physical security destruction testing.
    *   Social engineering targeting minors or youth participants.
    *   Third-party SaaS platforms where the Organization does not have explicit written permission from the vendor to conduct testing.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Penetration Testing** | An authorized simulated cyberattack on a computer system, performed to evaluate the security of the system. |
| **Rules of Engagement (RoE)** | A mandatory document defining the specific scope, timing, allowed methods, and emergency contacts for a penetration test. |
| **Vulnerability Scanning** | An automated process that proactively identifies security vulnerabilities of computing systems in a network to determine if and where a system can be exploited. |
| **Red Teaming** | A full-scope, multi-layered attack simulation designed to measure how well people, networks, and physical security controls can withstand an attack. |
| **Black Box Testing** | Testing where the tester has no prior knowledge of the target system. |
| **White Box Testing** | Testing where the tester has full knowledge of the target system, including source code and architecture. |

### 4. Policy Statements

#### 4.1 Authorization and Consent
All penetration testing activities targeting Study GRC Inc. assets must be explicitly authorized in writing prior to the commencement of any testing.
*   **Internal Testing:** Must be authorized by the CISO.
*   **External/Third-Party Testing:** Must be authorized by the CISO and the Executive Director.
*   **Unauthorized Testing:** Any penetration testing activity conducted without a signed Rules of Engagement (RoE) document will be considered a hostile act and a violation of the Computer Fraud and Abuse Act (CFAA) and Texas Penal Code § 33.02 (Breach of Computer Security).

#### 4.2 Frequency of Testing
To ensure continuous validation of security controls, penetration testing must occur at the following intervals:
*   **Annual External Test:** A comprehensive penetration test conducted by a qualified independent third-party vendor must be performed at least once per fiscal year.
*   **Significant Change:** Targeted penetration testing must be performed prior to the release of major system updates, significant architectural changes, or the deployment of new critical applications.
*   **Continuous Scanning:** Automated vulnerability scanning must be conducted at least monthly, with results reviewed by the IT/Security team.

#### 4.3 Rules of Engagement (RoE)
No testing may begin without a mutually agreed-upon RoE document. The RoE must define:
1.  **Scope:** Specific IP addresses, URLs, and domains to be tested.
2.  **Timing:** Testing windows to minimize operational disruption.
3.  **Excluded Activities:** Explicit prohibition of data destruction, unrecoverable system alteration, or testing that violates the privacy of youth participants.
4.  **Emergency Suspension:** Protocols for immediately halting the test if production systems become unstable.
5.  **Data Handling:** Requirements for the secure handling of any data accessed during the test, in compliance with the *Master Data Privacy Policy*.

#### 4.4 Third-Party Vendor Requirements
When engaging external firms for penetration testing, the Organization must ensure:
*   **Qualifications:** The vendor possesses recognized certifications (e.g., OSCP, CREST, CISSP) and a proven track record.
*   **Insurance:** The vendor maintains adequate professional liability and cyber insurance.
*   **Confidentiality:** The vendor executes a Non-Disclosure Agreement (NDA) pursuant to **Bylaws Article IX, Section 9.2**.
*   **Independence:** The vendor performing the test must be independent of the team that manages the systems to ensure objectivity.

#### 4.5 Remediation and Reporting
The results of penetration tests are confidential internal records.
*   **Reporting:** The tester must provide a detailed report classifying vulnerabilities by severity (Critical, High, Medium, Low) based on the Common Vulnerability Scoring System (CVSS).
*   **Remediation Timelines:**
    *   **Critical:** Remediation or mitigation within **48 hours** of discovery.
    *   **High:** Remediation within **14 days**.
    *   **Medium:** Remediation within **30 days**.
    *   **Low:** Remediation scheduled based on resource availability.
*   **Re-Testing:** All Critical and High findings must be re-tested (validated) by the tester to ensure the fix is effective.

#### 4.6 Community Researchers and Bug Bounties
As an open-source focused non-profit, Study GRC Inc. may engage with community security researchers.
*   Any "Bug Bounty" or "Responsible Disclosure" program must be formally established with clear legal safe harbor terms.
*   Community researchers are strictly prohibited from accessing, downloading, or viewing Personally Identifiable Information (PII) of members, particularly minors. Discovery of such data requires immediate cessation of testing and reporting to the CISO.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Board of Directors** | Approves the annual budget for external penetration testing; reviews high-level summary reports of security posture. |
| **Executive Director (CEO)** | Signs contracts with external penetration testing vendors; ensures operational cooperation with testing activities. |
| **Chief Information Security Officer (CISO)** | Owns this policy; defines the scope and RoE; selects vendors; oversees remediation efforts; signs off on "Acceptance of Risk" if a vulnerability cannot be fixed. |
| **System Owners / IT Staff** | Provide necessary access and documentation to testers; implement patches and configuration changes to remediate findings. |
| **External Testers** | Adhere strictly to the RoE; report critical vulnerabilities immediately upon discovery; protect all data accessed during the engagement. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

**Specific Prohibitions:**
*   Testing without a signed RoE is grounds for immediate termination and referral to law enforcement.
*   Falsifying remediation evidence (claiming a bug is fixed when it is not) is considered a violation of the *Code of Ethics*.

### 7. References
*   **NIST Cybersecurity Framework (CSF) 2.0:** PR.AT-01, ID.RA-01, PR.PS-02 (Validation)
*   **NIST SP 800-115:** Technical Guide to Information Security Testing and Assessment
*   **Study GRC Bylaws:** Article IX (Policies & Data Protection)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-PROC-040:** Vulnerability Remediation SLA

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | CISO | Initial Draft |