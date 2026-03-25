### Standard Contractual Clauses (SCCs) Implementation Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | DP-PRC-030 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Data Protection Officer (DPO) / General Counsel |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a mandatory framework for the identification, selection, execution, and management of **Standard Contractual Clauses (SCCs)**. This procedure ensures Study GRC Inc. (the "Organization") complies with **Article 46 of the General Data Protection Regulation (GDPR)** and equivalent UK data protection laws when transferring Personal Data from the European Economic Area (EEA) or the United Kingdom to "Third Countries" (including the United States) that have not received an adequacy decision.

This procedure mitigates legal risk, financial liability, and reputational damage associated with unauthorized cross-border data transfers.

### 2. Scope
This procedure applies to all Operational Officers, Board Directors, and volunteers involved in:
1.  **Vendor Procurement:** Selecting software, cloud services, or contractors located outside the EEA/UK.
2.  **Partnerships:** Collaborating with other non-profits or entities where data is shared across borders.
3.  **Internal Operations:** Transferring data regarding EEA/UK-based members, volunteers, or donors to the Organization's systems in Texas.

**Exclusions:** Transfers to countries with a valid Adequacy Decision from the European Commission (e.g., Canada, Japan) do not require SCCs, though other safeguards may apply.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Standard Contractual Clauses (SCCs)** | Model contract clauses pre-approved by the European Commission (Implementing Decision 2021/914) to ensure appropriate data protection safeguards for cross-border transfers. |
| **Data Exporter** | The entity (Controller or Processor) located in the EEA/UK that transfers data to a Third Country. |
| **Data Importer** | The entity (Controller or Processor) located in a Third Country (e.g., Study GRC Inc. in Texas) receiving the data. |
| **Transfer Impact Assessment (TIA)** | A mandatory risk assessment to determine if the laws of the Third Country (e.g., US FISA 702) impinge on the effectiveness of the SCCs. |
| **Restricted Transfer** | A transfer of personal data from the EEA/UK to a country not covered by an Adequacy Decision. |
| **UK Addendum** | A specific document required to append to EU SCCs to satisfy United Kingdom data protection laws post-Brexit. |

### 4. Procedures

#### 4.1 Identification of Restricted Transfers
Before onboarding any new vendor or initiating a data flow, the **Requesting Officer** must determine if a Restricted Transfer will occur.

1.  **Origin Check:** Does the data originate from an individual in the EEA or UK?
2.  **Destination Check:** Is the recipient (Vendor, Partner, or Study GRC Inc. itself) located in a country *without* an EU Adequacy Decision? (Note: The US is considered a Third Country requiring safeguards unless the entity is certified under the Data Privacy Framework, which requires verification).
3.  **Trigger:** If Yes to both, SCCs are **mandatory** before data flows.

#### 4.2 Transfer Impact Assessment (TIA)
Pursuant to the *Schrems II* ruling, SCCs cannot be signed blindly.
1.  The **Data Protection Officer (DPO)** must conduct a TIA using the *Transfer Impact Assessment Template (DP-FRM-031)*.
2.  The TIA must evaluate whether local laws (e.g., US surveillance laws) prevent the Data Importer from fulfilling the SCC obligations.
3.  If the TIA reveals high risk, **Supplementary Measures** (e.g., encryption where the importer does not hold the key) must be implemented.

#### 4.3 Selection of SCC Modules
The DPO or Legal Counsel must select the correct "Module" of the 2021 EU SCCs based on the relationship.

| Relationship Scenario | Correct Module | Example |
| :--- | :--- | :--- |
| **Module 1 (C2C)** | Controller to Controller | Study GRC (US) receives donor list from a European partner non-profit for joint research. |
| **Module 2 (C2P)** | Controller to Processor | Study GRC (EU Branch/Member) sends data to a US-based email marketing vendor. |
| **Module 3 (P2P)** | Processor to Processor | Study GRC (acting as a Processor for a client) sub-contracts to a US cloud storage provider. |
| **Module 4 (P2C)** | Processor to Controller | A US-based processor sends data back to an EU-based client/controller. |

