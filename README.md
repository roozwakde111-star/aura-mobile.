# AURA Mobile Companion v0.6

A mobile-first installable web app for Android Chrome. It provides push-to-talk speech capture (where browser speech recognition is supported), editable transcripts, spoken status, and a local task inbox.

## Important status

This is a **phone-side prototype**, not a deployed cloud service or autonomous agent. Tasks are stored in the browser's local storage on this phone. They are not transmitted to the existing FastAPI backend and are not executed. The existing v0.5 backend has no authentication and must not be exposed to the public internet.

## Install on Android

1. Host this folder on an HTTPS static host (for example, a private static deployment you control). Browser microphone access and PWA installation require a secure context; `localhost` is the main exception.
2. Open the HTTPS address in Chrome on Android.
3. Allow microphone access only when you tap **Tap to speak**.
4. Open Chrome's menu and choose **Add to Home screen** or **Install app** if offered.
5. Launch AURA from the home screen.

## Current capabilities

- Mobile responsive interface.
- English (India) and Hindi speech-recognition language selection.
- Push-to-talk, editable transcript, text-to-speech status.
- Local task inbox and JSON export.
- No always-on microphone, no external execution, no social account access, no file access, no payments, no publishing.

## Next required engineering before cloud operation

- Add authentication (passkeys/OAuth or strong device-bound credentials) to the backend.
- Add TLS, rate limits, audit and session controls.
- Add authenticated API connectivity and per-task authorization.
- Deploy backend to a private cloud environment; never expose the current unauthenticated prototype.
- Add model routing, tool execution workers, approval workflow and verified results.
