### Transfer Impact Assessment (TIA) Template

| Document Control | |
| :--- | :--- |
| **Document ID** | DP-FRM-005 |
| **Document Type** | Assessment / Form |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors / Data Protection Officer |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Confidential |

### 1. Purpose
The purpose of this Transfer Impact Assessment (TIA) is to evaluate the risks associated with transferring Personal Data from the European Economic Area (EEA), United Kingdom (UK), or Switzerland to a "Third Country" (a jurisdiction not deemed "adequate" by the European Commission).

This assessment is mandated by the Court of Justice of the European Union (CJEU) judgment in Case C-311/18 (*Schrems II*) and GDPR Article 46. It determines whether the laws and practices of the Third Country impinge on the effectiveness of the appropriate safeguards (e.g., Standard Contractual Clauses) relied upon for the transfer.

### 2. Scope
This assessment applies to:
*   **Data Importers:** Study GRC Inc. (when receiving data from EEA/UK partners or members).
*   **Data Exporters:** Study GRC Inc. (when sending EEA/UK data to third-party vendors located in non-adequate jurisdictions).
*   **Data Types:** All Personal Data and Special Category Data as defined by the Master Data Privacy Policy.

**Exclusions:** Transfers to countries with a valid Adequacy Decision from the European Commission are exempt from this specific assessment, provided the Adequacy Decision remains in force.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Data Exporter** | The entity located in the EEA/UK transferring the data. |
| **Data Importer** | The entity located in the Third Country receiving the data (often Study GRC Inc. or its vendors). |
| **Schrems II** | The CJEU ruling requiring exporters to verify that Third Country laws do not undermine GDPR protections, specifically regarding government surveillance. |
| **SCCs** | Standard Contractual Clauses; the legal mechanism used to legitimize the transfer. |
| **FISA 702** | Section 702 of the US Foreign Intelligence Surveillance Act, allowing US intelligence agencies to target non-US persons reasonably believed to be located outside the US. |
| **EO 12333** | US Executive Order 12333, authorizing intelligence collection by US agencies. |

### 4. Assessment Framework

#### Part A: Transfer Details
*To be completed by the Project Lead or Vendor Owner.*

| Question | Response |
| :--- | :--- |
| **1. Nature of the Transfer** | [Describe the workflow, e.g., "Storage of member data in cloud CRM"] |
| **2. Data Exporter (Entity/Country)** | [Name of Entity] / [Country] |
| **3. Data Importer (Entity/Country)** | Study GRC Inc. / United States (Texas) |
| **4. Categories of Data** | [e.g., Name, Email, IP Address, Payment Info] |
| **5. Transfer Tool Used** | [e.g., EU Standard Contractual Clauses (2021/914) - Module 1 or 2] |
| **6. Onward Transfers (Sub-processors)** | [List key sub-processors, e.g., AWS, Google Workspace, Slack] |

#### Part B: Laws and Practices of the Third Country (United States)
*To be completed by Legal Counsel or Privacy Officer. This section assesses whether US law impinges on the guarantees of the SCCs.*

**1. Applicability of FISA Section 702**
*Is the Data Importer an "Electronic Communication Service Provider" (ECSP) or a "Remote Computing Service" (RCS) as defined by 50 U.S.C. § 1881(b)(4)?*
*   [ ] **Yes:** The Importer provides cloud, email, or telecommunication services (e.g., AWS, Google, Microsoft).
*   [ ] **No:** The Importer is a non-profit educational entity that does not provide communication services to the public.
*   **Analysis:** *[Insert analysis. Example: Study GRC Inc. is a non-profit and likely not a direct target of FISA 702. However, Study GRC utilizes sub-processors (AWS/Google) that ARE subject to FISA 702. Therefore, the risk must be assessed based on the sub-processors.]*

**2. Applicability of EO 12333**
*Does the transfer involve data transit through internet cables where bulk interception is technically feasible?*
*   [ ] **Yes**
*   [ ] **No**
*   **Analysis:** *[Insert analysis regarding encryption in transit.]*

