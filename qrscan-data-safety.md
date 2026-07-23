# Data Safety — QR Scanner

This page supports the Google Play Data Safety declaration for the QR Scanner app.

---

## Data collected and shared

| Data type | Collected | Shared with third parties | Purpose |
|---|---|---|---|
| Camera data | Processed on-device only | No | QR code scanning |
| Photos / images | Processed on-device only (only when you choose "Scan from Image") | No | QR code scanning |
| Scan history (QR content + timestamp) | Stored on-device only | No | App functionality |
| Device identifiers (via AdMob) | Yes — by Google AdMob SDK (free version only; no ads loaded for Pro users) | Yes — to Google for ads | Advertising |
| Purchase status (`pro_upgrade`) | Cached on-device only (boolean flag in SharedPreferences) | No | Unlocking Pro features |
| Payment / billing data | Not collected by this app — handled entirely by Google Play | Yes — to Google by Google Play | In-app purchase processing |

---

## Data handling summary

- **No personal data** (name, email, location, contacts) is ever collected by this app
- **Scan history is local only** — stored in an on-device database, never uploaded
- **Camera and image access** is processed entirely on-device by ML Kit (Google's on-device barcode scanning library)
- **Advertising** is handled by Google AdMob (free version only). The AdMob SDK may collect device advertising IDs for ad personalisation. Pro users have no ads loaded or displayed. See [Google's Privacy Policy](https://policies.google.com/privacy) for full details.
- **Pro upgrade** is a one-time in-app purchase processed by Google Play. The App stores only a boolean on-device to remember the unlocked state. No payment data ever passes through app code.

---

## Onward transfer and recipient chain

- **App-level onward transfer intent**: This app does **not** perform onward transfers of user data.
- **Estimated further recipients by this app**: **0** (no app-operated servers, brokers, or downstream processors).
- **Estimated processing chain length by this app**: **0 hops** beyond on-device processing for scan history, camera data, and image scanning.
- **Third-party ecosystem note**: Where the free version uses Google AdMob, or purchases are handled by Google Play, any further processing is governed by Google's own privacy terms and infrastructure rather than by this app's own transfer pipeline.

---

## Safeguards against interception or disproportionate public-authority access

The following measures describe safeguards implemented by the Company for data handled by this app:

- **Contractual measures**: The app's policy commits to local-only processing for scan history, camera data, and image scanning. For third-party services used by the free and purchase flows (Google AdMob and Google Play Billing), processing is governed by Google's contractual and policy framework rather than by company-operated processing infrastructure.
- **Technical measures**: The Company does not operate app servers for user scan data and does not transmit scan history, camera frames, or selected images to company systems. On-device data is protected by Android app sandboxing. Because the app has no company-run transfer pipeline for this data, there is no company-controlled network path where interception risk is introduced for those data categories.
- **Organisational measures**: Data minimisation is enforced by design (local storage only for scan history, no account system, no direct collection of name/email/location/contacts). Access to user scan data by Company personnel is not part of operations because the data remains on device and is not ingested into company systems.
- **Scope clarification**: For AdMob and Google Play Billing processing, safeguards against interception or public-authority access are provided under Google's infrastructure and legal framework; those controls are outside the Company's direct operational control.

---

## Permissions used

| Permission | Why it is needed |
|---|---|
| `CAMERA` | Scanning QR codes via the live camera viewfinder |
| `INTERNET` | Loading advertisements via AdMob (free version); opening scanned URLs in a browser |
| `com.android.vending.BILLING` | Enabling the Google Play in-app purchase flow for the Pro upgrade |
| Photo / image access (no explicit permission) | The system content picker grants one-time access to the image you select for "Scan from Image" — the App never holds a blanket media permission |

---

## User controls

- **Delete scan history**: Individual entries or all history can be deleted from the History screen
- **Ad personalisation**: Can be adjusted in your device's Google settings → Ads (only relevant for free version users)
- **Pro upgrade**: A one-time purchase that permanently removes all advertising. The purchase can be restored on a new device through Google Play's standard purchase restoration.

---

## Security

All on-device data is stored in a standard Android SQLite database protected by the Android system's application sandbox. No data is transmitted to external servers by this app.
