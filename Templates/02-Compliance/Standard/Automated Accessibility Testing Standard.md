### Automated Accessibility Testing Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | ACC-STD-006 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training |
| **Classification** | Public |

### 1. Purpose
The purpose of this standard is to define the mandatory technical requirements, tooling configurations, and integration points for automated accessibility testing within Study GRC Inc.'s digital ecosystem.

In accordance with **Bylaws Article I, Section 1.3**, which commits the Organization to "removing financial barriers" and empowering learners, we must ensure our open-source resources are technically accessible to individuals with disabilities. This standard mitigates legal risk under the Americans with Disabilities Act (ADA) and ensures efficient identification of machine-detectable violations of the Web Content Accessibility Guidelines (WCAG).

### 2. Scope
This standard applies to all digital assets developed, maintained, or hosted by Study GRC Inc., including but not limited to:
*   Public-facing websites (studygrc.org).
*   Learning Management Systems (LMS) and curriculum platforms.
*   Open-source code repositories and documentation.
*   Internal administrative dashboards used by employees and volunteers.

**Exclusions:** Third-party platforms (e.g., donor processing gateways) where Study GRC Inc. has no code-level control, though these must be vetted per the *Vendor Security Risk Assessment*.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **WCAG 2.2 AA** | Web Content Accessibility Guidelines version 2.2, Level AA. The target compliance standard for the Organization. |
| **CI/CD Pipeline** | Continuous Integration/Continuous Deployment. The automated process of testing and deploying code changes. |
| **Axe-core** | The industry-standard, open-source accessibility testing engine required for use by this Organization. |
| **Blocking Error** | An accessibility violation detected by automation that prevents a code deployment from proceeding to production. |
| **False Positive** | A test result that incorrectly indicates a failure where none exists. |

### 4. Standards

#### 4.1 Approved Tooling and Engines
To ensure consistency across the Organization's open-source projects, all automated testing must utilize the **Axe-core** engine (or a wrapper utilizing it, such as `pa11y`, `jest-axe`, or `cypress-axe`).
*   **4.1.1** Proprietary or closed-source scanning tools require written approval from the Chief Information Security Officer (CISO) to ensure they do not violate the Organization’s Open Source Commitment (Bylaws Article IX, Section 9.3).
*   **4.1.2** Tools must be configured to test against **WCAG 2.2 Level AA** rulesets.

#### 4.2 Integration Points
Automated accessibility testing must occur at three distinct stages of the Software Development Life Cycle (SDLC):

**4.2.1 Local Development (Pre-Commit)**
*   Developers and contributors must utilize IDE plugins (e.g., VS Code Axe Linter) or local CLI tools to identify violations prior to committing code.
*   **Requirement:** Zero "Critical" or "Serious" violations allowed in new code blocks.

**4.2.2 CI/CD Pipeline (Pull Request)**
*   Automated scans must run on every Pull Request (PR) affecting User Interface (UI) code.
*   **Gatekeeper Rule:** The build **must fail** if the scanner detects any violation classified as "Critical" or "Serious" (e.g., missing alt text, empty buttons, invalid ARIA attributes).
*   PRs cannot be merged until these violations are remediated or explicitly waived as a False Positive by a designated reviewer.

**4.2.3 Production Monitoring (Scheduled)**
*   A full site crawl must be performed weekly on all public-facing domains.
*   Reports must be generated in a machine-readable format (JSON/CSV) and retained for 12 months for audit purposes.

#### 4.3 Configuration and Rulesets
*   **4.3.1** The testing configuration must enable rules for:
    *   Color Contrast (Ratio 4.5:1 for normal text).
    *   Document Structure (Headings, Landmarks).
    *   Forms (Labels, ARIA).
    *   Keyboard Focus indicators (where detectable by automation).
*   **4.3.2** "Best Practice" rules may be enabled as warnings but must not block deployment unless authorized by the VP of Education & Training.

#### 4.4 Limitations and Manual Testing Handoff
Automated testing captures approximately 30-50% of accessibility issues. It is **not** a replacement for manual review.
*   **4.4.1** Passing automated tests does not constitute certification of compliance.
*   **4.4.2** All features passing the automated gate must subsequently undergo manual review as defined in the *Accessibility Audit Procedure*.

#### 4.5 False Positive Management
*   **4.5.1** If a tool flags a False Positive, it may be suppressed via a configuration file (e.g., `axe-config.json`).
*   **4.5.2** Every suppression requires a code comment explaining *why* it is a false positive, including the date and the author's handle.
*   **4.5.3** Suppressions must be reviewed quarterly to determine if tool updates render the suppression unnecessary.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **VP of Education & Training** | Owner of the standard; ensures curriculum platforms meet tooling requirements. |
| **DevOps Engineer / IT Volunteer** | Implements and maintains the CI/CD pipeline integrations; ensures scanners are updated to the latest version. |
| **Developer / Contributor** | Runs local tests; remediates blocking errors identified during the PR process. |
| **QA Lead** | Reviews and approves False Positive suppressions; configures rulesets. |

### 6. Compliance and Enforcement
Failure to comply with this standard may result in the rejection of code contributions, revocation of repository write access, or disciplinary action for employees/volunteers. Deliberate circumvention of automated accessibility checks (e.g., disabling the linter without authorization) is considered a violation of the *Code of Ethics*.

### 7. References
*   **ACC-POL-001:** Digital Accessibility Policy
*   **ACC-PRC-002:** Accessibility Audit Procedure (Manual)
*   **Bylaws Article I:** Purposes (Charitable & Educational)
*   **W3C:** Web Content Accessibility Guidelines (WCAG) 2.2

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Compliance Architect | Initial Release |