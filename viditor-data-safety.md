# Data Safety — Viditor

This page supports the Google Play Data Safety declaration for the Viditor app.

---

## Data collected and shared

| Data type | Collected | Shared with third parties | Purpose |
|---|---|---|---|
| Videos / media files | Processed on-device only | No | Video editing and export |
| Face detection data | Processed on-device only (ML Kit) | No | Automatic face censoring |
| Project settings | Stored on-device only | No | Saving edit state between sessions |
| No personal data | — | — | — |

---

## Data handling summary

- **No personal data** (name, email, location, contacts) is ever collected by this app
- **Videos are never uploaded** — all editing and AI processing happens entirely on your device
- **Face detection is on-device only** — Google ML Kit runs locally; no frames or detection results leave the device
- **No analytics, no advertising, no tracking** — Viditor contains no ad SDKs, analytics libraries, or tracking code
- **No account required** — the app works fully offline with no sign-in

---

## Permissions used

| Permission | Why it is needed |
|---|---|
| `READ_MEDIA_VIDEO` / `READ_EXTERNAL_STORAGE` | Importing videos from your device gallery |
| `WRITE_MEDIA_VIDEO` / `MANAGE_MEDIA` | Saving the exported video to your gallery |
| `FOREGROUND_SERVICE` (type: `dataSync`) | Running video export as a foreground service so it completes reliably |
| `POST_NOTIFICATIONS` | Showing export progress and completion notifications |

---

## User controls

- **Project data**: Cleared automatically on uninstall. Can also be cleared from device Settings → Apps → Viditor → Storage → Clear Data
- **Exported videos**: Saved to your gallery — can be deleted like any other video

---

## Security

All data is stored in Android's application sandbox. No data is transmitted to external servers by this app.

---

## App does NOT use the following

- Advertising SDKs
- Analytics or crash reporting SDKs (beyond what Android provides by default)
- Cloud storage or sync
- User accounts or authentication
- In-app purchases
