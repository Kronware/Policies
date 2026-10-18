# Data Safety — BlurCut - Video Censor Editor

This page supports the Google Play Data Safety declaration for the BlurCut app.

**Last updated: October 18, 2026**

BlurCut collects and shares some data through Google SDKs. Answer **Yes** to the Play Data Safety question about collection or sharing. Video editing and AI media processing remain on-device.

---

## Data collected and shared

| Data type | Collected | Shared with third parties | Purpose |
|---|---|---|---|
| Videos / media files | Processed on-device only | No | Video editing and export |
| Face detection data | Processed on-device only (ML Kit + optional Post AI Analysis refinement) | No | Automatic face censoring and analysis refinement |
| Subject segmentation masks | Processed on-device only | No | Background Censoring foreground selection and background effects |
| Tracking cache data | Stored on-device only | No | Reusing analysis for faster repeat exports |
| Project settings | Stored on-device only | No | Saving edit state between sessions |
| Approximate location (IP-derived) | Yes | Yes, through AdMob | Advertising, analytics, fraud prevention, security, and compliance |
| App interactions | Yes | Yes, through AdMob | Advertising, analytics, fraud prevention, security, and compliance |
| Diagnostics | Yes | Yes, through AdMob | Advertising, analytics, fraud prevention, security, and compliance; SDK reliability |
| Device or other IDs | Yes | Yes, through AdMob | Advertising, analytics, fraud prevention, security, and compliance; installation identification |
| Crash logs | Yes, through Firebase Crashlytics | Generally service-provider processing, not sharing under Play's exception | Analytics and reliability analysis |
| Purchase history | Yes, through Firebase Analytics | Generally service-provider processing, not sharing under Play's exception | Purchase analytics |

Firebase-only sharing answers depend on the actual Analytics data-sharing settings, advertising integrations, and other enabled service features. Review those settings before submitting the form. SDK transmissions are not declared ephemeral. Automatic SDK collection has no general in-app opt-out. Purchase-event collection applies to users who make purchases.

---

## Data handling summary

- **Google SDK collection is included**: AdMob, Firebase Analytics, Crashlytics, and supporting services transmit identifiers, usage information, and diagnostics. Approximate location can be derived from IP addresses; the App does not request GPS location
- **Videos are never uploaded** — all editing and AI processing happens entirely on your device
- **Selected-file access only**: Android's system document picker grants access to the videos you choose. The App retains read access for reopening projects without requesting `READ_MEDIA_IMAGES` or `READ_MEDIA_VIDEO`
- **Face detection, Post AI Analysis, and background subject segmentation are on-device only** — all frames, masks, and analysis results stay on your device
- **Tracking cache is local only** — per-project analysis cache is stored in app-private storage for export reuse
- **Advertising and analytics**: the free version displays AdMob ads; Pro removes displayed ads, not all SDK data collection
- **ML Kit media stays local**: SDK usage and diagnostic metadata may still be transmitted to Google
- **Purchases**: Google Play Billing handles Pro purchases and subscriptions; Firebase Analytics may record purchase events. The App does not receive payment card details
- **No account creation or sign-in**: Google Play purchases do not create an account in BlurCut

---

## Permissions used

| Permission | Why it is needed |
|---|---|
| `INTERNET` and `ACCESS_NETWORK_STATE` (included through SDKs) | Connecting to Google advertising, analytics, diagnostics, and purchase services |
| `com.google.android.gms.permission.AD_ID` | Advertising ID access by Google SDKs where available and permitted |
| `FOREGROUND_SERVICE` + `FOREGROUND_SERVICE_DATA_SYNC` | Running long media operations (tracking analysis, preview baking, export) as user-visible foreground work so jobs complete reliably |
| `POST_NOTIFICATIONS` | Showing export progress and completion notifications |
| `WAKE_LOCK` | Keeping the device awake during long-running processing (export, tracking analysis) so jobs complete reliably |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Requesting exemption from battery optimization for reliable completion of user-initiated export and analysis jobs |

---

## User controls

- **Project data**: App-private device data can be cleared from Android Settings or by uninstalling. Android backup and restore may retain or restore data according to device settings
- **Exported videos**: Saved to your gallery — can be deleted like any other video
- **Advertising identifiers**: Android provides advertising ID reset or deletion controls where supported; these do not stop all SDK collection
- **Uploaded SDK data**: Clearing storage or uninstalling does not delete data already sent to Google. The App has no dedicated uploaded-data deletion request mechanism or general analytics/crash-reporting opt-out. Do not claim deletion within 90 days

---

## Security

Local app-private data is stored in Android's application sandbox. AdMob and Firebase encrypt SDK data in transit using TLS/HTTPS. Videos, frames, masks, and tracking results are not uploaded by the editing pipeline.

---

## Accounts and Additional Disclosures

- Select **My app does not allow users to create an account**; the App does not support external-account sign-in either
- Declare **Contains ads: Yes** and **Advertising ID usage: Yes** in the applicable Play Console sections
- Accessing local media for editing does not itself constitute off-device collection for Data Safety
- The declaration must cover applicable distributed versions and enabled Google service settings, not just one user's Pro status or privacy choices

## References

- [Privacy policy](blurcut-privacy-policy.md)
- [Google Mobile Ads SDK data disclosure](https://developers.google.com/admob/android/privacy/play-data-disclosure)
- [Firebase data disclosure](https://firebase.google.com/docs/android/play-data-disclosure)
- [Google Analytics data disclosure](https://support.google.com/analytics/answer/11582702)
