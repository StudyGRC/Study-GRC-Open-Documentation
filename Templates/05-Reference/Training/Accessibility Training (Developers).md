### Standard for Developer Accessibility Training

| Document Control | |
| :--- | :--- |
| **Document ID** | ACC-STD-018 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to define the mandatory curriculum, frequency, and competency requirements for technical staff regarding digital accessibility. This training ensures that **Study GRC Inc.** fulfills its mission under **Bylaws Article 1.3** to "remove barriers" and "empower learners" by guaranteeing that all software, websites, and digital resources are coded to be perceivable, operable, understandable, and robust for users with disabilities. This document ensures technical implementation compliance with **WCAG 2.2 Level AA** and the **Americans with Disabilities Act (ADA)**.

### 2. Scope
This Standard applies to all individuals contributing code or technical architecture to the Organization's digital ecosystem, including:
*   **Frontend and Full-Stack Developers** (Employees, Contractors, and Volunteers).
*   **QA Engineers** and Test Automation Specialists.
*   **UI/UX Designers** (regarding technical feasibility of designs).
*   **Product Managers** (regarding acceptance criteria).

**Exclusions:** Backend-only developers who do not touch API data structures consumed by user interfaces or generate HTML/DOM elements are exempt from the UI-specific modules but must complete the "Fundamentals" module.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **WCAG 2.2 AA** | Web Content Accessibility Guidelines version 2.2, Level AA; the technical standard adopted by the Organization for compliance. |
| **ARIA** | Accessible Rich Internet Applications; a set of attributes that define ways to make web content and web applications (especially those developed with Ajax and JavaScript) more accessible to people with disabilities. |
| **Assistive Technology (AT)** | Software or hardware used by people with disabilities to interact with digital content (e.g., NVDA, JAWS, VoiceOver, Sip-and-Puff switches). |
| **Semantic HTML** | The use of HTML markup to reinforce the semantics, or meaning, of the information in webpages and web applications rather than merely to define its presentation or look. |
| **DOM** | Document Object Model; the data representation of the objects that comprise the structure and content of a document on the web. |

### 4. Training Standards and Curriculum Requirements

#### 4.1 Training Frequency and Timing
To ensure "Implementation" compliance, training must occur at the following intervals:
1.  **Onboarding:** All new technical contributors must complete the **Core Curriculum** within their first fourteen (14) days of service and *prior* to their first code merge to the `main` or `production` branch.
2.  **Annual Refresher:** A condensed update course covering new WCAG success criteria and tooling updates must be completed annually.
3.  **Remediation Trigger:** Any developer who introduces a "Critical" accessibility regression into production (as defined in `ACC-POL-001`) must retake the relevant training module before regaining commit privileges.

#### 4.2 Core Curriculum Modules
The training program must include, at a minimum, the following technical modules:

**Module A: The Business and Legal Case (Fundamentals)**
*   Overview of **Bylaws Article 1.3** (Charitable Purpose).
*   Legal risks: ADA Title III, Section 508, and the Organization's **Digital Accessibility Policy**.
*   Types of disabilities (Visual, Auditory, Motor, Cognitive) and how they impact software usage.

**Module B: Semantic HTML & Structure**
*   Proper use of Heading levels (`h1`-`h6`) for navigation.
*   Landmarks (`<nav>`, `<main>`, `<aside>`, `<footer>`).
*   Button vs. Anchor links (When to use `<button>` vs `<a>`).
*   Lists and Tables structure.

**Module C: ARIA and Dynamic Content**
*   **The First Rule of ARIA:** Do not use ARIA if a native HTML element serves the purpose.
*   `aria-label`, `aria-labelledby`, and `aria-describedby`.
*   Managing state changes (e.g., `aria-expanded`, `aria-hidden`, `aria-live` regions).
*   Common anti-patterns and "ARIA bloat."

**Module D: Keyboard Navigation & Focus Management**
*   Ensuring all interactive elements are tab-accessible.
*   Managing focus programmatically (e.g., moving focus to a modal when opened, and back to the trigger when closed).
*   Visible focus indicators (CSS `outline` requirements).
*   Skip-to-content links.

**Module E: Forms and Input Validation**
*   Explicit label association (`<label for="id">`).
*   Error identification and description (programmatic association of error text).
*   Autocomplete attributes.

**Module F: Testing and Tooling**
*   **Automated Testing:** How to use the Organization's required linting tools (e.g., `eslint-plugin-jsx-a11y`, `axe-core`).
*   **Manual Testing:** Basic usage of a Screen Reader (NVDA or VoiceOver) for validation.
*   **Keyboard Testing:** Validating tab order and trap prevention.

#### 4.3 Assessment and Competency
*   **Knowledge Check:** Each module must conclude with a quiz requiring a score of 80% or higher to pass.
*   **Practical Exercise:** The training must include a "Fix the Bug" exercise where the developer identifies and remediates accessibility errors in a sample code repository.

#### 4.4 Record Keeping
Completion of training must be logged in the Organization's Learning Management System (LMS) or HR records. These records are subject to audit under **Bylaws Article VIII** (Records, Transparency & Finance).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **VP of Education & Training** | Develops and maintains the training curriculum; ensures content aligns with current WCAG standards. |
| **Engineering Lead** | Enforces training completion; blocks Pull Requests (PRs) from untrained contributors; mentors staff on complex accessibility implementations. |
| **Developer / Contributor** | Completes mandatory training; applies accessibility principles in all code; utilizes approved testing tools prior to submission. |
| **QA Engineer** | Verifies that code submissions meet the accessibility criteria defined in the training. |

### 6. Compliance and Enforcement
Failure to complete this mandatory training will result in the suspension of repository write access (commit/push privileges).

Repeated failure to apply training concepts, resulting in the introduction of accessibility barriers, may result in disciplinary action up to and including termination of employment or volunteer assignment, as this constitutes a violation of the Organization's core charitable purpose defined in the **Bylaws**.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article 1.3 - Purpose)
*   **ACC-POL-001:** Digital Accessibility Policy
*   **ACC-STD-005:** Automated Accessibility Testing Standard
*   **ACC-GUD-010:** Alt Text Writing Guidelines
*   **W3C Web Content Accessibility Guidelines (WCAG) 2.2**

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial Release of Developer Training Standard |