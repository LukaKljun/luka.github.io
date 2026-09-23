# FLOW — A calendar without the calendar

FLOW is an experimental, mobile-first visual calendar with a daily Flow, event Orbit and non-grid Space Map. Features: local event creation, editing, deletion, search, notes, locations, category colors, free time suggestions, JSON backup/import and iCalendar export. The app is an installable offline-first PWA.

The GitHub Pages deployment includes two gzip + base64 source bundles (app.js.b64 and styles.css.b64) which the loader in index.html decompresses in modern browsers. Readable JavaScript, CSS, HTML and other project files are in the complete FLOW source ZIP delivered with the app. This special packing is for deployment only.

**Google Calendar is optional and not yet connected by default.** To connect, enable the Google Calendar API at https://console.cloud.google.com/apis/library/calendar-json.googleapis.com, configure an OAuth consent screen and add yourself as a tester if necessary, create a Web Application OAuth Client ID, and authorize JavaScript origin https://lukakljun.github.io . Enter the public Client ID in FLOW Settings, then tap Connect Google. Never paste a client secret into the app. Google events are fetched for the signed-in browser session.

GitHub Pages path (if published from main /(root)): https://lukakljun.github.io/luka.github.io/flow/ . On iPhone use Safari → Share → Add to Home Screen. Local event data is stored on your device/browser, not in this GitHub repository.
