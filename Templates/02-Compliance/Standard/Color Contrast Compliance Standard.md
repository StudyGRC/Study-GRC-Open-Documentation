### Color Contrast Compliance Standard

| Document Control | |
| :--- | :--- |
| **Document ID** | ACC-STD-009 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to define the mandatory color contrast ratios for all digital properties, educational resources, and communications produced by Study GRC Inc. This ensures that text and interactive elements are legible for users with moderately low vision, color blindness, or age-related visual degradation.

This Standard directly supports the Organization’s charitable purpose defined in **Bylaws Article 1.3**, specifically the commitment to "empowering learners" by removing accessibility barriers to our open-source GRC knowledge base.

### 2. Scope
This Standard applies to all digital content and user interfaces developed, maintained, or published by Study GRC Inc.

**Applies to:**
*   Public-facing websites (studygrc.org) and subdomains.
*   Learning Management Systems (LMS) and courseware.
*   Digital documents (PDFs, slide decks, whitepapers).
*   Marketing emails and newsletters.
*   Software applications and open-source tools developed by the Organization.
*   Third-party platforms where the Organization controls the visual theme.

**Exclusions:**
*   **Incidental Text:** Text or images of text that are part of an inactive user interface component, that are pure decoration, that are not visible to anyone, or that are part of a picture that contains significant other visual content.
*   **Logotypes:** Text that is part of a logo or brand name.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Contrast Ratio** | A measure of the difference in perceived "luminance" or brightness between two colors (the foreground text and the background). The ratio ranges from 1:1 (white text on white background) to 21:1 (black text on white background). |
| **WCAG 2.2** | Web Content Accessibility Guidelines version 2.2, the technical standard developed by the World Wide Web Consortium (W3C). |
| **Normal Text** | Text that is less than 18 point (if not bold) or less than 14 point (if bold). |
| **Large Text** | Text that is at least 18 point (approx. 24px) or at least 14 point (approx. 18.66px) and bold weight. |
| **UI Component** | A part of the content that is perceived by users as a single control for a distinct function (e.g., buttons, form input borders, links). |

### 4. Standards

To ensure compliance with **WCAG 2.2 Success Criterion 1.4.3 (Contrast - Minimum)**, all Study GRC Inc. digital assets must adhere to the following quantifiable ratios.

#### 4.1 Normal Text Contrast
The visual presentation of text and images of text must have a contrast ratio of at least **4.5:1** against the adjacent background color.
*   **Requirement:** 4.5:1 minimum.
*   **Application:** Body text, navigation menus, footer text, and standard hyperlinks.

#### 4.2 Large Text Contrast
Large-scale text and images of large-scale text must have a contrast ratio of at least **3:1** against the adjacent background color.
*   **Requirement:** 3:1 minimum.
*   **Application:** Main headings (H1, H2), hero banner text, and large call-to-action buttons (provided the text size meets the definition of "Large Text").

#### 4.3 User Interface (UI) Components
While WCAG 1.4.3 focuses on text, Study GRC Inc. extends this standard to UI components to ensure usability (aligning with WCAG 1.4.11). Visual information required to identify user interface components and states must have a contrast ratio of at least **3:1** against adjacent colors.
*   **Requirement:** 3:1 minimum.
*   **Application:** Button boundaries, input field borders, focus indicators, and active state indicators.

#### 4.4 Text on Images
Text placed over background images or gradients must meet the required contrast ratio (4.5:1 or 3:1) across the **entirety** of the text string.
*   **Mandatory Control:** If the background image varies in lightness, a solid or semi-opaque background container (scrim) or a heavy drop shadow/outline must be used behind the text to guarantee the ratio is met.

#### 4.5 Disabled States
Text or UI components that are in a "disabled" or "inactive" state (e.g., a grayed-out submit button before a form is filled) are **exempt** from minimum contrast requirements under WCAG. However, where possible, designers should strive for legibility without implying interactivity.

#### 4.6 Verification Tools
Visual inspection is insufficient for compliance. All color combinations must be mathematically verified using an approved tool.
*   **Approved Tools:**
    *   WebAIM Contrast Checker
    *   Stark Plugin (Figma/Sketch)
    *   Chrome DevTools (CSS Overview/Inspect)
    *   TPGi Colour Contrast Analyser (CCA)

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **VP of Education & Training** | Ensures all curriculum materials (slides, PDFs) adhere to contrast standards before publication. |
| **UI/UX Designers** | Responsible for selecting color palettes and designing interfaces that meet or exceed the 4.5:1 and 3:1 ratios during the prototyping phase. |
| **Web Developers** | Responsible for implementing CSS/SASS variables that reflect compliant colors and ensuring dynamic states (hover/focus) maintain compliance. |
| **Content Contributors** | Responsible for checking contrast when using WYSIWYG editors or creating ad-hoc graphics for community posts. |
| **QA / Testers** | Responsible for auditing digital assets using automated tools and manual sampling prior to release. |

### 6. Compliance and Enforcement
Failure to comply with this standard may result in the rejection of code pull requests, the retraction of published marketing materials, or disciplinary action for repeated negligence.

Non-compliant assets identified during audits must be remediated within **30 days** of discovery, or immediately if the asset prevents a user from accessing critical Organization services (e.g., voting or donation portals).

### 7. References
*   **ACC-POL-001:** Digital Accessibility Policy
*   **MKT-GUD-002:** Brand Identity and Style Guide
*   **External:** [WCAG 2.2 Success Criterion 1.4.3 (Contrast - Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html)

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Compliance Architect | Initial Release aligned with WCAG 2.2 |