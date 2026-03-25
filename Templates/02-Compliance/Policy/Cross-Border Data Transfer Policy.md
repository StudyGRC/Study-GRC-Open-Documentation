### Cross-Border Data Transfer Policy

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-POL-029 |
| **Document Type** | Policy |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this policy is to establish a compliant framework for the transfer of Personal Data across international borders. Specifically, this policy addresses the requirements established by the General Data Protection Regulation (GDPR) and the Court of Justice of the European Union (CJEU) ruling in *Data Protection Commissioner v. Facebook Ireland and Maximillian Schrems* ("Schrems II").

As a Texas-based non-profit with a global community, Study GRC Inc. acts as a Data Importer. This policy ensures that the protection of natural persons guaranteed by international law is not undermined when data is transferred to the United States or other third countries.

### 2. Scope
This policy applies to all Study GRC Inc. personnel, volunteers, contractors, and third-party vendors.

**In Scope:**
*   All Personal Data originating from the European Economic Area (EEA), United Kingdom (UK), or Switzerland.
*   Transfers of data from any jurisdiction with data localization laws to Study GRC Inc. systems (hosted primarily in the United States).
*   Onward transfers to sub-processors (e.g., cloud service providers).

**Exclusions:**
*   Data that has been fully anonymized such that re-identification is impossible.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Cross-Border Transfer** | Any transmission of Personal Data to a recipient (controller or processor) located in a country different from the country where the data originated. |
| **Data Exporter** | The entity located in the EEA/UK that transfers the personal data (e.g., a European member or partner). |
| **Data Importer** | The entity receiving the personal data (Study GRC Inc. in the US). |
| **Adequacy Decision** | A formal decision by the European Commission that a third country provides an equivalent level of data protection. |
| **SCCs** | **Standard Contractual Clauses**. Legal templates approved by the European Commission to ensure data protection in transfers to third countries. |
| **Schrems II** | A 2020 CJEU ruling that invalidated the EU-US Privacy Shield and mandated that organizations verify the effectiveness of SCCs in light of destination country laws (specifically regarding government surveillance). |
| **TIA** | **Transfer Impact Assessment**. A documented risk assessment determining if the laws of the destination country impinge on the effectiveness of the transfer mechanism. |
| **Supplementary Measures** | Technical, contractual, or organizational measures applied to data to protect it from access by public authorities in the destination country. |

### 4. Policy Statements

#### 4.1 General Principles of Transfer
Study GRC Inc. shall not transfer Personal Data to a Third Country unless:
1.  The country has received an **Adequacy Decision**; OR
2.  Appropriate **Safeguards** (such as SCCs) are in place, accompanied by a valid TIA; OR
3.  A specific **Derogation** applies (e.g., explicit consent).

#### 4.2 Standard Contractual Clauses (SCCs)
In the absence of an Adequacy Decision (such as for transfers to the United States), Study GRC Inc. adopts the latest version of the European Commission’s Standard Contractual Clauses (SCCs) for all relevant vendor agreements and intra-group data flows.
*   **Module Selection:** We shall utilize the appropriate SCC Module (Controller-to-Controller, Controller-to-Processor, etc.) based on the specific nature of the relationship.
*   **No Modification:** The core text of the SCCs must not be modified, except to select modules or add commercial clauses that do not contradict the SCCs.

#### 4.3 Transfer Impact Assessments (TIA)
Pursuant to the *Schrems II* ruling, simply signing SCCs is insufficient. Before initiating a new data flow from the EEA/UK to a non-adequate jurisdiction (including the US), the Data Protection Officer (or designated privacy lead) must conduct a **Transfer Impact Assessment (TIA)**.

The TIA must evaluate:
1.  **Specific Circumstances:** Types of data, purpose, and duration of transfer.
2.  **Destination Laws:** Whether laws in the destination country (e.g., US FISA Section 702 or EO 12333) authorize public authorities to access the data in a manner disproportionate to democratic norms.
3.  **Safeguards:** Whether Supplementary Measures are sufficient to close the gap in protection.

