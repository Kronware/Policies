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

## 2) Photo and Video Access

### Why selected-file access is sufficient
BlurCut needs access only to videos selected by the user. It uses Android's system document picker (`ACTION_OPEN_DOCUMENT`) instead of requesting broad `READ_MEDIA_VIDEO` or `READ_MEDIA_IMAGES` permissions. Being a video editor does not by itself establish that system pickers are insufficient.

### How it is used
- The user selects a video through Android's system document picker; the App retains the selected URI's read grant for reopening projects
- The app reads the video for playback, frame extraction (thumbnails, ML face detection), and export processing
- Video data is processed entirely on-device; no frames or video content are transmitted externally

### User-facing justification
The user chooses which video the App can read in the system picker. No broad photo or video library runtime permission is requested at startup or during import.

### Play remediation
Publish a new app bundle without the restricted permissions and replace or deactivate affected artifacts on all tracks identified by Google. Updating policy pages alone does not remove permissions from already-uploaded bundles. Verify the merged release manifest before submitting.

## 3) Data Safety Form Suggested Answers

Scope here is based on current app behavior and manifest permissions.

### High-level
- Does your app collect or share any required user data types?: Yes
- Is all data encrypted in transit?: Yes for the Google SDK transmissions described in the privacy policy
- Do you provide a data deletion request mechanism?: No dedicated request mechanism for uploaded SDK data. Clearing local storage does not delete previously transmitted data
- Account creation: My app does not allow users to create an account; external-account sign-in is not supported
- See [Data Safety](blurcut-data-safety.md) for data types, purposes, and Google service configuration caveats

### Why this answer set is consistent
- Video editing and AI media processing are on-device only
- Optional Post AI Analysis is on-device only and does not upload frames or analysis data
- No account system
- AdMob collects and shares identifiers, IP-derived approximate location, interactions, and diagnostics
- Firebase Analytics and Crashlytics transmit usage, purchase, crash, installation, and diagnostic information
- Google Play Billing handles Pro purchases and subscriptions
- Manifest and SDK permissions include advertising ID and network access as well as local media and foreground-service permissions

## 4) Privacy Policy Wording (Publish-ready)

Use this summary at the top of your hosted privacy policy page:

BlurCut processes videos entirely on-device and does not upload video frames, audio, tracking results, or segmentation masks. No user account is required. The App uses AdMob for advertising, Firebase Analytics for usage and purchase analytics, Firebase Crashlytics for crash reporting, and Google Play Billing for Pro purchases. These services transmit identifiers, approximate location, interactions, purchase events, and diagnostics as described in the full privacy policy. Local storage controls do not delete data already sent to Google services.

## 5) Final Pre-Submission Checks

1. App content > Foreground services declaration completed for dataSync with feature videos uploaded.
2. Data Safety form answers exactly match shipped app behavior and SDK behavior.
3. Hosted privacy policy URL is live, public, and includes a support email address.
4. Re-verify current manifest before submission:
   - Confirm READ_MEDIA_VIDEO and READ_MEDIA_IMAGES are absent
   - FOREGROUND_SERVICE
   - FOREGROUND_SERVICE_DATA_SYNC
   - POST_NOTIFICATIONS
   - WAKE_LOCK
   - REQUEST_IGNORE_BATTERY_OPTIMIZATIONS
   - com.google.android.gms.permission.AD_ID
   - INTERNET and ACCESS_NETWORK_STATE (included through SDKs)
5. If any new SDK/permission is added later, update this file, policy page, and Data Safety form before release.
