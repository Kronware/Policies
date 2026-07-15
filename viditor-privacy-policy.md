# Privacy Policy — Viditor

**Last updated: July 2026**

This Privacy Policy explains how the Viditor app ("the App") handles your information.

---

## Information We Collect

### Videos and media
You grant the App access to videos on your device in order to import and edit them. Videos are processed entirely **on your device** and are never transmitted to any server or third party.

Edited videos are exported to your device's media gallery only when you explicitly tap the export button.

### On-device AI processing (face detection)
Viditor's automatic face censoring feature uses **Google ML Kit** to detect faces in your video. All face detection runs entirely on-device. No video frames, face data, or detection results are ever sent to any server.

### Project data
Project settings (effects, censor settings, overlays, trim points) are stored **locally on your device** in the app's private storage. This data is never transmitted.

### Tracking cache data
When you run tracking analysis, Viditor stores a per-project tracking cache locally in app-private storage. This cache contains timestamped detection regions and validation metadata (for example source/trim key and tracking analysis settings) so repeat exports can skip redundant analysis. This cache never leaves your device.

### Camera
The App does not request camera access.

---

## Information We Do NOT Collect

- We do not collect your name, email address, or any account information
- We do not transmit any video, audio, or image data to any server
- We do not collect location data
- We do not serve advertisements
- We do not use analytics SDKs or tracking libraries
- We do not sell any data to third parties

---

## Third-Party Libraries

Viditor uses the following third-party libraries, all of which run entirely on-device:

| Library | Purpose | Data leaves device? |
|---|---|---|
| Google ML Kit (Face Detection) | Detecting faces for auto-censor | No |
| AndroidX Media3 / ExoPlayer | Video playback during editing | No |
| AndroidX Media3 Transformer | Video export and effect rendering | No |

---

## Data Retention

All project data is stored locally on your device in the app's private storage. You can clear this data at any time by clearing the app's storage in your device settings. Uninstalling the App removes all locally stored data.

---

## Permissions Used

| Permission | Why it is needed |
|---|---|
| `FOREGROUND_SERVICE` + `FOREGROUND_SERVICE_DATA_SYNC` | Running long media operations (tracking analysis, preview baking, export) as explicit foreground work started by the user |
| `POST_NOTIFICATIONS` | Showing export progress in the notification bar |

Note: Viditor currently uses Android's system picker/storage access flow for media import and does not declare broad media read/write permissions in the app manifest.

---

## Children's Privacy

The App is not directed at children under 13. We do not knowingly collect personal information from children.

---

## Changes to This Policy

We may update this Privacy Policy from time to time. Any changes will be reflected by the "Last updated" date above.

---

## Contact

If you have any questions about this Privacy Policy, please contact the developer via the support email listed on the Google Play store listing.
