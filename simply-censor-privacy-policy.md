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

## Information We Do Not Collect

- We do not collect names, email addresses, account information, or contacts.
- We do not upload photos, videos, audio, face data, or censor settings.
- We do not collect location data.
- We do not use advertising, analytics, crash reporting, or tracking SDKs.
- We do not sell or share data with third parties.

## Third-Party Libraries

| Library | Purpose | Data leaves the device? |
| --- | --- | --- |
| Google ML Kit Face Detection | Finding faces for automatic censoring | No |
| Google ML Kit Selfie Segmentation | Identifying foreground subjects for background censoring | No |
| AndroidX Media3 | Video preview and local export processing | No |

## Permissions Used

| Permission | Why it is needed |
| --- | --- |
| `FOREGROUND_SERVICE` and `FOREGROUND_SERVICE_DATA_SYNC` | Keeping user-started video analysis and export visible and reliable while they run. |
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