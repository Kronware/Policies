# Data Safety — Vidlr

This page supports the Google Play Data Safety declaration for the Vidlr app.

---

## Data collected and shared

| Data type | Collected | Shared with third parties | Purpose |
|---|---|---|---|
| App settings (download path, resolution preference, home URL) | Stored on-device only | No | App functionality |
| Last visited URL (optional, only if "Open last page" is enabled) | Stored on-device only | No | Session restore |
| Downloaded video files | Saved to device storage chosen by you | No | App functionality |
| Device identifiers (via AdMob) | Yes — by Google AdMob SDK | Yes — to Google for ads | Advertising |

---

## Data handling summary

- **No personal data** (name, email, location, contacts) is ever collected by this app
- **Settings and session data are local only** — stored on-device, never uploaded to any server
- **Downloaded files** are saved directly to the folder you choose on your device and are not uploaded or shared by the app
- **Advertising** is handled by Google AdMob. The AdMob SDK may collect device advertising IDs for ad personalisation. See [Google's Privacy Policy](https://policies.google.com/privacy) for full details.

---

## Permissions used

| Permission | Why it is needed |
|---|---|
| `INTERNET` | Loading web pages in the built-in browser; detecting video stream URLs; loading advertisements via AdMob |
| `ACCESS_NETWORK_STATE` | Checking network connectivity to enforce the Wi-Fi-only download setting |
| `FOREGROUND_SERVICE` | Running the download service in the background so downloads continue while the app is not in focus |
| `FOREGROUND_SERVICE_DATA_SYNC` | Required foreground service type for background file download operations |
| `POST_NOTIFICATIONS` | Displaying download progress notifications (Android 13+) |
| `WRITE_EXTERNAL_STORAGE` (Android 9 and below only) | Writing downloaded files to external storage on older Android versions |
| `READ_MEDIA_VIDEO` | Reading video files in the download folder on Android 13+ |
| `WAKE_LOCK` | Preventing the CPU from sleeping during active downloads to ensure file integrity |

---

## User controls

- **Download folder**: Can be changed at any time in Settings
- **Wi-Fi only downloads**: Can be toggled in Settings to prevent downloads over mobile data
- **Session restore**: The "Open last page" setting can be disabled so no URL is remembered between sessions
- **Ad personalisation**: Can be adjusted in your device's Google settings → Ads

---

## Security

All on-device data is stored within the Android application sandbox. Downloaded files are written to a user-selected folder in external storage. No data is transmitted to servers operated by this app.
