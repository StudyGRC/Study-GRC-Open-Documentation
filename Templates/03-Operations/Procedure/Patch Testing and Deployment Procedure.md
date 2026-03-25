### Patch Testing and Deployment Procedure

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
The purpose of this procedure is to establish a standardized, repeatable process for the testing and deployment of software updates (patches) within Study GRC Inc. This procedure ensures that security vulnerabilities are remediated in a timely manner while minimizing the risk of operational disruption caused by defective or incompatible updates. This document operationalizes the requirements set forth in the *Patch Management Policy* and aligns with the Organization's Change Control standards.

### 2. Scope
This procedure applies to all Information Technology (IT) assets owned, managed, or operated by Study GRC Inc., including but not limited to:
*   Server Operating Systems (Cloud and On-Premise).
*   Workstation Operating Systems (Windows, macOS, Linux).
*   Network Infrastructure (Firewalls, Routers, Switches).
*   Server-side Applications and Middleware.
*   End-user Applications (Browsers, Office Suites, Productivity Tools).

**Exclusions:**
*   Third-party SaaS (Software as a Service) platforms where patching is managed exclusively by the vendor (e.g., Google Workspace, Slack), though configuration reviews remain mandatory.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Patch** | A set of changes to a computer program or its supporting data designed to update, fix, or improve it. This includes fixing security vulnerabilities and other bugs. |
| **Canary Deployment** | A phased rollout strategy where a patch is released to a small subset of users/systems (the "canaries") to test stability before a full rollout. |
| **Test Environment** | A non-production environment (Staging/QA) that mirrors the production environment as closely as possible. |
| **Rollback** | The process of reverting a system to its previous state before the patch was applied. |
| **CVSS** | Common Vulnerability Scoring System; a standard for assessing the severity of computer system security vulnerabilities. |
| **Change Advisory Board (CAB)** | A body that approves the assessment, prioritization, authorization, and scheduling of changes. |

### 4. Procedures

#### 4.1 Patch Identification and Categorization
1.  **Scanning:** The IT Security Team must utilize automated vulnerability scanning tools to identify missing patches across the infrastructure at least weekly.
2.  **Vendor Notification:** System Administrators must subscribe to vendor security notifications (e.g., Microsoft Patch Tuesday, US-CERT alerts).
3.  **Categorization:** Upon identification, patches must be categorized based on the *Vulnerability Management Standard*:
    *   **Critical:** CVSS 9.0-10.0 (Immediate action required; see *Emergency Patch Deployment Procedure*).
    *   **High:** CVSS 7.0-8.9.
    *   **Medium/Low:** CVSS < 6.9 or feature updates.

#### 4.2 Change Management Initiation
1.  **Ticket Creation:** A Change Request (CR) ticket must be created in the IT Service Management (ITSM) tool for every patch cycle.
2.  **Documentation:** The CR must include:
    *   List of patches (KB numbers/Versions).
    *   Affected systems.
    *   Risk assessment (Impact of patching vs. Impact of not patching).
    *   Proposed schedule.
    *   Rollback plan.
3.  **Approval:**
    *   **Standard Patches:** Pre-approved by the CISO or designee.
    *   **Major Updates/Service Packs:** Require formal approval from the Change Advisory Board (CAB).

#### 4.3 Testing Protocol
*Note: Patches must never be deployed to the entire production environment without validation.*

1.  **Environment Selection:** Patches must be applied to the **Test Environment** first. If a dedicated Test Environment does not exist for a specific asset, a non-critical "Pilot Group" of production assets must be used.
2.  **Functional Testing:**
    *   Verify the operating system boots and stabilizes.
    *   Verify critical business applications launch and connect to required services.
    *   Verify network connectivity (VPN, Wi-Fi, LAN).
    *   Check system logs for new error messages.
3.  **Security Validation:**
    *   Re-scan the test asset to confirm the vulnerability is remediated.
4.  **Testing Duration:**
    *   **Critical/High:** Minimum 24 hours observation in Test/Pilot.
    *   **Medium/Low:** Minimum 48 hours observation in Test/Pilot.
5.  **Failure Handling:** If a patch causes instability, the testing phase is halted. The issue must be documented, and the vendor contacted. The patch is marked "Do Not Deploy" until a resolution is found.

#### 4.4 Deployment Strategy (Phased Rollout)
To support the Organization's remote-first nature and minimize downtime, deployment follows a phased approach:

1.  **Phase 1: Pilot Group (10%)**
    *   Includes IT staff and volunteer "early adopters."
    *   **Action:** Deploy patch. Monitor for 24 hours.
2.  **Phase 2: General Availability - Wave A (45%)**
    *   Includes non-critical departments.
    *   **Action:** Deploy patch. Monitor for 24 hours.
3.  **Phase 3: General Availability - Wave B (45%)**
    *   Includes critical departments (e.g., Finance, Executive Leadership).
    *   **Action:** Deploy patch.

**Remote Endpoint Considerations:**
*   Patches for remote workstations must be configured to download in the background and prompt the user to install/reboot at a convenient time, with a forced deadline of 72 hours after release to the endpoint.

#### 4.5 Verification and Monitoring
1.  **Post-Deployment Scan:** 24 hours after the final deployment wave, a vulnerability scan must be executed to verify compliance.
2.  **Compliance Reporting:** The ITSM system must be updated to reflect the successful closure of the Change Request.
3.  **Exception Handling:** Systems that failed to patch (e.g., offline devices) must be quarantined or flagged for manual remediation by the IT Support Team.

#### 4.6 Rollback Procedure
If a patch causes a critical failure in Production:
1.  **Stop Deployment:** Immediately halt any ongoing deployment waves.
2.  **Execute Rollback:**
    *   **Workstations:** Uninstall the specific update via the Endpoint Management Console (MDM/RMM).
    *   **Servers/VMs:** Revert to the pre-patch snapshot taken during the backup window.
3.  **Notification:** Notify the CISO and affected users via the *System Availability/Uptime SLA* communication channels.
4.  **Post-Mortem:** Conduct a Root Cause Analysis (RCA) before attempting to re-deploy.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Accountable for the overall Patch Management program; authorizes Standard Changes; reports compliance to the Board per Bylaws Art. V §5.2. |
| **System Administrators / IT Ops** | Responsible for scanning, testing, scheduling, and deploying patches; executing rollback procedures. |
| **Change Advisory Board (CAB)** | Reviews and approves major updates or patches requiring significant downtime. |
| **End Users / Staff** | Responsible for rebooting devices when prompted and reporting any post-update anomalies to the Help Desk. |
| **Pilot Group Users** | Designated staff who receive updates early to validate functionality in a production-like scenario. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.

**Bylaws Reference:** This procedure supports the duties of the CISO as defined in **Article V, Section 5.2** of the Bylaws of Study GRC Inc., specifically regarding the management of the Organization's technology and security.

### 7. References
*   **IS-POL-038:** Patch Management Policy
*   **IS-PRC-039:** Emergency Patch Deployment Procedure
*   **IS-PRC-070:** Change Control and Management Procedure
*   **NIST SP 800-53 (Rev. 5):**
    *   *CM-3 (Configuration Change Control)*
    *   *SI-2 (Flaw Remediation)*

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Release |