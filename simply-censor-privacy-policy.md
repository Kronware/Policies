# Privacy Policy - Simply Censor

**Last updated: October 27, 2026**

This Privacy Policy explains how Simply Censor (the "App") handles information.

## Information We Process

### Photos and videos

You choose a single photo or video with Android's system media picker. The App processes the selected media on your device to preview censoring and create an exported copy. Your source media is never uploaded to a server.

Exports are saved to your device's media gallery only when you explicitly choose Export.

### On-device censor analysis

Simply Censor uses Google ML Kit face detection and on-device foreground segmentation to help identify faces and foreground subjects. Analysis, masks, detected face regions, and censor settings stay on your device. No media, analysis result, or biometric data is transmitted by the App.

### Temporary session data

The App keeps the selected media, preview data, and censor settings only for the active editing session. It has no account system, project library, cloud backup, or server-side storage.

### Foreground video processing

When you start video analysis or export, Simply Censor uses an Android foreground service with a persistent, cancellable notification. This keeps the user-requested operation visible while it runs and does not upload the selected video or derived analysis data.

### Advertising

The free version uses the Start.io (formerly StartApp) SDK to display banner ads and interstitial ads before export. Start.io may collect advertising identifiers, IP address and approximate location inferred from it, device and network information, app and ad interactions, information about whether certain apps are installed, and SDK diagnostic or crash information. This data is used for advertising (including personalized advertising where permitted), measurement, analytics, security, and fraud prevention. Start.io may share advertising-related data with advertisers, advertising networks, attribution providers, and other business or data partners under its privacy policy. SDK diagnostics are collected for troubleshooting and are not shared with advertising partners according to Start.io's SDK disclosure.

Simply Censor does not request location permission or provide precise GPS location to Start.io. Selected media, face results, masks, and censor settings are never supplied to the advertising SDK. Pro users do not see ads, and the App does not initialize the advertising SDK on launch when an existing Pro entitlement is recognized.

Start.io's built-in privacy disclosure and consent flow remains enabled. You can also use Android's advertising ID controls to reset or delete your advertising ID. For details about Start.io's processing, retention, international transfers, and privacy rights, see the [Start.io End User Privacy Policy](https://www.start.io/policy/privacy-policy/). To opt out of sale or sharing, use [Start.io's privacy choices](https://www.start.io/do-not-sell-or-sharemy-personal-information/) or contact privacy@start.io. Purchasing Pro stops future ad placements; it does not automatically delete data previously collected by Start.io.

### Crash and application-not-responding diagnostics

When Firebase Crashlytics is configured for a released version, Simply Censor sends uncaught-crash and application-not-responding diagnostic reports to Firebase. These reports can include device and app diagnostic information, app version, thread details, and stack traces. They do not include selected media, face results, censor settings, or exported files.

## Information We Do Not Collect

- The App does not request names, email addresses, account information, or contacts. Advertising-related SDK data is described above.
- We do not upload photos, videos, audio, face data, or censor settings.
- We do not use selected media, face data, or censor settings for advertising, analytics, or tracking.
- We do not sell selected media, face data, or censor settings.

## Third-Party Libraries

| Library | Purpose | Data leaves the device? |
| --- | --- | --- |
| Google ML Kit Face Detection | Finding faces for automatic censoring | No |
| Google ML Kit Selfie Segmentation | Identifying foreground subjects for background censoring | No |
| AndroidX Media3 | Video preview and local export processing | No |
| Start.io SDK | Banner and interstitial advertising | Yes, for advertising-related SDK data described above |
| Firebase Crashlytics | Crash and application-not-responding diagnostics | Yes, for diagnostic reports described above |

## Permissions Used

| Permission | Why it is needed |
| --- | --- |
| `FOREGROUND_SERVICE` and `FOREGROUND_SERVICE_DATA_SYNC` | Keeping user-started video analysis and export visible and reliable with a persistent, cancellable notification while they run. |
| `POST_NOTIFICATIONS` | Showing progress and completion notifications for user-started video processing. |
| `INTERNET` and `ACCESS_NETWORK_STATE` | Loading ads, processing purchases, and sending configured crash diagnostics. |
| `ACCESS_WIFI_STATE` | Network information used by the advertising SDK. |
| `com.google.android.gms.permission.AD_ID` and `ACCESS_ADSERVICES_TOPICS` | Advertising identifiers and Android advertising topics where available. |
| `RECEIVE_BOOT_COMPLETED` | Background scheduling support included by the advertising SDK; not media upload. |

The App uses Android's system media picker rather than requesting broad access to your photo or video library.

## Data Retention and Deletion

Session data is held locally only while you are editing. You can end a session by leaving the App, and you can remove any app data through Android Settings or by uninstalling the App. Exported photos and videos remain in your device gallery until you delete them.

Advertising and diagnostic data already transmitted to Start.io or Firebase is governed by those providers' retention and deletion practices. Clearing local app data does not delete data held by those providers. Start.io privacy and deletion requests can be sent to privacy@start.io or dpo@start.io.

## Children's Privacy

The App is not directed at children under 13. We do not knowingly collect personal information from children.

## Changes to This Policy

We may update this policy from time to time. Changes will appear on this page with an updated date.

## Contact

For privacy questions, contact the developer through the support email listed on the Google Play store listing.