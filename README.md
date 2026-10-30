# HabitFlow — Offline-first Android habit tracker

## What is included
- Responsive installable web app (PWA) designed for Android phones.
- Dashboard, Daily Tracker, Individual Habit Analysis, Weekly Report, Monthly Report and Habit Settings.
- 15 starter habits, editable; up to 50 habits.
- Daily check-ins, per-habit completion, streaks, weekly/monthly rates, trend charts and heatmap.
- Local browser storage and service-worker cache for offline use after the first successful load.
- JSON backup and restore.

## Run / install on Android
A Progressive Web App must be served from **HTTPS** (or localhost) for installation and service-worker offline caching. It cannot be installed as a PWA by simply opening `index.html` from a file manager.

1. Upload the contents of this folder to a static HTTPS host (for example, GitHub Pages, Cloudflare Pages or Netlify).
2. Open the resulting HTTPS address in Chrome on Android while online once.
3. Open Chrome's menu (⋮) and choose **Install app** or **Add to Home screen**.
4. Launch HabitFlow from the new home-screen icon. After the first successful load, the app shell is cached and the tracker works offline.
5. Use **Backup** regularly to save a JSON copy of your records. Keep the backup outside the app.

## Data and calculation notes
- Records are stored in the browser's local storage on this device and are not sent to a server.
- A missed day is counted in an individual habit's missed-day total only when that calendar date exists in the app's tracking log. Future days are excluded.
- Current streak counts consecutive completed days ending today. Overall streak counts days when every active habit was completed.
- Weekly and monthly percentages use all active habits and all days in the selected period up to today. Historical dates remain stored when changing the displayed month.
- Deactivating a habit hides it from the daily tracker and aggregate active-habit rates, but keeps its old log entries. Reactivating it restores it to active calculations.

## Important
This is a PWA source bundle, not a signed APK. For PWA installation, deploy it to HTTPS first. Clearing Chrome site data can erase local records, so use Backup.
