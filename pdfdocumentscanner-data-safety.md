# Data Safety — PDF Document Scanner

This page supports the Google Play Data Safety declaration for the PDF Document Scanner app.

---

## Data collected and shared

| Data type | Collected | Shared with third parties | Purpose |
|---|---|---|---|
| Camera data | Processed on-device only | No | Capturing document images |
| Document images (JPEG) | Stored on-device in app private storage only | No | App functionality |
| Exported PDFs | Stored on-device (private storage or Downloads) | No | App functionality |
| Document metadata (name, date, page count) | Stored on-device in JSON catalog only | No | App functionality |
| Device identifiers (via AdMob) | Yes — by Google AdMob SDK (free version only; no ads for Pro users) | Yes — to Google for ads | Advertising |
| Purchase status (`pro_upgrade`) | Verified against Google Play Billing (not stored locally beyond session) | No | Unlocking Pro features |
| Payment / billing data | Not collected by this app — handled entirely by Google Play | Yes — to Google by Google Play | In-app purchase processing |

---

## Data handling summary

- **No personal data** (name, email, location, contacts) is ever collected by this app
- **Document data is local only** — images and PDFs are stored in the app's private internal storage and are never uploaded
- **Camera access** is processed entirely on-device by CameraX (Android Jetpack library)
- **All image processing** (edge detection, perspective correction, PDF rendering) is done locally using pure Kotlin — no cloud service or ML API is involved
- **Advertising** is handled by Google AdMob (free version only). The AdMob SDK may collect device advertising IDs for ad personalisation. Pro users have no ads loaded or displayed. See [Google's Privacy Policy](https://policies.google.com/privacy) for full details.
- **Pro upgrade** is a one-time in-app purchase processed by Google Play. The App queries Google Play Billing to check purchase status. No payment data ever passes through app code.
- **Cleartext (HTTP) traffic is blocked** at the OS level via the app's network security configuration — all external connections use HTTPS only.

---

## Permissions used

| Permission | Why it is needed |
|---|---|
| `CAMERA` | Capturing document images via the live viewfinder |
| `com.android.vending.BILLING` | Enabling the Google Play in-app purchase flow for the Pro upgrade |

No storage permissions are requested. Scoped storage (Android 10+) covers all app-internal file access. The system MediaStore API is used for Downloads without requiring a permission.

No `INTERNET` permission is declared in the current version. Future versions adding AdMob will include `android.permission.INTERNET` with an explicit justification comment at that time.

---

## User controls

- **Delete documents**: Individual documents or all data can be deleted from the main screen
- **Export location**: Documents can be saved to the app's private storage or exported to Downloads
- **Ad personalisation**: Can be adjusted in your device's Google settings → Ads (only relevant for free version users)
- **Pro upgrade**: A one-time purchase that permanently removes all advertising. Purchase can be restored on a new device through Google Play's standard purchase restoration.

---

## Security

All on-device data is stored in the Android application sandbox (private internal storage). Exported PDFs written to Downloads are accessible to the user via the file manager. No data is transmitted to external servers by the app's own code. Cleartext HTTP traffic is explicitly blocked via `network_security_config.xml`.
