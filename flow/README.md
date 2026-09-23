# FLOW — A calendar without the calendar

FLOW is an experimental, mobile-first, installable web app that makes time feel like an environment instead of a grid.

- **Flow:** an organic daily timeline with floating event cards and free-time context.
- **Orbit:** one appointment in focus, with neighboring commitments floating around it.
- **Space:** a constellation of upcoming events, grouped by proximity in time, plus open time windows instead of a week grid.
- **Calendar essentials:** create, edit, delete, search, event categories, notes, location, date navigation, local-first storage, JSON backup/import, and `.ics` export.
- **Google Calendar:** optional in-browser OAuth to import, create, edit, and delete events in your primary calendar. No client secret or backend required. Requires a Google Cloud OAuth web client ID configured by the user.
- **iPhone:** Safari → Share → Add to Home Screen. The service worker supports offline use of the app and locally stored events.

## Google Calendar setup

1. Enable the **Google Calendar API** in [Google Cloud Console](https://console.cloud.google.com/apis/library/calendar-json.googleapis.com).
2. Configure an OAuth consent screen and, if the app is in Testing mode, add yourself as a test user.
3. Create an OAuth **Web application** client. Add the GitHub Pages *origin* `https://lukakljun.github.io` (not the `/luka.github.io/flow/` path) to **Authorized JavaScript origins**. Add `http://localhost:8080` for local testing if needed.
4. In FLOW → Settings, paste the **Client ID** (the public identifier, *never* a client secret), save it and tap **Connect Google**.
5. Allow requested calendar event access. Google events remain in the current browser session; local events are saved in browser storage. Reconnect after a page reload to fetch updated Google events.

Calendar data is transmitted directly between the browser and Google's Calendar API after the user authorizes access. FLOW itself runs as static files on GitHub Pages; it has no server, analytics or hidden account database.

## Hosting

This project lives inside `LukaKljun/luka.github.io/flow/`. If the repository has GitHub Pages configured to publish the `main` branch from `/ (root)`, visit `https://lukakljun.github.io/luka.github.io/flow/`. If it uses another Pages configuration, update that configuration or use the corresponding published URL. Google OAuth's allowed origin depends on the actual hosting domain.

## Local development

From this directory, run `python3 -m http.server 8080` and open `http://localhost:8080` (a server is necessary to test the service worker and GIS origin configuration).
