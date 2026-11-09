# Data Safety — Raging Roller

This page supports the Google Play Data Safety declaration for Raging Roller
(`com.kronware.ragingroller`). Before production rollout, verify the final
LevelPlay network configuration against
[Unity's Play disclosure guidance](https://docs.unity.com/en-us/grow/levelplay/sdk/android/regulations-index)
and Firebase's
[Crashlytics data disclosure](https://firebase.google.com/docs/android/play-data-disclosure).
This document does not submit the declaration for you.

---

## Data collected and shared

| Data type | Collected | Shared with third parties | Purpose |
|---|---|---|---|
| Settings, progress, unlocks, daily-challenge records | Stored on-device only | No | App functionality |
| Tilt (accelerometer/gyroscope) readings | Used on-device only, not stored | No | Game controls |
| IP address (UTC date request to timeapi.io / worldtimeapi.org) | Received by the time service as part of the request | No | App functionality (daily challenge date) |
| Crash logs (Firebase Crashlytics) | Yes | No (Google acts as a service provider) | App functionality, analytics (stability) |
| Diagnostics: device model, OS version, memory/disk state (Firebase Crashlytics) | Yes | No (service provider) | Analytics (stability) |
| Device or other identifiers: Firebase installation ID (Crashlytics) | Yes | No (service provider) | Analytics (stability) |
| Approximate location/IP address (LevelPlay/ironSource) | May be collected | Yes - to Unity/ironSource and advertising partners | Advertising, measurement, fraud prevention |
| Device or other identifiers: advertising ID, app set ID (LevelPlay/ironSource) | May be collected | Yes - to Unity/ironSource and advertising partners | Advertising, measurement, fraud prevention |
| App interactions: ad views and clicks (LevelPlay/ironSource) | May be collected | Yes - to Unity/ironSource and advertising partners | Advertising, measurement |
| Diagnostics: technical logs (LevelPlay/ironSource) | May be collected | According to Unity's policy and SDK configuration | Service reliability, analytics, fraud prevention |
| App activity: other actions (run scores sent to the Google Play Games leaderboard) | Yes, only when signed in to Play Games | No (Google provides the service) | App functionality |
| Play Games display name | Shown on-device only, not stored or sent by the App | No | App functionality |

### Play Console answers (summary)

- **Does the app collect or share user data?** Yes.
- **Is all collected data encrypted in transit?** Yes. Crashlytics and LevelPlay
  use HTTPS.
- **Can users request data deletion?** No. Kronware has no accounts or servers
  and can't delete data held by Google or Unity. Local data is deleted by
  uninstalling the App or clearing its storage. Advertising data, Crashlytics
  data, and Play Games scores and profiles are managed through each provider's
  own controls.
- **Categories to declare:**
  - Location: Approximate location.
  - Device or other IDs.
  - App activity: App interactions, Other actions (optional leaderboard scores).
  - App info and performance: Crash logs, Diagnostics.

---

## Data handling summary

- **No account or profile data.** The App doesn't request sign-in, and doesn't
  collect a name, email address, or phone number.
- **Game data is local only.** Settings and progress are stored in the Android
  app sandbox (`user://settings.cfg`) and are never uploaded.
- **Crash reporting.** Firebase Crashlytics reports Java and native crashes to
  the Kronware Firebase project (`kronware-7f5be`). Crash data is kept for
  90 days. See
  [Firebase privacy](https://firebase.google.com/support/privacy).
- **Advertising.** Unity LevelPlay with ironSource Ads shows interstitials
  between maps, and one rewarded ad after a real unlock. The App has no
  in-app consent dialog. Users can use Android's advertising-ID controls and
  [Unity's privacy choices](https://unity.com/legal/game-player-and-app-user-privacy-policy).
  Add a certified CMP before a broad EEA/UK rollout. Test ads do not imply that
  the SDK collects no data.

---

## Permissions used

| Permission | Why it is needed |
|---|---|
| `INTERNET` | Loading advertisements, sending crash reports, and getting the trusted UTC date for daily challenges |
| `ACCESS_NETWORK_STATE` | Checking connectivity before ad requests (LevelPlay) and crash uploads (Firebase) |
| `com.google.android.gms.permission.AD_ID` | Advertising-ID access for ad delivery and measurement, where available and permitted |
| `ACCESS_ADSERVICES_ATTRIBUTION` | Android Privacy Sandbox attribution APIs used by the advertising SDK |
| `VIBRATE` | Haptic feedback during gameplay |

---

## User controls

- **Audio and tilt calibration** can be changed in Settings.
- **Ad personalisation** is controlled through Android's advertising-ID
  settings and
  [Unity's privacy choices](https://unity.com/legal/game-player-and-app-user-privacy-policy).
- **Delete local data** by clearing the App's storage in Android settings, or by
  uninstalling the App.

---

## Security

All game data is stored in the Android application sandbox. Kronware operates no
servers. Network traffic goes only to the time services, Firebase, and the
advertising providers listed above.
