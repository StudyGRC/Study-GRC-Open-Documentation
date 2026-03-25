### Open Source Software (OSS) Vetting Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-065 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Director of Engineering |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized process for the selection, evaluation, and approval of Open Source Software (OSS) components within Study GRC Inc. ("the Organization"). This procedure mitigates **Licensing Risk** (legal liability and intellectual property infringement), **Security Risk** (supply chain vulnerabilities), and **Operational Risk** (abandoned projects) associated with third-party dependencies.

This procedure supports the Organization’s commitment to an open-source ecosystem as defined in **Bylaws Article I, Section 1.3**, while ensuring compliance with **Bylaws Article IX, Section 9.3** regarding Intellectual Property ownership and assignment.

### 2. Scope
This procedure applies to all software development activities undertaken by the Organization.
*   **Applies to:** All employees, contractors, and volunteers ("Contributors") who introduce third-party libraries, frameworks, binaries, or code snippets into the Organization’s repositories or production environments.
*   **Exclusions:** Standalone desktop applications used for general office productivity (e.g., web browsers, word processors) that are not integrated into the Organization's codebase or products.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **OSS (Open Source Software)** | Software with source code that anyone can inspect, modify, and enhance, governed by specific licensing terms. |
| **Copyleft (Viral) License** | A license (e.g., GPL, AGPL) that requires derivative works to be released under the same license terms, potentially forcing the Organization to release proprietary code. |
| **Permissive License** | A license (e.g., MIT, Apache 2.0) that guarantees the freedom to use, modify, and redistribute software with minimal requirements (usually just attribution). |
| **SCA (Software Composition Analysis)** | Automated tools used to identify OSS components, their licenses, and known security vulnerabilities. |
| **SBOM (Software Bill of Materials)** | A formal, machine-readable inventory of software components and dependencies. |
| **Transitive Dependency** | A library that is used by another library that the Organization has directly imported. |

### 4. Procedures

#### 4.1 Phase 1: Initial Selection and Health Check
Before introducing a new OSS component, the Contributor must perform a preliminary "Health Check" to ensure the component is viable and maintained.

1.  **Verify Maintenance Status:** The Contributor must verify the project is active.
    *   *Criteria:* Commits within the last 12 months; active issue tracking; responsive maintainers.
2.  **Community Review:** Check for community adoption (e.g., GitHub stars, NPM downloads) to ensure the tool is not obscure or abandoned.
3.  **License Identification:** Identify the license type immediately. If the license is missing or "All Rights Reserved," the component **must not** be used.

#### 4.2 Phase 2: License Compliance Review (The "Traffic Light" Protocol)
The Organization categorizes licenses into three tiers. Contributors must adhere to these categories prior to integration.

**4.2.1 Green List (Pre-Approved)**
*   *Action:* May be used without specific CISO approval, provided attribution requirements are met.
*   *Licenses:* MIT, Apache License 2.0, BSD (2-Clause/3-Clause), ISC.

**4.2.2 Yellow List (Conditional Review)**
*   *Action:* Requires written approval from the CISO or Legal Counsel. These often have "weak copyleft" provisions (file-level reciprocity).
*   *Licenses:* Mozilla Public License (MPL), Eclipse Public License (EPL), LGPL (Lesser GPL).
*   *Requirement:* Must be dynamically linked; modifications to the library itself must be contributed back.

**4.2.3 Red List (Prohibited)**
*   *Action:* **Strictly Prohibited** without a specific waiver from the Board of Directors. These licenses pose significant risk to the Organization's IP strategy or commercial viability.
*   *Licenses:* GNU GPL (v2/v3), GNU AGPL (Affero GPL), WTFPL, CC-BY-NC (Non-Commercial), or any proprietary license requiring payment not already budgeted.

#### 4.3 Phase 3: Security Vulnerability Scanning
1.  **Automated Scanning:** All dependencies must be scanned using an approved SCA tool (e.g., GitHub Dependabot, OWASP Dependency-Check, or Snyk).
2.  **Vulnerability Thresholds:**
    *   **Critical/High Severity:** Must be remediated (patched or replaced) **before** merging code into the `main` or `production` branch.
    *   **Medium/Low Severity:** Must be logged in the issue tracker and remediated within 30 days.
3.  **Typosquatting Check:** Contributors must verify the package name exactly matches the official repository to avoid malicious "look-alike" packages.

#### 4.4 Phase 4: Integration and Documentation
1.  **Package Management:** Dependencies must be declared in the project's manifest file (e.g., `package.json`, `requirements.txt`, `go.mod`) with version pinning (locking) enabled to prevent unexpected updates.
2.  **Attribution File:** The Contributor must update the project's `NOTICE` or `CREDITS` file to include the copyright notice and license text of the new component, as required by Permissive Licenses (e.g., Apache 2.0).
3.  **SBOM Update:** The project's Software Bill of Materials (SBOM) must be updated to reflect the new addition.

#### 4.5 Phase 5: Continuous Monitoring
1.  **Automated Alerts:** The Engineering team must configure the repository to send alerts (via email or Slack) when new vulnerabilities (CVEs) are discovered in existing dependencies.
2.  **Quarterly Audit:** The CISO or designee will perform a quarterly audit of all repositories to identify:
    *   Outdated dependencies.
    *   "License Drift" (where a dependency changes its license in a new version).
    *   Deprecated or abandoned packages.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Contributor (Dev/Volunteer)** | Performs initial health check; ensures license is on "Green List"; implements version pinning; updates attribution files. |
| **Lead Engineer** | Reviews Pull Requests (PRs) to ensure no unapproved dependencies are added; verifies SCA scan results pass thresholds. |
| **CISO** | Maintains the License Traffic Light list; approves "Yellow List" exceptions; conducts quarterly audits. |
| **Board of Directors** | Sole authority to approve "Red List" (AGPL/GPL) exceptions based on strategic alignment with Bylaws. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in:
1.  **Code Rejection:** Pull Requests containing unvetted or prohibited OSS will be blocked from merging.
2.  **Remediation:** Mandatory refactoring of codebases to remove infringing libraries at the Contributor's time/expense.
3.  **Disciplinary Action:** Repeated violations may result in revocation of repository access, termination of volunteer status, or employment termination.
4.  **Legal Action:** In cases where negligence leads to IP infringement lawsuits, the Organization reserves the right to seek indemnification as permitted by law.

### 7. References
*   **Bylaws of Study GRC Inc.** (Specifically Article IX: Intellectual Property)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-STD-022:** Secure Software Development Lifecycle (SDLC) Standard
*   **NIST SP 800-218:** Secure Software Development Framework (SSDF)
*   **Open Source Initiative (OSI):** Open Source Definition

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Legal Officer | Initial Release |