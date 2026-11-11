# Fundly

Finance management and budget planner for businesses and individuals. It runs entirely in the browser, with no server, database or sign-up.

## Features
- Business or personal profiles, each with an optional passcode lock
- Income and expense tracking with categories, a cash-flow chart, a spending donut chart and an activity feed
- Goals and targets with progress tracking
- Invoices, debts and VAT tools
- CSV import, plus reports and an audit log
- Backup and restore as a JSON file (Tools → Backup & data)
- Can be installed on a phone or desktop and works offline after the first visit

## Host it on GitHub Pages
1. Create a new repository on GitHub, for example `fundly`.
2. Upload **all** the files in this folder, keeping the `icons/` folder. On GitHub you can drag and drop them under **Add file → Upload files**. Then commit.
3. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose **Branch: `main`** and the **`/ (root)`** folder, then click **Save**.
4. After a minute or two the app will be at `https://<your-username>.github.io/fundly/`.

To install it, open that link and choose **Add to Home Screen** (iPhone/iPad: Share menu, Android: Chrome menu) or the install icon in the address bar on desktop Chrome or Edge.

## Your data
- Everything is saved in the browser's local storage on each device. Nothing is sent to GitHub or any server.
- Each device and browser keeps its own copy. To move data to another device, or from an older copy you opened as a local file, use **Tools → Backup & data → Backup**, then **Restore a backup** on the other device.
- Clearing your browser data deletes your Fundly data, so take regular backups.
- A GitHub Pages site is public, but only the app is published. Your financial data never leaves your device.

## Publishing updates
Replace `index.html` with the new version and commit. Then open `sw.js` and change `VERSION` (for example to `fundly-v2`) so installed copies pick up the update.

## Files
| File | Purpose |
|---|---|
| `index.html` | The whole app (HTML, CSS and JavaScript) |
| `manifest.webmanifest` | App name, icons and colours so it can be installed |
| `sw.js` | Service worker that lets the app work offline |
| `icons/` | App icons |
| `.nojekyll` | Tells GitHub Pages to serve the files exactly as they are |
