# Data Safety — Vidlr

This page supports the Google Play Data Safety declaration for the Vidlr app.

---

## Data collected and shared

| Data type | Collected | Shared with third parties | Purpose |
|---|---|---|---|
| App settings (download path, resolution preference, home URL, tab persistence) | Stored on-device only | No | App functionality |
| Browser cookies and cache | Stored on-device only | No | Web browsing session; clearable by user |
| Clipboard URL (read once, immediately cleared) | Read transiently, not stored | No | Offer to open copied URLs in browser |
| Downloaded video files | Saved to device storage chosen by you | No | App functionality |
| Device and account identifiers (via AdMob, free version only) | Yes — by Google Mobile Ads SDK | Yes — to Google and ad partners | Advertising, analytics, fraud prevention |
| Personal info (email address / phone number, if associated with account identifiers used by Google ads systems) | May be processed by Google Mobile Ads SDK | Yes — by Google and ad partners | Advertising, analytics, fraud prevention |

---

## Data handling summary

- **The app itself does not request account sign-in or directly collect profile fields** such as name, email, or phone number
- **Settings and session data are local only** — stored on-device, never uploaded to any server
- **Browser data** (cookies, cache, web storage) is stored locally and can be fully cleared from Settings at any time
- **Clipboard** is read only when the app gains focus and a URL is present; the content is cleared immediately and never stored or transmitted
- **Downloaded files** are saved directly to the folder you choose on your device and are not uploaded or shared by the app
- **Advertising** is shown only in the free version and is handled by Google AdMob (Google Mobile Ads SDK). The SDK may collect and share data such as IP address, app interactions, diagnostic data, device identifiers, and account-linked identifiers as described by Google. See [Google's Privacy Policy](https://policies.google.com/privacy) for full details. Pro users see no ads.

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
| `WAKE_LOCK` | Preventing the CPU from sleeping during active downloads to ensure file integrity |

---

## User controls

- **Download folder**: Can be changed at any time in Settings
- **Wi-Fi only downloads**: Can be toggled in Settings to prevent downloads over mobile data
- **Clear browser data**: Cookies, cache, and web storage can be fully cleared from Settings
- **Desktop mode**: Each browser tab can be switched between mobile and desktop user-agent independently
- **Tab limit**: Free users can open up to 2 browser tabs; Pro users have no limit
- **Ad personalisation**: Can be adjusted in your device's Google settings → Ads

---

## Security

All on-device data is stored within the Android application sandbox. Downloaded files are written to a user-selected folder in external storage. No data is transmitted to servers operated by this app.
