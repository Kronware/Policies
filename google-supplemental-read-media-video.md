# Supplemental: System Picker Video Access - BlurCut

**Package**: com.kronware.blurcut
**Access method**: Android Storage Access Framework (`ACTION_OPEN_DOCUMENT`)
**Date**: October 18, 2026

---

## App Purpose

BlurCut is an on-device video editor that allows users to blur or pixelate faces and eyes in videos. Video editing and AI media processing run locally; video content, tracking results, and segmentation masks are not uploaded. Separately, Google advertising, analytics, diagnostic, and billing services communicate with Google as described in the [privacy policy](blurcut-privacy-policy.md).

## Selected-File Access Instead of Broad Permissions

BlurCut's core functionality is editing user-selected videos. System pickers are sufficient for this workflow, so the App does not request `READ_MEDIA_VIDEO` or `READ_MEDIA_IMAGES`. Android grants access to the selected URI for:

1. **Open videos for editing** — The user selects a video from their library to import into a BlurCut project
2. **Extract video frames** — For timeline thumbnails, ML Kit face detection input, and paused preview rendering
3. **Read source video during export** — The Media3 Transformer pipeline reads the source video file to produce the processed output with censor effects applied

The App retains the selected URI's read permission so projects can reopen after process or device restarts, provided the document still exists and the grant remains available. It does not require write access to the source video.

## How Selected Files Are Used

| Action | Description |
|---|---|
| Video import | User selects a video via system picker or file browser; app reads the file for playback and editing |
| Frame extraction | Individual frames are decoded on-device for timeline thumbnails and ML Kit face/eye detection |
| Export processing | Media3 Transformer reads the source video to produce a new video with blur/pixelate effects applied |

## Access Boundaries

- No video data is uploaded, transmitted, or shared with external servers
- No background scanning or indexing of the user's media library
- No access to photos, audio, or other media types (only video)
- No analytics or tracking of video content

## User Control

- Video import opens the Android system document picker; there is no broad library permission prompt
- The user can cancel the picker without granting access to a new file
- App-private project data is stored locally and can be cleared through Android Settings or uninstalling; Android backup and restore may retain or restore data according to device settings

## Relevant Google Play Policy Categories

- **Photos & Videos** (core functionality): BlurCut is a video editor — reading video files is essential to its declared purpose
- **Declared app category**: Video Players & Editors

## Release Remediation

This replaces the earlier broad-permission justification. A new permission-free bundle must replace affected artifacts on the Play tracks identified by Google; changing this document does not modify existing uploaded bundles. Verify the merged release manifest and import/reopen/export behavior before submission.

## Additional Manifest Permissions

| Permission | Purpose |
|---|---|
| `INTERNET` and `ACCESS_NETWORK_STATE` (included through SDKs) | Advertising, analytics, crash reporting, and purchase service connections, not video uploads |
| `com.google.android.gms.permission.AD_ID` | Advertising identifier access by Google SDKs where available and permitted |
| `FOREGROUND_SERVICE` + `FOREGROUND_SERVICE_DATA_SYNC` | User-initiated long-running media processing (tracking analysis, export) |
| `POST_NOTIFICATIONS` | Export progress and completion notifications |
| `WAKE_LOCK` | Keeping device awake during processing |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Reliable completion of user-initiated processing |

## Contact

Support email and privacy policy URL are listed on the Google Play Store listing.
