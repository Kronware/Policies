# Data Safety - Simply Censor

This page supports the Google Play Data Safety declaration for Simply Censor.

Updated October 29, 2026 for Unity LevelPlay SDK 9.5.0 with ironSource Ads. Review the Play Console Data Safety form against all active releases when distributing this migration; publishing this document does not submit that form. Older active Start.io and AdMob releases must remain covered until retired.

## Data Collected and Shared

| Data type | Collected | Shared with third parties | Purpose |
| --- | --- | --- | --- |
| Photos and videos | Processed on-device only | No | Censor preview and local export |
| Face detection results | Processed on-device only | No | Automatic face censoring |
| Foreground segmentation masks | Processed on-device only | No | Background censoring |
| Session settings | Stored locally only for the active session | No | Applying the selected censor style and regions |
| Names, email addresses, and contacts | Not requested by the App | No | Not applicable |
| Approximate location | May be inferred from IP address by Unity/ironSource | Yes, with Unity/ironSource and advertising partners | Advertising, analytics, fraud prevention, and security |
| Precise location | No; the App does not request location permission | No | Not applicable |
| App interactions | May be collected through Unity/ironSource app/ad activity | Yes, with Unity/ironSource and advertising/measurement partners | Advertising, analytics, fraud prevention, and security |
| Installed apps (older Start.io releases) | May be collected where identifiers and platform access permit | May be used in profiles shared with Start.io partners | Advertising, analytics, fraud prevention, and security |
| Diagnostics and crash logs | May be collected by Unity/ironSource; Firebase Crashlytics sends configured crash reports | According to Unity's policy and SDK configuration; Firebase processes app crash reports | Analytics, SDK troubleshooting, and crash diagnostics |
| Device or other IDs | May be collected, including advertising and app-set identifiers where available | Yes, with Unity/ironSource and advertising/measurement partners | Advertising, analytics, fraud prevention, and security |

## Data Handling Summary

- Simply Censor itself does not collect, upload, or share selected media, face results, masks, or local editing settings.
- Photos and videos are never uploaded.
- Face detection and foreground segmentation run on-device.
- Current free builds use Unity LevelPlay with ironSource Ads for banners and pre-export interstitials. Advertising-related data can include IP-derived location, device/network details, identifiers, app/ad interactions, and technical logs. No location or Bluetooth permissions are requested.
- Free users allow or decline personalization before SDK initialization; the choice is stored locally, applied through LevelPlay's GDPR consent API, and editable in Settings > Ad privacy. Pro users see neither ads nor the prompt. Declining personalization does not guarantee zero SDK data processing. This manual dialog is not a certified CMP; review additional regional/network requirements before broad rollout.
- Firebase Crashlytics sends crash and application-not-responding diagnostics when configured for a released version. It does not receive selected media, face results, censor settings, or exported files.
- Consult [Unity's Game Player and App User Privacy Policy](https://unity.com/legal/game-player-and-app-user-privacy-policy) for handling, sharing, retention, and privacy rights. Selected media never accompanies advertising or diagnostic requests.
- Older Start.io releases may additionally collect installed-app query information. They retain Start.io's own consent flow; see its [SDK Data Disclosure](https://support.start.io/hc/en-us/articles/4413793394962-Google-Play-Safety-Section-Data-Disclosure) and [privacy policy](https://www.start.io/policy/privacy-policy/). Earlier AdMob releases may collect/share IP-derived location, app/ad interactions, diagnostics, device/account identifiers, and account-linked personal information under [Google's SDK disclosure](https://developers.google.com/admob/android/privacy/play-data-disclosure). Keep applicable categories for all active versions. Neither SDK is present in the new LevelPlay build.
- The core censoring and export workflow works without a network connection; ad loading requires network access.

## Google Play Console: App Interactions

For **App activity > App interactions**, select the following:

| Play Console prompt | Selection |
| --- | --- |
| Is this data collected, shared, or both? | Collected and shared |
| Is this data processed ephemerally? | No |
| Is this data required for the app, or can users choose whether it is collected? | Required for the free, ad-supported experience |
| Why is this data collected? | Advertising or marketing; Analytics; Fraud prevention, security, and compliance |
| Is this data encrypted in transit? | Verify against all shipped SDKs and network settings; do not infer this from a personalization choice |
| Can users request deletion of this data? | No account or app-held interaction records; Unity handles provider-held data requests through its privacy controls and DPO@unity3d.com |

The App does not upload editing interactions or media. Unity/ironSource may collect app/ad activity for advertising measurement. Also review **Location > Approximate location**, **Device or other IDs**, and **App info and performance > Crash logs / Diagnostics**. Retain applicable installed-app and Google-specific categories while older releases are active. Apply Google Play's service-provider sharing exceptions where appropriate for Firebase and diagnostic processing.

## Permissions Used

| Permission | Why it is needed |
| --- | --- |
| `FOREGROUND_SERVICE` and `FOREGROUND_SERVICE_DATA_SYNC` | User-started video analysis and export with a persistent, cancellable progress notification. Play review evidence: `store-assets/Simply_Censor_FOREGROUND_SERVICE_DATA_SYNC.mp4`. |
| `POST_NOTIFICATIONS` | Progress and completion notifications for user-started video processing. |
| `INTERNET` and `ACCESS_NETWORK_STATE` | Ads, purchases, and configured crash reporting. |
| `com.google.android.gms.permission.AD_ID` and `ACCESS_ADSERVICES_ATTRIBUTION` | Advertising identifiers and Android attribution where available. |
| `WAKE_LOCK` | SDK background-work support. |

The App uses Android's system media picker and does not request broad library access permissions.

Older Start.io builds also include `ACCESS_WIFI_STATE`, `ACCESS_ADSERVICES_TOPICS`, and `RECEIVE_BOOT_COMPLETED`; these are absent from current LevelPlay builds.

## User Controls

- End an active session or clear app storage to remove local app data.
- Delete exported photos and videos directly from your device gallery.
- Revoke notification permission through Android Settings at any time.
- Reset or delete the advertising ID using Android's advertising settings.
- Change personalization in Settings > Ad privacy. This updates LevelPlay's consent setting and replaces ad placements; it does not delete historical provider-held data.
- Use [Unity's privacy choices](https://unity.com/legal/game-player-and-app-user-privacy-policy) or contact DPO@unity3d.com for opt-out/deletion rights. Older Start.io versions use [Start.io's choices](https://www.start.io/do-not-sell-or-sharemy-personal-information/) or privacy@start.io. Clearing app storage does not delete provider-held data.
- Pro removes ad placements. When Pro is recognized at launch, the App does not initialize the ad SDK.

## Security

Selected media, analysis results, masks, and editing settings remain in Android's application sandbox or in your device gallery when exported. They are not transmitted to external servers.

Unity/ironSource independently transmits advertising-related data to its services and partners as described above; older providers do so in older builds. Firebase Crashlytics transmits configured crash diagnostics separately.