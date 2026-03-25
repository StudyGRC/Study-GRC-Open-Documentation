### AI Training Data Source Documentation

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-015 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-25 |
| **Next Review Date** | 2024-10-25 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to establish mandatory requirements for documenting the provenance, licensing, and composition of all data used to train, fine-tune, or ground Artificial Intelligence (AI) systems operated by Study GRC Inc.

As a non-profit dedicated to "fostering a community-driven ecosystem" (Bylaws Art. 1.3), we must ensure our AI initiatives are built upon a foundation of transparency, intellectual property respect, and ethical data sourcing. This standard mitigates legal risks associated with copyright infringement and operational risks regarding bias and data quality.

### 2. Scope
This Standard applies to all employees, contractors, and volunteers involved in the development, deployment, or maintenance of AI models for Study GRC Inc.

**In Scope:**
*   Datasets used for **Fine-Tuning** Large Language Models (LLMs).
*   Knowledge bases used for **Retrieval-Augmented Generation (RAG)** systems (e.g., a GRC Chatbot).
*   Datasets used to train predictive or classification models.

**Out of Scope:**
*   Transient user prompts entered into third-party tools (e.g., standard ChatGPT usage), which are governed by the *Acceptable Use Policy*.
*   System logs used solely for IT security monitoring, unless used to train an anomaly detection model.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Training Data** | Information used to teach an AI model patterns, logic, or specific knowledge. Includes training, validation, and test sets. |
| **Provenance** | The chronology of the ownership, custody, or location of a historical object or document; in this context, the origin of the data. |
| **RAG (Retrieval-Augmented Generation)** | A technique where an AI model retrieves facts from an external knowledge base to ground its responses, rather than relying solely on its pre-trained memory. |
| **Corpus** | A collection of written texts, especially the entire works of a particular author or a body of writing on a particular subject. |
| **Scraping** | The automated extraction of data from websites. |

### 4. Standards

#### 4.1 Data Source Registry
All AI projects must maintain a **Data Source Registry** (DSR). This registry must be stored in the Organization’s central document repository and be accessible to the CISO and Legal Counsel. The DSR must be updated *prior* to the commencement of any training or ingestion process.

#### 4.2 Mandatory Documentation Fields
For every dataset or document source included in the DSR, the following metadata **must** be recorded:

**4.2.1 Source Identification**
*   **Name of Source:** (e.g., "NIST Special Publication 800-53 Rev 5").
*   **Origin URL/Location:** Direct link to where the data was acquired.
*   **Date of Access/Collection:** ISO 8601 format (YYYY-MM-DD).
*   **Version/Revision:** (e.g., "v5.1.1").

**4.2.2 Collection Method**
*   **Method:** (e.g., API download, Manual PDF download, Web Scrape, Partner Data Transfer).
*   **Tools Used:** (e.g., Python Beautiful Soup, Official API Client).

**4.2.3 Licensing and Rights (Critical)**
*   **License Type:** (e.g., Creative Commons BY-SA 4.0, MIT, Public Domain/US Gov Work, Proprietary-with-Permission).
*   **Verification:** A brief statement confirming the license allows for AI processing/derivative works.
    *   *Note:* "Publicly available on the internet" does **not** mean Public Domain.
*   **Attribution Requirement:** Does the license require us to credit the author in the AI's output or system documentation? (Yes/No).

**4.2.4 Data Characteristics**
*   **Data Type:** (e.g., Text, Code, Image, Tabular).
*   **Size:** (e.g., 500MB, 10,000 tokens).
*   **Description:** Brief summary of content (e.g., "Federal regulatory text regarding information security").

#### 4.3 PII and Sensitive Data Screening
Prior to ingestion, all data sources must be certified as free of Prohibited Data.
*   **PII Removal:** All Personally Identifiable Information (names, emails, addresses) must be redacted or anonymized unless explicit consent exists (Bylaws Art. IX, §9.2).
*   **Confidentiality:** Data classified as "Confidential" or "Restricted" per the *Data Classification Standard* must not be fed into public-facing models or third-party closed models without a Data Processing Agreement (DPA).

#### 4.4 Bias and Representation Assessment
For datasets exceeding 1,000 records, a **Bias Assessment** must be documented in the DSR.
*   **Geographic Representation:** Does the data reflect global GRC standards or only US-centric laws?
*   **Temporal Relevance:** Is the data historical (outdated) or current?
*   **Language:** Primary language of the corpus.

#### 4.5 Version Control and Hash Integrity
To ensure reproducibility and security:
*   **Hashing:** A cryptographic hash (SHA-256) of the raw dataset file must be recorded in the DSR to verify integrity.
*   **Versioning:** If a dataset is modified (cleaned/scrubbed), it must be saved as a new version (e.g., `dataset_v1_raw` vs `dataset_v1_clean`).

#### 4.6 Transparency Publication
In alignment with Bylaws Article VIII (Transparency), Study GRC Inc. shall publish a **"Model Card"** or **"System Card"** for any public-facing AI tool. This public document must summarize the DSR, listing:
*   Primary data sources (e.g., "Trained on NIST and ISO standards").
*   Licensing status of training data.
*   Known limitations regarding data currency.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **AI Project Lead** | Responsible for populating the Data Source Registry and ensuring data accuracy before training begins. |
| **Chief Information Security Officer (CISO)** | Verifies that PII scrubbing has occurred and that data handling complies with the *Data Classification Standard*. |
| **Legal Counsel / Compliance** | Reviews the "Licensing and Rights" section of the DSR to prevent copyright infringement and ensure Open Source compliance. |
| **Executive Director** | Approves the final release of any AI model based on the transparency and risk assessment provided in the DSR. |

### 6. Compliance and Enforcement
Failure to comply with this standard could result in copyright litigation, reputational damage, and violation of the Organization's 501(c)(3) mandate to operate ethically.

**Enforcement:**
*   Models trained on undocumented data will be decommissioned immediately.
*   Personnel found willfully ingesting proprietary data without license (piracy) or failing to scrub PII may face disciplinary action, up to and including termination, per the *Employee Handbook*.

### 7. References
*   **Bylaws of Study GRC Inc.** (Article VIII - Transparency; Article IX - IP).
*   **NIST AI Risk Management Framework (AI RMF 1.0)** - Govern 1.2, Map 2.2.
*   **EU AI Act** - Transparency obligations for General Purpose AI.
*   **IS-STD-005 Data Classification Standard**.
*   **IS-POL-010 Intellectual Property Policy**.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-25 | Chief Compliance Architect | Initial Release |