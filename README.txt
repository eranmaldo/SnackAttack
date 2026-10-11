SNACK ATTACK v1.1.0 — OFFLINE IPHONE SALES TRACKER
Includes automatic update detection and a user-controlled Restart to update banner.

UPLOAD TO GITHUB PAGES
Upload ALL files in this folder into the ROOT of the existing SnackAttack GitHub repository.
index.html, sw.js, manifest.webmanifest, and icon-*.png must all be in the SAME root directory.
Commit changed files, then wait for GitHub Pages deployment.
Do not upload the ZIP as a single file and do not nest inside a SnackAttack folder.

UPDATES
Existing Home Screen installations do not need reinstalling.
On an online launch or when returning to the app, a new service worker is checked.
When a newer version has downloaded, a Restart to update banner appears.
Choose Later to keep working, or Restart to update to activate and reload.
An initial update from v1.0 may activate immediately because the OLD service worker used skipWaiting.
After v1.1 is installed, subsequent updates can use the approval banner.
Keep the same GitHub Pages URL and storage origin to preserve device data.

TESTING
1. Start a local HTTP server from this folder: npx --yes http-server . -p 8000 -c-1
2. Open http://localhost:8000, confirm logo and app features.
3. In browser DevTools > Application > Service Workers, verify registration.
4. Test offline with DevTools Offline or Airplane Mode AFTER an online visit.
5. To test update notification, deploy a future version with a NEW CACHE value in sw.js.
6. Test backup export. Do not clear site data: IndexedDB contains sales records.

SAFETY
Sales records remain in local IndexedDB; updates do not intentionally modify the database.
Always export a JSON backup before major updates.
Offline updates require internet temporarily to download new app files.
