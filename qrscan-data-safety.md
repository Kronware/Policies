# Data Safety — QR Scanner

This page supports the Google Play Data Safety declaration for the QR Scanner app.

---

## Data collected and shared

| Data type | Collected | Shared with third parties | Purpose |
|---|---|---|---|
| Camera data | Processed on-device only | No | QR code scanning |
| Photos / images | Processed on-device only (only when you choose "Scan from Image") | No | QR code scanning |
| Scan history (QR content + timestamp) | Stored on-device only | No | App functionality |
| Device identifiers (via AdMob) | Yes — by Google AdMob SDK | Yes — to Google for ads | Advertising |

---

## Data handling summary

- **No personal data** (name, email, location, contacts) is ever collected by this app
- **Scan history is local only** — stored in an on-device database, never uploaded
- **Camera and image access** is processed entirely on-device by ML Kit (Google's on-device barcode scanning library)
- **Advertising** is handled by Google AdMob. The AdMob SDK may collect device advertising IDs for ad personalisation. See [Google's Privacy Policy](https://policies.google.com/privacy) for full details.

---

## Permissions used

| Permission | Why it is needed |
|---|---|
| `CAMERA` | Scanning QR codes via the live camera viewfinder |
| `INTERNET` | Loading advertisements via AdMob; opening scanned URLs in a browser |
| `READ_MEDIA_IMAGES` (granted by system photo picker — no explicit permission request) | Selecting an image from your gallery to scan |

---

## User controls

- **Delete scan history**: Individual entries or all history can be deleted from the History screen
- **Ad personalisation**: Can be adjusted in your device's Google settings → Ads

---

## Security

All on-device data is stored in a standard Android SQLite database protected by the Android system's application sandbox. No data is transmitted to external servers by this app.
