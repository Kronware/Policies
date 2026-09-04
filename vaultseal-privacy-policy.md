# Privacy Policy for VaultSeal

**Effective Date:** August 30, 2026  
**Last Updated:** September 4, 2026  
**Publisher:** Kronware (kronware.io)

VaultSeal ("we", "our", or "us") is dedicated to protecting user privacy and ensuring full control over personal data. This Privacy Policy explains how VaultSeal handles information.

---

## 1. Core Principle: Zero-Knowledge & Offline-First

VaultSeal is an offline-first, local encrypted vault application for Android. 
- **No Cloud Sync:** Your encrypted vaults, media, documents, and notes are stored strictly on your device or in user-designated local storage via Android Storage Access Framework (SAF).
- **No Accounts or Logins:** You do not need to register an account, provide an email address, or create a remote identity to use VaultSeal.
- **Zero-Knowledge Encryption:** All content is encrypted client-side using industry-standard AES-256-GCM cryptography. We do not have access to your passphrases, master encryption keys, or decrypted data.

---

## 2. Information We Collect and Process

### A. Vault Data & Files
- **Storage:** All photos, videos, audio, notes, and files ingested into VaultSeal remain encrypted on your device.
- **Ingest & Sealed Operations:** When sharing items into VaultSeal while sealed, content is encrypted using one-way public key cryptography directly into local vault storage without decrypting existing data.

### B. Device & Session Privacy Features
- **Screenshot Protection:** VaultSeal enables Android's `FLAG_SECURE` by default to prevent unauthorized screenshots and obscure application contents in the Android app switcher / recents menu. Users can toggle this setting in Privacy Settings.
- **Metadata Purifier:** Optional feature that strips EXIF, GPS location tags, device signatures, and camera metadata from images before exporting or sharing.
- **Clipboard Sentinel:** Users can ingest clipboard contents into encrypted storage with optional automated clearing of the system clipboard to prevent third-party app snooping.

### C. Advertisements (Free Tier Only)
- For non-Pro users, VaultSeal may display non-intrusive banner ads provided by Google AdMob. AdMob may collect device identifiers and standard advertising metrics in compliance with Google Play Developer Policies and Privacy Guidelines.
- Pro users receive a completely ad-free experience.

### D. In-App Purchases & Billing
- VaultSeal offers optional Pro upgrades processed securely and directly through the Google Play In-App Billing system. We do not process, store, or receive your payment card credentials or personal billing details.

---

## 3. Data Sharing and Third Parties

We do not sell, rent, trade, or share your personal data with third parties. Content never leaves your device unless you explicitly initiate an export or share action to an external app through the Android system share sheet.

---

## 4. Data Retention and Deletion

- Because all data is stored locally on your device, you have complete control over data retention.
- Deleting items, deleting vaults, or clearing application storage permanently deletes the associated cryptographic keys and encrypted files.
- If you lose your passphrase and do not have a configured backup/biometric key, data recovery is mathematically impossible.

---

## 5. Security

VaultSeal incorporates defense-in-depth security mechanisms:
- Authenticated AES-GCM encryption with cryptographic envelope protection.
- Hardware-backed Android Keystore and BiometricPrompt integration (optional biometric unlock).
- Ephemeral in-memory key management (keys are zeroed upon vault seal or idle auto-seal timeout).

---

## 6. Contact Us

If you have questions, feedback, or concerns regarding this Privacy Policy or VaultSeal's security architecture, please contact us at:

- **Website:** [https://kronware.io](https://kronware.io)
- **Email:** support@kronware.io
