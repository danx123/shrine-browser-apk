# Shrine Browser

<p align="center">
  <img src="https://img.shields.io/badge/Release-v1.7.4-FF9E0B?style=for-the-badge" alt="Release Version" />
  <img src="https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Platform" />
  <img src="https://img.shields.io/badge/Architecture-Jetpack%20Compose-4285F4?style=for-the-badge" alt="Jetpack Compose" /> 
</p>

A calm, privacy-focused Android web browser built on a hardened WebView engine. Shrine combines a clean Material You interface with built-in tracker blocking, an encrypted password vault, reader mode, and optional Google cloud sync.

---

## Screenshot

<img width="2186" height="1600" alt="shrine-1" src="https://github.com/user-attachments/assets/b84bc227-9385-434f-a581-78f9bbd79587" />
<img width="2186" height="1600" alt="shrine-2" src="https://github.com/user-attachments/assets/ad865b54-8ee3-4d89-a4e7-5593f2c3a7be" />


---

## Features

### Browsing
- **Multi-tab browsing** with a Chrome-style tab switcher
- **Incognito mode** with isolated sessions: no history, cookies, cache, or favicons are stored, and everything is wiped when the tab closes
- **Real-time search suggestions** for DuckDuckGo and Google
- **Find in page**, **desktop site mode**, and **page preview** from the link context menu
- **Link and image context menu**: open in new tab, copy, share, download, and search images with Google Lens
- **Custom homepage** or the built-in Start Page

### Start Page
- Customizable **Speed Dial** with drag-and-drop ordering, automatic favicons, letter icons, and accent colors
- Wallpaper options: Material You gradient, solid color, or a photo from your gallery
- Optional start page search bar and tracker statistics

### Privacy and Security
- **Google Safe Browsing** protection against phishing and malware
- **Built-in tracker blocker** covering analytics, advertising, social pixels, and fingerprinting
- **Privacy Dashboard** with blocked-request log, one-tap data wipe, and site permission controls
- Third-party cookie blocking
- Hardened WebView: no JavaScript bridge, local file access disabled, mixed content blocked, invalid SSL connections rejected, and only `http`/`https` navigation allowed
- Granular control over camera, microphone, and location prompts from websites
- Configurable exit behavior: close all tabs and clear session data on exit

### Passwords and Autofill
- **Encrypted password vault** backed by Android Keystore and `EncryptedSharedPreferences`
- Save, update, and autofill prompts for login forms (disabled in Incognito)
- Registers as an **Android Autofill Service**, so it can fill logins in apps as well
- Credentials are excluded from Android cloud backup and device transfer

### Reader Mode
- Distraction-free article view with adjustable font (serif, sans, mono), text size, line spacing, margins, and theme (Auto, Paper, Sepia, Night)
- Estimated reading time

### Downloads
- Download confirmation with editable file name
- Smart file type detection from server headers, file extension, and file signature, so files don't end up as `.bin`
- Default save location in `Downloads/` (with optional subfolder) or any folder you choose through the Android file picker

### Sync and Import
- Sign in with Google to sync bookmarks, history, Quick Access shortcuts, and settings across devices
- Import bookmarks and history from Chrome (`.html` / `.json`) or a Google Takeout `BrowserHistory.json` file

### Languages
- English and Bahasa Indonesia, with the option to follow the system language

---

## Installation

1. Download the latest `Shrine-Browser-<version>.apk` file.
2. Open the APK on your Android device.
3. If prompted, allow your file manager or browser to **install unknown apps** (Settings > Apps > Special access > Install unknown apps).
4. Tap **Install**, then open **Shrine Browser**.

To update, simply install the newer APK over the existing version. Your data is preserved as long as the APK is signed with the same key.

### Enabling Shrine as your Autofill service (optional)

1. Open Shrine Browser > menu > **Saved Passwords**.
2. Tap **System Autofill Settings**.
3. Select **Shrine Browser Autofill**.

---

## Permissions

| Permission | Why it is needed |
|---|---|
| Internet / Network state | Loading web pages and sync |
| Camera | Only when a website requests it and you approve |
| Microphone | Only when a website requests it and you approve |
| Location | Only when a website requests it and you approve |
| Storage (Android 9 and below only) | Saving downloads to the public Downloads folder |

Sensitive permissions are never used silently. Each website request shows a prompt, and you can disable prompts per permission type from the Privacy Dashboard.

---

## Privacy Notes

- Browsing data is stored locally on your device.
- Cloud sync is **optional** and only active when you sign in with Google and keep Auto Cloud Sync enabled. Saved passwords are **not** synced.
- Incognito tabs are never recorded or synced.
- You can clear cache, cookies, web storage, and history at any time from the Privacy Dashboard.

---

## Tech Stack

Kotlin, Jetpack Compose (Material 3), Room, Firebase Authentication and Firestore, Android Credential Manager, AndroidX Security Crypto, and Coil.

---

## Support

Found a bug or have a suggestion? Please reach out to the developer through the channel where you received this APK and include your Android version, device model, and the Shrine Browser version (shown at the bottom of **Settings**).
