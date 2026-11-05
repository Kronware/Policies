# Privacy Policy for VaultSeal

**Effective Date:** August 30, 2026  
**Last Updated:** November 5, 2026  
**Publisher:** Kronware (kronware.io)

VaultSeal ("we", "our", or "us") is dedicated to protecting user privacy and ensuring full control over personal data. This Privacy Policy explains how VaultSeal handles information.

---

## 1. Core Principle: Zero-Knowledge & Offline-First

VaultSeal is an offline-first, local encrypted vault application for Android. 
- **No Cloud Sync:** Your encrypted vaults, media, documents, and notes are stored strictly on your device or in user-designated local storage via Android Storage Access Framework (SAF). VaultSeal does support optional, user-authorized peer-to-peer LAN sync with a paired VaultSeal PC or companion device; this uses the local network only and does not route data through Kronware or a cloud service.
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

### C. Android Device Permissions
To provide secure vault storage, encryption, and import capabilities, VaultSeal may request the following permissions:
- **Photos, Media & Files (no broad media or storage permission):** VaultSeal does not request permission to read your photo, video, audio, or file library. Items are imported only when you select them with the Android system file picker or share them to VaultSeal from another app, which grants access solely to the items you choose. Vault and backup folders are accessed only through locations you select via the Android Storage Access Framework. Imported files are encrypted locally and are not sent to developer servers. If you explicitly enable LAN sync, encrypted vault items may be transferred to a paired local peer.
- **Local Network Sync:** When you enable LAN sync, VaultSeal discovers nearby VaultSeal peers on the local network and may exchange device names, local network addresses, certificate fingerprints, encrypted vault manifests, and encrypted item payloads with a peer you authorize. Pairing requires an explicit six-digit PIN confirmation. This data is exchanged directly between the paired devices and is not sent to Kronware servers.
- **Camera (`CAMERA`):** Required only if you use the optional in-app secure camera to capture photos or videos directly into encrypted vault storage.
- **Notifications & Background Processing (`POST_NOTIFICATIONS`, `FOREGROUND_SERVICE_DATA_SYNC`):** Used to display real-time progress notifications when importing or encrypting large files and containers in the background.

### D. Advertisements (Free Tier Only)
- For non-Pro users, VaultSeal may display non-intrusive banner ads provided by Google AdMob. AdMob may collect device identifiers and standard advertising metrics in compliance with Google Play Developer Policies and Privacy Guidelines.
- Pro users receive a completely ad-free experience.

### E. In-App Purchases & Billing
- VaultSeal offers optional Pro upgrades processed securely and directly through the Google Play In-App Billing system. We do not process, store, or receive your payment card credentials or personal billing details.

---

## 3. Data Sharing and Third Parties

We do not sell, rent, trade, or share your personal data with third parties. Content never leaves your device unless you explicitly initiate an export/share action or authorize LAN sync with a paired local peer. LAN sync is direct device-to-device communication and does not use a Kronware relay or cloud service.

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
