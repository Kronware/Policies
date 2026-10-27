# Orbitalift Privacy Policy

**Effective date: October 27, 2026**

Orbitalift is an Android gravity and physics puzzle app developed by **Kronware**. This policy applies to Orbitalift, including the package **com.kronware.orbitalift**. For privacy questions or requests, email **[support@kronware.io](mailto:support@kronware.io)**.

## Local gameplay and settings

Orbitalift stores your progress on your device, including XP, level progression, saved arenas, inventory, prizes, unlocked themes, reward-meter charge, scores, difficulty, daily challenge attempts and results, pending account-bound score submissions, the date of a daily sharing bonus, and sound, display and gameplay preferences. The app also keeps a local backup of its save file to recover from a damaged save.

Kronware does not operate a gameplay account, cloud-save service or server that receives these saves. Orbitalift does not require an account, and it does not directly ask for your name, email address, contacts, photos, precise location or payment details. Device or platform backup features may separately retain app data according to your settings and their providers' policies.

## Advertising and consent

The current Android app uses the **Start.io Android SDK** for optional rewarded videos and occasional between-arena interstitial ads. This replaces Google AdMob and Google's User Messaging Platform (UMP). Current builds, including signed Internal testing releases, enforce Start.io test mode using its official demo App ID. Test ads do not generate advertising revenue, but test mode does not guarantee that the SDK processes no data. Older app versions may still use Google's advertising services under the prior policy.

Start.io describes processing information for advertising, measurement, diagnostics and fraud prevention. Depending on permissions, device settings, consent and SDK behavior, this may include:

- IP address, which can be used to estimate a device's approximate location.
- App and ad interactions, such as launches, taps and video views.
- SDK diagnostic, crash and performance information.
- Device identifiers, including the Android advertising ID where available, and device/OS, network and language information. Start.io also discloses installed-app queries where applicable.

This integration does not request precise-location or Bluetooth access for advertising or supply your gamer identity, scores or journey save to Start.io. An approximate location may still be inferred from your IP address. Start.io's own processing, sharing, retention and international transfers are governed by its policies and your applicable choices. Non-personalized ads do not necessarily mean that no information is processed.

Before initializing Start.io, the app asks whether to allow personal data to be used for personalized ads and passes your choice to the SDK. Declining personalization does not prevent local gameplay or promise that essential ad processing stops. An **Ad privacy options** entry in Pause lets you change this preference. Start.io may also present its own applicable consent message. Your choice does not guarantee that an ad will be available.

For Start.io's disclosures, privacy rights and opt-out or deletion requests, see:

- [Start.io End User Privacy Policy](https://www.start.io/policy/privacy-policy/)
- [Start.io Android SDK data disclosures](https://support.start.io/hc/en-us/articles/4413793394962-Google-Play-Safety-Section-Data-Disclosure)
- [Start.io opt-out choices](https://www.start.io/do-not-sell-or-sharemy-personal-information/)
- [Google Privacy Policy](https://policies.google.com/privacy), applicable to Google services below and older app versions using AdMob.

Orbitalift does not separately integrate Firebase Analytics, a Facebook SDK or a developer-operated analytics backend. Optional crash reporting is described below. Advertising SDK measurement and diagnostics still apply as described above.

## Optional crash and ANR diagnostics

Android builds with Firebase configured include Google Firebase Crashlytics and its native-crash SDK. Crash-report collection is off by default and can be enabled or disabled with **Crash reports** in Settings. When enabled, the SDK sends crash, nonfatal-error and supported Android application-not-responding (ANR) reports to Google for diagnosing reliability problems. Reports may include stack traces, app version and build identifiers, device/OS information, timestamps, installation identifiers and limited game-state context such as mode, difficulty and recent operations.

Our custom diagnostic context does not include saved-game contents, gamer names, email, Play Games player IDs, advertising IDs, credentials or arbitrary user text. On Android 11 and later, enabled diagnostics also inspect recent abnormal process exits on the next launch. When available, a bounded system trace is kept privately on the device, not automatically attached to the synthetic Firebase report. The latest trace is replaced by later captures and cleaned when enabled diagnostics next run after it is more than seven days old.

Disabling Crash reports stops our diagnostic reporting and asks Crashlytics to delete unsent reports. It does not delete reports already received by Google. Firebase retention, processing and deletion policies apply to received reports; contact support about requests concerning our crash-reporting project. See [Firebase Privacy and Security](https://firebase.google.com/support/privacy) and [Crashlytics data collection](https://firebase.google.com/docs/crashlytics/collection-use).

## Optional Google Play Games

Builds configured for Google Play Games support optional authentication, leaderboards and achievements. Local journey play does not require sign-in. Google manages the gamer name, avatar and player identifier. The app reads the profile and player identifier for displaying the connected player and keeping score submissions attached to the correct account; it does not ask for a separate real name, email or leaderboard nickname.

Publishing an eligible daily score sends the score and challenge identifier to Google Play Games. Leaderboards can display gamer identity and rank to other players according to Google's service and privacy settings. Pending submissions and their owning player identifier are stored locally for retry; switching accounts does not transfer those submissions. These features are unavailable where the build has no corresponding service/board configuration. They do not synchronize journey saves or access Facebook friends. Profile editing uses Google's official profile surface, governed by [Google's Privacy Policy](https://policies.google.com/privacy).

## Sharing your progress

Sharing is optional. Orbitalift creates a local image containing the visible arena and game achievements, such as your level, XP, glass count or completion time, together with Orbitalift branding and a Play Store link. On Android, it opens the system share sheet and makes the image and invitation text available to the app you choose. It does not automatically post to Facebook or any other service, and it does not access your social account or contacts.

The most recent share image is kept in the app's private storage and replaced when another share image is generated. A receiving app may keep its own copy. Anything you send or publish through that app is governed by that service's privacy settings and policy; Kronware cannot remove those copies. The app records the daily sharing-bonus date locally when the share sheet opens; it does not verify or track whether you publish a post.

## Retention, deletion and your choices

Local progress, settings, backup saves and the latest share image remain on the device until replaced or removed. Android's app-storage controls can remove local app data; uninstalling ordinarily removes the app's private data, although platform backups may remain. Removing app data also removes your saved progress, XP, inventory and settings. Orbitalift does not provide a cloud account from which Kronware can recover that progress.

Deleting local app data does not delete information already processed by Google, Start.io, advertising partners or a sharing destination. Orbitalift does not currently provide an in-app mechanism to delete those providers' records. Their retention periods and privacy-request processes apply. You can use Android's advertising privacy controls to reset or delete your advertising ID where supported; this does not stop all advertising or SDK processing.

You may have rights to access, correct, delete, restrict or object to processing, withdraw consent, or make a complaint to a privacy regulator, depending on your jurisdiction. Contact **support@kronware.io** with requests about Kronware's handling of your information. We may need information to understand or verify a request. If you email us, we receive your email address and the information you choose to include, and use them to respond and handle the request. Do not include passwords or other sensitive information unnecessarily. Requests concerning a provider's independent processing may need to be directed to that provider.

## Children's privacy

Orbitalift does not ask players to create accounts or submit a date of birth. Kronware does not knowingly ask children to provide personal information directly to us. Advertising SDK processing is described above. A parent or guardian with a concern about a child's information can contact **support@kronware.io** so we can investigate and explain available options.

## Security and changes

Android's app-storage protections help separate private app data from other apps. No storage or transmission method is completely secure. Do not treat game saves or shared images as a secure place for sensitive information.

We may update this policy when the app or its services change. The effective date at the top identifies the current version. Privacy questions can be sent to **[support@kronware.io](mailto:support@kronware.io)**.