#### 4.4 Drafting and Annex Completion
The SCCs are modular; the text of the clauses cannot be modified, but the Annexes must be populated specifically.

**4.4.1 Annex I: List of Parties**
*   Clearly identify the Exporter and Importer with contact details.
*   Specify the activities relevant to the transfer.

**4.4.2 Annex II: Technical and Organizational Measures**
*   The **Chief Information Security Officer (CISO)** must provide the content for Annex II.
*   This must detail specific security controls (e.g., "AES-256 encryption at rest," "MFA enforcement," "TLS 1.3 for transit").
*   *Note:* Generic statements like "We have good security" are legally insufficient and invalid.

**4.4.3 Annex III: List of Sub-processors**
*   If Module 2 or 3 is used, the Importer must list all sub-processors (e.g., AWS, Slack, Google Workspace) that will touch the data.

#### 4.5 UK Data Transfers (The UK Addendum)
If the data originates from the United Kingdom:
1.  The **International Data Transfer Addendum (IDTA)** or the "UK Addendum to the EU SCCs" must be executed alongside the EU SCCs.
2.  Study GRC Inc. adopts the approach of using the **EU SCCs with the UK Addendum** to maintain a single contract structure for dual-jurisdiction compliance.

#### 4.6 Execution and Signature
1.  **Authority:** Per **Bylaws Article V (Operational Leadership)** and the *Signature Authority Policy*, only the Executive Director or President may sign SCCs on behalf of the Organization.
2.  **Integration:** The SCCs must be appended to the Master Services Agreement (MSA) or Data Processing Agreement (DPA). If there is a conflict between the MSA and the SCCs, the SCCs prevail.

#### 4.7 Storage and Monitoring
1.  Executed SCCs must be stored in the **Central Legal Repository** under "Cross-Border Agreements."
2.  **Annual Review:** The DPO must review all active SCCs annually to ensure:
    *   The list of sub-processors in Annex III is current.
    *   Security measures in Annex II match current reality.
    *   The destination country's legal status has not changed (e.g., new adequacy decisions or sanctions).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Requesting Officer** | Identifies potential cross-border transfers during vendor selection or project planning. |
| **Data Protection Officer (DPO)** | Conducts the TIA, selects the correct SCC Module, and drafts the Annexes. |
| **Chief Info. Security Officer (CISO)** | Defines and validates the Technical and Organizational Measures (Annex II) to ensure they are accurate and sufficient. |
| **Executive Director** | Reviews and signs the SCCs as the authorized signatory. |
| **Legal Counsel** | Reviews the final package for legal sufficiency and compliance with GDPR Art. 46. |

### 6. Compliance and Enforcement
Failure to execute SCCs prior to transferring data from the EEA/UK is a violation of GDPR and Organization policy.
*   **Regulatory Risk:** Violations can result in fines up to **€20 million or 4% of global annual turnover**, whichever is higher.
*   **Internal Discipline:** Employees or volunteers who bypass this procedure or falsify TIA findings may be subject to disciplinary action, up to and including termination of employment or volunteer service, in accordance with the *Progressive Discipline Policy*.
*   **Indemnification:** Per **Bylaws Article VII**, indemnification for Officers may be jeopardized if actions are found to be grossly negligent or taken in bad faith (e.g., knowingly ignoring data export laws).

### 7. References
*   **Bylaws of Study GRC Inc.**
    *   Article IX (Policies & Data Protection)
    *   Article V (Operational Leadership - Authority)
*   **External Regulations**
    *   GDPR Article 46 (Transfers subject to appropriate safeguards)
    *   European Commission Decision 2021/914 (Standard Contractual Clauses)
    *   UK International Data Transfer Agreement (IDTA)
*   **Related Internal Documents**
    *   *Master Data Privacy Policy (DP-POL-001)*
    *   *Transfer Impact Assessment Template (DP-FRM-031)*
    *   *Signature Authority Policy (FIN-POL-015)*

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | Chief Legal Officer | Initial release aligned with EU 2021 SCCs and UK Addendum requirements. |