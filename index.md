# PomoDuo Privacy Policy

**Last updated:** November 2026

PomoDuo is a collaborative Pomodoro timer that helps you and a study partner hold each other accountable during focus sessions. We take your privacy seriously and have designed the app to collect the absolute minimum data needed to function.

## What We Collect

| Data | Purpose | Stored Where | Retention |
|---|---|---|---|
| **Account ID** | A random Firebase user ID that identifies your account for friends, pairing and session sync. You can start without signing in. | Firebase Authentication | Until you delete your account. |
| **Email address** (optional) | Only if you sign in with email, or with Apple and choose to share it. Used to sign you in and recover your account. | Firebase Authentication | Until you delete your account. |
| **Display name** (optional) | Shown to your friends and study partners. You choose it, or it comes from Sign in with Apple. | Firestore (`users/{id}`) and your friendships | Until you change it or delete your account. |
| **Username** (optional) | Lets friends find you and powers your friend link. | Firestore (`usernames/`, `users/{id}`) | Until you delete your account. |
| **Friends and friend requests** | Your friend list and pending requests. | Firestore (`friendships/`, `friendRequests/`) | Until you remove a friend or delete your account. |
| **Focus stats** | Minutes focused today, this week and in total, your current streak and last session date, for the friends leaderboard. | Firestore (`users/{id}`) | Until you delete your account. |
| **Push token** | Delivers notifications when a friend sends a request or your partner starts, pauses, resumes or ends a session. | Firestore (`users/{id}/private/device`), readable only by you | Refreshed automatically; deleted when it expires or when you delete your account. |
| **Session state** | Syncs a paired timer (focus, break, paused) between both devices in real time. | Firestore (`sessions/{id}`) | Deleted with your account. |
| **Heartbeat timestamp** | Once-per-minute timestamp during a paired session, so your partner isn't left waiting if your phone dies. | Firestore (inside the session) | Deleted with the session. |
| **Pairing code** | A temporary 6-character code used to link two devices. | Firestore (`pairingCodes/{code}`) | Deleted once used, or within about an hour if unused. |
| **Session history** | Your completed focus rounds. | On-device only (SwiftData) | Stored locally. Never uploaded; only the totals above are shared. |
| **App selection tokens** | Opaque tokens for the apps you choose to block. Managed by Apple's Screen Time API. | On-device only | Cleared when you remove the selection. |

Feedback you send from **Settings → Suggest a Feature** opens your own Mail app with a pre-filled message. Nothing is sent unless you choose to send that email.

## What We Do NOT Collect

- **No browsing history.** We never see which apps you use, which websites you visit, or how often. Websites shown in Apple's app picker come from your iPhone's Screen Time and are never shared with PomoDuo.
- **No app names or bundle IDs.** Apple's Screen Time API uses opaque tokens, so we cannot see which apps you selected.
- **No location data.**
- **No contacts or address book access.**
- **No health data.**
- **No analytics, crash reporting or tracking.** Google Analytics is disabled in our Firebase project, and PomoDuo does not track you across other companies' apps or websites.
- **No advertising identifiers.**
- **No third-party SDKs** beyond Firebase (Authentication, Firestore, Cloud Messaging).

## Screen Time API

PomoDuo uses Apple's Family Controls and Managed Settings frameworks to block distracting apps during focus sessions. This works through opaque tokens - your specific app choices are never visible to us, our servers, or your study partner. Both partners must explicitly opt in to each session. Either partner can pause or end the session at any time, immediately removing all restrictions.

## Data Sharing

We do not sell or share your data, and we do not use it for advertising. Google (Firebase) stores and processes it on our behalf to run the app.

**Your friends** can see your display name, username, focus stats and streak on the leaderboard.

**Your study partner** can also see your current session state (focusing, on break, paused) and whether your device is active during a session.

No one else can read these: our database rules limit each record to the people it belongs to. Nobody can see which apps you block, your detailed session history, or your push token.

## Data Deletion

- **Your account** can be deleted from **Settings → Account → Delete Account**. This removes your profile, username, friendships, friend requests, sessions, partnerships, pairing codes and push token from our servers. A server-side cleanup repeats this in case the app is interrupted.
- **Pairing codes** expire and are deleted automatically.
- **Local history** stays on your device and is removed when you uninstall the app.

## Children's Privacy

PomoDuo does not knowingly collect data from children under 13. The app requires Apple's Screen Time authorization (for: .individual), which is designed for personal use by the device owner.

## Contact

If you have questions about this privacy policy, please contact us at arieltyson30190@gmail.com.
