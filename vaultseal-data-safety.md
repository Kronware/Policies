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
- **Offline-First:** Yes. Optional LAN sync uses direct, user-authorized local-network connections only.

---

## 2. Data Types & Handling

### User Content (Photos, Videos, Audio, Files, Docs, Notes, Clipboard)
- **Collected:** No
- **Shared:** No
- **Details:** All user content is encrypted and stored strictly on-device or in user-designated local storage via Android Storage Access Framework (SAF). Optional LAN sync can transfer encrypted manifests and encrypted item payloads directly to a paired VaultSeal peer on the same local network. No user content is transmitted to developer servers.

### Local Network Sync
- **Purpose:** Explicitly authorized peer-to-peer synchronization with VaultSeal PC or another paired companion device.
- **Network data:** Device name, local network address, certificate fingerprint, encrypted vault manifests, and encrypted item payloads may be exchanged between paired devices.
- **Authorization:** Pairing requires user confirmation of a six-digit PIN. Trusted peers are stored locally and can be removed by the user.
- **Third parties:** No Kronware relay, cloud storage, analytics service, or other third party receives LAN sync data.

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
