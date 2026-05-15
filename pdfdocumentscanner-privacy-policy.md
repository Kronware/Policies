# Privacy Policy — PDF Document Scanner

**Last updated: May 10, 2026**

This Privacy Policy explains how the PDF Document Scanner app ("the App") handles your information.

---

## Information We Collect

### Information stored on your device

The App stores your scanned documents as image files and exported PDFs in the app's private internal storage on your device. This data is **never transmitted to any server or third party**.

Stored data includes:
- Scanned document images (JPEG)
- Exported PDF files
- A local JSON catalog of document metadata (name, date, page count)

### Camera

The App requests access to your device camera solely to capture document images. Camera frames are processed entirely on-device using the CameraX library and are never transmitted anywhere.

### Storage

Scanned documents are saved to the app's private internal storage using Android scoped storage. No broad storage permission (`READ_EXTERNAL_STORAGE` or `WRITE_EXTERNAL_STORAGE`) is requested or used.

When you choose **Save to Downloads**, the exported PDF is written to your public Downloads folder using the Android MediaStore API. No additional permission is required on Android 10 (API 29) and above.

### Advertising

The free version of the App uses **Google AdMob** to display banner advertisements. AdMob may collect device identifiers and usage data in accordance with Google's own privacy policies to serve personalised ads.

If you have purchased the Pro upgrade, no ads are requested or displayed and the AdMob SDK does not load any ad content.

For more information, see:
- [Google Privacy Policy](https://policies.google.com/privacy)
- [How Google uses data when you use partners' apps](https://policies.google.com/technologies/partner-sites)

To opt out of personalised advertising, you can adjust your device's ad personalisation settings.

### Pro Version (in-app purchase)

The App offers a one-time **Pro upgrade** (`pro_upgrade`) purchased through Google Play. The purchase transaction is handled entirely by Google Play — the App never receives, stores, or transmits your payment details. Upon a confirmed purchase, the App queries Google Play Billing to confirm active purchase status. No payment data is stored by the App itself.

For information about how Google handles purchase data, see the [Google Play Terms of Service](https://play.google.com/about/play-terms/).

---

## Information We Do NOT Collect

- We do not collect your name, email address, or any account information
- We do not collect location data
- We do not transmit document images or PDF files to any server
- We do not receive or store payment or billing information (purchases are handled entirely by Google Play)
- We do not sell any data to third parties
- We do not use analytics SDKs or crash-reporting SDKs
- We do not track usage behaviour

---

## Network access

The App does not make any network requests from its own code. The only external network connections are:
- **Google Play Billing** — to verify purchase status (HTTPS, Google's servers)
- **Google AdMob** — to load ads in the free version (HTTPS, Google's servers)

All cleartext (HTTP) traffic is explicitly blocked in the app's network security configuration.

---

## Data Retention

All document data is stored locally on your device. You can delete individual documents or all data at any time from within the App. Uninstalling the App removes all locally stored data.

---

## Children's Privacy

The App is not directed at children under 13. We do not knowingly collect personal information from children.

---

## Changes to This Policy

We may update this Privacy Policy from time to time. Any changes will be reflected by the "Last updated" date above and shipped with the next app update.

---

## Contact

If you have any questions about this Privacy Policy, please contact:
**privacy@kronware.com**
