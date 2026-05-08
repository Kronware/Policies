# media-shredder Privacy Policy

**Last Updated:** May 8, 2026

## Overview

Media Shredder ("the App") is an Android application designed to help users securely and permanently delete media files (photos and videos) from their devices. This Privacy Policy explains how we handle data related to the App.

## Data Collection

**Media Shredder does not collect, transmit, store, or share any personal data with the developer.**

All shredding operations are performed entirely on your device. No information about you, your device, or your media is sent to any server operated by the developer.

If you purchase **Media Shredder Pro**, your purchase is processed exclusively by Google Play. The App receives only a confirmation of purchase status from Google Play Billing. The developer does not receive or store your payment details, name, or billing address.

## Permissions Used

The App requests the following permissions:

| Permission | Purpose |
|---|---|
| `READ_MEDIA_IMAGES` | Browse photos on your device |
| `READ_MEDIA_VIDEO` | Browse videos on your device |
| `READ_MEDIA_VISUAL_USER_SELECTED` | Supports Android 14+ partial photo/video access |
| `READ_EXTERNAL_STORAGE` | Browse media on devices running Android 9 and below (not requested on Android 10+) |
| `WRITE_EXTERNAL_STORAGE` | Write access for devices running Android 9 and below (not requested on Android 10+) |
| `MANAGE_MEDIA` | Requests one-time write access to media files via Android MediaStore on Android 12+, enabling secure overwrite without per-file system dialogs |
| `POST_NOTIFICATIONS` | Required on Android 13+ to display progress notifications during shredding operations |
| `INTERNET` | Required for AdMob advertising SDK (free tier) and Google Play Billing (Pro purchase) |
| `ACCESS_NETWORK_STATE` | Required for AdMob advertising SDK |

## Advertising

The free version of this App uses **Google AdMob** to display banner advertisements. AdMob may collect and use data in accordance with [Google's Privacy Policy](https://policies.google.com/privacy). This may include:

- Device identifiers
- IP address
- Advertising ID
- Usage data for ad targeting and measurement

**Users who have purchased Media Shredder Pro are shown no advertisements.** AdMob is not initialised at all for Pro users.

Free-tier users may opt out of personalized advertising through their device settings under **Google → Ads → Opt out of Ads Personalization**.

## Pro Upgrade & Billing

Media Shredder offers an optional one-time in-app purchase called **Media Shredder Pro**, processed by Google Play Billing.

- Payment is handled entirely by Google Play. The developer has no access to your payment information.
- After a successful purchase, the App stores only a boolean flag locally on your device (in Android SharedPreferences) indicating that Pro status has been confirmed. This data never leaves your device.
- Purchase history and receipts are managed by your Google Play account.
- For refund requests, please follow Google Play's standard refund process.

## File Operations

When you choose to shred files:

1. The App overwrites the file contents with cryptographically random data (3 passes).
2. The App deletes the file from the file system via Android's MediaStore API.
3. No copy of the file data is retained by the App.

## Local Data Storage

The App stores the following data locally on your device only:

| Data | Storage | Purpose |
|---|---|---|
| Pro status cache | SharedPreferences | Avoid querying Google Play on every app launch |

This data is never transmitted off-device.

## Children's Privacy

This App is not directed at children under 13. We do not knowingly collect information from children.

## Changes to This Policy

We may update this Privacy Policy. Continued use of the App after any changes constitutes acceptance of the new policy.

## Contact

For questions about this Privacy Policy, contact: **mediashredder@proton.me**
