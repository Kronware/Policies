# Data Safety - Simply Censor

This page supports the Google Play Data Safety declaration for Simply Censor.

Updated October 27, 2026 for Start.io SDK 5.3.1. Review the Play Console Data Safety form against these disclosures when releasing this SDK migration; publishing this document does not update that form automatically.

## Data Collected and Shared

| Data type | Collected | Shared with third parties | Purpose |
| --- | --- | --- | --- |
| Photos and videos | Processed on-device only | No | Censor preview and local export |
| Face detection results | Processed on-device only | No | Automatic face censoring |
| Foreground segmentation masks | Processed on-device only | No | Background censoring |
| Session settings | Stored locally only for the active session | No | Applying the selected censor style and regions |
| Names, email addresses, and contacts | Not requested by the App | No | Not applicable |
| Approximate location | Yes, inferred from IP address by Start.io | Yes, with Start.io and advertising/data partners | Advertising, analytics, fraud prevention, and security |
| Precise location | No; the App does not request location permission | No | Not applicable |
| App interactions | Yes, app and ad activity through Start.io | Yes, with Start.io and advertising/measurement partners | Advertising, analytics, fraud prevention, and security |
| Installed apps | May be collected through Start.io queries about whether certain apps are installed, where identifiers and platform access permit | May be used in profiles shared with Start.io partners | Advertising, analytics, fraud prevention, and security |
| Diagnostics and crash logs | Yes, through Start.io and Firebase Crashlytics when configured | Start.io does not share SDK diagnostics with advertising partners; Firebase processes app crash reports | Analytics, SDK troubleshooting, and crash diagnostics |
| Device or other IDs | Yes, including advertising identifiers through Start.io where available | Yes, with Start.io and advertising/measurement partners | Advertising, analytics, fraud prevention, and security |

## Data Handling Summary

- Simply Censor itself does not collect, upload, or share selected media, face results, masks, or local editing settings.
- Photos and videos are never uploaded.
- Face detection and foreground segmentation run on-device.
- The free version uses Start.io for banners and pre-export interstitials. Advertising-related data includes IP address, inferred location, device/network details, advertising identifiers, app/ad interactions, and installed-app query information where available. Start.io's built-in disclosure/consent flow remains enabled; the App does not assume consent on the user's behalf.
- Firebase Crashlytics sends crash and application-not-responding diagnostics when configured for a released version. It does not receive selected media, face results, censor settings, or exported files.
- Consult [Start.io's SDK Data Disclosure](https://support.start.io/hc/en-us/articles/4413793394962-Google-Play-Safety-Section-Data-Disclosure) and [End User Privacy Policy](https://www.start.io/policy/privacy-policy/) for SDK handling, sharing, and retention. Advertising and diagnostic requests use network access; selected media never accompanies them.
- The core censoring and export workflow works without a network connection; ad loading requires network access.

## Google Play Console: App Interactions

For **App activity > App interactions**, select the following:

| Play Console prompt | Selection |
| --- | --- |
| Is this data collected, shared, or both? | Collected and shared |
| Is this data processed ephemerally? | No |
| Is this data required for the app, or can users choose whether it is collected? | Required for the free, ad-supported experience |
| Why is this data collected? | Advertising or marketing; Analytics; Fraud prevention, security, and compliance |
| Is this data encrypted in transit? | Yes |
| Can users request deletion of this data? | No account or app-held interaction records; Start.io handles requests through privacy@start.io or dpo@start.io and its privacy controls |

The App does not upload editing interactions or media. Start.io may collect app/ad activity for advertising measurement. Also review **App activity > Installed apps**, **Location > Approximate location**, **Device or other IDs**, and **App info and performance > Crash logs / Diagnostics**. Start.io's SDK diagnostics are not shared with advertising partners. Apply Google Play's service-provider sharing exceptions where appropriate for Firebase and diagnostic processing.

## Permissions Used

| Permission | Why it is needed |
| --- | --- |
| `FOREGROUND_SERVICE` and `FOREGROUND_SERVICE_DATA_SYNC` | User-started video analysis and export with a persistent, cancellable progress notification. Play review evidence: `store-assets/Simply_Censor_FOREGROUND_SERVICE_DATA_SYNC.mp4`. |
| `POST_NOTIFICATIONS` | Progress and completion notifications for user-started video processing. |
| `INTERNET` and `ACCESS_NETWORK_STATE` | Ads, purchases, and configured crash reporting. |
| `ACCESS_WIFI_STATE` | Advertising SDK network information. |
| `com.google.android.gms.permission.AD_ID` and `ACCESS_ADSERVICES_TOPICS` | Advertising ID and Android advertising topics where available. |
| `RECEIVE_BOOT_COMPLETED` | Advertising SDK background scheduling support. |

The App uses Android's system media picker and does not request broad library access permissions.

## User Controls

- End an active session or clear app storage to remove local app data.
- Delete exported photos and videos directly from your device gallery.
- Revoke notification permission through Android Settings at any time.
- Reset or delete the advertising ID using Android's advertising settings.
- Use [Start.io's privacy choices](https://www.start.io/do-not-sell-or-sharemy-personal-information/) or contact privacy@start.io for opt-out/deletion rights. Clearing app storage does not delete provider-held data.
- Pro removes ad placements. When Pro is recognized at launch, the App does not initialize the ad SDK.

## Security

Selected media, analysis results, masks, and editing settings remain in Android's application sandbox or in your device gallery when exported. They are not transmitted to external servers.

Start.io independently transmits its advertising-related data to its services and partners as described above. Firebase Crashlytics transmits configured crash diagnostics separately.