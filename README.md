# Spend Log

A small personal app for tracking what you spend each month. You type in your own share of each spend, and it shows the month by category, your limits, and a yearly view.

Everything is stored on your phone, in the browser. There is no server, no account and no login.

## Files

| File | What it does |
|---|---|
| `index.html` | The app itself |
| `sw.js` | Lets the app open without internet |
| `manifest.webmanifest` | Gives it the app name and full-screen mode on the home screen |
| `icon-192.png`, `icon-512.png` | Home-screen icon |

All five files must be uploaded together.

## Put it online (GitHub Pages, free)

1. Create a new public repository on GitHub, for example `spend-log`.
2. Upload the five files to the top level of the repository (not inside a folder).
3. Go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**, and save.
4. After a minute or two the page shows your link: `https://<your-username>.github.io/spend-log/`.

## Add it to your phone

- **Android (Chrome):** open the link, tap the ⋮ menu, then **Add to Home screen**.
- **iPhone (Safari):** open the link, tap **Share**, then **Add to Home Screen**.

Open it from the home-screen icon from then on.

## Using it

- **Add (home):** type the amount (your share only), pick a category, and tap **Save spend**. Below the form you see this month's spending by category with limit balances, and your last few days of entries.
- **Month / Year:** switch between the two at the top. Use the arrows to move between months or years. Tap an entry to edit or delete it. Tap a month bar in Year view to open that month.
- **Backup:** export, import, categories, monthly limits, and currency.

### Monthly limits

On the Backup screen, each category has a **Monthly limit** box. Type an amount to set it, or leave it empty for no limit. You can also set one when creating a new category. Limits reset at the start of each month. Going over is allowed; the home screen shows how much you are over in red.

## Backups (important)

Your data lives only in this browser on this phone. It is lost if you clear browser data, uninstall the browser, or lose the phone.

- Tap **Export backup (JSON)** about once a week and keep the file somewhere safe (Google Drive, email it to yourself). The home screen reminds you when your last backup is more than 7 days old.
- **Export CSV** gives a spreadsheet of all entries for Excel or Google Sheets. It cannot be imported back.
- **Import backup** reads a JSON backup. If the phone already has entries, you can either add only the new ones or replace everything.

## Moving to a new phone (Android → iPhone)

1. On the old phone, tap **Export backup (JSON)** and save the file somewhere you can reach from the new phone.
2. On the new phone, open your GitHub Pages link in Safari and add it to the home screen.
3. Open the app, go to **Backup → Import backup**, and choose the file.

Data belongs to the exact address you open the app from. If you change the link (a new repository name, for example), export from the old link and import on the new one.

## Updating the app

When you change any file:

1. Open `sw.js` and raise the version number on the `CACHE` line, for example `spendlog-v7` to `spendlog-v8`.
2. Upload all changed files to GitHub.
3. On your phone, open the app, close it fully, and open it again to load the new version.

Without step 1, phones may keep showing the old version.
