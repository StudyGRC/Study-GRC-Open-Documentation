### Accessibility Testing Protocol

| Document Control | |
| :--- | :--- |
| **Document ID** | DA-PRC-005 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training |
| **Classification** | Public |

### 1. Purpose
The purpose of this protocol is to establish a standardized, repeatable methodology for validating that Study GRC Inc.’s digital assets comply with the Web Content Accessibility Guidelines (WCAG) 2.2 Level AA. This procedure supports the Organization’s charitable purpose as defined in **Bylaws Article I, Section 1.3**, specifically the commitment to "removing financial barriers" and "empowering learners," by ensuring that disability is not a barrier to accessing our open-source resources. This protocol serves as the primary Quality Assurance (QA) mechanism for digital inclusion.

### 2. Scope
This procedure applies to all digital products and content developed, maintained, or procured by Study GRC Inc.

**In Scope:**
*   Public-facing websites (studygrc.org and subdomains).
*   Learning Management Systems (LMS) and courseware.
*   Open-source repositories and documentation hosted on GitHub/GitLab.
*   Digital documents (PDF, DOCX, PPT) distributed to the community.
*   Third-party integrations where configuration control exists.

**Exclusions:**
*   Third-party content or platforms where Study GRC Inc. has no administrative control over the code or interface (e.g., external social media platforms), though best efforts must be made regarding content posted thereon.
*   Archived legacy content published prior to [Date], unless a specific request for remediation is received.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **WCAG 2.2 AA** | Web Content Accessibility Guidelines version 2.2, Level AA. The international standard for web accessibility and the target compliance level for the Organization. |
| **AT (Assistive Technology)** | Software or hardware used by people with disabilities to interact with digital content (e.g., screen readers, braille displays, switch controls). |
| **Focus Indicator** | A visual cue (usually a border or outline) that shows which element on a web page currently has the keyboard focus. |
| **Keyboard Trap** | A situation where a keyboard user can enter a component or section of a page but cannot exit it using standard keyboard commands. |
| **ARIA** | Accessible Rich Internet Applications. A set of attributes that define ways to make web content and web applications more accessible to people with disabilities. |
| **Remediation** | The process of correcting accessibility violations in code or content. |

### 4. Procedures

Testing must occur at three stages: **Design Review** (pre-code), **Development Testing** (automated), and **QA Validation** (manual/AT).

#### 4.1 Automated Testing (Stage 1)
Automated testing captures approximately 30-40% of accessibility issues. It must be run prior to any manual testing.

1.  **Tool Selection:** Use approved automated scanning tools (e.g., Axe-core, WAVE, or Lighthouse).
2.  **Execution:**
    *   Run the scanner on every unique page template.
    *   Run the scanner on any page with dynamic state changes (e.g., after a modal opens).
3.  **Zero-Error Standard:** All "Critical" and "Serious" errors flagged by the automated tool must be resolved before proceeding to manual testing.
4.  **False Positives:** Any flagged issue deemed a "false positive" must be documented with a technical justification in the testing log.

#### 4.2 Manual Keyboard Navigation Testing (Stage 2)
Manual testing is required to verify operability for users with motor impairments.

1.  **Setup:** Disconnect the mouse or disable the trackpad.
2.  **Tab Order (SC 2.4.3):** Use the `Tab` key to navigate through the page. Verify that the focus order follows a logical, sequential path (usually left-to-right, top-to-bottom).
3.  **Focus Visible (SC 2.4.7):** Verify that every interactive element (links, buttons, form fields) has a clearly visible focus indicator when active.
4.  **Keyboard Operability (SC 2.1.1):**
    *   Verify all interactive elements can be activated using `Enter` or `Spacebar`.
    *   Verify custom widgets (sliders, menus) can be operated with arrow keys.
5.  **No Keyboard Traps (SC 2.1.2):** Ensure focus can be moved *away* from any component using standard keys (Tab, Esc, Arrows) without refreshing the page.
6.  **Bypass Blocks (SC 2.4.1):** Verify a "Skip to Main Content" link exists and functions correctly as the first focusable element.

#### 4.3 Screen Reader Testing (Stage 3)
Testing with Assistive Technology (AT) verifies compatibility for visually impaired users.

