# Data Safety — Vidlr

This page supports the Google Play Data Safety declaration for the Vidlr app.

Current builds use Start.io; older active releases use Google AdMob. Disclosures
must cover all active releases, not just the latest Internal testing build.

---

## Data collected and shared

| Data type | Collected | Shared with third parties | Purpose |
|---|---|---|---|
| App settings (download path, resolution preference, home URL, tab persistence) | Stored on-device only | No | App functionality |
| Browser cookies and cache | Stored on-device only | No | Web browsing session; clearable by user |
| Clipboard URL (read once, immediately cleared) | Read transiently, not stored | No | Offer to open copied URLs in browser |
| Downloaded video files | Saved to device storage chosen by you | No | App functionality |
| Approximate location/IP address (Start.io, free version only) | Yes | Yes - to Start.io and advertising partners | Advertising, measurement, fraud prevention |
| Device or other identifiers (Start.io advertising ID, where available) | Yes | Yes - to Start.io and advertising/measurement partners | Advertising, measurement, fraud prevention |
| App interactions (Start.io ad views/clicks, free version only) | Yes | Yes - to Start.io and advertising/measurement partners | Advertising, measurement |
| Installed apps (Start.io queries, where available and permitted) | May be collected | May be used in shared advertising profiles | Advertising |
| Diagnostics and crash logs (Start.io SDK) | Yes | Not shared onward according to Start.io's SDK disclosure | SDK analytics and reliability |
| Approximate location (derived from network signals via AdMob, free version only) | May be collected by Google Mobile Ads SDK | Yes — to Google and ad partners | Advertising, analytics |
| App interactions (ad views/clicks/session interaction via AdMob, free version only) | Yes — by Google Mobile Ads SDK | Yes — to Google and ad partners | Advertising, analytics |
| Diagnostics (app/SDK performance via AdMob, free version only) | Yes — by Google Mobile Ads SDK | Yes — to Google and ad partners | Analytics, fraud prevention |
| Device and account identifiers (via AdMob, free version only) | Yes — by Google Mobile Ads SDK | Yes — to Google and ad partners | Advertising, analytics, fraud prevention |
| Personal info (email address / phone number, if associated with account identifiers used by Google ads systems) | May be processed by Google Mobile Ads SDK | Yes — by Google and ad partners | Advertising, analytics, fraud prevention |

---

## Data handling summary

- **The app itself does not request account sign-in or directly collect profile fields** such as name, email, or phone number
- **Settings and session data are local only** — stored on-device, never uploaded to any server
- **Browser data** (cookies, cache, web storage) is stored locally and can be fully cleared from Settings at any time
- **Clipboard** is read only when the app gains focus and a URL is present; the content is cleared immediately and never stored or transmitted
- **Downloaded files** are saved directly to the folder you choose on your device and are not uploaded or shared by the app
- **Advertising** is shown only in the free version. Current builds use Start.io with its built-in disclosure/consent feature enabled. See [Start.io's Privacy Policy](https://www.start.io/policy/privacy-policy/) and [Android SDK data disclosure](https://support.start.io/hc/en-us/articles/4413793394962-Google-Play-Safety-Section-Data-Disclosure). No precise-location or Bluetooth permissions are requested for advertising. Test-ad mode does not imply zero SDK data collection. Pro users see no ads.
- **Older releases** use Google AdMob (Google Mobile Ads SDK), subject to [Google's Privacy Policy](https://policies.google.com/privacy). Keep the Google-specific categories below while those releases remain active.

### Google Mobile Ads SDK categories for older active releases

When ads are enabled (free version), the app's Play Data safety declaration includes data categories that may be collected/shared by Google Mobile Ads SDK:

- Personal info: Email address, Phone number (when associated with account-linked identifiers in Google ads systems)
- Location: Approximate location
- Identifiers: Device or other identifiers
- App activity: App interactions
- App info and performance: Diagnostics

---

## Permissions used

| Permission | Why it is needed |
|---|---|
| `INTERNET` | Loading web pages in the built-in browser; detecting video stream URLs; loading advertisements via Start.io (AdMob in older releases) |
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
- **Ad personalisation**: Use Android's advertising-ID controls and [Start.io's opt-out rights](https://www.start.io/policy/privacy-policy/); older AdMob releases use Google's advertising controls

---

## Security

All on-device data is stored within the Android application sandbox. Downloaded files are written to a user-selected folder in external storage. No data is transmitted to servers operated by this app.
