# Supplemental: READ_MEDIA_VIDEO Permission Justification — BlurCut

**Package**: com.kronware.blurcut
**Permission**: android.permission.READ_MEDIA_VIDEO
**Date**: August 2026

---

## App Purpose

BlurCut is a privacy-focused on-device video editor that allows users to blur or pixelate faces and eyes in videos. The app performs all processing locally on the device — no data is uploaded to external servers.

## Why READ_MEDIA_VIDEO Is Required

BlurCut's core functionality is editing videos stored on the user's device. The `READ_MEDIA_VIDEO` permission (introduced in Android 13 / API 33) is required to:

1. **Open videos for editing** — The user selects a video from their library to import into a BlurCut project
2. **Extract video frames** — For timeline thumbnails, ML Kit face detection input, and paused preview rendering
3. **Read source video during export** — The Media3 Transformer pipeline reads the source video file to produce the processed output with censor effects applied

Without this permission, the app cannot access any video content and is non-functional.

## How the Permission Is Used

| Action | Description |
|---|---|
| Video import | User selects a video via system picker or file browser; app reads the file for playback and editing |
| Frame extraction | Individual frames are decoded on-device for timeline thumbnails and ML Kit face/eye detection |
| Export processing | Media3 Transformer reads the source video to produce a new video with blur/pixelate effects applied |

## What the Permission Is NOT Used For

- No video data is uploaded, transmitted, or shared with external servers
- No background scanning or indexing of the user's media library
- No access to photos, audio, or other media types (only video)
- No analytics or tracking of video content

## User Control

- Permission is requested at runtime only when the user initiates a video import
- The user can revoke the permission at any time via device Settings → Apps → BlurCut → Permissions
- All project data is stored locally and removed on app uninstall

## Relevant Google Play Policy Categories

- **Photos & Videos** (core functionality): BlurCut is a video editor — reading video files is essential to its declared purpose
- **Declared app category**: Video Players & Editors

## Additional Manifest Permissions

| Permission | Purpose |
|---|---|
| `FOREGROUND_SERVICE` + `FOREGROUND_SERVICE_DATA_SYNC` | User-initiated long-running media processing (tracking analysis, export) |
| `POST_NOTIFICATIONS` | Export progress and completion notifications |
| `WAKE_LOCK` | Keeping device awake during processing |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Reliable completion of user-initiated processing |

## Contact

Support email and privacy policy URL are listed on the Google Play Store listing.