#### 4.4 Supplementary Measures (Schrems II Compliance)
If a TIA identifies that the destination country's laws may impinge on the data protection guarantees (e.g., US surveillance laws), Study GRC Inc. mandates the implementation of **Supplementary Measures**:

*   **Technical Measures (Primary):**
    *   **Encryption in Transit:** All cross-border data must be encrypted using TLS 1.2 or higher.
    *   **Encryption at Rest:** Data stored in US cloud environments must be encrypted.
    *   **Key Management:** Where technically feasible, encryption keys should be managed in a way that prevents the cloud provider from accessing the data (Bring Your Own Key - BYOK), or data should be pseudonymized prior to transfer.
*   **Contractual Measures:**
    *   Agreements must include "Warrant Canary" clauses or obligations for the vendor to challenge government access requests to the fullest extent of the law.
*   **Organizational Measures:**
    *   Strict data minimization and internal access controls.

#### 4.5 Government Access Requests
If Study GRC Inc. receives a request from a public authority (e.g., law enforcement, intelligence agencies) for access to Personal Data originating from the EEA/UK:
1.  **Verify Legality:** Legal Counsel must review the request to determine if it is legally binding.
2.  **Challenge:** If there are legal grounds to do so, Study GRC Inc. shall challenge the request.
3.  **Notify:** Unless prohibited by law (e.g., a gag order), Study GRC Inc. shall notify the Data Exporter (the member or partner) immediately.
4.  **Minimize:** If disclosure is compelled, only the minimum amount of data necessary shall be disclosed.

#### 4.6 Derogations (Exceptions)
In limited circumstances where SCCs and Supplementary Measures are not feasible, transfers may occur based on Article 49 Derogations. These are not to be used for repetitive, bulk transfers.
*   **Explicit Consent:** The data subject has been informed of the possible risks of such transfers due to the absence of an adequacy decision and appropriate safeguards and has explicitly consented.
*   **Contract Performance:** The transfer is necessary for the performance of a contract between the data subject and the controller (e.g., processing a membership payment).

#### 4.7 Onward Transfers (Sub-processors)
Study GRC Inc. shall not transfer EEA/UK data to a third-party vendor (Sub-processor) unless that vendor:
1.  Signs a Data Processing Agreement (DPA) incorporating SCCs.
2.  Passes a Vendor Security Risk Assessment (VSRA) confirming their ability to implement required Supplementary Measures.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Board of Directors** | Ensures the organization allocates resources to maintain legal compliance with international data laws. |
| **Chief Legal Officer / DPO** | Conducts Transfer Impact Assessments (TIAs); reviews and signs SCCs; handles government access requests. |
| **CISO** | Implements Technical Supplementary Measures (Encryption, Access Control) required to satisfy *Schrems II* requirements. |
| **Operational Officers** | Consults with Legal/Privacy team before onboarding new vendors or tools that process international member data. |
| **Vendors/Contractors** | Must adhere to the DPA and SCCs; must notify Study GRC Inc. of any inability to comply with these clauses. |

### 6. Compliance and Enforcement
Failure to comply with this policy puts Study GRC Inc. at risk of significant regulatory fines (up to 4% of global turnover under GDPR) and reputational damage.

**Internal Enforcement:** Employees found to have willfully bypassed cross-border transfer controls (e.g., using unauthorized "Shadow IT" to store member data) may be subject to disciplinary action, up to and including termination.

**Vendor Enforcement:** Vendors failing to maintain the agreed-upon Supplementary Measures will be subject to contract termination and claims for damages.

### 7. References
*   **GDPR Articles 44-50** (Transfers of personal data to third countries).
*   **CJEU Case C-311/18 (Schrems II)**.
*   **EDPB Recommendations 01/2020** on measures that supplement transfer tools.
*   **Study GRC Bylaws Article IX** (Policies & Data Protection).
*   **IS-POL-001** Master Information Security Policy.
*   **IS-PRC-022** Vendor Security Risk Assessment (VSRA).

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial release aligned with *Schrems II* requirements. |