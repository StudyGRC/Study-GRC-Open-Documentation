### Emergency Patch Deployment Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-040 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to define the standardized process for the rapid deployment of security patches and updates in response to critical vulnerabilities, "Zero-Day" threats, or active exploitation. This procedure serves as an exception to the standard Change Management process to ensure Study GRC Inc. can mitigate imminent risks to its infrastructure, member data, and intellectual property within strict timeframes.

This document aligns with the **Master Information Security Policy** and supports the Organization’s obligation to protect donor and member data under **Bylaws Article IX (Policies & Data Protection)**.

### 2. Scope
This procedure applies to all Information Technology (IT) assets owned, leased, or managed by Study GRC Inc., including but not limited to:
*   Cloud infrastructure (AWS, Azure, GCP).
*   SaaS applications and administrative consoles.
*   Server operating systems and applications.
*   Network devices (firewalls, routers, VPN concentrators).
*   End-user devices (laptops, mobile devices) used by employees and contractors.

**Exclusions:** Third-party systems not managed by Study GRC Inc. (e.g., banking portals), though vendor notification procedures still apply.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Zero-Day Vulnerability** | A software security flaw that is known to the software vendor but doesn't have a patch in place to fix the flaw, or a flaw recently discovered that is being actively exploited. |
| **Emergency Change** | A change that must be implemented immediately to correct a major incident or prevent an imminent system failure/security breach. |
| **CVSS** | Common Vulnerability Scoring System. A framework for rating the severity of security vulnerabilities. |
| **ECB** | Emergency Change Board. A subset of the Change Advisory Board authorized to make rapid decisions during a crisis. |
| **CISA KEV** | Cybersecurity and Infrastructure Security Agency Known Exploited Vulnerabilities Catalog. |
| **RMM** | Remote Monitoring and Management tool used to push updates to remote endpoints. |

### 4. Procedures

#### 4.1 Phase 1: Identification and Classification
**Trigger:** Notification from threat intelligence feeds, vendor alerts, CISA alerts, or internal vulnerability scanning.

1.  **Vulnerability Intake:** The Security Team monitors sources for high-severity alerts.
2.  **Severity Assessment:** The CISO or designee must assess the vulnerability against the Study GRC environment. An **Emergency Patch** is required if:
    *   The CVSS Base Score is **9.0 or higher**; OR
    *   The vulnerability is listed in the **CISA KEV** catalog; OR
    *   There is evidence of active targeting against the non-profit sector; OR
    *   The vulnerability affects a public-facing asset containing PII or sensitive IP.
3.  **Declaration:** The CISO formally declares an "Emergency Patch Cycle," triggering this procedure.

#### 4.2 Phase 2: Emergency Approval (ECB)
Unlike standard changes, emergency patches do not wait for the weekly Change Advisory Board (CAB).

1.  **ECB Convening:** The CISO convenes the Emergency Change Board (ECB) via instant messaging (Slack/Teams) or phone.
    *   *Minimum Quorum:* CISO + One Operational Officer (e.g., VP of Education or CTO).
2.  **Risk-Benefit Analysis:** The ECB reviews:
    *   Risk of not patching (e.g., Ransomware, Data Exfiltration).
    *   Risk of patching (e.g., System downtime, broken functionality).
3.  **Approval:** Verbal or chat-based approval is sufficient to proceed.
4.  **Ticket Creation:** An Emergency Change Ticket is created in the ITSM system. If time does not permit, the ticket must be created retroactively within 24 hours (See Section 4.6).

#### 4.3 Phase 3: Accelerated Testing
Due to the urgency, full regression testing may not be possible. A "Risk-Based Testing" approach is used.

1.  **Sandbox Deployment:** Deploy the patch to a non-production (staging) environment immediately.
2.  **Critical Function Check:** Verify only core critical functions (e.g., "Can users log in?", "Is the database accessible?").
3.  **Canary Group (Endpoints):** For workstation patches, deploy to the "IT/Security" device group first to verify stability over a 1-hour window.
4.  **Go/No-Go Decision:** If the system remains stable, proceed to deployment. If the patch fails, the CISO determines if a workaround (e.g., disabling a service, firewall block) is a viable alternative.

#### 4.4 Phase 4: Deployment (Execution)
Deployment targets are prioritized based on exposure.

1.  **Public-Facing Systems:** Patch internet-accessible servers and network appliances immediately (Target: < 24 hours from release).
2.  **Internal Critical Infrastructure:** Patch internal servers and databases (Target: < 48 hours).
3.  **End-User Devices:**
    *   Push patches via RMM/MDM tools.
    *   Force a reboot if required.
    *   **User Notification:** Send a "High Priority Action Required" email/slack notification to all staff instructing them to connect to the internet and accept updates.

#### 4.5 Phase 5: Verification
1.  **Rescan:** Run a targeted vulnerability scan against the affected assets to confirm the vulnerability is remediated.
2.  **Manual Verification:** Check version numbers on critical assets.
3.  **Compliance Report:** Generate a report showing % of assets patched.
    *   *Target:* 100% of critical assets; 95% of endpoints within 72 hours.

#### 4.6 Phase 6: Documentation and Post-Mortem
1.  **Retroactive Documentation:** Update the Emergency Change Ticket with:
    *   Time of deployment.
    *   Assets affected.
    *   Testing results.
    *   Unintended side effects.
2.  **Post-Implementation Review (PIR):** If the patch caused service disruption, a PIR must be conducted during the next standard CAB meeting to discuss lessons learned.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Authority to declare an Emergency Patch Cycle; convenes the ECB; accountable for the security of the ecosystem (per **Bylaws Art. V, Sec 5.2**). |
| **Emergency Change Board (ECB)** | Provides rapid authorization for emergency changes; accepts residual risk of accelerated testing. |
| **IT Operations / DevOps** | Executes the patching process; performs accelerated testing; manages RMM/MDM tools. |
| **Executive Director (CEO)** | Informed of all Emergency Declarations that may impact business continuity or public availability of resources. |
| **All Staff/Volunteers** | Required to save work and reboot devices immediately upon receiving an Emergency Patch notification. |

### 6. Compliance and Enforcement
Failure to adhere to this procedure can result in catastrophic compromise of the Organization's "zero-cost, open-source resources" and member data.

*   **IT Staff:** Failure to execute emergency patching protocols due to negligence may result in disciplinary action, up to and including termination.
*   **End Users:** Tampering with RMM agents or refusing to apply emergency updates violates the **Acceptable Use Policy** and may result in revocation of system access.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-038:** Patch Management Policy
*   **IS-PLN-045:** Incident Response Plan
*   **External:** NIST SP 800-40 Rev. 3 (Guide to Enterprise Patch Management)
*   **External:** CISA Known Exploited Vulnerabilities (KEV) Catalog

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial Release aligned with Zero-Day Response requirements. |