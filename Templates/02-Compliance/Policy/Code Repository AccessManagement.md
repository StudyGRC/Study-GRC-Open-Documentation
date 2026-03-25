### Code Repository Access and Management Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-019 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Chief Information Security Officer (CISO) |
| **Document Owner** | VP of Education & Training / Lead Engineer |
| **Classification** | Public |

### 1. Purpose
The purpose of this policy is to establish security controls, access standards, and management protocols for all source code repositories maintained by Study GRC Inc. (the "Organization"). This policy ensures the integrity, availability, and confidentiality of the Organization’s intellectual property and open-source contributions while mitigating risks associated with unauthorized access, code injection, and secret leakage.

This policy directly supports **Article IX, Section 9.3** of the Bylaws regarding Intellectual Property ownership and the Organization's commitment to maintaining an open-source ecosystem as defined in **Article I, Section 1.3**.

### 2. Scope
This policy applies to:
*   **Assets:** All code repositories hosted by the Organization (e.g., GitHub, GitLab, Bitbucket), including public open-source projects and private internal tools.
*   **Personnel:** All Employees, Board Directors, Operational Officers, Volunteers, Contractors, and external Community Contributors who access or contribute code.

**Exclusions:** Personal repositories of volunteers that are not forked from or intended for contribution to the Organization’s official codebase.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Repository (Repo)** | A central file storage location used by version control systems (e.g., Git) to manage source code and history. |
| **Branch Protection** | Rules that enforce specific workflows, such as requiring code reviews before merging changes into the main codebase. |
| **Secret** | Sensitive credentials including API keys, private encryption keys, database passwords, and authentication tokens. |
| **Pull Request (PR)** | A method of submitting contributions to a project where changes are reviewed before being merged. |
| **MFA** | Multi-Factor Authentication; a security system that requires more than one method of authentication to verify the user's identity. |
| **CLA** | Contributor License Agreement; a legal document defining the terms under which intellectual property has been contributed to the Organization. |

### 4. Policy Statements

#### 4.1 Access Control and Authentication
To protect the Organization's digital assets, access to repositories is granted on a strict "Need-to-Know" and "Least Privilege" basis.

*   **4.1.1 Mandatory MFA:** All users with write access to Organization repositories **must** have Multi-Factor Authentication (MFA) enabled on their accounts. Accounts without MFA will be removed from the Organization’s repository access list immediately.
*   **4.1.2 Role-Based Access Control (RBAC):**
    *   **Admin/Owner:** Restricted to the CISO, VP of Education, and designated Lead Engineers.
    *   **Maintainer:** Granted to Senior Volunteers/Staff responsible for managing specific projects.
    *   **Write/Push:** Granted to active developers for specific repositories only.
    *   **Read/Triage:** Default for general volunteers and community participants.
*   **4.1.3 Service Accounts:** Automated systems (CI/CD pipelines) must use restricted-scope tokens with expiration dates, not personal user credentials.

#### 4.2 Branch Protection and Workflow
To ensure code quality and prevent malicious code injection, the following rules apply to all `main`, `master`, and `production` branches:

*   **4.2.1 No Direct Commits:** Direct pushes to protected branches are strictly prohibited for all users, including Administrators.
*   **4.2.2 Peer Review Requirement:** All code changes must be submitted via Pull Request (PR). A minimum of **one (1)** independent review and approval from a qualified Maintainer is required before merging.
*   **4.2.3 Status Checks:** PRs must pass all automated status checks (e.g., unit tests, linters, security scans) before merging is permitted.
*   **4.2.4 Signed Commits:** Contributors are strongly encouraged to use GPG-signed commits to verify the authenticity of the author.

#### 4.3 Secrets Management
The accidental exposure of credentials is a critical risk.

*   **4.3.1 Prohibition:** Hardcoding secrets (API keys, passwords, tokens) directly into source code or configuration files committed to the repository is **strictly prohibited**.
*   **4.3.2 Detection:** Automated secret scanning tools must be enabled on all repositories to detect and block commits containing potential secrets.
*   **4.3.3 Remediation:** If a secret is committed, it must be considered compromised immediately. The secret must be revoked/rotated, and the repository history scrubbed (if private) or the incident documented (if public).

#### 4.4 Intellectual Property and Licensing
In accordance with **Bylaws Article IX, Section 9.3**:

*   **4.4.1 Work Made for Hire:** All code created by Officers, Directors, and Volunteers in the course of their duties is the property of Study GRC Inc.
*   **4.4.2 Licensing:** All public repositories must contain a `LICENSE` file in the root directory. Unless otherwise authorized by the Board, the license shall be a permissive open-source license (e.g., MIT or Apache 2.0) to align with the Organization's charitable purpose.
*   **4.4.3 Contributor License Agreement (CLA):** External contributors making significant changes may be required to sign a CLA to ensure the Organization has the legal right to distribute the code.

#### 4.5 Repository Lifecycle Management
*   **4.5.1 Creation:** Only Administrators or Maintainers may create new repositories under the Organization’s namespace.
*   **4.5.2 Archival:** Repositories that are no longer actively maintained must be marked as "Archived" (read-only) to prevent unauthorized changes while preserving history.
*   **4.5.3 Visibility:** Repositories containing sensitive operational data (e.g., infrastructure-as-code for internal finance systems) must be set to **Private**. Educational resources intended for the community must be set to **Public**.

#### 4.6 Offboarding
Upon the resignation or termination of a volunteer or staff member (per **Bylaws Article III, Section 3.7** or **Article V, Section 5.3**):
*   Access to all repositories must be revoked within **24 hours**.
*   Personal Access Tokens (PATs) and SSH keys associated with the user must be rotated if shared credentials were suspected (though shared credentials are prohibited).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Defines security standards; audits repository access logs; manages incident response for leaked secrets. |
| **VP of Education & Training** | Approves the creation of new repositories; ensures code quality standards align with educational goals. |
| **Maintainers** | Review and merge Pull Requests; enforce branch protection rules; manage issue triage. |
| **Contributors (Staff/Volunteers)** | Enable MFA; protect personal credentials; adhere to the "No Secrets" policy; sign IP assignment/CLA agreements. |

### 6. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, up to and including revocation of repository access, termination of volunteer assignment or employment, and potential legal action for intellectual property theft or intentional sabotage.

**Audit Requirement:** The CISO shall conduct a quarterly audit of all users with "Admin" or "Maintainer" access to ensure permissions remain appropriate.

### 7. References
*   **Bylaws of Study GRC Inc.** (specifically Articles I, III, V, and IX)
*   **IS-POL-001:** Master Information Security Policy
*   **IS-STD-005:** Secure Software Development Lifecycle (SDLC) Standard
*   **GitHub Security Best Practices**
*   **NIST SP 800-218:** Secure Software Development Framework (SSDF)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial Draft based on Bylaws and GitHub Security Standards |