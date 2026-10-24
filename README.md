# Garage Bill PWA

Responsive mobile-friendly garage billing app. Features shop settings, preset items and prices, quantity selection, discount, bill preview, PDF download, share sheet, local bill history and CSV export. Data is stored in browser localStorage; no account/backend/database is used.

## Publish using GitHub Pages
1. Create a repository named `garage-bill` on GitHub.
2. Upload all files in this folder into the repository root.
3. Open Settings → Pages → Deploy from a branch → `main` → `/(root)` → Save.
4. Wait for the published HTTPS URL, then open it on your phone.
5. Android Chrome: menu → Install app/Add to Home screen. iPhone Safari: Share → Add to Home Screen.

## Notes
- Sample items are provided; change them in Items & prices.
- Bills and settings are stored on this browser/device only; no cross-device sync or cloud backup.
- PDF download uses jsPDF from a CDN. If unavailable, use Print / Save PDF.
- Do not use as a production accounting system without backups, testing and suitable privacy/security controls.

## Admin PIN for shop settings and prices

- Open **Items & prices** or **Shop settings** for the first time and create a 4–12 digit admin PIN.
- After setup, those pages require the PIN when entering the admin area.
- To change it, open either admin page and tap **Change admin PIN**. Enter the current PIN, then enter and confirm the new PIN.
- Leaving the admin area for Create Bill or Bill History locks the settings again.
- The PIN verifier is stored locally on this browser/device. This is a basic privacy barrier, not strong authentication: because this app is hosted as a static GitHub Pages site, a technically skilled person could bypass client-side checks. Use a trusted device and keep regular data backups.
- The PIN is not included in JSON data backups. If you forget it, the app currently has no secure PIN recovery feature; contact the app maintainer before clearing browser data, because clearing it may also erase local bills.
