# FLOW — A calendar without the calendar

FLOW is an experimental, mobile-first, installable calendar interface. Instead of seven-column grids it uses a winding daily Flow, a central event Orbit, and an organic Space Map of floating commitments and open time windows.

Features: event creation, editing, deletion, search, notes and locations, free-time suggestions, local storage, JSON backup and import, .ics export, example events, and offline home-screen installation on iPhone.

This folder contains the readable original HTML, JavaScript, and CSS source. No dependencies or build tooling. Open via a local HTTP server or GitHub Pages. Pages URL when publishing main from / (root): https://lukakljun.github.io/luka.github.io/flow/ .

## Google Calendar

Google Calendar integration uses user-initiated OAuth directly in the browser; it is not connected by default. To connect:
1. Enable Google Calendar API in https://console.cloud.google.com/apis/library/calendar-json.googleapis.com .
2. Configure an OAuth consent screen. Add yourself as a test user while in Testing.
3. Create a Web Application OAuth Client ID and authorize JavaScript origin https://lukakljun.github.io (no URL path).
4. Enter the public client ID (never a secret) in FLOW Settings and select Connect Google.

App data stays on your device unless you explicitly connect and modify Google events. Safari → Share → Add to Home Screen installs the web app.
