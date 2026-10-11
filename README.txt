SNACK ATTACK v1.0 — OFFLINE IPHONE DAILY SALES TRACKER

CONTENTS
index.html — complete application
manifest.webmanifest — iPhone/PWA installation metadata
sw.js — offline application cache
icons/ — app icons derived from your supplied logo

HOW TO TEST ON YOUR COMPUTER
1. Extract the ZIP.
2. Open a terminal in the extracted snack_attack_app folder.
3. Run: python -m http.server 8000
4. Visit http://localhost:8000 in Chrome, Edge, or Safari.
5. Add a product, start a day, tap + and -, and end the day.
6. Reload and confirm your data persists. Test offline after the first load.

HOW TO INSTALL ON IPHONE
1. Upload the extracted app folder contents to a static HTTPS host such as GitHub Pages, Netlify, or Cloudflare Pages. Hosting serves only app files; your sales records stay on the iPhone.
2. On the iPhone, open the HTTPS site in Safari while online.
3. Tap Share > Add to Home Screen > Add.
4. Open Snack Attack from the new icon once while online.
5. Enable Airplane Mode and verify that the app still launches, records sales, and keeps data after closing and reopening.

IMPORTANT
- Do not open index.html directly from the iPhone Files app; offline caching requires HTTPS and a service worker.
- Data is saved in the installed app's local IndexedDB, not in a cloud account.
- Do not delete the app or clear website data before exporting a JSON backup.
- The Weekly screen exports completed daily records to CSV and a full JSON backup; use the Files app to keep backups.
- A day can only be finalized once. Start a new day with fresh quantities; nothing carries over automatically.
- Editing product prices only affects future days, not active or completed sales records.
- Changing a product's price during an active day will take effect on the next day, not the active session.
- If your brother brings more stock of a product already active that day, this v1 app does not support increasing that item's starting quantity; set the full daily amount before beginning.
- If the app is served from a different URL/domain, local records do not move automatically. Export/restore a backup.