**3. History of Requests**
*Has the Data Importer received requests from public authorities for access to personal data in the past 5 years?*
*   [ ] **Yes** (Provide details in confidential annex)
*   [ ] **No**

#### Part C: Supplementary Measures (Technical & Organizational)
*To be completed by the CISO or Technical Lead. If the laws in Part B are problematic, these measures must prevent access.*

**1. Technical Measures**

| Measure | Implementation Status | Description |
| :--- | :--- | :--- |
| **Encryption in Transit** | [Implemented / Not Implemented] | [e.g., TLS 1.2 or higher for all data flows.] |
| **Encryption at Rest** | [Implemented / Not Implemented] | [e.g., AES-256 encryption on all databases.] |
| **Key Management** | [Importer Managed / Exporter Managed] | [Who holds the keys? If the Importer holds keys, can they be compelled to decrypt?] |
| **Pseudonymization** | [Implemented / Not Implemented] | [Is data tokenized before leaving the EEA?] |

**2. Organizational Measures**

| Measure | Implementation Status | Description |
| :--- | :--- | :--- |
| **Data Minimization** | [Implemented] | Only data strictly necessary for the purpose is transferred. |
| **Transparency Reports** | [Planned / Implemented] | Study GRC publishes a "Transparency" page per Bylaws Art. VIII §8.2. |
| **Challenge Government Access** | [Policy Active] | Policy to legally challenge any non-binding or overbroad request for data access. |
| **Internal Policies** | [Active] | DP-POL-001 (Master Privacy Policy) and IS-POL-001 (InfoSec Policy) are in force. |

#### Part D: Risk Assessment and Conclusion
*To be completed by the Data Protection Officer (DPO).*

**1. Severity of Risk**
*   [ ] **Low:** Laws do not apply; strong encryption exists.
*   [ ] **Medium:** Laws apply to sub-processors; encryption exists but keys are managed by US cloud provider.
*   [ ] **High:** Laws apply; data is in clear text; no supplementary measures.

**2. Conclusion**
Based on the assessment above, the transfer of personal data:
*   [ ] **Can Proceed:** The combination of the Transfer Tool and Supplementary Measures provides an essentially equivalent level of protection.
*   [ ] **Can Proceed with Conditions:** (List conditions below).
*   [ ] **Must Be Suspended:** The risks cannot be mitigated.

**3. Rationale:**
*[Insert detailed rationale. Example: While US surveillance laws exist, Study GRC Inc. encrypts all data in transit and at rest. Furthermore, the nature of the data (educational records) is of low interest to intelligence agencies. The risk of bulk surveillance impacting this specific data set is negligible.]*

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Data Exporter (Project Owner)** | Initiates the TIA request and provides data flow details (Part A). |
| **Legal Counsel / Privacy Officer** | Analyzes Third Country laws and applicability of surveillance statutes (Part B). |
| **CISO** | Validates technical supplementary measures (Encryption, Access Control) (Part C). |
| **Data Protection Officer (DPO)** | Reviews the assessment, assigns risk rating, and authorizes or denies the transfer (Part D). |

### 6. Compliance and Enforcement
Failure to complete a TIA prior to initiating a new cross-border data transfer involving EEA/UK data is a violation of the **Master Data Privacy Policy**.

If a TIA reveals that a Third Country's laws prevent compliance with the SCCs, Study GRC Inc. must suspend the transfer immediately. Continuing a transfer in violation of this assessment may result in disciplinary action and exposes the Organization to severe regulatory fines under GDPR (up to 4% of global turnover).

### 7. References
*   **GDPR Article 46:** Transfers subject to appropriate safeguards.
*   **CJEU Case C-311/18 (Schrems II):** Judgment regarding the validity of SCCs.
*   **EDPB Recommendations 01/2020:** Measures that supplement transfer tools to ensure compliance with the EU level of protection of personal data.
*   **Study GRC Bylaws Article IX:** Policies & Data Protection.
*   **DP-POL-001:** Master Data Privacy Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial Release aligned with Schrems II requirements. |