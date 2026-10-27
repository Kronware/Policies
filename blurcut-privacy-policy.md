# Privacy Policy — BlurCut - Video Censor Editor

**Last updated: October 27, 2026**

This Privacy Policy explains how the BlurCut app ("the App") handles your information.

---

## Information We Collect

### Videos and media
You grant the App access to videos on your device in order to import and edit them. Videos are processed entirely **on your device** and are never transmitted to any server or third party.

Video import uses Android's system document picker. Access is limited to the files you select, and read access can be retained to reopen projects. The App does not request broad photo or video library permissions (`READ_MEDIA_IMAGES` or `READ_MEDIA_VIDEO`).

Edited videos are exported to your device's media gallery only when you explicitly tap the export button.

### On-device AI processing (face detection, analysis refinement, and background segmentation)
BlurCut's automatic face censoring feature uses **Google ML Kit** for baseline face detection and an optional **Post AI Analysis** refinement pass to augment detections and improve continuity in difficult sections. Background Censoring uses on-device subject segmentation to preserve selected foreground silhouettes while blurring or pixelating the surrounding background. All of this processing runs entirely on-device. No video frames, segmentation masks, face data, or detection results are ever sent to any server.

### Project data
Project settings (effects, censor settings, overlays, trim points) are stored **locally on your device** in the app's private storage. This data is never transmitted.

### Tracking cache data
When you run tracking analysis or Background Censoring, BlurCut stores a per-project tracking cache locally in app-private storage. This cache contains timestamped detection regions, segmentation masks, and validation metadata (for example source/trim key and tracking analysis settings) so repeat exports can skip redundant analysis. When optional Post AI Analysis is enabled, the cached tracking data may also include on-device refinement results derived from the same video segment. This cache never leaves your device.

### Camera
The App does not request camera access.

### Advertising
The free version uses **Start.io** to display banner and full-page advertisements. Start.io collects and shares IP addresses (which can be used to estimate approximate location) and device identifiers such as the Android advertising ID where available and permitted, and processes ad interactions and SDK diagnostic/crash information. Start.io's SDK can collect installed-app information when the advertising ID is applicable. This information supports advertising, measurement, and SDK reliability. BlurCut does not request GPS location or Bluetooth permissions or supply video content to Start.io. Start.io's built-in advertising disclosure and consent experience remains enabled; applicable choices and regional availability depend on the advertising service. Pro removes displayed advertisements; it does not provide a general opt-out from analytics or crash reporting. Older distributed versions use Google AdMob instead of Start.io.

### Analytics
The App includes **Google Analytics for Firebase**, which automatically collects app-instance identifiers, advertising identifiers where available, approximate location derived from IP addresses, and app usage information such as sessions and screen views. It can also collect in-app purchase and subscription events, including product identifiers and prices. This information is used to understand app usage and improve the App. Advertising-related use also depends on the applicable Google service settings and your privacy choices.

### Crash reporting and diagnostics
The App uses **Firebase Crashlytics** to report crashes and non-fatal errors. Reports can include stack traces, device and operating system information, app state, installation identifiers, session information, and diagnostic logs or custom context associated with a failure. Analytics events may provide breadcrumbs for crash diagnosis. These services help identify reliability issues and improve the App; they are not used to upload video frames or tracking masks.

### Purchases and accounts
Pro purchases and subscriptions are handled by **Google Play Billing**. The App receives purchase status and product information to enable and restore Pro features. Google handles payment processing; the App does not receive your payment card details. Purchase events may also be recorded by Firebase Analytics as described above. The App does not offer account creation or sign-in.

---

## Information We Do NOT Collect

- We do not ask you to create an account or provide your name or email address to use the editor
- We do not transmit any video, audio, or image data to any server
- We do not request precise or GPS location; advertising and Google services may derive approximate location from IP addresses
- We do not access your contacts or payment card details

These statements do not exclude the SDK identifiers, usage information, and diagnostics described above.

---

## Third-Party Libraries

BlurCut uses on-device media libraries and network-connected Start.io and Google services:

| Library | Purpose | Data leaves device? |
|---|---|---|
| Google ML Kit (Face Detection) | Baseline face detection for auto-censor and Post AI Analysis refinement inputs | No input frames or detection results; SDK usage and diagnostic metadata may be sent to Google |
| Google ML Kit (Selfie Segmentation) | Foreground subject masks for Background Censoring | No input frames or masks; SDK usage and diagnostic metadata may be sent to Google |
| AndroidX Media3 / ExoPlayer | Video playback during editing | No |
| AndroidX Media3 Transformer | Video export and effect rendering | No |
| Start.io | Advertising, measurement, and SDK reliability | Yes: identifiers, IP-derived approximate location, ad interactions, installed-app information where applicable, and diagnostics |
| Google Analytics for Firebase | Usage and purchase analytics | Yes: identifiers, approximate location, usage and purchase events |
| Firebase Crashlytics and supporting Firebase services | Crash reporting and reliability analysis | Yes: crash reports, installation identifiers, session and diagnostic information |
| Google Play Billing | Pro purchases, subscriptions, and entitlement restoration | Yes: purchase-related communications with Google Play |

Start.io and Google process data under their respective terms and privacy policies. Firebase services generally process data on the developer's behalf; Start.io collects and shares data for advertising purposes. Additional processing depends on service configuration and applicable privacy settings. Older AdMob-based versions remain subject to Google's advertising disclosures.

- [Google Privacy Policy](https://policies.google.com/privacy)
- [Start.io Privacy Policy](https://www.start.io/policy/privacy-policy/)
- [Start.io data disclosures](https://support.start.io/hc/en-us/articles/4413793394962)
- [How Google uses information from apps that use its services](https://policies.google.com/technologies/partner-sites)
- [AdMob data disclosures](https://developers.google.com/admob/android/privacy/play-data-disclosure)
- [Firebase data disclosures](https://firebase.google.com/docs/android/play-data-disclosure)
- [Google Analytics data disclosures](https://support.google.com/analytics/answer/11582702)

---

## Data Retention

Project and tracking data is stored locally in the app's private storage. You can clear that storage through Android Settings. Uninstalling removes app-private data on the device, but exported videos remain in your gallery until you delete them. Android system backup and restore may retain or restore app data according to your device settings.

Advertising, analytics, purchase, and crash-reporting data is handled by Start.io and the respective Google services under their retention policies and applicable service settings. Clearing app storage or uninstalling does not delete data already transmitted to those services. We do not promise that all such data is deleted within 90 days.

The App currently has no dedicated in-app request mechanism for deleting uploaded SDK data. For privacy questions, contact the developer through the support email on the Google Play listing. Start.io and Google also provide privacy information and controls through their services where applicable.

## Security and Privacy Controls

Advertising and Firebase services use network connections to transmit SDK data. Firebase encrypts its SDK transmissions in transit using TLS/HTTPS; Start.io's handling is described in its privacy disclosures. This does not mean data is end-to-end encrypted. Local app-private data is protected by Android's application sandbox.

You can reset or delete your advertising ID through Android's advertising privacy settings where supported. This limits use of that identifier but does not stop all advertising, analytics, or diagnostic collection. The App currently does not provide a general analytics or crash-reporting opt-out.

---

## Permissions Used

| Permission | Why it is needed |
|---|---|
| `INTERNET` and `ACCESS_NETWORK_STATE` (included through SDKs) | Connecting to advertising, analytics, crash-reporting, and purchase services |
| `com.google.android.gms.permission.AD_ID` | Allowing advertising and Google SDKs to access the advertising ID where available and permitted |
| `ACCESS_WIFI_STATE` (included through Start.io) | Network/Wi-Fi state used by the advertising SDK; does not grant GPS access |
| `RECEIVE_BOOT_COMPLETED` (included through Start.io) | Advertising SDK background scheduling after device restart |
| `ACCESS_ADSERVICES_TOPICS` (included through Start.io) | Advertising Topics access where supported and permitted |
| `com.google.android.finsky.permission.BIND_GET_INSTALL_REFERRER_SERVICE` (included through Start.io) | Advertising install-referrer attribution |
| `FOREGROUND_SERVICE` + `FOREGROUND_SERVICE_DATA_SYNC` | Running long media operations (tracking analysis, preview baking, export) as explicit foreground work started by the user |
| `POST_NOTIFICATIONS` | Showing export progress in the notification bar |
| `WAKE_LOCK` | Keeping the device awake during long-running processing so jobs complete reliably |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Requesting exemption from battery optimization for reliable completion of user-initiated processing jobs |

---

## Children's Privacy

The App is not directed at children under 13. We do not knowingly collect personal information from children.

---

## Changes to This Policy

We may update this Privacy Policy from time to time. Any changes will be reflected by the "Last updated" date above.

---

## Contact

If you have any questions about this Privacy Policy, please contact the developer via the support email listed on the Google Play store listing.