1.  **Approved Combinations:**
    *   **Windows:** NVDA (NonVisual Desktop Access) with Firefox or Chrome.
    *   **macOS:** VoiceOver with Safari.
2.  **Navigation Verification:**
    *   **Headings:** Navigate by headings (`H` key). Verify the hierarchy is logical (H1 -> H2 -> H3) and describes the content structure.
    *   **Landmarks:** Navigate by landmarks/regions. Ensure main, navigation, and footer regions are correctly identified.
3.  **Interactive Elements:**
    *   **Buttons vs. Links:** Verify that buttons are announced as "Button" and links as "Link."
    *   **Forms:** Verify that all form fields have associated labels announced by the screen reader.
    *   **Dynamic Content:** Trigger modals or alerts. Verify the screen reader announces the new content or status message immediately (ARIA Live Regions).
4.  **Images (SC 1.1.1):** Verify that meaningful images have descriptive Alt Text and decorative images are ignored by the screen reader.

#### 4.4 Visual and Zoom Testing (Stage 4)
Verifies support for low-vision users.

1.  **Zoom (SC 1.4.4):** Set browser zoom to **200%**. Verify that:
    *   No text is cut off or overlapping.
    *   No horizontal scrolling is required (Reflow SC 1.4.10).
    *   All functionality remains available.
2.  **Color Contrast (SC 1.4.3):** Use a Color Contrast Analyzer (CCA) to verify:
    *   Normal text has a ratio of at least **4.5:1** against the background.
    *   Large text (18pt+ or 14pt bold) has a ratio of at least **3:1**.
    *   UI Components (borders, icons) have a ratio of at least **3:1** (SC 1.4.11).
3.  **Use of Color (SC 1.4.1):** Ensure color is not the *only* visual means of conveying information (e.g., error messages must have an icon or text prefix, not just red text).

#### 4.5 Document Remediation (PDFs)
For downloadable resources:

1.  **Source File:** Remediation should occur in the source document (Word/InDesign) before export.
2.  **Tagging:** Verify the PDF is "Tagged" using Adobe Acrobat Pro Accessibility Checker.
3.  **Reading Order:** Manually verify the reading order in the Tags panel matches the visual logic.
4.  **Metadata:** Ensure the document has a Title and Language set in properties.

#### 4.6 Defect Reporting and Blocking
1.  **Logging:** All failures must be logged in the Organization’s issue tracking system (e.g., GitHub Issues/Jira) with the tag `Accessibility`.
2.  **Severity Classification:**
    *   **Blocker:** Prevents access to core functionality (e.g., "Sign Up" button inaccessible). *Release is blocked.*
    *   **Critical:** Significant barrier but workaround exists. *Must be fixed before next minor release.*
    *   **Major:** Frustrating but accessible. *Scheduled for next sprint.*
    *   **Minor:** Cosmetic or technical adherence issue. *Backlog.*

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **VP of Education & Training** | Accountable for the overall accessibility of curriculum and LMS platforms. Approves final release of major educational products. |
| **QA Lead / Tester** | Executes this protocol. Maintains testing tools and environments. Logs defects and verifies fixes. |
| **Developers / Engineers** | Responsible for writing semantic HTML and ARIA code. Must perform "Unit Testing" (Stage 1 & 2) prior to committing code. |
| **Content Creators** | Responsible for non-technical accessibility (Alt text, heading structure, color contrast in graphics). |
| **Executive Director** | Ensures budget and resources are available for accessibility tools and training. |

### 6. Compliance and Enforcement
**Release Gating:** Digital products or major updates that fail Stage 1 (Automated) or Stage 2 (Keyboard) testing are strictly prohibited from being deployed to the production environment.

**Vendor Compliance:** External vendors delivering digital work products must provide a completed Voluntary Product Accessibility Template (VPAT) or equivalent testing report demonstrating adherence to this protocol.

Failure to adhere to this protocol may result in disciplinary action, up to and including termination of employment or contract, particularly if negligence exposes the Organization to legal liability under the ADA or reputational damage.

### 7. References
*   **Study GRC Inc. Digital Accessibility Policy (DA-POL-001)**
*   **Web Content Accessibility Guidelines (WCAG) 2.2**
*   **Section 508 of the Rehabilitation Act**
*   **Americans with Disabilities Act (ADA) Title III**

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Compliance Architect | Initial Release |