### Accessible PDF Creation Checklist

| Document Control | |
| :--- | :--- |
| **Document ID** | ACC-CHK-001 |
| **Document Type** | Checklist / Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training |
| **Classification** | Public |

### 1. Purpose
The purpose of this checklist is to ensure that all Portable Document Format (PDF) files produced, published, or distributed by Study GRC Inc. meet the **PDF/UA (ISO 14289-1)** standard and **WCAG 2.2 Level AA** success criteria. This ensures our educational resources, financial transparency reports, and governance documents are accessible to individuals with disabilities, including those using assistive technologies (e.g., screen readers, braille displays).

This document supports the Organization’s mission to "remove financial and access barriers" as defined in **Article I, Section 1.3** of the Bylaws.

### 2. Scope
This checklist applies to:
*   **All Personnel:** Employees, Board Directors, Volunteers, and Contractors.
*   **All Content:** Educational materials, white papers, annual financial reports (per Bylaws Article VIII), governance documents, and marketing collateral.
*   **Exclusions:** Legacy documents published prior to [Date] are subject to remediation upon request but are not required to pass this checklist retroactively unless updated.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **PDF/UA** | "Universal Accessibility" (ISO 14289). The technical standard for accessible PDF documents. |
| **Tags** | The invisible structure within a PDF that defines the logical reading order and meaning of content (e.g., defining text as a "Heading" vs. a "Paragraph"). |
| **Alt Text** | Alternative text descriptions applied to images for users who cannot see them. |
| **Artifact** | A decorative element (line, background image) that conveys no meaning and should be hidden from screen readers. |
| **PAC 2024** | The "PDF Accessibility Checker," a free tool used to validate PDF/UA compliance. |

### 4. Checklist Requirements

Content Creators must verify every item below before finalizing a PDF for publication.

#### 4.1 Document Properties & Metadata
*   [ ] **Document Title Set:** The document has a descriptive Title set in `File > Properties > Description`. (Note: The Title is different from the Filename).
*   [ ] **Title Display:** The PDF is configured to display the "Document Title" rather than the "File Name" in the window title bar (`File > Properties > Initial View > Window Options > Show: Document Title`).
*   [ ] **Primary Language:** The document language (e.g., English) is explicitly defined in the Advanced Properties.
*   [ ] **Security Settings:** Security settings (encryption/passwords) do not block assistive technology from accessing the content.

#### 4.2 Content Structure (Tagging)
*   [ ] **Document is Tagged:** The "Tags" panel confirms the document structure exists.
*   [ ] **Logical Reading Order:** The reading order in the "Order" or "Tags" panel matches the visual logic of the document. (e.g., Columns are read top-to-bottom, left-to-right, not across columns).
*   [ ] **Headings:** Text that looks like a heading is tagged as `<H1>` through `<H6>`.
    *   [ ] Hierarchy is nested correctly (e.g., `<H1>` is followed by `<H2>`, not `<H4>`).
    *   [ ] There is only one `<H1>` per document (usually the main title).
*   [ ] **Lists:** Lists are tagged properly using `<L>`, `<LI>`, `<LBody>`, and `<Lbl>` structures. They are not just paragraphs with bullet characters.
*   [ ] **Links:** All hyperlinks are active, tagged as `<Link>`, and possess an `OBJR` (Object Reference).
    *   [ ] Link text is descriptive (Avoid "Click Here"; use "Download the 2024 Annual Report").

#### 4.3 Images and Non-Text Elements
*   [ ] **Alternative Text:** All informative images, charts, and graphs have concise, accurate Alt Text.
*   [ ] **Decorative Images:** Elements that add no information (borders, stock photos used for mood only) are marked as **Artifacts** (background) so screen readers ignore them.
*   [ ] **Complex Images:** Complex charts or diagrams have a brief Alt Text description *and* a reference to a long-form description in the main text or an appendix.

#### 4.4 Tables
*   [ ] **Header Rows:** Data tables have designated Header Rows (`<TH>`) and Data Cells (`<TD>`).
*   [ ] **Scope:** Headers have the correct scope assigned (Row vs. Column).
*   [ ] **Regularity:** Tables are regular (no merged cells unless absolutely necessary and properly tagged with `RowSpan` or `ColSpan`).
*   [ ] **Layout Tables:** Tables used strictly for visual layout (not data) are tagged as generic content or artifacts, not as `<Table>`.

#### 4.5 Visual Design & Color
*   [ ] **Color Contrast:** Text and functional graphics meet **WCAG AA** contrast ratio (4.5:1 for normal text; 3:1 for large text).
*   [ ] **Color Independence:** Color is not the *only* means of conveying information (e.g., "Required fields are in red" is accompanied by an asterisk or text label).
*   [ ] **Font Embedding:** All fonts are embedded to ensure characters render correctly for all users.

#### 4.6 Validation
*   [ ] **Adobe Acrobat Check:** Run the "Accessibility Check" in Adobe Acrobat Pro. Result: **Passed**.
*   [ ] **PAC Tool Check:** Run the PDF through the **PDF Accessibility Checker (PAC)**. Result: **No PDF/UA errors**.
*   [ ] **Manual Spot Check:** Tab through the document to ensure focus moves in a logical order.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Content Creator** | Responsible for applying this checklist during the document creation and export process. Must fix all errors flagged by validation tools. |
| **VP of Education & Training** | Final approver for educational resources. Ensures staff/volunteers have access to Adobe Acrobat Pro or equivalent accessibility tools. |
| **Web/IT Team** | Responsible for rejecting any PDF submitted for website publication that fails the PAC validation check. |

### 6. Compliance and Enforcement
**Rejection of Work:** Documents submitted for publication that do not meet the criteria in Section 4 will be returned to the author for remediation.

**Disciplinary Action:** Repeated failure to adhere to accessibility standards, particularly regarding public-facing compliance documents required by Bylaws Article VIII (Transparency), may result in disciplinary action up to and including termination of employment or volunteer assignment.

### 7. References
*   **ISO 14289-1:** Document management applications — Electronic document file format enhancement for accessibility (PDF/UA-1).
*   **W3C WCAG 2.2:** Web Content Accessibility Guidelines.
*   **ACC-POL-001:** Digital Accessibility Policy.
*   **Study GRC Bylaws:** Article I (Purpose) and Article VIII (Transparency).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Compliance Architect | Initial release aligned with PDF/UA standards. |