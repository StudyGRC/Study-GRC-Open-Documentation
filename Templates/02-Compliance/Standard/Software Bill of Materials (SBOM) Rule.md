### Software Bill of Materials (SBOM) Rule

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-STD-065 |
| **Document Type** | Standard |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Public |

### 1. Purpose
The purpose of this Standard is to mandate the generation, maintenance, and consumption of a Software Bill of Materials (SBOM) for all software developed, procured, or operated by Study GRC Inc. This standard aligns with Executive Order 14028 and CISA guidelines to enhance software supply chain security. By maintaining a transparent inventory of software components, the Organization ensures the integrity of its open-source resources (pursuant to Bylaws Article IX) and enables rapid response to zero-day vulnerabilities (e.g., Log4j).

### 2. Scope
This Standard applies to:
*   **Internal Development:** All software, code repositories, and educational platforms developed by Study GRC Inc. staff, volunteers, or contractors.
*   **Procurement:** All third-party software (SaaS, on-premise, or libraries) procured or utilized by the Organization.
*   **Open Source Contributions:** Code contributions accepted into the Organization’s repositories.

**Exclusions:**
*   Low-risk administrative tools that do not process Personally Identifiable Information (PII) or interact with the Organization’s production environment, subject to CISO approval.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **SBOM (Software Bill of Materials)** | A formal, machine-readable inventory of software components and dependencies, the hierarchical relationships between them, and their associated metadata. |
| **CycloneDX** | A lightweight software bill of materials (SBOM) standard designed for use in application security contexts and supply chain component analysis. |
| **SPDX (Software Package Data Exchange)** | An open standard for communicating software bill of material information, including components, licenses, copyrights, and security references. |
| **Transitive Dependency** | A component that is a dependency of a direct dependency (e.g., a library used by a library you use). |
| **VEX (Vulnerability Exploitability eXchange)** | A companion artifact to an SBOM that allows a software supplier to communicate the exploitability status of vulnerabilities within the product. |
| **NTIA Minimum Elements** | The baseline data fields required for an SBOM as defined by the National Telecommunications and Information Administration (NTIA) and adopted by CISA. |

### 4. Standard Requirements

#### 4.1 Approved Data Formats
To ensure interoperability and automated analysis, all SBOMs generated or consumed by Study GRC Inc. must adhere to one of the following machine-readable formats:
*   **CycloneDX** (JSON or XML) - *Preferred for internal development.*
*   **SPDX** (JSON, XML, or Tag-Value) - *Acceptable for third-party vendors.*

Proprietary or non-standard formats (e.g., PDF, Excel spreadsheets) are **prohibited** for compliance with this Standard.

#### 4.2 Minimum Data Elements (CISA/NTIA Compliance)
All SBOMs must contain, at a minimum, the following data fields for every component:
1.  **Supplier Name:** The entity that creates, defines, and identifies components.
2.  **Component Name:** The designation assigned to a unit of software defined by the original supplier.
3.  **Component Version:** The identifier used by the supplier to specify a change in software from a previously identified version.
4.  **Other Unique Identifiers:** PURL (Package URL), CPE (Common Platform Enumeration), or SWID tags.
5.  **Dependency Relationship:** The upstream relationship (e.g., `X includes Y`).
6.  **Author of SBOM Data:** The entity that created the SBOM data.
7.  **Timestamp:** The date and time when the SBOM data was assembled.

#### 4.3 Internal Development Requirements
For all "Work Product" as defined in **Bylaws Article IX, Section 9.3**:
*   **Automated Generation:** SBOM generation must be integrated into the CI/CD pipeline. An SBOM must be generated automatically for every release build.
*   **Depth:** The SBOM must inventory all top-level components and **transitive dependencies** (dependencies of dependencies).
*   **Repository Storage:** The generated SBOM must be stored in the root directory of the repository or a designated `/security` folder for every release.
*   **Vulnerability Mapping:** The development team must utilize Software Composition Analysis (SCA) tools to map SBOM components against the National Vulnerability Database (NVD).

#### 4.4 Procurement and Vendor Requirements
Prior to the execution of any contract or the deployment of any third-party software:
*   **Mandatory Submission:** Vendors must provide a valid SBOM meeting the requirements of Section 4.1 and 4.2.
*   **Legacy Software:** If a vendor cannot provide an SBOM, they must provide a roadmap for compliance within 90 days, or the CISO must approve a Risk Acceptance Form.
*   **Updates:** Vendors are contractually required to provide an updated SBOM upon every major version release or significant patch.

#### 4.5 Open Source Contribution Integrity
To maintain the "Zero-cost, open-source resources" mission (Bylaws Article I, Section 1.3):
*   Contributors must not introduce obfuscated binaries.
*   All dependencies introduced in a Pull Request (PR) must be declared in standard manifest files (e.g., `package.json`, `requirements.txt`, `go.mod`) to ensure accurate SBOM generation.

#### 4.6 Vulnerability Exploitability eXchange (VEX)
For systems classified as **Critical** in the *Data Classification Standard*, the generation of a VEX document is required to clarify false positives in the SBOM (i.e., vulnerable components that are not exploitable in the specific configuration used).

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owns this Standard; validates SBOM tools; approves Risk Acceptances for vendors unable to provide SBOMs. |
| **VP of Education & Training** | Ensures all educational software platforms and curriculum code repositories generate compliant SBOMs. |
| **DevSecOps / IT Team** | Configures CI/CD pipelines to automate SBOM generation; maintains SCA tooling. |
| **Procurement/Finance** | Enforces SBOM requirements in vendor contracts and purchase orders. |
| **Volunteers/Contributors** | Adhere to dependency declaration standards in code contributions. |

### 6. Compliance and Enforcement
**Technical Enforcement:** Code merges may be blocked automatically by CI/CD controls if an SBOM cannot be generated or if high-severity vulnerabilities are detected in the dependencies.

**Administrative Enforcement:** Failure to comply with this standard may result in:
*   **Employees:** Disciplinary action up to and including termination.
*   **Volunteers:** Revocation of repository access and membership termination.
*   **Vendors:** Termination of contract for breach of security requirements.

### 7. References
*   **Executive Order 14028:** *Improving the Nation’s Cybersecurity* (Sec. 4 - Enhancing Software Supply Chain Security).
*   **CISA/NTIA:** *The Minimum Elements for a Software Bill of Materials (SBOM)*.
*   **NIST SP 800-218:** *Secure Software Development Framework (SSDF)*.
*   **Study GRC Bylaws:** Article IX (Intellectual Property & Open Source).
*   **IS-POL-060:** Master Information Security Policy.
*   **IS-STD-050:** Data Classification Standard.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Compliance Architect | Initial Release aligned with CISA guidelines. |