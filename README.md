# HillCharge — Offline EV Hill-Trip Planner

A self-contained, offline-first website prototype for planning EV journeys through hill routes where mobile internet coverage may be unreliable.

## Run it
1. Download `index.html`.
2. Save it on your laptop.
3. Open the file in a current browser (Chrome, Edge, Firefox).
4. It needs no internet connection, installation, account, third-party library, map API or external server.

## Features
- Calculates estimated range to a configurable battery reserve.
- Uses locally saved charging-point markers to suggest a charging sequence.
- Lets a user add and remove charging points.
- Saves data locally in the browser when browser storage is available.
- Exports/imports charging data as JSON.
- Exports a plain-text trip summary.
- Uses fictional demo markers at first; users must replace them with independently confirmed charging points.

## Important limitations
- This is an ideathon prototype, not a production navigation or safety system.
- It cannot discover charging stations or check availability live while offline.
- It does not include a map, GPS, elevation profile, traffic, road closures, charging queues, connector verification or guaranteed range.
- It estimates each stop as able to charge the vehicle to the configured target state of charge.
- Hill climbs, temperature, speed, detours, vehicle load and charger failure can materially change results.
- Verify charging points, connector compatibility, access and opening hours from reliable current sources before any actual trip.

## Technical detail
All CSS and JavaScript are embedded in `index.html`; the page makes no network requests. It is a local offline web app, not a hosted progressive web app. A production PWA with service-worker installation would normally require HTTPS or localhost for initial installation, but that is not needed to open this single HTML file offline.
