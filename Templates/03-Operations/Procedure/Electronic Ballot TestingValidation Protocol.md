### Electronic Ballot Testing/Validation Protocol

| Document Control | |
| :--- | :--- |
| **Document ID** | MEM-PRC-019 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2025-10-25 (Bi-Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Secretary |
| **Classification** | Internal |

### 1. Purpose
The purpose of this protocol is to establish a rigorous, auditable process for configuring, testing, and validating the electronic voting systems used by Study GRC Inc. This procedure ensures the integrity of elections, compliance with **Bylaws Article II, Section 2.3** (Prohibition of Proxy Voting), and adherence to the Texas Business Organizations Code (TBOC) requirements for member voting rights. It serves as the primary control mechanism to prevent election fraud, system error, or data corruption during binding organizational votes.

### 2. Scope
This procedure applies to all binding votes conducted by the Organization, including but not limited to:
*   Annual Election of Directors.
*   Removal of Directors or Officers.
*   Amendments to Bylaws or Certificate of Formation.
*   Fundamental Actions (Mergers, Dissolution, Sale of Assets).

**Exclusions:** This procedure does not apply to non-binding straw polls, community sentiment surveys, or committee-level operational decisions not requiring full membership ratification.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Election Administrator** | The individual (usually the Secretary or a designated third-party) responsible for configuring the voting platform. |
| **Voter Roll** | The certified list of Supporting and Honorary Members in good standing as defined in Bylaws Article II, Section 2.6. |
| **Test Ballot** | A dummy vote cast during the Quality Assurance (QA) phase to verify system logic. |
| **Token/Key** | A unique, cryptographically generated identifier assigned to a specific voter to ensure they can only vote once. |
| **Scrutineer** | An independent observer (internal or external) designated to verify the integrity of the election process. |

### 4. Procedures

#### 4.1 Phase 1: Voter Roll Certification & Data Integrity
*Prior to configuring the electronic system, the voter list must be sanitized and certified.*

1.  **Record Date Determination:** The Board must establish a Record Date in accordance with **Bylaws Article II, Section 2.6**. Only members in good standing as of this date are eligible.
2.  **Data Extraction:** The Secretary shall extract the list of eligible Voting Members from the Membership Registry.
3.  **Data Verification:**
    *   Verify that no "Community Participants" (non-voting) are included.
    *   Verify that email addresses are valid and unique.
    *   **Duplicate Check:** Ensure no individual holds multiple voting accounts. If a member has multiple email aliases, they must be consolidated to a single voting token.
4.  **Certification:** The Secretary and Treasurer must sign off on the Voter Roll as accurate and complete.

#### 4.2 Phase 2: Ballot Configuration & Logic Setup
1.  **Candidate/Issue Input:** The Election Administrator inputs all candidates, bios, and issue text exactly as approved by the Board.
2.  **Parameter Configuration:**
    *   **Voting Window:** Set to open immediately following the Annual Meeting and close exactly seven (7) days later (168 hours), per **Bylaws Article II, Section 2.5**.
    *   **Selection Limits:** Configure constraints (e.g., "Select up to 3 candidates").
    *   **Abstentions:** Ensure an "Abstain" option is available if required by Robert's Rules of Order.
    *   **Anonymity:** Configure the system to anonymize ballots (secret ballot) while retaining a list of *who* voted (audit trail).

#### 4.3 Phase 3: Pre-Election Testing (The "Dry Run")
*This phase must be completed at least 48 hours before the election opens.*

1.  **Test Group Creation:** Create a "Test Election" instance separate from the "Live Election" instance.
2.  **Scenario Testing:** The Election Administrator and at least one other Director must perform the following tests:
    *   **Standard Vote:** Cast a valid vote within limits. Verify it is recorded.
    *   **Over-Voting:** Attempt to select more candidates than allowed. Verify the system blocks this action.
    *   **Under-Voting:** Cast a vote with fewer selections than positions. Verify the system accepts this (unless mandatory full-slate voting is specified).
    *   **Double Voting:** Attempt to use the same unique link/token to vote a second time. **System must reject the second attempt.**
    *   **Proxy Simulation:** Forward a used voting link to a different device/IP address to ensure the token cannot be reused by another party.
3.  **Mobile Responsiveness:** Verify the ballot renders correctly on mobile devices.
4.  **Purge:** Once testing is confirmed successful, the Test Election instance is archived, and the Live Election instance is set to "Ready." **Under no circumstances shall test data be mixed with live data.**

#### 4.4 Phase 4: Live Monitoring
1.  **Bounce Management:** During the first 24 hours of the election, the Election Administrator must monitor for email delivery failures (bounces).
2.  **Remediation:** If a ballot bounces, the Administrator must attempt to contact the member via alternative means (e.g., community platform DM) to update the email address and re-issue the ballot.
3.  **Uptime Monitoring:** The CISO or IT designee must monitor the availability of the third-party voting platform.

#### 4.5 Phase 5: Post-Election Validation & Audit
*Before results are announced, the following validation steps must occur.*

1.  **Quorum Verification:**
    *   Calculate the total number of votes cast.
    *   Compare against the total Voter Roll.
    *   Confirm if the participation meets the "Majority (>50%)" requirement defined in **Bylaws Article II, Section 2.4**.
2.  **Anomaly Detection:**
    *   Review the audit log for suspicious patterns (e.g., 50 votes cast from the same IP address in 10 minutes).
    *   *Note:* While families may share an IP, high-volume clustering warrants investigation.
3.  **Reconciliation:** Ensure the number of "Voted" statuses in the system matches the number of ballots in the final report.
4.  **Archive:** Download the **Certificate of Validity** or Audit Trail provided by the electronic voting vendor. This document must include timestamps, IP hashes (if available), and token verification proofs.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Secretary** | Owner of the Voter Roll; certifies the list of eligible voters; signs off on final election results. |
| **Election Administrator** | Configures the platform, conducts the "Dry Run" testing, and manages technical support during the election window. |
| **CISO** | Vets the security of the third-party voting vendor (e.g., encryption standards, SOC 2 compliance) prior to contract renewal. |
| **Scrutineer** | (If appointed) Independently reviews the testing logs and final audit trail to confirm fairness. |
| **Board of Directors** | Reviews and accepts the final certified results. |

### 6. Compliance and Enforcement
*   **Invalidation:** Failure to perform the "Dry Run" testing (Phase 3) or failure to certify the Voter Roll (Phase 1) may result in the election results being challenged or declared void by the Membership.
*   **Disciplinary Action:** Any attempt by an Officer or Director to manipulate the testing process, alter the Voter Roll to exclude eligible members, or tamper with the electronic audit trail constitutes "Cause" for removal under **Bylaws Article III, Section 3.6**.
*   **Audit Requirement:** All testing logs and the final Election Audit Trail must be retained for a minimum of five (5) years in accordance with the **Document Retention and Destruction Policy**.

### 7. References
*   **Bylaws of Study GRC Inc.** (Specifically Article II and Article III)
*   **Texas Business Organizations Code (TBOC)** § 22.160 (Voting of Members)
*   **MEM-POL-001:** Membership Policy Manual
*   **GOV-POL-012:** Document Retention and Destruction Policy
*   **IS-STD-017:** Electronic Voting System Security Standards

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Legal/Compliance | Initial release of protocol. |