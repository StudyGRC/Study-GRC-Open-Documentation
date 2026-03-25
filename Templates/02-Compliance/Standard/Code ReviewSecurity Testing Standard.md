### Code Review/Security Testing Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-065 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-26 |
| **Next Review Date** | 2024-10-26 (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | Application Security Lead |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to define the mandatory technical requirements for code review and security testing within the software development lifecycle (SDLC) of Study GRC Inc. This standard ensures that all "Work Product," as defined in **Bylaws Article IX, Section 9.3**, is free from known vulnerabilities, malicious code, and logic errors before being deployed to production or released as open-source resources. This standard mitigates the risks of data breaches, service interruptions, and the compromise of member data, including sensitive youth information.

### 2. Scope
This standard applies to:
*   **Assets:** All software source code, scripts, infrastructure-as-code (IaC), and configuration files hosted in Study GRC Inc. repositories (e.g., GitHub, GitLab).
*   **Personnel:** All internal employees, contractors, and volunteers contributing code.
*   **External Contributors:** Open-source community participants submitting Pull Requests (PRs) to Organization-managed repositories.

**Exclusions:**
*   Personal "sandbox" repositories that are strictly isolated from the Organization’s networks, production data, and official release channels.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **SAST** | Static Application Security Testing. Analyzing source code for security vulnerabilities without executing the application. |
| **SCA** | Software Composition Analysis. Identifying open-source components and dependencies that contain known vulnerabilities (CVEs). |
| **Secret Scanning** | Automated detection of hardcoded credentials (API keys, passwords, tokens) within the codebase. |
| **Pull Request (PR)** | A method of submitting contributions to a software project where changes are reviewed before being merged into the main branch. |
| **Blocking Finding** | A security vulnerability or quality issue that prevents code from being merged or deployed until remediated. |
| **CVSS** | Common Vulnerability Scoring System. A standard for assessing the severity of computer system security vulnerabilities. |

### 4. Standard Requirements

#### 4.1 Manual Peer Review (The "Four-Eyes" Principle)
To ensure code quality and shared knowledge, no code may be merged into a protected branch (e.g., `main`, `production`, `release`) without human review.

*   **4.1.1 Mandatory Review:** All Pull Requests (PRs) must receive an approving review from at least one (1) qualified reviewer other than the author.
*   **4.1.2 Self-Approval Prohibition:** Authors are strictly prohibited from approving or merging their own PRs into protected branches.
*   **4.1.3 Review Scope:** Reviewers must assess:
    *   Logic correctness and adherence to business requirements.
    *   Absence of hardcoded secrets.
    *   Proper error handling and logging (without logging sensitive data).
    *   Adherence to the Organization's Coding Style Guide.

#### 4.2 Automated Static Analysis (SAST)
Automated security scanning must be integrated into the Continuous Integration (CI) pipeline.

*   **4.2.1 Execution:** SAST tools must run automatically on every commit and PR.
*   **4.2.2 Blocking Criteria:** The merge must be automatically blocked if the SAST tool identifies:
    *   Any vulnerability rated **High** or **Critical** (CVSS ≥ 7.0).
    *   Any instance of the **OWASP Top 10** vulnerabilities (e.g., SQL Injection, XSS).
*   **4.2.3 Tooling:** Approved tools include GitHub Advanced Security (CodeQL), SonarQube, or equivalent open-source alternatives approved by the CISO.

#### 4.3 Software Composition Analysis (SCA)
Given the Organization's reliance on open-source ecosystems, dependency management is critical.

*   **4.3.1 Dependency Scanning:** SCA tools (e.g., Dependabot, Snyk, OWASP Dependency-Check) must run on all repositories containing package manifests (e.g., `package.json`, `requirements.txt`).
*   **4.3.2 Vulnerable Libraries:** Code utilizing libraries with known vulnerabilities (CVEs) with a CVSS score of **7.0 or higher** must not be merged.
*   **4.3.3 License Compliance:** Dependencies must be scanned for license compatibility to ensure compliance with the Organization's open-source commitment (Bylaws Article IX). Restrictive licenses (e.g., AGPL) that conflict with the Organization's licensing strategy are prohibited.

#### 4.4 Secret Scanning and Prevention
*   **4.4.1 Pre-Commit Hooks:** Developers must utilize local pre-commit hooks (e.g., `git-secrets`, `trufflehog`) to prevent committing credentials.
*   **4.4.2 Repository Scanning:** Automated secret scanning must be enabled on all repositories.
*   **4.4.3 Remediation:** If a secret is committed and pushed to a remote repository, it must be considered compromised. The secret must be **revoked and rotated immediately**, and the commit history must be scrubbed or the repository recreated.

#### 4.5 Dynamic Application Security Testing (DAST)
For web applications and APIs exposed to the public internet:

*   **4.5.1 Staging Scans:** DAST scans must be performed against a staging/test environment prior to any major release (vX.0) or significant architectural change.
*   **4.5.2 Authentication:** Scans must be configured to test both authenticated and unauthenticated pathways.

#### 4.6 Vulnerability Remediation Timelines
Vulnerabilities discovered during code review or testing must be remediated according to the following Service Level Objectives (SLOs):

*   **Critical (CVSS 9.0-10.0):** Remediation required before merge/deployment. (Immediate hotfix for production).
*   **High (CVSS 7.0-8.9):** Remediation required before merge/deployment.
*   **Medium (CVSS 4.0-6.9):** Remediation required within 30 days; exception required to merge.
*   **Low (CVSS 0.1-3.9):** Remediation prioritized against technical debt backlog.

#### 4.7 Infrastructure as Code (IaC)
*   **4.7.1 Configuration Scanning:** All IaC templates (Terraform, CloudFormation, Kubernetes manifests) must be scanned for misconfigurations (e.g., open S3 buckets, root user access) using tools like Checkov or tfsec.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Developer / Volunteer** | Ensure code is self-tested prior to submission; resolve findings generated by automated tools; never bypass branch protection rules. |
| **Code Reviewer** | Perform manual inspection of logic and security; reject PRs that fail to meet this Standard. |
| **Application Security Lead** | Configure SAST/SCA/DAST toolsets; maintain rule sets; review and approve False Positive exceptions. |
| **DevOps Engineer** | Maintain the CI/CD pipeline integrity; ensure gating mechanisms (blocking rules) are functional and cannot be bypassed. |
| **CISO** | Final authority on risk acceptance for critical vulnerabilities that cannot be immediately remediated. |

### 6. Compliance and Enforcement
Failure to comply with this standard puts the Organization and its community at risk.
*   **Technical Enforcement:** Branch protection rules will be configured to technically prevent merging code that fails the requirements defined in Section 4.
*   **Policy Enforcement:** Personnel found intentionally bypassing security controls, disabling scanners without authorization, or embedding malicious code will be subject to disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action.

### 7. References
*   **Study GRC Inc. Bylaws:** Article IX (Intellectual Property & Work Product).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-030:** Secure SDLC Policy.
*   **External Standard:** OWASP Top 10 (Current Version).
*   **External Standard:** NIST SP 800-218 (Secure Software Development Framework).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-26 | CISO | Initial release of standard. |