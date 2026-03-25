### Accessibility Audit Procedure (Annual)

| Document Control | |
| :--- | :--- |
| **Document ID** | DA-PRC-001 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a systematic, annual evaluation of Study GRC Inc.’s digital assets to ensure compliance with the Web Content Accessibility Guidelines (WCAG) 2.2 Level AA, the Americans with Disabilities Act (ADA), and Section 508 of the Rehabilitation Act.

This procedure directly supports **Article I, Section 1.3** of the Bylaws, which mandates the Organization to "remove barriers" and "empower learners." By ensuring our open-source resources are accessible to individuals with disabilities, we fulfill our charitable mission and maintain eligibility for federal grant funding.

### 2. Scope
This procedure applies to all public-facing and internal digital properties owned or controlled by Study GRC Inc., including but not limited to:
*   **Public Website:** Main marketing and community pages.
*   **Learning Management System (LMS):** Course players, quizzes, and student dashboards.
*   **Digital Resources:** PDFs, documents, and downloadable assets.
*   **Volunteer Portals:** Administrative interfaces used by volunteers and staff.

**Exclusions:** Third-party content or platforms not under the direct technical control of the Organization, though best efforts must be made to select accessible vendors.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **WCAG 2.2 AA** | Web Content Accessibility Guidelines version 2.2, Level AA. The international standard for web accessibility and the Organization's target compliance level. |
| **Assistive Technology (AT)** | Software or hardware used by people with disabilities to interact with digital content (e.g., screen readers like NVDA or VoiceOver, screen magnifiers, switch controls). |
| **VPAT** | Voluntary Product Accessibility Template. A document explaining how an information and communication technology (ICT) product conforms to Section 508 standards. |
| **Remediation** | The process of correcting code, design, or content to resolve accessibility violations. |
| **Critical Violation** | An issue that prevents a user from accessing core content or completing a primary function (e.g., unable to donate, unable to start a course). |

### 4. Procedures

#### 4.1 Phase 1: Audit Scope and Sampling
**Responsibility:** CISO / Audit Lead
1.  **Define the Audit Boundary:** Identify all domains, subdomains, and applications to be tested.
2.  **Select Representative Sample:** Due to the volume of content, the Audit Lead must select a representative sample of pages that includes:
    *   The Homepage and Global Navigation (Header/Footer).
    *   Core "User Journey" pages (e.g., Donation Flow, Membership Sign-up, Contact Form).
    *   One (1) example of every distinct page template (e.g., Blog Post, Event Page, Course Module).
    *   High-traffic pages based on analytics from the previous 12 months.
    *   Any new features deployed since the last audit.

#### 4.2 Phase 2: Automated Testing
**Responsibility:** IT/Web Team
1.  **Tool Selection:** Use an approved automated scanning tool (e.g., Axe, WAVE, or Lighthouse).
2.  **Execution:** Run site-wide crawls or page-specific scans on the sample set defined in Phase 1.
3.  **Analysis:** Filter results to identify systemic issues (e.g., missing alt text on all images, improper heading hierarchy).
4.  **Documentation:** Export automated reports to the audit repository.
    *   *Note:* Automated testing typically catches only 30-40% of accessibility issues. It must not be the sole testing method.

#### 4.3 Phase 3: Manual Technical Testing
**Responsibility:** QA Tester / Accessibility Specialist
1.  **Keyboard Navigation:** Navigate the sample pages using **only** the keyboard (Tab, Enter, Space, Arrows).
    *   Verify visual focus indicators are visible at all times.
    *   Verify no "keyboard traps" exist.
    *   Verify logical tab order (left-to-right, top-to-bottom).
2.  **Zoom and Reflow:**
    *   Zoom the browser to 200% and 400%. Verify content does not overlap or disappear and that horizontal scrolling is not required (reflow).
3.  **Color Contrast:**
    *   Manually spot-check text and UI components against the 4.5:1 (normal text) and 3:1 (large text/UI) contrast ratio requirements.

#### 4.4 Phase 4: Assistive Technology (Screen Reader) Testing
**Responsibility:** QA Tester / Accessibility Specialist
1.  **Environment:** Test using at least one desktop screen reader (e.g., NVDA on Windows or VoiceOver on macOS) and one mobile screen reader (e.g., TalkBack on Android or VoiceOver on iOS).
2.  **Core Tasks:** Attempt to complete primary tasks solely via screen reader:
    *   Register for an account.
    *   Navigate a course module.
    *   Download a resource.
3.  **Verification Points:**
    *   Ensure all images have appropriate alternative text.
    *   Ensure form labels are properly associated with inputs.
    *   Ensure dynamic content (pop-ups, error messages) is announced to the user.

#### 4.5 Phase 5: Reporting and Prioritization
**Responsibility:** Audit Lead
1.  **Compile Findings:** Aggregate data from automated, manual, and AT testing into a single **Accessibility Audit Report**.
2.  **Risk Classification:** Assign a severity level to each finding:
    *   **Critical:** Blocks a user from completing a task. Immediate fix required (SLA: 48 hours).
    *   **High:** Significant barrier/frustration but a workaround exists. Fix required (SLA: 14 days).
    *   **Medium/Low:** Minor annoyance or cosmetic issue. Fix scheduled in backlog (SLA: 90 days).
3.  **Remediation Plan:** Create Jira/GitHub tickets for all findings, assigned to the appropriate developers or content creators.

#### 4.6 Phase 6: Remediation and Re-Testing
**Responsibility:** IT/Web Team & Audit Lead
1.  **Fix Implementation:** Developers apply code fixes; Content Creators update text/media.
2.  **Regression Testing:** The Audit Lead verifies the fix and ensures no new issues were introduced.
3.  **Closure:** Mark tickets as "Resolved" only after verification.

#### 4.7 Phase 7: Transparency and Disclosure
**Responsibility:** VP of Education & Training / CISO
1.  **Update Accessibility Statement:** Update the "Last Updated" date on the public Accessibility Statement (footer link).
2.  **VPAT Generation (If applicable):** If required for federal grant reporting, generate an updated VPAT based on the audit results.
3.  **Board Reporting:** Submit a summary of the Audit Report to the Board of Directors as part of the Annual Technology Review.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Executive Director** | Approves the audit budget and resources; ensures organizational commitment to remediation. |
| **CISO / Audit Lead** | Owns the audit process, selects tools, classifies risks, and reports to the Board. |
| **IT/Web Team** | Performs automated scans, implements code-level remediation, and manages the deployment pipeline. |
| **VP of Education** | Ensures all curriculum content (PDFs, videos, slides) included in the audit is remediated. |
| **QA Tester** | Conducts manual keyboard and screen reader testing. |

### 6. Compliance and Enforcement
Failure to adhere to this procedure may result in the Organization creating discriminatory barriers, violating federal grant conditions (2 CFR 200 / Section 508), and facing legal liability under the ADA.

Employees or volunteers found to be repeatedly deploying inaccessible code or content without regard for this procedure may be subject to disciplinary action, up to and including termination of employment or volunteer assignment, in accordance with the **Progressive Discipline Policy**.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article I, Section 1.3; Article IX, Section 9.3)
*   **Web Content Accessibility Guidelines (WCAG) 2.2**
*   **DA-POL-001:** Digital Accessibility Policy
*   **DA-STD-001:** Automated Accessibility Testing Standard
*   **DA-CKL-001:** WCAG 2.2 Level AA Compliance Checklist

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Compliance Architect | Initial Release |