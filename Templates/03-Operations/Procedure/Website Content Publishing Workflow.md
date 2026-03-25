### Website Content Publishing Workflow

| Document Control | |
| :--- | :--- |
| **Document ID** | COM-PRC-008 |
| **Document Type** | Procedure |
| **Version** | v0.1 (Draft) |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Director of Communications |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized Quality Assurance (QA) and approval process for all content published to Study GRC Inc. web properties. This workflow mitigates reputational risk, ensures compliance with intellectual property and privacy laws (including COPPA), guarantees adherence to brand standards, and verifies technical accessibility (WCAG 2.2 AA) prior to public release.

### 2. Scope
This procedure applies to all employees, volunteers, Board members, and contractors ("Contributors") who create, edit, or publish content on the Organization’s official websites (e.g., studygrc.org).

**In Scope:**
*   Blog posts, articles, and educational resources.
*   Policy pages and governance documents.
*   Event landing pages.
*   Press releases and official announcements.

**Exclusions:**
*   User-generated content (UGC) posted by community members in forums or chat channels (governed by the *Community Moderation Guidelines*).
*   Social media posts (governed by the *Social Media Approval Workflow*).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **CMS** | Content Management System (e.g., WordPress, Ghost, Hugo) used to manage website content. |
| **Staging Environment** | A non-public mirror of the website used for testing and review before content goes live. |
| **Production** | The live, public-facing website. |
| **SME** | Subject Matter Expert; the individual responsible for verifying the factual accuracy of the content. |
| **Alt Text** | Alternative text descriptions for images, required for accessibility compliance. |
| **PII** | Personally Identifiable Information. |

### 4. Procedures

#### 4.1 Content Classification and Approval Tiers
Contributors must determine the classification of the content to identify the required approval level.

| Classification | Examples | Required Approvers |
| :--- | :--- | :--- |
| **Tier 1: Routine** | Minor typo fixes, date updates, routine blog posts. | 1. Peer Reviewer<br>2. Webmaster |
| **Tier 2: Educational** | New curriculum, technical guides, whitepapers. | 1. SME (Technical Accuracy)<br>2. VP of Education<br>3. Webmaster |
| **Tier 3: High Impact** | Press releases, Policy changes, Fundraising campaigns, Crisis comms. | 1. Legal/Compliance<br>2. Executive Director<br>3. Webmaster |

#### 4.2 Phase 1: Drafting and Asset Preparation
1.  **Drafting:** The Author creates the content in a shared document format (e.g., Google Doc, Markdown file) rather than directly in the CMS Production environment.
2.  **IP Verification:** Pursuant to **Bylaws Article IX (Intellectual Property)**, the Author must ensure:
    *   All text is original or properly cited.
    *   All images are either Organization-owned, Creative Commons (with attribution), or licensed stock.
    *   No proprietary third-party data is disclosed without a Data Sharing Agreement.
3.  **Privacy Scrub:** The Author must verify that no PII is included unless explicitly authorized.
    *   *Youth Protection:* Photos of minors must have a signed *Parental Consent and Liability Waiver* on file. Names of minors must never be published alongside their photos.

#### 4.3 Phase 2: Content Review (Editorial & Legal)
1.  **Submission:** The Author submits the draft via the Organization’s ticketing system (e.g., Jira/Trello) or designated communication channel.
2.  **SME Review:** The designated SME reviews for factual accuracy, tone, and alignment with the Organization’s mission.
3.  **Copy Editing:** The Editor checks for grammar, spelling, and adherence to the *Brand Identity and Style Guide*.

#### 4.4 Phase 3: Technical Staging and Accessibility QA
1.  **Staging Upload:** The Webmaster or authorized Contributor uploads the approved draft to the **Staging Environment**.
2.  **Accessibility Check (Mandatory):** The Webmaster must verify compliance with the *Digital Accessibility Policy* (WCAG 2.2 AA):
    *   All images have descriptive **Alt Text**.
    *   Heading structures (H1, H2, H3) are hierarchical and logical.
    *   Link text is descriptive (no "click here").
    *   Color contrast ratios meet the 4.5:1 standard.
3.  **Responsive Testing:** Content is previewed on Desktop, Tablet, and Mobile viewports to ensure layout integrity.
4.  **Link Validation:** All internal and external hyperlinks are tested to ensure they do not return 404 errors.

#### 4.5 Phase 4: Final Approval and Deployment
1.  **Final Sign-Off:** The Approving Authority (based on Tier in 4.1) reviews the Staging link. Approval must be documented (email, ticket comment, or digital signature).
2.  **Deployment:** Upon receiving documented approval, the Webmaster pushes the content from Staging to **Production**.
3.  **Cache Clearing:** The Webmaster clears the CMS and CDN (Content Delivery Network) caches to ensure immediate visibility.

#### 4.6 Phase 5: Post-Publication Verification
1.  **Live Verification:** The Author verifies the live URL to ensure formatting rendered correctly.
2.  **Transparency Indexing:** If the content is a financial report or governance document, the Webmaster must update the "Transparency" page index in accordance with **Bylaws Article VIII (Records, Transparency & Finance)**.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Content Author** | Creates original content; ensures initial IP and privacy compliance; secures necessary waivers. |
| **Subject Matter Expert (SME)** | Validates factual accuracy and technical correctness of educational material. |
| **Webmaster** | Manages the CMS; performs Accessibility QA; executes the deployment from Staging to Production. |
| **Director of Communications** | Acts as the primary Editor; enforces brand standards; manages the content calendar. |
| **Executive Director** | Provides final authorization for Tier 3 (High Impact) content and fundamental policy changes. |

### 6. Compliance and Enforcement
Failure to comply with this procedure—specifically the publishing of unapproved content, copyright infringement, or violation of youth privacy standards—may result in disciplinary action, up to and including termination of employment or volunteer assignment. Unauthorized modification of the Production environment is considered a security incident and will be handled under the *Incident Response Plan*.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article VIII: Transparency; Article IX: Intellectual Property)
*   **COM-POL-001:** Brand Identity and Style Guide
*   **IT-POL-009:** Digital Accessibility Policy (WCAG 2.2 AA)
*   **LEG-POL-004:** Intellectual Property Policy
*   **YTH-POL-002:** Digital Interaction with Minors Policy

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v0.1 | 2023-10-27 | Chief Legal Officer | Initial Draft |