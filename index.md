---
layout: default
title: Pitru Calendar — Privacy Policy
---

# Pitru Calendar — Privacy Policy

**Effective Date:** June 6, 2026
**App:** Pitru Calendar (`family.sadhasiva.pitru`)
**Developer:** Sadhasivasubramanian Hariharasubramanian
**Contact:** sadhasiva1984@gmail.com

---

## Summary

**Pitru Calendar does not collect any personal data.** Everything you enter — ancestor records, srardham dates, family details, preferences — stays on your device. Nothing is sent to us, to any third party, or to any analytics service. There is no account, no login, no online sync, and no telemetry.

This privacy policy describes that posture in detail and lists every system API the app uses to which Apple's Required Reason API rules apply.

---

## 1. Data we collect

**None.**

The app's data model — your ancestors, your gothram preference, your tradition selection (Iyer/Iyengar), your notification subscriptions — lives entirely in the local SwiftData database on your device. It never leaves your device.

In our App Store privacy declaration, every category under "Data Used to Track You" and "Data Linked to You" is empty. The same is true of "Data Not Linked to You."

This matches the [`PrivacyInfo.xcprivacy`](https://developer.apple.com/documentation/bundleresources/privacy_manifest_files) manifest bundled with the app, which sets `NSPrivacyCollectedDataTypes` to an empty array.

## 2. Tracking

**We do not track you.**

The app's privacy manifest sets `NSPrivacyTracking = false` and `NSPrivacyTrackingDomains` to an empty list. The app does not display the App Tracking Transparency prompt because there is nothing to ask permission for.

## 3. Third parties

**None.**

The app does not embed any third-party SDK. Its only external Swift package is [Yams](https://github.com/jpsim/Yams) (a YAML parser used to load the bundled panchanga data; MIT licensed). Yams does no network I/O.

The app makes no network requests of its own. It does not contact our servers, advertising networks, analytics services, or any other backend. All panchanga data, festival catalog, eclipse data, and Vakya/Drik overrides are bundled with the app at install time.

## 4. Required Reason API declarations

Apple requires apps to declare a reason for using certain system APIs. Below is every API category our app uses and the corresponding Apple-approved reason code (mirroring the `PrivacyInfo.xcprivacy` file in the bundle):

| API category | Apple code | Why we use it |
|---|---|---|
| User Defaults (`UserDefaults`) | `CA92.1` | Reading and writing the app's own preferences (locale, tradition, onboarding state, per-observance subscription toggles). The store is scoped to the app's own container. |
| File Timestamp (`Date()` on file metadata) | `C617.1` | Internal timestamps used by the event materializer and the local notification scheduler. All operations are on files inside the app's own sandbox. |
| System Boot Time (`mach_absolute_time`) | `35F9.1` | Foundation uses this internally for some Date arithmetic. The app does not access boot time directly; the declaration covers system-level usage. |

The app does **not** use any other Required Reason API category (no Disk Space query, no Active Keyboards query, no File Access timestamps beyond its own container).

## 5. Notifications

The app schedules **local notifications** for upcoming srardham dates and tarpanam reminders. Local notifications are delivered by iOS itself; they do not involve any push notification server, Apple Push Notification service (APNs), or our infrastructure. The app uses `UNUserNotificationCenter` only — never the remote notification APIs.

You control which observances trigger notifications via the Subscriptions screen. Disabling an observance immediately cancels its pending reminders.

## 6. Permissions

The app requests:

- **Notifications** — required for srardham and tarpanam reminders to fire. Granted on first launch via the standard iOS prompt. You can revoke this at any time in Settings → Notifications → Pitru Calendar.

The app does **not** request:

- Location services
- Photos / Camera
- Contacts / Address Book
- Microphone
- Bluetooth
- HealthKit
- Tracking permission (App Tracking Transparency)

## 7. iCloud and Sync

The app is **device-only** in version 1. iCloud sync is feature-flagged off; the iCloud entitlement is not requested.

A future version may add iCloud sync between your own devices via Apple's CloudKit private database. If we add that feature, this policy will be updated, and you will see an in-app prompt the first time the feature is offered. We will never sync your ancestor data to any database we control.

## 8. Children

The app does not knowingly collect data from anyone, including children under 13.

## 9. Data export and deletion

The app supports an encrypted export feature that writes your full data set (ancestors, preferences, subscriptions) to a `.pitru` file on your device. The export is encrypted with a passphrase you supply (AES-GCM with PBKDF2 key derivation). The file never leaves your device unless you share it — for example, AirDrop to another phone you own, or save it to your iCloud Drive folder for backup.

**To delete your data**, uninstall the app. iOS removes the app's entire sandbox including the SwiftData store. There is no remote copy to delete because we never had one.

## 10. Changes to this policy

If we materially change how the app handles data — for example, by introducing iCloud sync or a future opt-in telemetry feature — we will update this page and bump the **Effective Date** at the top. The App Store listing's "What's New" section for the corresponding release will describe the change.

We will never retroactively change the on-device data handling of an existing release. If you do not want to accept a future change, you can choose not to update.

## 11. Contact

Privacy questions:

- Email: **sadhasiva1984@gmail.com**
- Subject line: "Pitru Calendar privacy"

We will respond to good-faith privacy questions within 30 days.

---

*This privacy policy mirrors the machine-readable [`PrivacyInfo.xcprivacy`](https://developer.apple.com/documentation/bundleresources/privacy_manifest_files) manifest shipped with every release of the app. If the two ever disagree, the manifest is authoritative because it is what Apple's App Store review system reads — but we maintain this page to match.*
