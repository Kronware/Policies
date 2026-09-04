# VaultSeal — Release Notes

---

## Version 1.0.138

- Added on-demand thumbnail generation for fast, responsive media browsing.
- Added full subfolder navigation support across List, Icons, and Large Icons view modes.
- Enhanced grid layouts with distinct compact desktop-style icon view and high-detail large card preview view.
- Added preference persistence to keep your view mode and sort order selections saved across app restarts.

---

## Version 1.0.137

- Redesigned the vault browser interface with a clean selection bar for multi-file operations.
- Enhanced file deletion workflow and automatic vault container optimization.

---

## Version 1.0.136

- Maintenance updates, development tooling optimizations, and stability improvements.

---

## Version 1.0.135

- Diagnostics and database recovery optimizations.

---

## Version 1.0.134

- Added automatic discovery and self-healing for existing vault containers on startup.

---

## Version 1.0.133

- Streaming optimizations for importing large media and files without memory overhead.

---

## Version 1.0.132

- Improved error reporting and diagnostics for import operations.

---

## Version 1.0.131

- Improved encrypted entry streaming for background and queued imports.

---

## Version 1.0.130

- Enhanced direct import processing and responsiveness on the import confirmation screen.

---

## Version 1.0.129

- Internal verification and reliability enhancements for file ingest.

---

## Version 1.0.128

- Added real-time import progress feedback and chunked data streaming for maximum reliability.

---

## Version 1.0.127

- Enhanced user messaging and error notifications in the import queue.

---

## Version 1.0.126

- Memory usage optimizations for rapid vault indexing and large container rescans.

---

## Version 1.0.125

- Fixed Pro feature state synchronization and startup initialization.

---

## Version 1.0.124

- Improved Pro feature verification across background tasks.

---

## Version 1.0.123

- Enhanced vault storage tier limits and streaming performance tests.

---

## Version 1.0.122

- Prevented duplicate import requests when tapping rapidly.

---

## Version 1.0.121

- Improved import button states and clearer tier limit messaging.

---

## Version 1.0.120

- Implemented generous free tier limits with seamless streaming file encryption.

---

## Version 1.0.119

- Improved app memory allocation and user feedback for large file handling.

---

## Version 1.0.118

- Synchronized background and in-app file import queues for smooth multitasking.

---

## Version 1.0.117

- Added complete Pro Features Suite:
  - **Stealth Mode:** Disguise the app icon on your home screen.
  - **Break-In Alerts:** Track failed passphrase attempts with timestamps.
  - **Outbound App Restriction:** Restrict which apps can receive shared files.
  - Streamlined Pro navigation drawer.

---

## Version 1.0.116

- Build automation and release cleanup optimizations.

---

## Version 1.0.115

- Release pipeline and packaging refinements.

---

## Version 1.0.114

- Automated release build scripts for app bundles and standalone APKs.

---

## Version 1.0.113

- Refined dark theme contrast and icon visibility across all menus and navigation drawer items.

---

## Version 1.0.112

- Improved surface colors and visual contrast in dark mode.

---

## Version 1.0.111

- Improved tab navigation to seamlessly close active file viewers when switching tabs.

---

## Version 1.0.110

- Feature roadmap and enhancements documentation.

---

## Version 1.0.109

- Enhanced external share staging to ensure files shared from other apps are queued instantly.

---

## Version 1.0.108

- Enhanced vault synchronization to automatically clean up orphaned items during rescan.

---

## Version 1.0.107

- Preserved cached thumbnails and item metadata during storage optimization and container rescans.

---

## Version 1.0.106

- Fixed item deletion ordering during container compaction.

---

## Version 1.0.105

- Added enhanced error handling and stream safety during storage compaction.

---

## Version 1.0.104

- Enhanced custom storage path routing and file permissions handling.

---

## Version 1.0.103

- Added delete confirmation toast feedback and improved thumbnail decryption.

---

## Version 1.0.102

- Enhanced outbound file sharing diagnostics and security lifecycle checks.

---

## Version 1.0.101

- Synchronized vault catalog with physical container contents and removed phantom items.

---

## Version 1.0.100

- Database schema update and container health patch utilities.

---

## Version 1.0.99

- Enhanced vault container header handling and fixed startup unlock stability.

---

## Version 1.0.98

- Fine-tuned container header compaction and offset tracking.

---

## Version 1.0.97

