# UPSC Companion — beginner-friendly offline-first web app

A small, framework-free web app for personal UPSC study. It uses HTML, CSS and JavaScript and saves notes, tasks, plans, flashcards and quiz data in your browser's `localStorage`.

## Features
- Dashboard and daily checklist
- Notes maker with subjects, tags, search, backup export/import
- Scroll reader for saved notes, with text-size control and bookmark position
- Flashcards and simple self-rating
- Study planner and study-time log
- Custom MCQ bank with answer explanations and score tracking
- PDF library and text extraction for PDFs that contain selectable text
- Basic service-worker caching for offline use after first load

## Important limitations
- No account or cloud sync. Data stays in the browser profile on this device.
- Export JSON backups regularly. Clearing browser data can erase your work.
- PDF reader extracts selectable text only; scanned/image-only PDFs need OCR. It processes at most 30 pages per import in this starter.
- The PDF.js library is loaded from a CDN, so PDF reading needs internet unless you download and self-host PDF.js. The core notes/planner works offline after the app has been cached.
- This is a starter app, not an official UPSC question bank. Add your own questions and content.
- For best offline/PWA behavior, serve over `localhost` or HTTPS; opening the HTML file directly may limit service-worker features.

## Run locally
Python 3:
```bash
python -m http.server 8000
```
Open `http://localhost:8000`.

## Run in GitHub Codespaces
From the folder containing `index.html`:
```bash
python -m http.server 8000 --bind 0.0.0.0
```
Open the forwarded port 8000 in the Ports tab. Use the preview's HTTPS URL.

## Install on Android
1. Open the app URL in Chrome.
2. Open the browser menu and choose **Add to Home screen** (or **Install app**, if shown).
3. Launch it from the home screen. Open it once while online so the app shell can cache.
4. Export backups from Notes regularly.

## Data backup
Use **Notes maker → Export backup** to download `upsc-companion-backup.json`. To restore, choose **Import backup** and select the file. Import replaces current app data after confirmation.

## Files
- `index.html`: app structure
- `styles.css`: responsive visual design
- `app.js`: all app behavior and local data storage
- `manifest.json`: install metadata
- `sw.js`: service worker for app-shell caching
