### Screen Reader Testing Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | ACC-PRC-007 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized methodology for validating the accessibility of Study GRC Inc.’s digital assets using assistive technology. This procedure ensures that the Organization’s "zero-cost, open-source resources" (Bylaws Art. I, §1.3) are functionally usable by individuals with visual impairments. This protocol mitigates legal risk under the Americans with Disabilities Act (ADA) and ensures compliance with the Web Content Accessibility Guidelines (WCAG) 2.2 Level AA.

### 2. Scope
This procedure applies to all public-facing and internal digital platforms managed by Study GRC Inc.

*   **Inclusions:**
    *   Public Website (studygrc.org) and Community Forums.
    *   Learning Management Systems (LMS) and course interfaces.
    *   Digital documents (PDF, DOCX) intended for public distribution.
    *   Third-party integrations where configuration control exists.
*   **Exclusions:**
    *   Raw code repositories (e.g., GitHub) not intended for direct content consumption (though the *interface* of the repository is subject to the provider's accessibility).
    *   Archived content published prior to January 1, 2023, unless a specific accommodation request is received.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Screen Reader** | Software that converts digital text into synthesized speech or Braille output (e.g., NVDA, JAWS, VoiceOver). |
| **Focus Indicator** | A visual cue (usually a border or highlight) that shows which element on the page currently has the keyboard focus. |
| **ARIA** | Accessible Rich Internet Applications; a set of attributes that define ways to make web content and web applications more accessible to people with disabilities. |
| **Reading Order** | The sequence in which a screen reader navigates through the content, which must match the logical visual flow. |
| **NVDA** | NonVisual Desktop Access; a free, open-source screen reader for Windows. |
| **VoiceOver** | The built-in screen reader for Apple (macOS/iOS) devices. |

### 4. Procedures

#### 4.1 Testing Environment Configuration
Testers must configure their environment to match the most common user setups.

1.  **Primary Test Combination (Windows):** NVDA (latest stable version) with Firefox or Chrome.
2.  **Secondary Test Combination (macOS):** VoiceOver with Safari.
3.  **Mobile Test Combination:** VoiceOver (iOS) or TalkBack (Android) on physical devices, not emulators.
4.  **Audio Configuration:** Testers must use headphones to accurately hear the synthesis without background noise interference.

#### 4.2 Navigation and Wayfinding Testing
Testers must verify that users can navigate the structure of the page efficiently.

1.  **Skip Links:** Load the page and immediately press `Tab`. Verify a "Skip to Main Content" link appears and, when activated, moves focus to the main content area (`<main>`).
2.  **Heading Hierarchy:**
    *   **NVDA:** Press `H` to cycle through headings.
    *   **Verification:** Ensure headings follow a logical hierarchy (H1 -> H2 -> H3) without skipping levels. The H1 must accurately describe the page topic.
3.  **Landmarks:**
    *   **NVDA:** Press `D` to cycle through landmarks (Banner, Navigation, Main, Contentinfo).
    *   **Verification:** Ensure all major page regions are identified programmatically.

#### 4.3 Content Consumption Testing
Testers must verify that content is read in a logical order and images are described.

1.  **Reading Order:**
    *   **NVDA:** Use the `Down Arrow` key to read through the page line-by-line.
    *   **Verification:** Ensure the reading order matches the visual layout. Multi-column layouts must read top-to-bottom, left-to-right (column by column), not across columns illogically.
2.  **Images and Graphics:**
    *   **Verification:** Ensure informative images have descriptive Alt Text.
    *   **Decorative Images:** Verify that decorative images (backgrounds, spacers) are ignored by the screen reader (Alt attribute is null/empty).
3.  **Data Tables:**
    *   **NVDA:** Navigate into the table. Use `Ctrl + Alt + Arrow Keys` to move between cells.
    *   **Verification:** Ensure column and row headers are announced before the cell data (e.g., "Column: Price, Row: Basic Plan, Cell: Free").

#### 4.4 Interactive Element Testing (Forms & Controls)
Testers must verify that all interactive elements are announced correctly and operable.

1.  **Keyboard Focus:** Press `Tab` to move through all interactive elements. Verify the **Focus Indicator** is always visible.
2.  **Links:**
    *   **Verification:** Link text must be descriptive out of context. (e.g., "Read more about GRC" instead of just "Read more").
3.  **Buttons vs. Links:** Verify that buttons (triggering actions) are announced as "Button" and links (navigation) are announced as "Link".
4.  **Forms:**
    *   **NVDA:** Enter "Focus Mode" (usually automatic) when tabbing into a field.
    *   **Verification:** Ensure the `<label>` is announced when the field receives focus. Placeholder text alone is insufficient.
    *   **Error Handling:** Trigger a form error. Verify the screen reader immediately announces the error message or moves focus to the error summary.

#### 4.5 Dynamic Content and Modals
1.  **Modal Dialogs:**
    *   Open a modal (pop-up).
    *   **Verification:** Focus must move *inside* the modal immediately.
    *   **Trapping:** Verify focus cannot escape the modal to the background page until the modal is closed.
    *   **Closing:** Verify pressing `Esc` closes the modal and returns focus to the trigger button.
2.  **Status Updates:**
    *   Trigger a dynamic change (e.g., "Item added to cart").
    *   **Verification:** Ensure the update is announced via `aria-live` regions without moving the user's focus.

#### 4.6 Defect Reporting
If a test step fails, the tester must log a defect in the issue tracking system (e.g., GitHub Issues/Jira) with the following details:

1.  **Title:** [Accessibility] - [Component Name] - [Issue Summary].
2.  **Environment:** OS version, Browser version, Screen Reader version.
3.  **Steps to Reproduce:** Specific keyboard commands used.
4.  **Expected Behavior:** What the screen reader *should* have announced.
5.  **Actual Behavior:** What the screen reader *did* announce (or silence).
6.  **Severity:**
    *   **Critical:** User cannot access content or complete a task (Blocker).
    *   **Major:** User can complete task with significant difficulty/workaround.
    *   **Minor:** Annoyance or verbose output that does not prevent task completion.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **QA Tester / Volunteer** | Execute this procedure using the designated software; log defects accurately. |
| **Front-End Developer** | Remediate identified defects; ensure semantic HTML is used during development. |
| **VP of Education & Training** | Ensure all course materials (PDFs, Slides) undergo screen reader validation before publication. |
| **Product Owner** | Prioritize accessibility defects in the backlog; ensure "Critical" defects block release. |

### 6. Compliance and Enforcement
Accessibility is a core component of the Organization's non-profit status and ethical mission.
*   **Release Gating:** No software update or course module may be released to the public with known **Critical** accessibility defects.
*   **Disciplinary Action:** Failure to adhere to this procedure, specifically the intentional bypassing of accessibility checks, may result in disciplinary action, up to and including termination of employment or volunteer assignment.

### 7. References
*   **ACC-POL-001:** Digital Accessibility Policy
*   **ACC-STD-001:** WCAG 2.2 Level AA Compliance Checklist
*   **External:** Web Content Accessibility Guidelines (WCAG) 2.2
*   **External:** NVDA User Guide (NV Access)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Compliance Architect | Initial release of testing procedure. |