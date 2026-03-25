### Course Material Update Cycle

| Document Control | |
| :--- | :--- |
| **Document ID** | OPS-PRC-020 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2025-10-25 (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | VP of Education & Training |
| **Classification** | Public |

### 1. Purpose
The Governance, Risk, and Compliance (GRC) landscape is dynamic, with frequent changes to laws, regulations, and industry frameworks (e.g., NIST, ISO, GDPR). To fulfill the Organization’s charitable purpose defined in **Bylaws Article I, Section 1.3** ("Advancing GRC knowledge"), Study GRC Inc. must ensure all educational resources are accurate, current, and reliable.

This procedure establishes a mandatory lifecycle for reviewing, updating, and deprecating course materials to mitigate the risk of disseminating obsolete or legally inaccurate information.

### 2. Scope
This procedure applies to all educational content owned, hosted, or distributed by Study GRC Inc., including but not limited to:
*   Video lectures and transcripts.
*   Slide decks and presentation materials.
*   Study guides, white papers, and PDF resources.
*   Practice quizzes, exam banks, and assessment tools.
*   Open-source repositories (e.g., GitHub code/templates).

**Exclusions:**
*   Blog posts (unless marked as "Evergreen" educational content).
*   Third-party content linked for reference purposes (though links must be checked for validity).
*   Archived content clearly labeled as "Legacy/Historical."

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Asset** | A distinct unit of educational content (e.g., "CMMC 2.0 Study Guide v1"). |
| **Volatility Rating** | A classification assigned to an Asset determining how frequently it requires review based on the stability of its subject matter. |
| **Trigger Event** | An external occurrence (e.g., passage of a new law, release of a new framework version) that necessitates an immediate, out-of-cycle review. |
| **SME** | Subject Matter Expert; a qualified individual assigned to review technical accuracy. |
| **Deprecation** | The process of formally retiring an Asset that is no longer accurate or useful, removing it from active circulation. |
| **Pull Request (PR)** | A mechanism for the community to suggest edits to open-source materials. |

### 4. Procedures

#### 4.1 Asset Classification and Review Cadence
Upon creation, the **VP of Education & Training** must assign a Volatility Rating to every educational Asset. This rating dictates the mandatory review schedule.

| Volatility Rating | Description | Review Cycle | Examples |
| :--- | :--- | :--- | :--- |
| **High** | Subject to frequent legislative or technical changes. | **Quarterly** | Cybersecurity threats, Privacy laws (state-level), AI governance. |
| **Medium** | Subject to periodic framework updates (3-5 years). | **Annually** | ISO Standards, NIST SPs, COBIT, PMBOK. |
| **Low** | Foundational theory or historical context. | **Bi-Annually** | History of GRC, Ethics theory, Soft skills. |

#### 4.2 Scheduled Review Process
The **VP of Education & Training** is responsible for initiating the review cycle based on the schedule defined in Section 4.1.

1.  **Notification:** 30 days prior to the review deadline, the Asset is flagged in the Content Management System (CMS).
2.  **SME Assignment:** A Subject Matter Expert (SME) is assigned to audit the content. This may be the original author or a new reviewer.
3.  **Audit:** The SME reviews the material against current industry standards and regulations.
4.  **Determination:** The SME selects one of three outcomes:
    *   **Pass:** Content remains accurate. No changes needed. Update "Last Reviewed Date."
    *   **Update Required:** Content contains inaccuracies. Proceed to Section 4.3.
    *   **Deprecate:** Content is fundamentally obsolete. Proceed to Section 4.5.

#### 4.3 Update and Revision Protocol
If an Asset requires modification:

1.  **Drafting:** The SME or assigned Instructional Designer drafts the revisions.
2.  **Verification:** A second SME or the VP of Education verifies the technical accuracy of the changes.
3.  **Version Control:**
    *   **Minor Changes (Typos, broken links):** Increment the patch version (e.g., v1.0 to v1.1).
    *   **Substantive Changes (Regulatory updates, new slides):** Increment the major version (e.g., v1.0 to v2.0).
4.  **Publishing:** The updated Asset is uploaded to the Learning Management System (LMS) and/or GitHub repository.
5.  **Change Log:** A summary of changes must be appended to the Asset description for transparency.

#### 4.4 Trigger-Based (Emergency) Updates
Regardless of the scheduled review cycle, a **Trigger Event** initiates an immediate review.

1.  **Identification:** Any Team Member or Community Participant may report a Trigger Event (e.g., "NIST released CSF 2.0 today") via the **Content Error Reporting Form**.
2.  **Triage:** The VP of Education assesses the impact within 48 hours.
3.  **Notice:** If an immediate update is not possible, a "Warning Banner" must be placed on the Asset stating: *"Note: This content reflects [Previous Standard]. An update is in progress following the release of [New Standard]."*
4.  **Expedited Update:** The Asset is prioritized for immediate revision following the steps in Section 4.3.

#### 4.5 Deprecation (Retirement)
When an Asset is no longer salvageable or relevant:

1.  **Approval:** The VP of Education must approve the deprecation.
2.  **Archival:** The Asset is moved to the "Legacy Archive." It is not deleted but is removed from active learning paths.
3.  **Labeling:** If the Asset remains accessible for historical reference, it must be watermarked or clearly labeled: **"ARCHIVED - FOR HISTORICAL REFERENCE ONLY."**
4.  **Redirect:** Users attempting to access the Asset should be redirected to the current equivalent resource, if applicable.

#### 4.6 Community Contributions (Open Source)
As a community-driven organization, Study GRC Inc. accepts corrections via the community.

1.  **Submission:** Community members may submit "Pull Requests" (for code/text) or "Content Feedback Tickets" (for video/LMS).
2.  **Review:** The VP of Education or delegate must review community submissions within 14 days.
3.  **Attribution:** If a community contribution is accepted and integrated, the contributor shall be credited in the Asset's release notes, subject to the **Intellectual Property Policy**.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **VP of Education & Training** | Process Owner. Assigns Volatility Ratings. Approves Deprecations. Ensures adherence to the schedule. |
| **Subject Matter Expert (SME)** | Conducts technical accuracy reviews. Drafts content updates. |
| **Instructional Designer** | Implements updates in the LMS/CMS. Manages version control numbering. |
| **Community Member** | Reports inaccuracies. Submits Pull Requests for updates. |
| **IT / Web Team** | Maintains the technical infrastructure for versioning and archiving. |

### 6. Compliance and Enforcement
**Accuracy is paramount to our mission.** Failure to adhere to this procedure may result in the dissemination of false information, leading to reputational damage and potential liability.

*   **Staff/Volunteers:** Failure to perform assigned reviews or knowingly publishing inaccurate information may result in disciplinary action, up to and including termination of role.
*   **Assets:** Assets that miss their review deadline by more than 30 days will be automatically flagged as "Outdated" or hidden from public view until a review is completed.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article I, Section 1.3 - Purposes)
*   **Intellectual Property Policy** (Ownership of updates)
*   **Record Retention Policy** (Archival of educational materials)
*   **OPS-STD-005 Instructor Qualification Standard**

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | VP of Education | Initial Release |