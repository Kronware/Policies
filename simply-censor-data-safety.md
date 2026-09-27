# Data Safety - Simply Censor

This page supports the Google Play Data Safety declaration for Simply Censor.

## Data Collected and Shared

| Data type | Collected | Shared with third parties | Purpose |
| --- | --- | --- | --- |
| Photos and videos | Processed on-device only | No | Censor preview and local export |
| Face detection results | Processed on-device only | No | Automatic face censoring |
| Foreground segmentation masks | Processed on-device only | No | Background censoring |
| Session settings | Stored locally only for the active session | No | Applying the selected censor style and regions |
| Personal data | No | No | Not applicable |
| Approximate location | Yes, through the Google Mobile Ads SDK IP-address collection | Yes, with Google advertising services | Advertising, analytics, fraud prevention, and security |
| App interactions | Yes, through the Google Mobile Ads SDK | Yes, with Google advertising services | Advertising, analytics, fraud prevention, and security |
| Diagnostics | Yes, through the Google Mobile Ads SDK | Yes, with Google advertising services | Advertising, analytics, fraud prevention, and security |
| Device or other IDs | Yes, including advertising and app-set identifiers through the Google Mobile Ads SDK | Yes, with Google advertising services | Advertising, analytics, fraud prevention, and security |

## Data Handling Summary

- Simply Censor itself does not collect, upload, or share selected media, face results, masks, or local editing settings.
- Photos and videos are never uploaded.
- Face detection and foreground segmentation run on-device.
- The free version uses Google Mobile Ads SDK for banner and interstitial ads. Google Mobile Ads SDK automatically collects and shares IP address, app interactions, diagnostics, and device/account identifiers for advertising, analytics, and fraud prevention.
- Google Mobile Ads SDK data is encrypted in transit with TLS. See Google's [Mobile Ads SDK Play Data Disclosure](https://developers.google.com/admob/android/privacy/play-data-disclosure).
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
| Can users request deletion of this data? | No user account or app-held interaction data exists to delete; Google handles SDK data under its own controls |

The App itself does not log or upload interaction events. These selections are required because Google Mobile Ads SDK automatically collects and shares app launch, tap, and video-view interaction data.

## Permissions Used

| Permission | Why it is needed |
| --- | --- |
| `FOREGROUND_SERVICE` and `FOREGROUND_SERVICE_DATA_SYNC` | User-started video analysis and export with a persistent, cancellable progress notification. Play review evidence: `store-assets/Simply_Censor_FOREGROUND_SERVICE_DATA_SYNC.mp4`. |
| `POST_NOTIFICATIONS` | Progress and completion notifications for user-started video processing. |

The App uses Android's system media picker and does not request broad library access permissions.

## User Controls

- End an active session or clear app storage to remove local app data.
- Delete exported photos and videos directly from your device gallery.
- Revoke notification permission through Android Settings at any time.

## Security

All App data remains in Android's application sandbox or in your device gallery when you export it. The App does not transmit data to external servers.

Google Mobile Ads SDK independently transmits its advertising-related data to Google services as described above.