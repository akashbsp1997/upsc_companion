# UPSC Companion — 180-day content update

This is an updated static web app for the supplied Codespaces project. It includes 180 dated day entries starting **19 October 2026** and ending **16 April 2027**, an 8-hour daily structure, GS/CSAT/Essay/GS Ethics/PSIR Paper I & II topic progression, daily current-affairs workflows, practice prompts, weekly revision/test days, local task completion, notes, progress summaries and JSON backup/restore.

## Run in GitHub Codespaces
1. Extract this ZIP into your project folder, replacing the existing `index.html` and adding the other files.
2. In the Codespaces terminal, from this folder run: `python3 -m http.server 8000` (or restart your existing server).
3. Open the forwarded port 8000. If the server is already running, refresh the preview.

## Data and offline behavior
Task completion and notes are saved in this browser profile using `localStorage`. The service worker caches the app shell after the first successful visit when served over HTTPS/localhost. Export JSON backups regularly. Clearing site data or using a different browser/device will not carry progress across. This web build does not provide native Android folder access or scanned-PDF OCR.

## Schedule notes
The schedule is a structured preparation framework, not a guarantee of exam coverage. Match it against the latest official UPSC syllabus and current exam notification, and adapt it to your baseline, chosen resources and exam date. Current-affairs entries are workflows/prompts rather than a live news feed. Daily topic entries should be used alongside standard texts and official documents. Weekly review days appear every seventh day; the final 180-day window ends 16 April 2027.

## Included files
- `plan-data.js`: 180 dated daily entries and task lists
- `app.js`: dashboard, plan browser, task persistence, notes, progress and backup/restore
- `sw.js`, `manifest.json`: basic offline app-shell support
- `styles.css`, `index.html`: responsive UI
