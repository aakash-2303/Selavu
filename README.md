# Kharcha: personal expense tracker

Offline web app. Install it on your phone's Home Screen. All data stays on the device.

## Files
- `index.html`: the whole app
- `manifest.webmanifest`, `sw.js`, `icons/`: let it install and work offline

## Deploy on GitHub Pages (about 5 minutes, free)
1. On github.com, create a new repository, e.g. `kharcha`. It can be public. Your data is never uploaded, only the app code.
2. Choose **Add file → Upload files**, drag in everything from this folder (including the `icons` folder), then **Commit**.
3. Go to **Settings → Pages**. Under Source, pick **Deploy from a branch**, then branch `main`, folder `/ (root)`, and **Save**.
4. After about a minute the site is live at `https://<your-username>.github.io/kharcha/`.

## Install on iPhone
1. Open that URL in **Safari**.
2. Tap **Share → Add to Home Screen → Add**.
3. Launch it from the Home Screen icon. From then on it opens full screen and works offline.

Use the Home Screen icon, not a Safari tab. Data saved in the installed app is separate from Safari's and is better protected from automatic clearing.

## Keep your data safe
- **Settings → Save a backup** creates a `.json` file. Save it to iCloud Drive or Files, and do this monthly.
- **Settings → Restore from a backup** loads it back, for example on a new phone.
- **Export as CSV** opens in Excel or Numbers.

## Updating the app later
Upload the new `index.html`. Also change `VERSION` in `sw.js` (e.g. `kharcha-v2`) so phones pick up the update. Your data is unaffected.

## How recurring expenses post
Each time the app opens, it adds any recurring entries whose day has arrived, for every month since the item's start month. Each entry is created once per item per month, so it never duplicates. If you delete one, it stays deleted.
- **Add automatically**: posted at the set amount. Use for rent, wifi, SIM and subscriptions.
- **Ask me to confirm**: shows under "To confirm" with your estimate until you enter the actual bill amount. Use for electricity. Unconfirmed bills aren't counted in totals.
