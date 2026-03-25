### Right to Object and Opt-Out Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | GOV-PRC-045 |
| **Document Type** | Procedure |
| **Version** | v0.1 (Draft) |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-04-25 (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this procedure is to operationalize the rights of individuals to object to specific processing activities or opt-out of the sale, sharing, or use of their Personal Data for targeted advertising and profiling. This document ensures Study GRC Inc. complies with the Texas Data Privacy and Security Act (TDPSA) and the California Consumer Privacy Act (CCPA), while reinforcing our organizational commitment to transparency and user agency as outlined in **Article I, Section 1.3** of the Bylaws.

### 2. Scope
This procedure applies to all Personal Data collected, processed, or stored by Study GRC Inc. regarding:
*   **Data Subjects:** Community Participants, Supporting Members, Honorary Members, donors, website visitors, and event attendees.
*   **Processing Activities:** Targeted advertising, cross-context behavioral advertising, the sale of data (if applicable), and automated profiling that produces legal or similarly significant effects.

**Exclusions:**
*   Transactional communications required for membership administration (e.g., voting notices pursuant to **Bylaws Article II, Section 2.5**).
*   Data processing required by law (e.g., tax reporting for donors).

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Opt-Out** | The affirmative act by a Data Subject to direct the Organization not to sell their data or use it for targeted advertising. |
| **Sale of Data** | The exchange of Personal Data for monetary or other valuable consideration. (Note: While Study GRC is a non-profit, "valuable consideration" under CCPA is broad). |
| **Targeted Advertising** | Displaying advertisements to a consumer where the advertisement is selected based on personal data obtained from that consumer’s activities over time and across nonaffiliated websites or online applications. |
| **Profiling** | Any form of automated processing of personal data to evaluate, analyze, or predict personal aspects concerning an identified or identifiable natural person's economic situation, health, personal preferences, interests, reliability, behavior, location, or movements. |
| **Global Privacy Control (GPC)** | A browser setting that notifies websites of a user's privacy preference (e.g., "Do Not Sell or Share My Personal Information"). |
| **Authorized Agent** | A natural person or a business entity registered with the Secretary of State that a consumer has authorized to act on their behalf to submit an opt-out request. |

### 4. Procedures

#### 4.1. Intake Channels for Opt-Out Requests
Study GRC Inc. provides two primary mechanisms for Data Subjects to exercise their right to opt-out/object:

1.  **Automated Signal Detection (GPC):** The Organization’s website must automatically detect and respect the Global Privacy Control (GPC) signal. If detected, tracking cookies and pixels related to advertising must be disabled immediately for that session.
2.  **Manual Request Submission:**
    *   **Web Form:** A dedicated "Do Not Sell or Share My Personal Information" link in the website footer.
    *   **Email:** Direct requests sent to `privacy@studygrc.org`.

#### 4.2. Verification of Requests
Unlike deletion or access requests, **requests to opt-out of sale/sharing or targeted advertising do not require strict identity verification**.
*   **Standard:** If the information provided in the request allows the Organization to identify the browser, device, or record in our systems, the request must be honored.
*   **Authorized Agents:** If a request is submitted by an agent, the CISO or designee may request proof of signed authorization from the consumer, unless the agent is using a recognized automated signal (GPC).

#### 4.3. Processing the Opt-Out (Workflow)
Upon receipt of a valid opt-out request, the following steps must be taken within **15 business days**:

**Step 1: Marketing & AdTech Suppression (Immediate)**
*   **Action:** The CISO or Marketing Lead must ensure the user's email/ID is added to the "Suppression List" in all marketing platforms (e.g., HubSpot, Mailchimp, Google Ads).
*   **Technical Control:** Update the Consent Management Platform (CMP) to ensure tracking pixels do not fire for that user.

**Step 2: Data Sharing Cessation**
*   **Action:** If Study GRC shares donor lists or member lists with partners (e.g., for joint events), the opting-out user's record must be flagged as `Restricted - Do Not Share`.
*   **Verification:** Check the "Transparency" page disclosures to ensure no active data flows violate this opt-out.

**Step 3: Profiling Adjustment**
*   **Action:** If the Organization uses automated tools to score member engagement for "Honorary Member" eligibility (**Bylaws Article II, Section 2.1**), and the user objects to this profiling, the user must be removed from automated scoring and switched to manual review processes.

#### 4.4. Handling Minors (Youth Protection)
Study GRC Inc. strictly adheres to the "Opt-In" standard for minors, superseding "Opt-Out" procedures.
*   **Under 16:** The Organization **shall not** sell or share the personal information of consumers we have actual knowledge are less than 16 years of age, unless the consumer (or parent/guardian for those under 13) has affirmatively authorized (opted-in) to the sale/sharing.
*   **Procedure:** If a user is identified as under 16, the `Opt-Out` flag is set to `TRUE` by default in all systems.

#### 4.5. Response and Confirmation
Once the technical changes are made, the Director of Kindness and Generosity (DKG) or designee must send a confirmation to the Data Subject:
1.  Confirm that the opt-out has been processed.
2.  Clarify that they may still receive non-promotional, transactional communications (e.g., membership renewal invoices, governance voting ballots).
3.  Provide a link to the Privacy Policy for further information.

#### 4.6. Conflict with Membership Duties
If an objection to processing fundamentally prevents the Organization from fulfilling its contractual obligations to a **Supporting Member** (e.g., a member objects to their data being stored in the secure voting system required by **Bylaws Article II, Section 2.3**):
1.  The DKG must notify the member that this objection constitutes a voluntary termination of voting rights, as the Organization cannot facilitate secure voting without processing the member's identity.
2.  The member must be given the option to withdraw the objection or convert their membership to "Community Participant" (Non-Voting).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owner of the technical implementation of the Consent Management Platform (CMP) and GPC signal detection. Responsible for data flow mapping. |
| **Director of Kindness & Generosity (DKG)** | Responsible for intake of manual requests, communicating with Data Subjects, and ensuring the "human element" of the response is empathetic and clear. |
| **Marketing Lead** | Responsible for executing suppression lists within advertising and email marketing platforms. |
| **Executive Director** | Final escalation point for disputes regarding "legitimate interest" processing vs. user objections. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in regulatory fines under the TDPSA (up to $7,500 per violation) or CCPA ($2,500 to $7,500 per violation).

**Internal Enforcement:**
Employees or volunteers found to be intentionally bypassing opt-out flags (e.g., manually re-adding an opted-out user to a marketing list) will be subject to disciplinary action, up to and including termination of employment or volunteer assignment, per the **Code of Ethics and Conduct**.

### 7. References
*   **Texas Data Privacy and Security Act (TDPSA)** - Sec. 541.051 (Consumer Rights)
*   **California Consumer Privacy Act (CCPA)** - Cal. Civ. Code § 1798.120 (Right to Opt-Out)
*   **Study GRC Bylaws** - Article I (Purpose) & Article II (Membership)
*   **GOV-POL-040:** Master Data Privacy Policy
*   **IS-STD-015:** Cookie Consent Technical Implementation

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v0.1 | 2023-10-25 | Chief Compliance Architect | Initial Draft aligned with TDPSA/CCPA requirements. |