### App Security Testing (SAST/DAST)

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-065 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to mandate and standardize the execution of Static Application Security Testing (SAST) and Dynamic Application Security Testing (DAST) within the Study GRC Inc. software development lifecycle (SDLC). This procedure operationalizes the "Shift Left" security philosophy, ensuring vulnerabilities are identified and remediated early in the development process to protect the Organization’s intellectual property, member data, and open-source reputation.

### 2. Scope
This procedure applies to all software, applications, APIs, and code repositories owned, developed, or maintained by Study GRC Inc., including:
*   **In-Scope:** All GitHub repositories (public and private), web applications, mobile applications, and infrastructure-as-code (IaC) templates.
*   **Personnel:** All employees, volunteers, contractors, and third-party contributors submitting code to Organization repositories.
*   **Exclusions:** Third-party commercial off-the-shelf (COTS) software where the Organization does not have access to source code, though DAST may still be applied to deployed instances.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **SAST (Static Application Security Testing)** | A testing methodology that analyzes source code to find security vulnerabilities that make the organization's applications susceptible to attack. It scans the application before the code is compiled. |
| **DAST (Dynamic Application Security Testing)** | A testing methodology that communicates with a web application through the web front-end in order to identify potential security vulnerabilities in the web application and architectural weaknesses. It performs a "black-box" test. |
| **CI/CD Pipeline** | Continuous Integration/Continuous Deployment; a method to frequently deliver apps to customers by introducing automation into the stages of app development. |
| **Blocking Finding** | A vulnerability severity level (typically High or Critical) that triggers an automatic failure of a build or pull request, preventing code from merging. |
| **False Positive** | A test result which incorrectly indicates that a particular vulnerability is present. |

### 4. Procedures

#### 4.1 Tool Selection and Configuration
The Chief Information Security Officer (CISO), in accordance with **Bylaws Article V Section 5.2**, is responsible for selecting and maintaining the security testing toolset.

1.  **Approved Tools:** The Organization shall utilize industry-standard tools compatible with the Organization’s primary code repository (e.g., GitHub Advanced Security, CodeQL, OWASP ZAP, SonarQube).
2.  **Rule Sets:**
    *   SAST tools must be configured to check against the **OWASP Top 10** and **CWE Top 25** at a minimum.
    *   Secret scanning must be enabled to detect hardcoded API keys, passwords, and tokens.
3.  **Configuration Management:** Security rulesets must be stored as code within the repository (e.g., `.github/workflows`) to ensure version control and transparency.

#### 4.2 Static Application Security Testing (SAST) Workflow
SAST is integrated directly into the Continuous Integration (CI) pipeline.

1.  **Trigger Event:** SAST scans must execute automatically upon every **Pull Request (PR)** created against the `main`, `master`, or `production` branches.
2.  **Execution:**
    *   The CI pipeline initiates the scanner.
    *   The scanner analyzes the delta (new code) and the full codebase context.
3.  **Gating Criteria (Enforcement):**
    *   **Critical/High Severity:** The pipeline **must fail**. The PR cannot be merged until the finding is remediated or marked as a False Positive by an authorized approver.
    *   **Medium/Low Severity:** The pipeline will pass with warnings. Remediation should be scheduled for the next sprint.
4.  **Developer Notification:** Results must be posted directly to the PR comment thread or the "Security" tab of the repository to ensure immediate visibility for the contributor.

#### 4.3 Dynamic Application Security Testing (DAST) Workflow
DAST is performed on running applications in a staging or test environment.

1.  **Trigger Event:** DAST scans must execute:
    *   Automatically upon successful deployment to the **Staging** environment.
    *   On a scheduled weekly basis against the **Production** environment (non-destructive mode only).
2.  **Authentication:** DAST tools must be configured with a dedicated test user account to ensure authenticated routes are scanned. **Never** use administrative credentials for automated DAST scans.
3.  **Reporting:** DAST results are aggregated into the Organization’s Vulnerability Management dashboard.
4.  **Critical Findings:** If a Critical vulnerability is discovered in Staging, the promotion to Production is strictly prohibited until remediation is verified.

#### 4.4 Secrets Detection
To protect the Organization's infrastructure and member data:

1.  **Pre-Commit Hooks:** Developers are required to install pre-commit hooks (e.g., `git-secrets` or `trufflehog`) to prevent committing secrets locally.
2.  **Pipeline Scanning:** The CI pipeline must run a secrets detection scan on every push.
3.  **Incident Response:** If a live secret is detected in a public repository:
    *   The secret must be **revoked/rotated immediately**.
    *   The commit history must be rewritten (if possible and safe) or the repository state managed per the *Data Breach Notification Procedure*.

#### 4.5 Vulnerability Triage and Remediation
Upon detection of a vulnerability via SAST or DAST:

1.  **Validation:** The Lead Developer or Security Engineer reviews the finding to confirm validity.
2.  **False Positive Management:**
    *   If a finding is a False Positive, it must be dismissed in the tool with a written justification.
    *   **Prohibited:** Dismissing findings without analysis to "pass the build."
3.  **Remediation Timelines (SLAs):**
    *   **Critical:** Fix within 24 hours or rollback deployment.
    *   **High:** Fix within 7 days.
    *   **Medium:** Fix within 30 days.
    *   **Low:** Fix within 90 days or accept risk.
4.  **Verification:** A re-scan must be triggered manually or via a new PR to verify the fix.

#### 4.6 Third-Party Dependency Scanning (SCA)
While distinct from custom code SAST, Software Composition Analysis (SCA) must run concurrently.

1.  **Manifest Analysis:** The pipeline must scan `package.json`, `requirements.txt`, `pom.xml`, etc.
2.  **Vulnerable Libraries:** Builds must fail if a dependency contains a known Critical CVE (Common Vulnerabilities and Exposures) with an available patch.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Define security rulesets; select tools; audit False Positive dismissals; override blocking builds in emergency scenarios. |
| **DevOps Engineer** | Integrate SAST/DAST tools into the CI/CD pipeline; ensure tool uptime and performance. |
| **Developer / Contributor** | Review scan results; remediate vulnerabilities prior to merging code; install local pre-commit hooks. |
| **Repository Owner** | Enforce branch protection rules that require passing security checks before merging. |

### 6. Compliance and Enforcement
This procedure is mandatory for all code contributing to Study GRC Inc. products.

*   **Technical Enforcement:** Branch protection rules will be configured to technically prevent the merging of code that fails Critical/High SAST checks.
*   **Policy Enforcement:** Circumventing security checks (e.g., disabling the pipeline, using admin force-merges without authorization) is a violation of the *Code of Ethics and Conduct*.
*   **Consequences:** Failure to comply may result in revocation of repository access, removal from volunteer roles, or termination of employment/contract.

### 7. References
*   **IS-POL-001:** Master Information Security Policy
*   **IS-POL-040:** Patch Management Policy
*   **IS-STD-063:** Secure SDLC Policy
*   **Bylaws Article IX:** Intellectual Property (Work Product Ownership)
*   **NIST SP 800-53 (RA-5):** Vulnerability Monitoring and Scanning

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | CISO | Initial release of SAST/DAST procedures. |