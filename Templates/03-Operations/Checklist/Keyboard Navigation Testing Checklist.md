### Keyboard Navigation Testing Checklist

| Document Control | |
| :--- | :--- |
| **Document ID** | ACC-CHK-008 |
| **Document Type** | Checklist / Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-04-27 (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training |
| **Classification** | Public |

### 1. Purpose
The purpose of this checklist is to ensure that all digital assets, learning management systems (LMS), and open-source resources produced by **Study GRC Inc.** are fully functional and accessible via keyboard interfaces. This document operationalizes the Organization's commitment to "empowering learners" as defined in **Bylaws Article I, Section 1.3**, and ensures compliance with the **Web Content Accessibility Guidelines (WCAG) 2.2**, specifically **Guideline 2.1 (Keyboard Accessible)**.

### 2. Scope
This checklist applies to all web-based content, software, and digital resources developed, maintained, or procured by Study GRC Inc.
*   **Applies to:** All front-end developers, QA testers, content creators, and third-party vendors delivering digital products.
*   **Includes:** The public website, community forums, LMS platforms, and interactive open-source tools.
*   **Exclusions:** Native mobile applications (covered under separate mobile accessibility standards), though similar principles apply.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Focus Indicator** | A visual effect (usually a border or outline) that indicates which component currently has the keyboard focus. |
| **Keyboard Trap** | A situation where a keyboard user can move focus into a component (like a modal or widget) but cannot move focus out of it using standard keyboard commands. |
| **Tab Order** | The sequence in which focusable elements (links, buttons, form fields) receive focus when the user presses the `Tab` key. |
| **Semantic HTML** | The use of HTML markup to reinforce the meaning of the information in web pages and web applications rather than merely to define its presentation (e.g., using `<button>` instead of `<div>` for clickable actions). |

### 4. Testing Procedures

Testers must perform the following checks without the use of a mouse or trackpad. All failures must be logged as "Critical" bugs in the issue tracking system, as keyboard inaccessibility prevents use by assistive technology (screen readers).

#### 4.1 Preparation
*   [ ] **Disconnect Mouse:** Physically move the mouse out of reach or disable the trackpad to ensure no accidental usage.
*   [ ] **Browser Setup:** Ensure the browser is configured to allow tabbing through all interactive elements (e.g., macOS System Settings > Keyboard > "Keyboard navigation" toggle is ON).

#### 4.2 Navigation and Focus (WCAG 2.4.3, 2.4.7)
*   [ ] **Tab Key Navigation:** Press `Tab` to move forward through the page. Focus must move to all interactive elements (links, buttons, form fields, media player controls).
*   [ ] **Shift+Tab Navigation:** Press `Shift + Tab` to move backward. The order must be consistent with the forward navigation.
*   [ ] **Logical Order:** The focus order must match the visual layout and logical reading order of the page (e.g., Left-to-Right, Top-to-Bottom).
*   [ ] **Visual Focus Indicator:** Every element receiving focus must have a clearly visible focus indicator (e.g., a high-contrast outline).
    *   *Note:* The CSS rule `outline: none` is strictly prohibited unless replaced by a compliant alternative style.
*   [ ] **Off-Screen Content:** Focus must not move to elements that are hidden or off-screen unless that action triggers the content to become visible (e.g., a "Skip to Content" link).

#### 4.3 Interaction and Functionality (WCAG 2.1.1)
*   [ ] **Links:** Press `Enter` on a focused link. It must navigate to the target.
*   [ ] **Buttons:** Press `Enter` or `Space` on a focused button. The action (submit, toggle, delete) must execute.
*   [ ] **Checkboxes:** Press `Space` to check/uncheck.
*   [ ] **Radio Buttons:** Use `Arrow Keys` to move between options; `Space` to select (if not auto-selected).
*   [ ] **Dropdowns/Select Menus:**
    *   Press `Enter` or `Space` to open.
    *   Use `Arrow Keys` to navigate options.
    *   Press `Enter` to select an option.
    *   Press `Esc` to close without selecting (if applicable).
*   [ ] **Sliders:** Use `Arrow Keys` to adjust values.

#### 4.4 No Keyboard Traps (WCAG 2.1.2)
*   [ ] **Entry/Exit:** Ensure that for every element you can tab *into*, you can also tab *out of*.
*   [ ] **Modals/Pop-ups:**
    *   When a modal opens, focus must move *inside* the modal immediately.
    *   Focus must be "trapped" within the modal while it is open (tabbing should cycle through modal elements only, not the background page).
    *   Pressing `Esc` must close the modal and return focus to the element that triggered the modal.

#### 4.5 Bypass Blocks (WCAG 2.4.1)
*   [ ] **Skip Link:** A "Skip to Main Content" link must be the first focusable element on the page.
*   [ ] **Activation:** Activating the Skip Link must move focus directly to the main content area, bypassing navigation menus.

#### 4.6 Time Limits (WCAG 2.2.1)
*   [ ] **Session Timeouts:** If a timeout warning appears, the user must be able to extend the session using only the keyboard.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Front-End Developers** | Ensure semantic HTML is used; manage focus states via CSS/JS; prevent keyboard traps in custom widgets. |
| **QA Testers** | Execute this checklist on all new features prior to deployment; log accessibility defects. |
| **Content Creators** | Ensure content order is logical; avoid using non-interactive elements (like `<div>` or `<span>`) for interactive features without proper ARIA roles. |
| **VP of Education** | Final sign-off authority for LMS and educational resource accessibility compliance. |

### 6. Compliance and Enforcement
Failure to comply with this standard constitutes a violation of the Organization's commitment to inclusivity and its **Digital Accessibility Policy**.
*   **Release Blocking:** Any "Critical" failure identified in this checklist (e.g., a keyboard trap or missing focus indicator) is considered a release blocker. The software or content update may not be published until remediated.
*   **Remediation:** Existing content found to be non-compliant must be prioritized for remediation in the immediate next sprint or maintenance cycle.

### 7. References
*   **ACC-POL-001:** Digital Accessibility Policy
*   **W3C Recommendation:** [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
*   **Study GRC Bylaws:** Article I, Section 1.3 (Nonprofit & Tax-Exempt Purpose)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Compliance Architect | Initial release aligned with WCAG 2.2. |