### Remote Board Meeting Technology Standards

| Document Control | |
| :--- | :--- |
| **Document ID** | GOV-STD-017 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Secretary of the Board |
| **Classification** | Internal |

### 1. Purpose
The purpose of this Standard is to define the mandatory technical requirements and configurations for conducting remote meetings of the Board of Directors and its Committees for Study GRC Inc. This document ensures compliance with **Texas Business Organizations Code (TBOC) § 22.002**, which requires that remote communication systems allow all participants to communicate substantially concurrently. Furthermore, this Standard mitigates cybersecurity risks (e.g., unauthorized access, data interception) and ensures the integrity of the governance process.

### 2. Scope
This Standard applies to:
*   **Meetings:** All Regular, Special, and Emergency meetings of the Board of Directors, Board Committees, and the Annual Meeting of Members.
*   **Personnel:** All Directors, Officers, Staff, and invited guests participating in official governance meetings.
*   **Devices:** Any hardware (laptop, mobile, tablet) used to access the meeting platform.

**Exclusions:** This Standard does not strictly apply to informal working sessions or ad-hoc staff collaborations where binding votes are not taken, though adherence to security best practices is encouraged.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **RCCS** | **Remote Communication Conference System.** The software platform (e.g., Zoom, Microsoft Teams) used to facilitate the meeting. |
| **Meeting Host** | The individual (usually the Secretary or IT designate) with administrative privileges to control the RCCS settings (mute, remove participants, screen share). |
| **Waiting Room** | A virtual staging area that prevents participants from joining the active meeting until admitted by the Meeting Host. |
| **Substantially Concurrent** | The legal requirement that audio and/or video transmission allows all participants to hear and be heard in real-time without significant delay. |
| **Executive Session** | A portion of the meeting closed to non-Directors to discuss sensitive legal, personnel, or security matters. |

### 4. Standards

#### 4.1 Approved Platforms
To ensure security and reliability, all official Board meetings must be conducted using an enterprise-grade RCCS that meets the following criteria:
*   **Encryption:** Must support TLS 1.2 or higher for data in transit and AES-256 for data at rest (recordings).
*   **Audit Logs:** Must provide logs of participant entry/exit times.
*   **Access Control:** Must support unique meeting IDs, passwords, and waiting rooms.

**Approved Platforms List:**
1.  Zoom (Pro/Business/Enterprise)
2.  Microsoft Teams
3.  Google Meet (Enterprise/Workspace editions only)

*Use of consumer-grade free versions (which may have time limits or reduced security features) is prohibited for Board meetings.*

#### 4.2 Mandatory Configuration Settings
The Meeting Host must configure the RCCS with the following settings prior to the start of any meeting:

**4.2.1 Access Control**
*   **Waiting Room:** Must be enabled. The Host must manually verify and admit each attendee.
*   **Passcodes:** All meetings must be protected by a complex alphanumeric passcode or tokenized link.
*   **Join Before Host:** Must be **disabled**.

**4.2.2 Participant Management**
*   **Screen Sharing:** Default setting must be "Host Only." The Host may grant permission to specific presenters temporarily.
*   **Annotation:** Shared screen annotation by participants must be **disabled** to prevent disruption.
*   **Chat:** File transfer via chat should be **disabled** to prevent malware distribution. Links to secure repositories (e.g., SharePoint/Google Drive) are permitted.

#### 4.3 Identity Verification and Quorum
Pursuant to **Bylaws Article III, Section 3.5**, a quorum must be established.
*   **Video Requirement:** Directors are required to have their video camera enabled during roll call and voting to verify identity and ensure no unauthorized persons are present in their physical vicinity (coercion check).
*   **Display Names:** Participants must use their real legal names or recognized professional names. "iPhone 3" or generic aliases are not permitted; the Host must rename or remove unidentified users.

#### 4.4 Voting Technology
*   **Voice Vote:** For unanimous consent or simple motions, a voice vote or "physical hand raise" visible on camera is sufficient.
*   **Electronic Polling:** For contested motions or elections:
    *   The RCCS polling feature or a separate secure voting tool (e.g., ElectionBuddy) must be used.
    *   The tool must prevent multiple votes from a single user.
    *   The tool must provide a tally record for the Minutes.
*   **Proxy Prohibition:** In accordance with **Bylaws Article II, Section 2.3**, the technology must not allow for automated proxy voting. The Director must be present to cast the vote.

#### 4.5 Executive Session Protocols
When the Board moves into Executive Session:
1.  **Lock Meeting:** The Host must enable the "Lock Meeting" feature to prevent new attendees from joining.
2.  **Guest Removal:** The Host must move all non-Directors (staff, guests) to the Waiting Room or remove them from the meeting entirely.
3.  **Recording Stop:** Cloud and local recording must be strictly **stopped**.
4.  **Smart Devices:** Directors must ensure smart speakers (e.g., Alexa, Siri, Google Home) in their physical location are muted or removed.

#### 4.6 Recording and Retention
*   **Official Record:** Only the Secretary (or designate) is authorized to record the meeting.
*   **Consent:** The RCCS must be configured to provide an automated audio/visual notification to all participants that recording is active.
*   **Storage:** Recordings must be stored directly to the Organization’s secure cloud storage (governed by the *Document Retention Policy*). Local recording to personal hard drives is prohibited.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Secretary** | Acts as the primary Meeting Host; verifies quorum; manages the Waiting Room; ensures recordings are started/stopped appropriately. |
| **Chief Information Security Officer (CISO)** | Vets and approves the RCCS platform; audits configuration settings annually; investigates any security incidents (e.g., "Zoom-bombing"). |
| **Directors** | Ensure their local connection is secure (avoiding public Wi-Fi without VPN); maintain a professional environment free from unauthorized eavesdroppers. |
| **Executive Director** | Ensures the organization maintains valid licenses for the approved RCCS platforms. |

### 6. Compliance and Enforcement
Failure to adhere to these standards may result in the following:
*   **Invalidation of Meeting:** Technical failures that prevent "substantial concurrency" (e.g., mass audio failure) may render business transacted at the meeting void under Texas law.
*   **Disciplinary Action:** Staff or Officers who intentionally bypass security controls (e.g., sharing Host keys, disabling Waiting Rooms) are subject to disciplinary action up to and including termination.
*   **Removal:** Directors who repeatedly fail to maintain a secure environment may be subject to removal for cause as outlined in **Bylaws Article III, Section 3.6**.

### 7. References
*   **Study GRC Inc. Bylaws:** Article III (Board of Directors), Section 3.4 (Regular Meetings).
*   **Texas Business Organizations Code:** § 22.002 (Meetings by Remote Communications Technology).
*   **NIST SP 800-177:** Trustworthy Email and Web Conferencing.
*   **GOV-POL-012:** Document Retention and Destruction Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial Release |