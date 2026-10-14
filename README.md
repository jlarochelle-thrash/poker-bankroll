# Poker Bankroll Tracker

An installable web app (PWA) for tracking poker sessions, hand histories and your bankroll. It has no dependencies or build step, works offline once installed, and keeps all data on the device.

## Files
- `index.html`: the whole app (UI, logic, styles)
- `manifest.webmanifest`, `icons/`: what Android needs to install it as an app
- `sw.js`: service worker for offline use. Bump `VERSION` after changing files.

## Installing on Android
Android only installs a PWA from an **https://** address, so host this folder somewhere first. Either of these is free:

- **Netlify Drop:** go to https://app.netlify.com/drop and drag the `poker-bankroll` folder onto the page. You get an https URL.
- **GitHub Pages:** push the folder to a GitHub repo, then turn on Settings → Pages (deploy from branch `main`, folder `/`).

Then on the phone:
1. Open the URL in **Chrome**.
2. Tap ⋮ → **Add to Home screen** → **Install**.
3. Launch it from the home-screen icon. It runs full-screen and works offline.

## Data & backups
Data is saved in the browser storage of the installed app on your phone. The host never sees it.
Use **Settings → Export backup** regularly. The JSON file can be restored on any device with **Restore backup**.
Uninstalling the app or clearing Chrome's site data erases it.
