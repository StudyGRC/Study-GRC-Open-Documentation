### Secure SDLC Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-065 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this policy is to integrate security into every phase of the software development lifecycle (SDLC) at Study GRC Inc. By adopting a "Secure by Design" and "Shift Left" approach, the Organization aims to minimize vulnerabilities in its open-source resources, educational platforms, and internal tools. This policy mitigates risks associated with data breaches, supply chain attacks, and reputational damage, ensuring that the Organization's deliverables remain trustworthy for the community.

### 2. Scope
This policy applies to:
*   **Personnel:** All employees, contractors, and volunteers (including "Community Participants" contributing code) involved in the design, development, testing, or maintenance of software.
*   **Assets:** All software, code repositories (e.g., GitHub), scripts, APIs, and web applications developed or managed by Study GRC Inc.
*   **Exclusions:** Third-party Commercial Off-The-Shelf (COTS) software where Study GRC Inc. has no access to the source code (governed by *Vendor Risk Management Policy*), though integration with such software is included in this scope.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **SDLC** | Software Development Lifecycle; the process used to design, develop, and test high-quality software. |
| **OWASP** | Open Web Application Security Project; a non-profit foundation that works to improve the security of software. |
| **SAST** | Static Application Security Testing; analyzing source code for security vulnerabilities without executing the code. |
| **DAST** | Dynamic Application Security Testing; analyzing a running application for vulnerabilities. |
| **SCA** | Software Composition Analysis; identifying open-source components and their known vulnerabilities in the codebase. |
| **Work Product** | As defined in **Bylaws Article IX, Section 9.3**, all content, code, and materials created by leaders, volunteers, or contractors during their service. |
| **CI/CD** | Continuous Integration/Continuous Deployment; the method to frequently deliver apps to customers by introducing automation into the stages of app development. |

### 4. Policy Statements

#### 4.1 General Principles
4.1.1 **Security by Design:** Security requirements must be identified and defined during the initial planning phase of any project, not added as an afterthought.
4.1.2 **Shift Left:** Security testing must occur as early as possible in the development lifecycle to reduce the cost and impact of remediation.
4.1.3 **Open Source Transparency:** As an organization dedicated to open-source resources (**Bylaws Article I, Section 1.3**), all released code must be sanitized of internal secrets, keys, and sensitive data prior to public publication.

#### 4.2 Phase 1: Requirements and Design
4.2.1 **Threat Modeling:** For any new application or significant feature update involving sensitive data (including member data or youth participant data), a Threat Model must be created and reviewed by the CISO or their designee.
4.2.2 **Privacy by Design:** All software must be designed to minimize data collection. Features interacting with minors must strictly adhere to COPPA requirements as defined in the *Child and Youth Safeguarding Policy*.
4.2.3 **Security Requirements:** Functional requirements must include specific security controls (e.g., "User passwords must be hashed using Argon2," not just "System must be secure").

#### 4.3 Phase 2: Development (Coding)
4.3.1 **Coding Standards:** All developers must adhere to the **OWASP Secure Coding Practices**.
4.3.2 **Prohibited Functions:** The use of insecure functions (e.g., `eval()`, weak random number generators) is prohibited unless explicitly authorized via a risk acceptance waiver.
4.3.3 **Secrets Management:** Hardcoding credentials, API keys, or tokens in source code is strictly prohibited. Secrets must be managed via environment variables or a dedicated secrets management vault.
4.3.4 **Intellectual Property:** In accordance with **Bylaws Article IX, Section 9.3**, all contributors must acknowledge that code committed to Organization repositories is "work made for hire" or assigned to the Organization to ensure continued open-source availability.

#### 4.4 Phase 3: Verification (Testing)
4.4.1 **Static Analysis (SAST):** Automated SAST tools must be integrated into the CI/CD pipeline. Builds containing "Critical" or "High" severity vulnerabilities must fail automatically.
4.4.2 **Dependency Scanning (SCA):** All third-party libraries and dependencies must be scanned for known vulnerabilities (CVEs). Components with known critical vulnerabilities must be updated or replaced before deployment.
4.4.3 **Dynamic Analysis (DAST):** Public-facing web applications must undergo DAST scanning prior to major releases.
4.4.4 **Peer Review:** All code changes require a peer review (Pull Request approval) by a second qualified individual before merging into the main branch.

#### 4.5 Phase 4: Deployment and Maintenance
4.5.1 **Separation of Duties:** Developers should not have direct write access to the production environment. Deployments must be automated via the CI/CD pipeline.
4.5.2 **Vulnerability Management:** The Organization must maintain a process to receive and respond to external vulnerability reports (e.g., a `security.txt` file or Bug Bounty program).
4.5.3 **Patching:** Critical security patches for underlying infrastructure or dependencies must be applied within the timelines defined in the *Patch Management Policy*.

#### 4.6 Training and Awareness
4.6.1 **Developer Training:** All personnel contributing code must complete annual secure coding training based on the **OWASP Top 10**.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this policy; selects security tooling (SAST/DAST); approves Threat Models; acts as the final gatekeeper for releases with identified risks. |
| **VP of Education & Training** | Ensures educational platforms developed under their purview adhere to these standards; allocates time for team training. |
| **Lead Developer / Engineering Manager** | Enforces peer reviews; maintains the CI/CD pipeline; ensures developers remediate findings. |
| **Developers / Volunteers** | Write secure code; attend training; fix vulnerabilities identified during testing; do not bypass security checks. |
| **Executive Director** | Allocates budget for security tooling and training resources. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including termination of employment or volunteer assignment, and potential legal action depending on the severity of the violation.
*   **Code Rejection:** Code that does not meet these standards will be rejected from the main codebase.
*   **Repository Access:** Volunteers repeatedly violating secure coding practices (e.g., committing secrets) may have their repository access revoked.

### 7. References
*   **OWASP Top 10:** Standard for web application security.
*   **OWASP ASVS:** Application Security Verification Standard.
*   **NIST SSDF (SP 800-218):** Secure Software Development Framework.
*   **Bylaws of Study GRC Inc.:** Article I (Purpose), Article IX (Intellectual Property).
*   **IS-POL-001:** Master Information Security Policy.
*   **IS-POL-038:** Patch Management Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name], CISO | Initial Policy Release |