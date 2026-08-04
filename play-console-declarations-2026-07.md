# Google Play Submission Pack (July 2026) — BlurCut - Video Censor Editor

This file provides copy-ready text for Play Console declarations.

## 1) Foreground Service Declaration (App content)

### Declared FGS type
- dataSync

### Features that use FGS
- Tracking analysis for auto-censor processing, including optional Post AI Analysis refinement (user taps Apply in Tracking modal)
- Preview baking for effect previews (user-triggered preview generation)
- Final video export/transcode (user taps Export)

### Description of app functionality using this type
BlurCut is an on-device video editor. When the user starts tracking analysis, optional Post AI Analysis refinement, preview baking, or export, the app performs long-running local media processing. These jobs are started directly by the user and run as foreground services with persistent notifications so the work remains reliable and user-visible.

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

## 2) READ_MEDIA_VIDEO Permission Declaration

### Why the permission is needed
BlurCut is a video editor. `READ_MEDIA_VIDEO` (Android 13+) is required to access video files from the user's device storage for editing, applying censor effects, and exporting processed video. Without this permission, the app cannot open videos for editing.

### How it is used
- The user selects a video from their library via the system media picker or file browser
- The app reads the video for playback, frame extraction (thumbnails, ML face detection), and export processing
- Video data is processed entirely on-device; no frames or video content are transmitted externally

### User-facing justification
The app requests this permission only when the user initiates a video import action. A runtime permission dialog is shown on Android 13+ before any video access occurs.

## 3) Data Safety Form Suggested Answers

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

## 4) Privacy Policy Wording (Publish-ready)

Use this summary at the top of your hosted privacy policy page:

BlurCut processes videos entirely on-device. The app does not upload video, image, audio, or personal data to external servers. No user account is required. BlurCut's automatic censor workflow may include optional Post AI Analysis refinement, which also runs entirely on-device. BlurCut uses foreground-service notifications only to keep user-initiated media processing visible and reliable while running. Users can remove local project data at any time by clearing app storage or uninstalling the app.

## 5) Final Pre-Submission Checks

1. App content > Foreground services declaration completed for dataSync with feature videos uploaded.
2. Data Safety form answers exactly match shipped app behavior and SDK behavior.
3. Hosted privacy policy URL is live, public, and includes a support email address.
4. Re-verify current manifest before submission:
   - READ_MEDIA_VIDEO
   - FOREGROUND_SERVICE
   - FOREGROUND_SERVICE_DATA_SYNC
   - POST_NOTIFICATIONS
   - WAKE_LOCK
   - REQUEST_IGNORE_BATTERY_OPTIMIZATIONS
5. If any new SDK/permission is added later, update this file, policy page, and Data Safety form before release.
