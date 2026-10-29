# Privacy Policy - Simply Censor

**Last updated: October 29, 2026**

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

Current versions of the free App use Unity LevelPlay with ironSource Ads for banner ads and interstitial ads before export. Unity/ironSource may collect device and advertising identifiers, IP addresses and approximate location inferred from them, device/network information, app and ad interactions, and technical logs for ad delivery, personalized advertising where allowed, measurement, analytics, security, fraud prevention, and service reliability. Information may be shared with advertising, bidding, measurement, and service partners as described in [Unity's Game Player and App User Privacy Policy](https://unity.com/legal/game-player-and-app-user-privacy-policy), which also explains retention, international transfers, and privacy rights.

Before LevelPlay initializes, free users can allow or decline ad personalization. The choice is saved on this device and passed to LevelPlay through its GDPR consent API. You can change it under Settings > Ad privacy (the label is localized). Declining personalization does not remove all advertising or guarantee zero SDK processing: information may still be processed for ad delivery, security, and fraud prevention. Changing the choice replaces existing ad placements. Test-device settings are separate from privacy choices and do not imply zero SDK data collection.

Simply Censor does not request location or Bluetooth permissions for advertising. Selected media, face results, masks, and censor settings are never supplied to the advertising SDK. Pro users do not see ads or the personalization prompt, and the App does not initialize the advertising SDK on launch when an existing Pro entitlement is recognized. Purchasing Pro stops future ad placements; it does not automatically delete provider-held data. You can also reset or delete your advertising ID using Android's advertising controls and exercise [Unity's privacy choices](https://unity.com/legal/game-player-and-app-user-privacy-policy) or contact DPO@unity3d.com.

Older versions use Start.io (formerly StartApp), which may collect advertising identifiers, IP-derived location, device/network information, app/ad interactions, installed-app query information where available, and SDK diagnostics. Advertising-related data may be shared with advertising and data partners; SDK diagnostics are not shared onward according to Start.io's SDK disclosure. Those versions retain Start.io's built-in disclosure/consent flow. See the [Start.io End User Privacy Policy](https://www.start.io/policy/privacy-policy/) and [privacy choices](https://www.start.io/do-not-sell-or-sharemy-personal-information/), or contact privacy@start.io. Earlier AdMob versions are governed by [Google's Privacy Policy](https://policies.google.com/privacy) and may collect/share IP-derived location, ad/app interactions, diagnostics, and device or account-linked identifiers for advertising, analytics, and fraud prevention. Neither older SDK is included in current LevelPlay builds.

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
| Unity LevelPlay / ironSource Ads | Banner and interstitial advertising in current versions | Yes, for advertising-related SDK data described above |
| Start.io / Google Mobile Ads SDK | Advertising in older versions only | Yes, according to those providers' policies |
| Firebase Crashlytics | Crash and application-not-responding diagnostics | Yes, for diagnostic reports described above |

## Permissions Used

| Permission | Why it is needed |
| --- | --- |
| `FOREGROUND_SERVICE` and `FOREGROUND_SERVICE_DATA_SYNC` | Keeping user-started video analysis and export visible and reliable with a persistent, cancellable notification while they run. |
| `POST_NOTIFICATIONS` | Showing progress and completion notifications for user-started video processing. |
| `INTERNET` and `ACCESS_NETWORK_STATE` | Loading ads, processing purchases, and sending configured crash diagnostics. |
| `com.google.android.gms.permission.AD_ID` and `ACCESS_ADSERVICES_ATTRIBUTION` | Advertising identifiers and Android advertising attribution where available. |
| `WAKE_LOCK` | SDK background-work support. |

The App uses Android's system media picker rather than requesting broad access to your photo or video library.

Older Start.io versions also include `ACCESS_WIFI_STATE`, `ACCESS_ADSERVICES_TOPICS`, and `RECEIVE_BOOT_COMPLETED` for that SDK's network, advertising, and scheduling features. Current LevelPlay builds do not include those permissions.

## Data Retention and Deletion

Session data is held locally only while you are editing. You can end a session by leaving the App, and you can remove any app data through Android Settings or by uninstalling the App. Exported photos and videos remain in your device gallery until you delete them.

Advertising and diagnostic data already transmitted to Unity/ironSource, Firebase, or providers used in older versions is governed by their retention and deletion practices. Clearing local app data or changing personalization does not delete provider-held data. Unity privacy and deletion requests can be sent to DPO@unity3d.com; Start.io requests can be sent to privacy@start.io or dpo@start.io.

## Children's Privacy

The App is not directed at children under 13. We do not knowingly collect personal information from children.

## Changes to This Policy

We may update this policy from time to time. Changes will appear on this page with an updated date.

## Contact

For privacy questions, contact the developer through the support email listed on the Google Play store listing.