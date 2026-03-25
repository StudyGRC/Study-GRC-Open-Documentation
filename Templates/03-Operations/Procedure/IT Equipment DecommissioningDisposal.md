### IT Equipment Decommissioning and Disposal Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-083 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2025-10-27 (Bi-Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized process for the secure decommissioning, sanitization, and disposal of Information Technology (IT) assets. This procedure ensures that Study GRC Inc. mitigates the risk of unauthorized data disclosure (data leakage) involving Personally Identifiable Information (PII), Intellectual Property (IP), or sensitive organizational data when hardware reaches its end-of-life or is transferred. This aligns with **Bylaws Article IX (Policies & Data Protection)** and federal grant requirements under **2 CFR 200.313**.

### 2. Scope
This procedure applies to all Study GRC Inc. personnel (employees, contractors, and volunteers) and covers all IT assets capable of storing data, owned or leased by the Organization.

**In Scope:**
*   End-user devices (Laptops, Desktops, Tablets, Smartphones).
*   External storage media (USB drives, External HDDs/SSDs, SD Cards).
*   Networking equipment with storage capabilities (Routers, Switches, Firewalls).
*   Printers/MFPs with internal hard drives.
*   Servers and backup tapes.

**Exclusions:**
*   BYOD devices (governed by *IS-POL-022 Bring Your Own Device Policy*), except where Organization data must be remotely wiped prior to the device leaving the Organization's ecosystem.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Sanitization** | A process to render access to "Target Data" on the media infeasible for a given level of effort. |
| **Clear** | A method of sanitization that applies logical techniques to sanitize data in all user-addressable storage locations (e.g., Factory Reset, Re-imaging). Suitable for assets remaining within the Organization. |
| **Purge** | A method of sanitization that applies physical or logical techniques that render Target Data recovery infeasible using state-of-the-art laboratory techniques (e.g., Cryptographic Erase, Block Overwrite). Required for assets leaving the Organization. |
| **Destroy** | A method of sanitization that renders Target Data recovery infeasible using state-of-the-art laboratory techniques and results in the subsequent inability to use the media for storage of data (e.g., Shredding, Incineration). |
| **Cryptographic Erase (CE)** | A technique that sanitizes media by erasing the encryption key used to encrypt the data, rendering the data unreadable. |
| **CoS** | Certificate of Sanitization. A formal record attesting that a specific asset was sanitized. |

### 4. Procedures

#### 4.1 Asset Identification and Evaluation
Before any action is taken, the asset must be identified and its future state determined.

1.  **Initiate Request:** The Asset Custodian or Department Head must submit a "Decommissioning Request" ticket to the IT Department.
2.  **Verify Asset Record:** IT Staff must verify the asset against the Master Asset Inventory (*IS-REG-001*) to confirm ownership and funding source (e.g., Federal Grant vs. General Fund).
3.  **Determine Disposition Path:**
    *   **Re-deployment:** Asset is functional and will be reassigned to another user.
    *   **Donation/Sale:** Asset is functional but no longer meets Organization standards. (Note: Assets purchased with Federal funds >$5,000 must follow **2 CFR 200.313(e)** disposition rules).
    *   **Destruction/E-Waste:** Asset is broken or obsolete.
    *   **Lease Return:** Asset is being returned to a vendor.

#### 4.2 Data Sanitization (NIST SP 800-88 Rev. 1)
The level of sanitization is determined by the data classification of the device and its destination.

**4.2.1 Level 1: Clear (Internal Re-deployment)**
*   **Applicability:** Device is staying within Study GRC Inc. control.
*   **Procedure:**
    1.  Perform a "Factory Reset" or re-image the device using the standard corporate image.
    2.  Verify that previous user profiles and local data are removed.
    3.  Update the Asset Inventory with the new assignee.

**4.2.2 Level 2: Purge (Donation, Sale, or Lease Return)**
*   **Applicability:** Device is leaving Study GRC Inc. but remains functional.
*   **Procedure (SSD/Flash Media):**
    1.  Execute a **Cryptographic Erase (CE)** if the drive was encrypted (BitLocker/FileVault).
    2.  If unencrypted, use a NIST-compliant overwrite tool (minimum 2 passes) or manufacturer "Secure Erase" command.
