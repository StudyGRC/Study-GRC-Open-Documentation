### Cryptocurrency Processing Procedure

| Document Control | |
| :--- | :--- |
| **Document ID** | FIN-PRC-060 |
| **Document Type** | Procedure |
| **Version** | v1.0 |
| **Effective Date** | [YYYY-MM-DD] |
| **Next Review Date** | [YYYY-MM-DD] (Annual) |
| **Approving Authority** | Board of Directors |
| **Document Owner** | Chief Financial Officer (CFO) |
| **Classification** | Confidential |

### 1. Purpose
The purpose of this procedure is to establish strict security protocols and operational steps for the acceptance, custody, and liquidation of cryptocurrency donations. This document is designed to mitigate risks associated with digital asset volatility, theft, loss of private keys, and money laundering, ensuring compliance with IRS property regulations and **Study GRC Inc.**'s financial controls.

### 2. Scope
This procedure applies to all Directors, Officers (specifically the Treasurer and CFO), and authorized finance personnel involved in the handling of digital assets on behalf of the Organization.
*   **In Scope:** Setup of institutional wallets, custody of private keys/seed phrases, processing of incoming donations, and liquidation into fiat currency (USD).
*   **Out of Scope:** Personal trading activities of employees; blockchain technology development unrelated to financial transactions.

### 3. Definitions

| Term | Definition |
| :--- | :--- |
| **Cold Storage** | An offline cryptocurrency wallet (hardware) not connected to the internet, offering the highest level of security against hacking. |
| **Hot Wallet** | A cryptocurrency wallet connected to the internet (e.g., a mobile app or exchange account), used for immediate transactions but higher risk. |
| **Multi-Signature (Multi-Sig)** | A wallet configuration requiring two or more private keys to authorize a transaction, preventing a single individual from moving funds unilaterally. |
| **Seed Phrase** | A series of 12-24 words that grant full access to a cryptocurrency wallet. Loss or theft of this phrase results in total loss of funds. |
| **Liquidation** | The process of selling cryptocurrency assets for fiat currency (USD) to stabilize value. |
| **KYC/AML** | "Know Your Customer" and "Anti-Money Laundering" regulations requiring the identification of donors to prevent illicit financial flows. |

### 4. Procedures

#### 4.1 Wallet Architecture and Security
To ensure the safety of assets, the Organization utilizes a tiered wallet structure.

1.  **Institutional Exchange Account (Hot Wallet):**
    *   The CFO must establish a corporate account with a US-domiciled, regulated exchange (e.g., Coinbase, Gemini) compliant with BitLicense or federal banking standards.
    *   **Access Control:** Access to the exchange account must be protected by a unique, complex password and hardware-based Multi-Factor Authentication (MFA) (e.g., YubiKey). SMS-based MFA is strictly prohibited.
2.  **Multi-Signature Requirement:**
    *   For any holdings exceeding **$5,000 USD** in value that are not immediately liquidated, funds must be moved to a Multi-Sig wallet or a Cold Storage Hardware Wallet (e.g., Ledger/Trezor).
    *   **Key Sharding:** If a hardware wallet is used, the Seed Phrase must be split into two parts (e.g., words 1-12 and words 13-24).
    *   **Physical Custody:**
        *   **Part A** is held in a fireproof safe at the Registered Office or by the Treasurer.
        *   **Part B** is held in a safety deposit box at the Organization's primary banking institution.
        *   Accessing both parts requires the physical presence of two authorized officers (Two-Person Integrity).

#### 4.2 Donation Intake and Screening
1.  **Public Addresses:** The Organization shall publish specific public wallet addresses or QR codes on the "Transparency" page for standard donations.
2.  **Donor Identification (KYC):**
    *   For donations valued at **$1,000 USD or more**, the donor must complete a *Gift Acceptance Form* providing their legal name and address.
    *   The CFO must screen the donor’s name and the originating wallet address against the **OFAC Specially Designated Nationals (SDN) List** to ensure compliance with anti-terrorism laws.
    *   Anonymous donations exceeding $1,000 must be reviewed by the Board before acceptance.

