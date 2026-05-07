# media-shredder Privacy Policy

**Last Updated:** May 6, 2026

## Overview

Media Shredder ("the App") is an Android application designed to help users securely and permanently delete media files (photos and videos) from their devices. This Privacy Policy explains how we handle data related to the App.

## Data Collection

**Media Shredder does not collect, transmit, store, or share any personal data.**

All operations performed by the App occur entirely on your device. No information about you, your device, or your media is sent to any server operated by the developer.

## Permissions Used

The App requests the following permissions:

| Permission | Purpose |
|---|---|
| `READ_MEDIA_IMAGES` | Browse photos on your device |
| `READ_MEDIA_VIDEO` | Browse videos on your device |
| `READ_EXTERNAL_STORAGE` | Browse media on devices running Android 9 and below (not requested on Android 10+) |
| `WRITE_EXTERNAL_STORAGE` | Write access for devices running Android 9 and below (not requested on Android 10+) |
| `MANAGE_EXTERNAL_STORAGE` | Required to locate, overwrite, and permanently delete media files. This is a restricted permission; its use is limited solely to the core shredding function of the App and is never used to access unrelated user files. |
| `MANAGE_MEDIA` | Required to request permanent deletion of media directly from the Android MediaStore on Android 11+ without leaving files in the system Trash |
| `POST_NOTIFICATIONS` | Required on Android 13+ to display progress notifications during background shredding operations |
| `INTERNET` | Required for AdMob advertising SDK |
| `ACCESS_NETWORK_STATE` | Required for AdMob advertising SDK |

## Advertising

This App uses **Google AdMob** to display banner advertisements. AdMob may collect and use data in accordance with [Google's Privacy Policy](https://policies.google.com/privacy). This may include:

- Device identifiers
- IP address
- Advertising ID
- Usage data for ad targeting and measurement

You may opt out of personalized advertising through your device settings under **Google → Ads → Opt out of Ads Personalization**.

## File Operations

When you choose to shred files:

1. The App overwrites the file contents with cryptographically random data (3 passes).
2. The App deletes the file from the file system via Android's MediaStore API.
3. No copy of the file data is retained by the App.

## Children's Privacy

This App is not directed at children under 13. We do not knowingly collect information from children.

## Changes to This Policy

We may update this Privacy Policy. Continued use of the App after any changes constitutes acceptance of the new policy.

## Contact

For questions about this Privacy Policy, contact: **mediashredder@proton.me**