*   **Procedure (Magnetic HDD):**
    1.  Use a NIST-compliant overwrite tool (minimum 3 passes) to overwrite all addressable locations.
*   **Verification:**
    1.  IT Staff must verify 10% of the drive (random sampling) to ensure data is unreadable.
    2.  Generate a **Certificate of Sanitization (CoS)** containing the Serial Number, Date, Method Used, and Technician Name.

**4.2.3 Level 3: Destroy (Failed Media or High Security)**
*   **Applicability:** Device is broken, or contained "Restricted/Confidential" data and cannot be successfully Purged.
*   **Procedure:**
    1.  Remove the storage media (Hard Drive/SSD) from the chassis.
    2.  **Physical Destruction:**
        *   **Shredding:** Pass through a mechanical shredder (particle size < 6mm for SSDs).
        *   **Disintegration/Pulverization:** For solid-state media.
        *   **Drilling:** (Emergency/Remote only) Drill at least four holes through the platters (HDD) or controller/chips (SSD) to prevent spin-up/read.
    3.  Photograph the destroyed media showing the Serial Number if possible.

#### 4.3 Remote/Distributed Workforce Handling
As a remote-first organization, physical access to devices is not always immediate.

1.  **Remote Wipe:** Prior to shipping a device back to HQ, IT Staff must issue a **Remote Wipe** command via the Mobile Device Management (MDM) platform (e.g., Intune/Jamf).
2.  **Shipping:** The user must ship the device using a provided prepaid shipping label with tracking and insurance.
3.  **HQ Receipt:** Upon receipt, IT Staff must physically verify the wipe and proceed with Section 4.2 based on the final disposition.
4.  **Remote Destruction (Exception):** If shipping is cost-prohibitive or the device is damaged, the CISO may authorize the user to physically destroy the storage media (e.g., drill/hammer) on video call or provide photo evidence, followed by local e-waste recycling.

#### 4.4 Environmental Disposal (E-Waste)
Study GRC Inc. is committed to environmentally responsible disposal.

1.  **Vendor Selection:** Electronic waste must only be handed over to R2 (Responsible Recycling) or e-Stewards certified recyclers.
2.  **Chain of Custody:** The vendor must provide a transfer of custody document listing the weight or count of assets.
3.  **Prohibition:** IT equipment must **never** be disposed of in municipal trash or landfill bins.

#### 4.5 Documentation and Record Retention
1.  **Asset Inventory Update:** The Master Asset Inventory must be updated to status "Disposed" with the date and method recorded.
2.  **Certificate Retention:** Certificates of Sanitization (CoS) and E-Waste Transfer documents must be retained for **seven (7) years** in accordance with the *Document Retention and Destruction Policy (GOV-POL-012)*.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **CISO** | Defines sanitization standards; approves exceptions to destruction methods; selects certified e-waste vendors. |
| **IT Manager** | Oversees the execution of the decommissioning process; maintains the CoS repository; ensures Asset Inventory accuracy. |
| **IT Staff** | Performs technical sanitization (Wipe/Purge/Destroy); verifies successful data removal; coordinates shipping logistics. |
| **Asset Custodian (User)** | Returns equipment promptly upon request; performs physical shipping tasks; protects equipment until custody transfer. |

### 6. Compliance and Enforcement
Failure to adhere to this procedure may result in the leakage of sensitive data, leading to regulatory fines (GDPR, CCPA/CPRA), loss of 501(c)(3) status, or breach of federal grant conditions.

**Enforcement:**
*   Employees found to have disposed of IT assets in unauthorized trash receptacles or sold assets without sanitization will be subject to disciplinary action, up to and including termination.
*   Civil or criminal penalties may apply if negligence leads to a data breach.

### 7. References
*   **NIST SP 800-88 Rev. 1:** *Guidelines for Media Sanitization*
*   **2 CFR 200.313:** *Equipment (Uniform Guidance)*
*   **IS-POL-001:** *Master Information Security Policy*
*   **IS-POL-080:** *Asset Inventory and Management Policy*
*   **GOV-POL-012:** *Document Retention and Destruction Policy*

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | [Name] | Initial Release aligned with NIST SP 800-88. |