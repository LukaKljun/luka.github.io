# SOVEREIGN — Command your day

A mobile-first, local-first gentleman's personal dashboard inspired by classic intelligence briefings and luxury instrument design. Hosted as a standalone folder of the existing `luka.github.io` GitHub Pages repository.

## Open

https://lukakljun.github.io/luka.github.io/sovereign/

## Features

- Daily briefing, daily priorities and chronological timeline
- Missions with linked actions and progress
- A private contacts rolodex with birthdays and follow-up reminders (shown within the app)
- Focus timer, session history and optional browser alerts
- Intelligence dashboards and evening debriefs
- Q, a rule-based **on-device command assistant** (not a generative AI service)
- Import/export iCalendar (.ics) events; import/export JSON backups
- Discreet on-screen masking and offline-capable progressive web app

## Security and limitations

Data stays in this browser's local storage, is **not encrypted**, is not synchronized across devices and may disappear if browser data is cleared. Keep backups. Discreet mode merely obscures on-screen labels. Importing an ICS file does not create a live Google Calendar sync. Recurrence and unusual timezone rules may require manual checking. Q understands a defined set of commands; it is not connected to an AI service or Gmail.

## Development

No build step. Serve this directory over localhost or HTTPS. The root entry point is `index.html`; `styles.css` and `app.js` contain the source. GitHub Pages serves the folder directly once Pages is enabled for the repository.
