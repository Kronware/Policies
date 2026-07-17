# Google Play Submission Pack (July 2026) — Viditor

This file provides copy-ready text for Play Console declarations.

## 1) Foreground Service Declaration (App content)

### Declared FGS type
- dataSync

### Features that use FGS
- Tracking analysis for auto-censor processing, including optional Post AI Analysis refinement (user taps Apply in Tracking modal)
- Preview baking for effect previews (user-triggered preview generation)
- Final video export/transcode (user taps Export)

### Description of app functionality using this type
Viditor is an on-device video editor. When the user starts tracking analysis, optional Post AI Analysis refinement, preview baking, or export, the app performs long-running local media processing. These jobs are started directly by the user and run as foreground services with persistent notifications so the work remains reliable and user-visible.

### User impact if deferred or interrupted
If deferred, users experience delayed completion of the processing operation they explicitly started (analysis, preview generation, or export), which blocks the expected editing/export flow. If interrupted, the job may fail or require restart, resulting in incomplete outputs and a degraded editing experience.

### Suggested use-case selections for TYPE_DATA_SYNC
- Local processing: Import or export
- Local processing: Other (user-initiated media processing)

### Video evidence checklist for Play review
Record one short clip per feature showing:
1. User action that starts the operation (Apply or Export)
2. Foreground notification appears
3. Progress updates in notification and/or in-app blocking progress UI
4. Completion/cancel path

## 2) Data Safety Form Suggested Answers

Scope here is based on current app behavior and manifest permissions.

### High-level
- Does your app collect or share any required user data types?: No
- Is all data encrypted in transit?: Not applicable (no data transmitted to remote servers)
- Do you provide a data deletion request mechanism?: Not applicable for server-side data (no server-side user data). Local data can be removed by uninstalling or clearing app storage.

### Why this answer set is consistent
- Processing is on-device only
- Optional Post AI Analysis is on-device only and does not upload frames or analysis data
- No account system
- No ad SDKs
- No analytics/crash SDKs that transmit user data
- Manifest declares foreground service and notifications only

## 3) Privacy Policy Wording (Publish-ready)

Use this summary at the top of your hosted privacy policy page:

Viditor processes videos entirely on-device. The app does not upload video, image, audio, or personal data to external servers. No user account is required. Viditor's automatic censor workflow may include optional Post AI Analysis refinement, which also runs entirely on-device. Viditor uses foreground-service notifications only to keep user-initiated media processing visible and reliable while running. Users can remove local project data at any time by clearing app storage or uninstalling the app.

## 4) Final Pre-Submission Checks

1. App content > Foreground services declaration completed for dataSync with feature videos uploaded.
2. Data Safety form answers exactly match shipped app behavior and SDK behavior.
3. Hosted privacy policy URL is live, public, and includes a support email address.
4. Re-verify current manifest before submission:
   - FOREGROUND_SERVICE
   - FOREGROUND_SERVICE_DATA_SYNC
   - POST_NOTIFICATIONS
5. If any new SDK/permission is added later, update this file, policy page, and Data Safety form before release.

## 5) Photo and Video Permissions Declaration (July 2026)

**Submitted via**: App content → Photo and Video Permissions → Declaration form in Play Console.

**Permission**: `READ_MEDIA_IMAGES` / `READ_MEDIA_VIDEO`

**Declaration text:**

Viditor is an on-device video editor. The app does not declare or request `READ_MEDIA_IMAGES` or `READ_MEDIA_VIDEO` permissions — neither is present in the manifest. File selection is handled entirely via the Storage Access Framework system picker (`ACTION_OPEN_DOCUMENT`), which is itself a system-provided picker requiring no storage permissions.

The reason `PickVisualMedia` (Android photo picker) is technically insufficient for core app functionality is that it returns URIs with temporary grants only. Viditor stores project references persistently — when a user creates a project, the selected video URI is saved so the project can be reopened across app restarts and device reboots. This requires `ContentResolver.takePersistableUriPermission()`, which is only available for URIs returned by `ACTION_OPEN_DOCUMENT`. The `PickVisualMedia` API explicitly does not support persistable URI grants, making it unsuitable for a video editor that must access the source file in future sessions.

No broad media storage permissions are used or requested at any point in the app. The current implementation already meets the intended spirit of the photo/video permissions policy by using an OS-provided system picker with zero permission footprint.
