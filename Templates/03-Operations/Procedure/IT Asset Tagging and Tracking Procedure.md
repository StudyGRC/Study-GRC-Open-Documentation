### IT Asset Tagging and Tracking Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | IS-PRC-008 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | 2023-10-27 |
| **Next Review Date** | 2024-10-27 (Annual) |
| **Approving Authority** | Executive Director |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Classification** | Internal |

### 1. Purpose
The purpose of this procedure is to establish a standardized method for the identification, tagging, and tracking of Study GRC Inc. ("the Organization") information technology assets. This procedure ensures accurate financial reporting, facilitates effective lifecycle management, enhances security by maintaining visibility of authorized devices, and ensures compliance with **2 CFR § 200.313 (Equipment)** regarding the management of assets purchased with federal funds.

### 2. Scope
This procedure applies to all hardware and software assets owned, leased, or managed by the Organization.

**In Scope:**
*   End-user computing devices (Laptops, Desktops, Tablets).
*   Servers, storage devices, and networking equipment (Firewalls, Switches, Routers).
*   Mobile devices (Smartphones) owned by the Organization.
*   Peripherals with a purchase cost exceeding $500.00 USD.
*   **Any** equipment, regardless of cost, purchased in whole or in part with Federal Grant funds.

**Out of Scope:**
*   Consumable IT supplies (cables, toner, mice/keyboards under $100).
*   Personally Owned Devices (BYOD), which are governed by the *Bring Your Own Device Policy*, except for the requirement of MDM registration.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Asset Tag** | A tamper-evident physical label with a unique identification number and barcode/QR code applied to hardware. |
| **CMDB** | Configuration Management Database; the central repository used to store information about IT assets. |
| **Custodian** | The individual (employee, volunteer, or contractor) to whom an asset is assigned and who is responsible for its care. |
| **FAIN** | Federal Award Identification Number; required for tracking assets purchased via grants. |
| **MDM** | Mobile Device Management; software used to secure and enforce policies on mobile devices and laptops. |

### 4. Procedures

#### 4.1 Asset Acquisition and Intake
1.  **Procurement:** All IT assets must be purchased in accordance with the *Procurement Policy*.
2.  **Receiving:**
    *   **Centralized Receiving:** Whenever feasible, assets should be shipped to the designated IT processing location for configuration and tagging prior to deployment.
    *   **Remote/Drop-Ship:** For remote employees where direct shipping is necessary, the asset is considered "Received" when the vendor delivery confirmation is generated. The CISO or designee must record the serial number from the purchase order immediately.

#### 4.2 Physical Tagging Standards
1.  **Tag Specification:** Tags must be tamper-resistant, barcoded, and bear the logo or name of Study GRC Inc.
2.  **Placement:**
    *   **Laptops:** Bottom of the chassis, avoiding vents or removable battery covers.
    *   **Desktops/Servers:** Top or side of the chassis, clearly visible without moving the device.
    *   **Monitors:** Back of the panel near the input ports.
    *   **Mobile Devices:** If a case is provided, on the device back; if not, electronic tracking (MDM) serves as the primary identifier.
3.  **Remote Tagging:** For drop-shipped items, IT will mail an asset tag to the Custodian. The Custodian must apply the tag within three (3) business days of receipt and upload a photo of the applied tag to the IT Help Desk ticket.

#### 4.3 Digital Identification (Naming Convention)
All assets must be assigned a unique hostname during the provisioning process to match the Asset Tag.

**Format:** `SGRC-[TYPE]-[TAG#]`
*   **SGRC:** Organization Prefix
*   **TYPE:** Device Type (e.g., LPT=Laptop, SRV=Server, MOB=Mobile)
*   **TAG#:** The 4-6 digit number from the physical asset tag.

*Example:* `SGRC-LPT-00452`

#### 4.4 Asset Register (CMDB) Entry
Upon tagging, the IT Administrator must create a record in the Asset Management System (CMDB). In compliance with **2 CFR § 200.313(d)(1)**, the record **must** contain:

1.  **Description:** (e.g., MacBook Pro 14-inch).
2.  **Serial Number:** Manufacturer's unique ID.
3.  **Asset Tag Number:** Study GRC unique ID.
4.  **Source of Funding:** Explicitly listing the Federal Award Identification Number (FAIN) if applicable.
5.  **Title Holder:** (e.g., Study GRC Inc. or Federal Government).
6.  **Acquisition Date:** Date of purchase.
7.  **Cost:** Purchase price.
8.  **Percentage of Federal Participation:** (0% to 100%).
9.  **Location:** Physical location (e.g., "Remote - Austin, TX").
10. **Condition:** (e.g., New, Good, Fair, Poor).
11. **Disposition Data:** (Date of disposal and sale price, if applicable).

#### 4.5 Assignment and Custody
1.  **Check-Out:** Assets are assigned to a specific Custodian. The Custodian must sign (electronically) an *Asset Acceptance Form* acknowledging receipt and responsibility.
2.  **Transfers:** Assets must not be swapped between employees without notifying IT. A ticket must be filed to update the Custodian in the CMDB.
3.  **Return:** Upon termination of employment or volunteer service, assets must be returned within five (5) business days. IT will update the status to "In Stock" or "Pending Disposal."

#### 4.6 Verification and Inventory Audits
1.  **Automated Verification:** The MDM system shall continuously report the "Last Seen" status of all enrolled devices. Devices not seen for 30 days will be flagged for investigation.
2.  **Physical Inventory:**
    *   **Frequency:** A physical inventory of all assets must be reconciled with the CMDB records at least once every two (2) years (per **2 CFR § 200.313(d)(2)**).
    *   **Remote Verification:** Remote staff may be required to submit photo evidence of the asset and its tag during the audit period or attend a video call for visual verification.

#### 4.7 Lost or Stolen Assets
1.  **Reporting:** Custodians must report lost or stolen assets to the CISO immediately (within 24 hours).
2.  **Remote Wipe:** IT will initiate a remote wipe command via MDM for any lost/stolen device containing sensitive data.
3.  **Documentation:** An *Incident Report* must be filed. If the asset was federally funded, the CFO must determine if reporting to the awarding agency is required.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Chief Information Security Officer (CISO)** | Owner of the Asset Management process; ensures security controls (MDM) are active on all tracked assets. |
| **IT Administrator** | Performs physical tagging, updates the CMDB, and conducts inventory audits. |
| **Chief Financial Officer (CFO)** | Reconciles the IT Asset Register with the General Ledger; ensures grant compliance regarding asset funding sources. |
| **Custodian (Employee/Volunteer)** | Protects the asset from damage/theft; applies tags (if remote); reports loss immediately; returns asset upon departure. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in inaccurate financial reporting and non-compliance with federal grant conditions, potentially leading to the repayment of funds (disallowance).

Internal disciplinary action for failure to follow this procedure (e.g., unauthorized transfer of assets, failure to return assets) may include termination of employment or volunteer assignment and legal action to recover the value of the property.

### 7. References
*   **2 CFR § 200.313 (Equipment)** - Uniform Guidance for Federal Awards.
*   **Bylaws of Study GRC Inc.** - Article VIII (Records, Transparency & Finance).
*   **IS-POL-001:** Master Information Security Policy.
*   **FIN-POL-013:** Fixed Asset Capitalization Policy.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-10-27 | CISO | Initial Release aligned with 2 CFR 200. |