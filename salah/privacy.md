# Privacy Policy — Salah

_Last updated: 2026-04-20_

_Published at: https://irtiza07.github.io/ios-apps/salah/_

Salah is a prayer companion app. This policy explains what the app does with your data. We wrote it to be readable — no dark patterns, no hidden clauses.

## The short version

- **No accounts, no sign-in.** You don't create a user, you don't share data with us.
- **No analytics, no tracking, no ads.** We do not run analytics, crash reporting, or advertising SDKs.
- **Your prayer logs and settings never leave your device.** They are stored in a local SQLite database on your phone.
- **Your location is used on-device** to compute prayer times and qibla direction. It leaves your device only when you explicitly tap "Nearby Mosques", and only to query Google's Places service.

## What data the app uses

### 1. Location

- **What:** Your device's approximate latitude and longitude, plus the reverse-geocoded city and country name.
- **Why:** Prayer times (Fajr, Dhuhr, Asr, Maghrib, Isha) depend on sun position at your location. Qibla direction is a bearing from your location to Makkah. "Nearby Mosques" needs your location to query places near you.
- **How it's stored:** Cached locally on your device in SQLite and in app storage so the app works offline and does not re-query every launch.
- **Who else sees it:**
  - When you open **Nearby Mosques**, your coordinates are sent to **Google Places API** to retrieve a list of nearby mosques. Google's use of that data is governed by [Google's Privacy Policy](https://policies.google.com/privacy).
  - Otherwise, your location never leaves your device.
- **You can revoke location access** at any time in iOS Settings → Privacy & Security → Location Services → Salah. The app will show an explanatory empty state if location is denied.

### 2. Prayer logs

- **What:** For each prayer, whether you prayed it, whether it was on time, late, at the mosque, or missed, plus an optional note you type in.
- **Why:** Track your prayers in the Track and Insights tabs.
- **Where:** A local SQLite database on your device. They are **never** sent anywhere.
- **Deleting:** Uninstalling the app removes this data permanently. There is no cloud backup (yet).

### 3. Settings

- **What:** Your choice of calculation method, madhab, theme preference (light/dark/system), notification preferences, and favorited duas.
- **Where:** Local SQLite + AsyncStorage. Never transmitted.

### 4. Notifications

- **What:** Local prayer-time reminders scheduled via iOS's own notification system.
- **How:** The app computes upcoming prayer times on-device and schedules local notifications with iOS. Notifications are **not** pushed from a server — no server is involved.
- **Revoking:** iOS Settings → Notifications → Salah.

## What the app does NOT do

- No user accounts
- No cloud sync
- No analytics (Segment, Amplitude, Mixpanel, PostHog, Firebase, etc.)
- No crash reporting (Sentry, Bugsnag, etc.)
- No advertising SDKs
- No third-party tracking or fingerprinting
- No selling or sharing your data with third parties
- No cross-app or cross-device tracking

## Third-party services

The only external service the app talks to is:

- **Google Places API (New)** — queried only when you open Nearby Mosques. Your coordinates and a search radius are sent. No personal identifier is attached. See [Google's Privacy Policy](https://policies.google.com/privacy).

## Children's privacy

Salah does not knowingly collect data from children under 13. There is no user account and no personal information is ever transmitted.

## Data retention

Data lives on your device until you delete the app. Cached location is refreshed automatically as you move. There is no server-side retention because there is no server.

## Changes to this policy

If this policy changes materially, a new version will be published with an updated date at the top. Material changes will also be noted in app release notes.

## Contact

Questions or concerns? Email: **support@irtizahafiz.com**
