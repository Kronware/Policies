# Privacy Policy — BlurCut - Video Censor Editor

**Last updated: October 18, 2026**

This Privacy Policy explains how the BlurCut app ("the App") handles your information.

---

## Information We Collect

### Videos and media
You grant the App access to videos on your device in order to import and edit them. Videos are processed entirely **on your device** and are never transmitted to any server or third party.

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
The free version uses **Google AdMob** to display advertisements. The Google Mobile Ads SDK collects and shares IP addresses (which can be used to estimate approximate location), app and ad interactions, diagnostic information, and device or other identifiers such as the Android advertising ID and app set ID. Google uses this information for advertising, analytics, and fraud prevention, security, and compliance. This does not require access to your device's GPS location. Pro removes displayed advertisements; it does not provide a general opt-out from analytics or crash reporting.

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
- We do not request precise or GPS location; Google services may derive approximate location from IP addresses
- We do not access your contacts or payment card details

These statements do not exclude the SDK identifiers, usage information, and diagnostics described above.

---

## Third-Party Libraries

BlurCut uses both on-device media libraries and network-connected Google services:

| Library | Purpose | Data leaves device? |
|---|---|---|
| Google ML Kit (Face Detection) | Baseline face detection for auto-censor and Post AI Analysis refinement inputs | No input frames or detection results; SDK usage and diagnostic metadata may be sent to Google |
| Google ML Kit (Selfie Segmentation) | Foreground subject masks for Background Censoring | No input frames or masks; SDK usage and diagnostic metadata may be sent to Google |
| AndroidX Media3 / ExoPlayer | Video playback during editing | No |
| AndroidX Media3 Transformer | Video export and effect rendering | No |
| Google AdMob | Advertising, measurement, and fraud prevention | Yes: identifiers, IP-derived approximate location, interactions, and diagnostics |
| Google Analytics for Firebase | Usage and purchase analytics | Yes: identifiers, approximate location, usage and purchase events |
| Firebase Crashlytics and supporting Firebase services | Crash reporting and reliability analysis | Yes: crash reports, installation identifiers, session and diagnostic information |
| Google Play Billing | Pro purchases, subscriptions, and entitlement restoration | Yes: purchase-related communications with Google Play |

Google processes these data under its applicable terms and privacy policies. Firebase services generally process data on the developer's behalf; AdMob also collects and shares data for advertising purposes. Additional processing can depend on Google service configuration and applicable privacy settings.

- [Google Privacy Policy](https://policies.google.com/privacy)
- [How Google uses information from apps that use its services](https://policies.google.com/technologies/partner-sites)
- [AdMob data disclosures](https://developers.google.com/admob/android/privacy/play-data-disclosure)
- [Firebase data disclosures](https://firebase.google.com/docs/android/play-data-disclosure)
- [Google Analytics data disclosures](https://support.google.com/analytics/answer/11582702)

---

## Data Retention

Project and tracking data is stored locally in the app's private storage. You can clear that storage through Android Settings. Uninstalling removes app-private data on the device, but exported videos remain in your gallery until you delete them. Android system backup and restore may retain or restore app data according to your device settings.

Advertising, analytics, purchase, and crash-reporting data is handled by the respective Google services under their retention policies and applicable service settings. Clearing app storage or uninstalling does not delete data already transmitted to those services. We do not promise that all such data is deleted within 90 days.

The App currently has no dedicated in-app request mechanism for deleting uploaded SDK data. For privacy questions, contact the developer through the support email on the Google Play listing. Google also provides privacy controls through its services and your Google account where applicable.

## Security and Privacy Controls

AdMob and Firebase encrypt their SDK transmissions in transit using TLS/HTTPS. This does not mean data is end-to-end encrypted. Local app-private data is protected by Android's application sandbox.

You can reset or delete your advertising ID through Android's advertising privacy settings where supported. This limits use of that identifier but does not stop all advertising, analytics, or diagnostic collection. The App currently does not provide a general analytics or crash-reporting opt-out.

---

## Permissions Used

| Permission | Why it is needed |
|---|---|
| `INTERNET` and `ACCESS_NETWORK_STATE` (included through SDKs) | Connecting to advertising, analytics, crash-reporting, and purchase services |
| `com.google.android.gms.permission.AD_ID` | Allowing Google SDKs to access the advertising ID where available and permitted |
| `READ_MEDIA_VIDEO` | Reading video files from device storage for editing. Required on Android 13+ to access the user's video library |
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
