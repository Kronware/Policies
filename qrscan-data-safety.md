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
