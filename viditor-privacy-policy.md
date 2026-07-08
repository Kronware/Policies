# Privacy Policy — Viditor

**Last updated: July 2026**

This Privacy Policy explains how the Viditor app ("the App") handles your information.

---

## Information We Collect

### Videos and media
You grant the App access to videos on your device in order to import and edit them. Videos are processed entirely **on your device** and are never transmitted to any server or third party.

Edited videos are exported to your device's media gallery only when you explicitly tap the export button.

### On-device AI processing (face detection)
Viditor's automatic face censoring feature uses **Google ML Kit** to detect faces in your video. All face detection runs entirely on-device. No video frames, face data, or detection results are ever sent to a server or stored beyond the current editing session.

### Project data
Project settings (effects, censor settings, overlays, trim points) are stored **locally on your device** in the app's private storage. This data is never transmitted.

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
| `READ_MEDIA_VIDEO` / storage access | Importing videos from your device for editing |
| `WRITE_MEDIA_VIDEO` / `MANAGE_MEDIA` | Saving the exported video to your gallery |
| `FOREGROUND_SERVICE` | Keeping the export process running while the screen is on |
| `POST_NOTIFICATIONS` | Showing export progress in the notification bar |

---

## Children's Privacy

The App is not directed at children under 13. We do not knowingly collect personal information from children.

---

## Changes to This Policy

We may update this Privacy Policy from time to time. Any changes will be reflected by the "Last updated" date above.

---

## Contact

If you have any questions about this Privacy Policy, please open an issue on the project repository or contact the developer via the email address listed on the Google Play store listing.
