# Privacy Policy - Simply Censor

**Last updated: September 2026**

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

The free version uses Google Mobile Ads SDK to display banner and interstitial ads. Google Mobile Ads SDK may collect and share IP address, app interactions, diagnostic information, and device or account identifiers for advertising, analytics, and fraud prevention. This SDK data is encrypted in transit. Simply Censor does not use selected media, face results, or censor settings for advertising.

### Crash and application-not-responding diagnostics

When Firebase Crashlytics is configured for a released version, Simply Censor sends uncaught-crash and application-not-responding diagnostic reports to Firebase. These reports can include device and app diagnostic information, app version, thread details, and stack traces. They do not include selected media, face results, censor settings, or exported files.

## Information We Do Not Collect

- We do not collect names, email addresses, account information, or contacts.
- We do not upload photos, videos, audio, face data, or censor settings.
- We do not use selected media, face data, or censor settings for advertising, analytics, or tracking.
- We do not sell selected media, face data, or censor settings.

## Third-Party Libraries

| Library | Purpose | Data leaves the device? |
| --- | --- | --- |
| Google ML Kit Face Detection | Finding faces for automatic censoring | No |
| Google ML Kit Selfie Segmentation | Identifying foreground subjects for background censoring | No |
| AndroidX Media3 | Video preview and local export processing | No |
| Google Mobile Ads SDK | Banner and interstitial advertising | Yes, for advertising-related SDK data described above |
| Firebase Crashlytics | Crash and application-not-responding diagnostics | Yes, for diagnostic reports described above |

## Permissions Used

| Permission | Why it is needed |
| --- | --- |
| `FOREGROUND_SERVICE` and `FOREGROUND_SERVICE_DATA_SYNC` | Keeping user-started video analysis and export visible and reliable with a persistent, cancellable notification while they run. |
| `POST_NOTIFICATIONS` | Showing progress and completion notifications for user-started video processing. |

The App uses Android's system media picker rather than requesting broad access to your photo or video library.

## Data Retention and Deletion

Session data is held locally only while you are editing. You can end a session by leaving the App, and you can remove any app data through Android Settings or by uninstalling the App. Exported photos and videos remain in your device gallery until you delete them.

## Children's Privacy

The App is not directed at children under 13. We do not knowingly collect personal information from children.

## Changes to This Policy

We may update this policy from time to time. Changes will appear on this page with an updated date.

## Contact

For privacy questions, contact the developer through the support email listed on the Google Play store listing.