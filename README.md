# Workout Tracker

A simple workout tracker for iPhone. Log exercises, sets, weight and reps, then save the finished workout to Google Calendar as an event.

Live at: https://mkloi9988.github.io/Workout-Tracker/

## Files
- `index.html`: the whole app (layout, styles and code)
- `manifest.webmanifest`, `apple-touch-icon.png`, `icon-512.png`: home-screen app name and icon

## Google Calendar setup (one time)
1. Go to https://console.cloud.google.com and create a project (e.g. "Workout Tracker").
2. APIs & Services → Library → enable **Google Calendar API**.
3. APIs & Services → OAuth consent screen: set it to External, add your app name and email, then add your own Gmail under **Test users**.
4. APIs & Services → Credentials → Create credentials → **OAuth client ID** → Web application.
   - Authorized JavaScript origins: `https://mkloi9988.github.io`
   - Authorized redirect URIs: `https://mkloi9988.github.io/Workout-Tracker/`
5. Copy the Client ID into `CLIENT_ID` in `index.html`.

Your workout stays on your phone until you save it. Google sign-in lasts about an hour, and the app asks you to sign in again after that.
