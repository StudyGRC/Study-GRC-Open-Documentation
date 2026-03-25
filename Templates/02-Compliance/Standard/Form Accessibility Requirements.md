### Form Accessibility Requirements

| Document Control | |
| :--- | :--- |
| **Document ID** | ACC-STD-014 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to define the mandatory technical and design requirements for all digital forms used by Study GRC Inc. This ensures that all users, regardless of ability or assistive technology used, can successfully identify, understand, and complete input fields. This Standard directly supports the Organization’s mission to "remove financial and access barriers" and aligns with the **Digital Accessibility Policy (ACC-POL-001)** by enforcing compliance with the Web Content Accessibility Guidelines (WCAG) 2.2 Level AA, specifically regarding Input Assistance.

### 2. Scope
This Standard applies to all digital forms created, hosted, or utilized by Study GRC Inc., including but not limited to:
*   **Web-based forms:** Membership applications, donation portals, contact forms, and newsletter sign-ups.
*   **Educational assessments:** Quizzes and exams within the Learning Management System (LMS).
*   **Administrative forms:** Volunteer applications, conflict of interest disclosures, and expense reports.
*   **Third-party integrations:** External tools (e.g., Typeform, Google Forms, Stripe) embedded in or linked from Organization properties.
*   **Document-based forms:** Interactive PDFs or electronic documents requiring user input.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Input Assistance** | A category of WCAG success criteria designed to help users avoid mistakes and correct them if they occur. |
| **Programmatic Label** | A label that is associated with a form control in the code (e.g., using the HTML `<label>` element with the `for` attribute), allowing assistive technology to identify the purpose of the control. |
| **Focus Indicator** | A visual effect (such as a border or color change) that indicates which element on the page currently has the keyboard focus. |
| **ARIA (Accessible Rich Internet Applications)** | A set of attributes that define ways to make web content and web applications (especially those developed with Ajax and JavaScript) more accessible to people with disabilities. |
| **Autocomplete** | A feature that allows the browser to predict the value of an input field based on the user's previous entries (e.g., name, email, address). |

### 4. Standards

#### 4.1 Labels and Instructions (WCAG 3.3.2)
To ensure users understand what input is expected:
*   **4.1.1 Visible Labels:** All form fields must have a permanently visible label. Placeholder text (text inside the input box that disappears when typing) **must not** be used as the sole method of labeling.
*   **4.1.2 Programmatic Association:** Visual labels must be programmatically associated with their corresponding input fields using the HTML `for` and `id` attributes or `aria-labelledby`.
*   **4.1.3 Required Field Indication:** Required fields must be clearly identified both visually (e.g., using an asterisk `*` or the word "Required") and programmatically (using the `required` attribute or `aria-required="true"`).
*   **4.1.4 Formatting Instructions:** Specific formatting requirements (e.g., dates as DD/MM/YYYY or passwords requiring special characters) must be included in the label or description text and associated via `aria-describedby`.

#### 4.2 Keyboard Navigation and Focus
To ensure operability without a mouse:
*   **4.2.1 Logical Tab Order:** Users must be able to navigate through the form fields in a logical, sequential order (typically left-to-right, top-to-bottom) using only the keyboard.
*   **4.2.2 Visible Focus:** The element currently receiving input focus must have a highly visible focus indicator with a contrast ratio of at least 3:1 against the background.
*   **4.2.3 No Keyboard Traps:** Users must be able to navigate into and out of all form controls (including calendar pickers and dropdowns) using standard keyboard keys.

#### 4.3 Error Identification and Recovery (WCAG 3.3.1, 3.3.3)
To assist users in correcting mistakes:
*   **4.3.1 Text-Based Error Messages:** Errors must be identified in text. Color alone (e.g., outlining a box in red) **must not** be used to indicate an error.
*   **4.3.2 Location of Errors:** Error messages must be programmatically associated with the field in error (using `aria-describedby`) or summarized in a focused alert container at the top of the form.
*   **4.3.3 Error Suggestions:** If an input error is automatically detected and suggestions for correction are known (e.g., "Did you mean .com?"), the suggestions must be provided to the user.

#### 4.4 Review and Confirmation (WCAG 3.3.4)
For forms that involve legal commitments, financial transactions, or modifying user data (e.g., **Membership Applications** per Bylaws Article II, or **Donations**):
*   **4.4.1 Reversibility or Review:** The system must provide a mechanism for the user to either:
    1.  Reverse the submission;
    2.  Check the data entered for input errors and have an opportunity to correct them before final submission; or
    3.  Review, confirm, and correct information before finalizing the submission.

#### 4.5 Autocomplete and Redundant Entry (WCAG 1.3.5, 3.3.7)
To reduce cognitive load and motor fatigue:
*   **4.5.1 Autocomplete Attributes:** Input fields that collect specific personal information (e.g., Name, Email, Address, Credit Card) must use the appropriate HTML `autocomplete` attribute values to allow browsers to auto-fill the data.
*   **4.5.2 Redundant Entry:** Information previously entered by the user in the same session (e.g., Billing Address same as Shipping Address) must be either auto-populated or available for selection, rather than requiring re-entry.

#### 4.6 Timing
*   **4.6.1 Time Limits:** If a form has a time limit (e.g., a security timeout on a donation page), the user must be given the option to turn off, adjust, or extend the limit by at least 10 times the default setting, unless the time limit is essential (e.g., a live auction).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Web Developers / IT** | Implement semantic HTML, ARIA attributes, and error handling logic in compliance with this Standard. Ensure third-party tools are technically compliant before integration. |
| **Content Creators** | Write clear, concise labels and instructions. Ensure error messages are helpful and polite. |
| **QA / Testers** | Validate forms using automated tools (e.g., WAVE, Axe) and manual keyboard testing. Verify screen reader compatibility. |
| **VP of Education & Training** | Ensure all LMS assessments and educational forms meet these standards to support diverse learners. |
| **Director of Kindness and Generosity (DKG)** | Ensure community outreach forms and surveys are accessible to maintain an inclusive culture. |
| **Chief Financial Officer (CFO)** | Verify that financial transaction forms (donations, dues) include the required Review/Confirmation steps (Section 4.4). |

### 6. Compliance and Enforcement
Failure to comply with this Standard may result in the rejection of code deployments, the removal of non-compliant forms from public-facing sites, or disciplinary action for repeated negligence.

**Remediation:** Any existing forms identified as non-compliant must be logged in the **Accessibility Remediation Matrix** and prioritized for correction based on user impact. Critical barriers (e.g., inability to submit a membership application or donation) must be remediated immediately.

### 7. References
*   **ACC-POL-001:** Digital Accessibility Policy
*   **Bylaws of Study GRC Inc.:** Article II (Membership), Article VIII (Records, Transparency & Finance)
*   **W3C Recommendation:** Web Content Accessibility Guidelines (WCAG) 2.2
*   **Regulation:** Americans with Disabilities Act (ADA) Title III

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Compliance Architect | Initial Draft based on WCAG 2.2 Input Assistance criteria. |