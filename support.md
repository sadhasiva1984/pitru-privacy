---
layout: default
title: Pitru Calendar — Support
---

# Pitru Calendar — Support

**App:** Pitru Calendar (`family.sadhasiva.pitru`)
**Developer:** Sadhasivasubramanian Hariharasubramanian

---

## Get help

The fastest way to reach me is by email:

**📧 sadhasiva1984@gmail.com**

Subject line: "Pitru Calendar — <short description>"

I respond to support questions within 1–3 days.

## Common questions

### The app crashes / shows the wrong date / a notification didn't fire

Email me with:

1. The version number (Settings → About inside the app)
2. The device model and iOS version (Settings → General → About on iOS)
3. What you were doing when the issue happened
4. The expected behavior vs. what you saw

A screenshot helps but is optional. I never ask for personal information; please don't share names or birthdates of real ancestors in a support email.

### How do I back up my ancestor data?

Settings → Export. Choose a passphrase you can remember. The file is encrypted with AES-GCM (per ADR 0008 in the codebase) and lives on your device. Share it with yourself via AirDrop or save it to your iCloud Drive folder to keep it across device upgrades.

### How do I restore from a backup?

Settings → Import. Pick the encrypted `.pitru` file and enter the passphrase you used at export time.

### Can I use the app without notifications?

Yes. Tap "Don't Allow" when the iOS notification prompt appears, or revoke later in iOS Settings → Notifications → Pitru Calendar. The app still works — you just won't get reminders.

### Is there a watch app?

Yes, a companion watchOS app ships in the same bundle. Install the iPhone app first; the watch will offer to install the watchOS app automatically.

### Where are the panchanga dates from?

The bundled data is computed via Swiss Ephemeris (Drik baseline) and cross-checked against Pambu Panchangam (Vakya) for the years 2026–2035. Specific Vakya/Drik divergences are surfaced as "(வாக் / Vakya)" and "(த்ருக் / Drik)" pills on the affected days.

### How do I report a wrong tarpanam date?

Email me with the specific date and the source you're cross-referencing against (Vaithikasri, Pambu, or another almanac). I add per-year overrides on a rolling basis as discrepancies are confirmed.

## Privacy

See the [privacy policy](./) for details on data handling. tl;dr: the app collects no data, and everything you enter stays on your device.

## Source code

The app's source is not public, but the bundled `PrivacyInfo.xcprivacy` manifest is — that's what Apple's App Review machine pipeline reads, and it's what determines the App Store privacy nutrition label.