#### 4.3 Immediate Liquidation Protocol
Pursuant to the Organization's *Investment Policy*, Study GRC Inc. does not speculate on cryptocurrency markets.

1.  **Auto-Liquidation:** Where the exchange platform permits, the account must be configured to automatically convert incoming cryptocurrency to USD immediately upon receipt.
2.  **Manual Liquidation:** If auto-liquidation is not available:
    *   The CFO receives a notification of the deposit.
    *   The CFO must log in and execute a "Sell" order at the current market rate within **24 hours** of receipt.
    *   Funds must be withdrawn to the Organization’s operating bank account via ACH or Wire Transfer within **3 business days**.
3.  **Exception:** Retention of cryptocurrency (holding) requires a specific affirmative vote by the Board of Directors, documented in meeting minutes, acknowledging the volatility risk.

#### 4.4 Accounting and Substantiation
1.  **Valuation:**
    *   Donations are recorded as revenue at the **Fair Market Value (FMV)** in USD at the exact time of receipt, per IRS Notice 2014-21.
    *   Any difference between the FMV at receipt and the final sale price (liquidation) must be recorded as *Gain/Loss on Sale of Assets*.
2.  **Donor Acknowledgment:**
    *   The Organization shall provide a written acknowledgment to the donor describing the cryptocurrency received (e.g., "0.5 Bitcoin") and the date of receipt.
    *   **Note:** The acknowledgment must **not** assign a dollar value to the donation; valuation is the donor's responsibility.
3.  **IRS Form 8282:**
    *   If the Organization sells, exchanges, or disposes of the cryptocurrency within three years of receipt, and the value exceeds $500, the CFO must file **IRS Form 8282** (Donee Information Return) within 125 days of the disposition and provide a copy to the donor.

#### 4.5 Incident Response (Compromise)
1.  If a private key is suspected to be compromised or a device is lost:
    *   **Immediate Freeze:** The CFO must contact the exchange to freeze the account.
    *   **Asset Migration:** If using a self-custody wallet, authorized officers must immediately transfer remaining funds to a new, secure wallet.
    *   **Reporting:** The incident must be reported to the Board of Directors and the CISO immediately, and documented via the *Incident Response Plan*.

### 5. Roles and Responsibilities

| Role | Responsibility |
| :--- | :--- |
| **Treasurer** | Holds custodial authority over backup seed phrases (Part A). Reviews monthly reconciliation of crypto-to-fiat transactions. |
| **Chief Financial Officer (CFO)** | Manages the exchange account, executes liquidations, performs OFAC screening, and ensures IRS reporting (Form 8282). |
| **Chief Info. Security Officer (CISO)** | Audits wallet security configurations, approves hardware wallet models, and manages MFA device issuance. |
| **Executive Director** | Serves as the emergency backup signatory for exchange access in the event of the CFO's incapacitation. |

### 6. Compliance and Enforcement
Failure to comply with this procedure may result in disciplinary action, up to and including termination of employment and legal action for breach of fiduciary duty.
*   **IRS Compliance:** Failure to properly report crypto transactions can jeopardize the Organization's 501(c)(3) status.
*   **Internal Controls:** Violation of the Two-Person Integrity rule for cold storage access is a "Critical" severity infraction.

### 7. References
*   **Bylaws Article VIII:** Records, Transparency & Finance.
*   **FIN-POL-058:** Gift Acceptance Policy.
*   **FIN-POL-012:** Investment Policy.
*   **IRS Notice 2014-21:** IRS guidance on virtual currency.
*   **IRS Pub 561:** Determining the Value of Donated Property.

### 8. Revision History

| Version | Date | Author | Change Description |
| :--- | :--- | :--- | :--- |
| v1.0 | [Date] | Chief Legal Officer | Initial Release |