- Fixed batch deletion container synchronization and restored secure preview exports.

---

## Version 1.0.96

- Prevented duplicate item indexing and consolidated background imports.

---

## Version 1.0.95

- Framework for seamless container upgrades and data migrations.

---

## Version 1.0.94

- Added non-destructive, automatic in-place container upgrade system.

---

## Version 1.0.93

- Enhanced container header format identification.

---

## Version 1.0.92

- Ensured background file imports automatically resume upon unlocking your vault.

---

## Version 1.0.91

- Added development guidelines and workspace configuration.

---

## Version 1.0.90

- Enhanced key derivation persistence across sealed and unsealed states.

---

## Version 1.0.89

- Ensured vault container inventory automatically syncs upon unlock.

---

## Version 1.0.88

- Enabled import queue retries while vault is sealed.

---

## Version 1.0.87

- Enhanced security architecture for queued file imports and background processing.

---

## Version 1.0.86

- Updated visual theme with refined surface variants and clean outline styles.

---

## Version 1.0.85

- Google Play Store compatibility updates.

---

## Version 1.0.84

- Reordered settings and help actions in the top app bar for quicker access.

---

## Version 1.0.83

- Improved biometric unlock compatibility across a wider variety of Android devices.

---

## Version 1.0.82

- Consolidated in-app documentation into a dedicated, searchable Help & FAQ activity.

---

## Version 1.0.81

- Added contextual help dialogs and support for in-app language selection.

---

## Version 1.0.80

- Added vault backup tracking, automated reminders, and auto-cleanup for old import logs.

---

## Version 1.0.79

- Redesigned app brand icon and polished vault setup prompts.

---

## Version 1.0.78

- Added store assets and improved release build automation.

---

## Version 1.0.77

- Renamed security setting to Screenshot Protection with refreshed theme colors.

---

## Version 1.0.76

- Modernized card layouts with clean OutlinedCard styling.

---

## Version 1.0.75

- Added animated splash screen branding and theme configurations.

---

## Version 1.0.74

- Overhauled app visual branding with crisp multi-resolution assets and refined dark theme navigation drawer.

---

## Version 1.0.73

- Implemented new brand assets and automated graphic generation.

---

## Version 1.0.72

- Eliminated main screen UI flicker on startup while loading vault status.

---

## Version 1.0.71

- Streamlined auto-seal behavior to return directly to the main screen.

---

## Version 1.0.70

- Clarified status notifications after changing your vault passphrase.

---

## Version 1.0.69

- Applied screenshot and app switcher protection earlier in app launch to prevent preview flashes.

---

## Version 1.0.68

- Fixed startup race condition on initial vault creation check.

---

## Version 1.0.67

- Added auto-seal timeout configuration (1, 2, 5, 10 min) and app switcher privacy toggle.

---

## Version 1.0.66

- Fixed auto-seal timer activation for newly created vaults.

---

## Version 1.0.65

- Fixed setup filename handling and added real import progress notifications.

---

## Version 1.0.64

- General vault stability fixes.

---

## Version 1.0.63

- Streamlined vault setup, added passphrase confirmation, and simplified biometric enrollment.

---

## Version 1.0.62

- Added **Backup Vault**: easily create timestamped backups of your encrypted vault to any storage location.

---

## Version 1.0.61

- Clarified setup dialog descriptions.

---

## Version 1.0.60

- Added explicit confirmation warning explaining storage behavior for Simple Setup vaults.

---

## Version 1.0.59

- Fixed storage resolution crash for app-private paths.

---

## Version 1.0.58

- Improved error recovery and storage checks during vault setup.

---

## Version 1.0.57

- Fixed vault setup retry behavior.

---

## Version 1.0.56

- Modernized UI controls by adopting clean switches app-wide.

---

## Version 1.0.55

- Made Simple Setup seamless with zero permission prompts using app-private storage.

---

## Version 1.0.54

- Added 3 flexible vault setup options: **Simple Setup**, **Advanced Setup**, and **Select Existing Vault**.

---

## Version 1.0.53

- Simplified initial vault setup flow.

---

## Version 1.0.52

- Improved missing storage detection.

---

## Version 1.0.51

- Streamlined main screen layout when no vault has been created yet.

---

## Version 1.0.50

- Disabled unlock controls when a vault container is missing.

---

## Version 1.0.49

- Redesigned vault creation flow with custom folder selection.

