# Data Safety — BlurCut - Video Censor Editor

This page supports the Google Play Data Safety declaration for the BlurCut app.

---

## Data collected and shared

| Data type | Collected | Shared with third parties | Purpose |
|---|---|---|---|
| Videos / media files | Processed on-device only | No | Video editing and export |
| Face detection data | Processed on-device only (ML Kit + optional Post AI Analysis refinement) | No | Automatic face censoring and analysis refinement |
| Tracking cache data | Stored on-device only | No | Reusing analysis for faster repeat exports |
| Project settings | Stored on-device only | No | Saving edit state between sessions |
| No personal data | — | — | — |

---

## Data handling summary

- **No personal data** (name, email, location, contacts) is ever collected by this app
- **Videos are never uploaded** — all editing and AI processing happens entirely on your device
- **Face detection and Post AI Analysis are on-device only** — all frames and analysis results stay on your device
- **Tracking cache is local only** — per-project analysis cache is stored in app-private storage for export reuse
- **No analytics, no advertising, no tracking** — BlurCut contains no ad SDKs, analytics libraries, or tracking code
- **No account required** — the app works fully offline with no sign-in

---

## Permissions used

| Permission | Why it is needed |
|---|---|
| `FOREGROUND_SERVICE` + `FOREGROUND_SERVICE_DATA_SYNC` | Running long media operations (tracking analysis, preview baking, export) as user-visible foreground work so jobs complete reliably |
| `POST_NOTIFICATIONS` | Showing export progress and completion notifications |

Note: BlurCut currently uses the Android system picker/storage access flow for media selection and does not declare broad media read/write permissions in the manifest.

---

## User controls

- **Project data**: Cleared automatically on uninstall. Can also be cleared from device Settings → Apps → BlurCut → Storage → Clear Data
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
