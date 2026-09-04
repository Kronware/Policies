# Google Play Data Safety Declaration for VaultSeal

**Application ID:** app.kronware.vaultseal  
**Publisher:** Kronware (kronware.io)  
**Last Updated:** September 4, 2026  

---

## 1. Overview
- **Personal Data Collection:** No
- **Data Shared with Third Parties:** No
- **Encryption in Transit:** Yes
- **Encryption at Rest:** Yes (AES-256-GCM local cryptographic container)
- **User Can Request Data Deletion:** Yes (Local deletion removes files and cryptographic keys permanently)
- **Offline-First:** Yes

---

## 2. Data Types & Handling

### User Content (Photos, Videos, Audio, Files, Docs, Notes, Clipboard)
- **Collected:** No
- **Shared:** No
- **Details:** All user content is encrypted and stored strictly on-device or in user-designated local storage via Android Storage Access Framework (SAF). Zero-knowledge design ensures no user content is ever transmitted to developer servers.

### Personal Identifiers (Name, Email, User ID, Phone Number, Address)
- **Collected:** No
- **Shared:** No

### Financial Information
- **Payment Info:** Not collected by Kronware.
- **Purchase History:** Processed securely and directly by Google Play In-App Billing.

---

## 3. Advertising & Analytics (Free Tier Only)
- **Provider:** Google AdMob (Google Mobile Ads SDK)
- **Purpose:** App functionality and advertising for free-tier users.
- **Pro Tier:** 100% ad-free with all ad SDK activity disabled.

---

## 4. Security & Privacy Practices
- **Encryption Standard:** Authenticated AES-256-GCM encryption with cryptographic envelope protection.
- **Ephemeral Key Storage:** Master encryption keys reside in volatile memory (RAM) only while the vault is actively unsealed.
- **Biometric Authentication:** Optional hardware-backed biometric unlock via Android Keystore and BiometricPrompt.
- **Screenshot & App Switcher Protection:** Configurable `FLAG_SECURE` window protection.
- **Metadata Purifier:** Optional stripping of EXIF, GPS location, and camera metadata on exports.
- **Outbound Sandbox:** Configurable restrictions on external app sharing destinations.
- **Stealth Disguise & Break-In Alerts:** Local tamper and failed-access tracking for Pro users.