---

## Version 1.0.48

- Polished biometric unlock flow and fixed Media tab filter dropdown.

---

## Version 1.0.47

- Improved recovery workflow when an existing vault container is moved or missing.

---

## Version 1.0.46

- Added automatic prompt to recreate or locate a vault if deleted outside the app.

---

## Version 1.0.45

- Hardened passphrase rotation flow and polished browser navigation tabs.

---

## Version 1.0.44

- General vault browser fixes and stability improvements.

---

## Version 1.0.43

- Polished locked vault card layout and refined media UI.

---

## Version 1.0.42

- Made the Media tab the default view and improved passphrase input fields.

---

## Version 1.0.41

- Prevented duplicate biometric prompts during vault unlock.

---

## Version 1.0.40

- Added dedicated Passphrase Change management screen.

---

## Version 1.0.39

- Vault stability fixes and UI tweaks.

---

## Version 1.0.38

- Improved back button navigation, folder hierarchy handling, and file operations.

---

## Version 1.0.37

- Added navigation drawer and improved browser routing.

---

## Version 1.0.36

- Added multiple view modes (List, Icons, Large Icons) and multi-file selection actions.

---

## Version 1.0.35

- Added clear action and compact styling for the import history log.

---

## Version 1.0.34

- Improved reliability of file ingestion.

---

## Version 1.0.33

- Refined navigation drawer styling.

---

## Version 1.0.32

- Persisted file picker document permissions for background processing.

---

## Version 1.0.31

- Fixed startup crash related to navigation icons and background import services.

---

## Version 1.0.30

- Fixed drawer dismissal and background service handling.

---

## Version 1.0.29

- Made import errors visible with an active import progress queue.

---

## Version 1.0.28

- Improved pending import handling and localized UI labels.

---

## Version 1.0.27

- Fixed screen edge-to-edge insets and enabled immediate file processing.

---

## Version 1.0.26

- Moved vault switching and primary management actions into the navigation drawer.

---

## Version 1.0.25

- Applied UI and code formatting cleanups across import screens.

---

## Version 1.0.24

- Improved unlock screen navigation and added quick import actions.

---

## Version 1.0.23

- Required passphrase confirmation during initial vault setup.

---

## Version 1.0.22

- Internal code formatting and queue processor optimizations.

---

## Version 1.0.21

- Added container compaction when deleting vault files to reclaim storage space.

---

## Version 1.0.20

- Upgraded vault storage architecture to a unified sealed container format.

---

## Version 1.0.19

- Key derivation from passphrase and encrypted file metadata at rest.

---

## Version 1.0.18

- Icon-based browser navigation bar, unseal popup dialog, and auto-triggered biometric unlock.

---

## Version 1.0.17

- Overhauled main screen with clean Material 3 design and full light/dark theme support.

---

## Version 1.0.16

- Improved dark theme contrast, error toasts, and default storage location setup.

---

## Version 1.0.15

- Default new vault naming improvements.

---

## Version 1.0.14

- Added default folder creation setup and organized subfolder management.

---

## Version 1.0.13

- Polished theme colors and streamlined vault creation dialog.

---

## Version 1.0.12

- Added Biometric Unlock, Metadata Purifier privacy toggle, and System theme support.

---

## Version 1.0.11

- Fixed status and navigation bar insets across all screens.

---

## Version 1.0.10

- Complete Material 3 UI/UX overhaul, Settings screen, and built-in Media & File viewers.

---

## Version 1.0.9

- Database schema and file relationship handling updates.

---

## Version 1.0.8

- Added support for folders, favorites, recents, and item categorization.

---

## Version 1.0.7

- Built Pro gating system, upgrade screen, and privacy feature toggles.

---

## Version 1.0.6

- Added sealed/unsealed vault session state machine and passphrase verification UI.

---

## Version 1.0.5

- Added internal Compose vault browser and secure URI handling.

---

## Version 1.0.4

- Built outbound sharing sandbox to restrict external file leaks.

---

## Version 1.0.3

- Development build configuration and artifact tracking updates.

---

## Version 1.0.2

- Added secure clipboard auto-clear and background monitor.

---

## Version 1.0.1 — Initial Release

- Initial VaultSeal release.
- Encrypted file vault with AES-256 encryption.
- Import files, photos, videos, audio, and documents.
- Passphrase protection and secure file storage.
