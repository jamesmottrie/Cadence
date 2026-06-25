# Cadence — subscription tracker (PWA)

A private, installable subscription tracker. All data stays on your device. Works offline. No accounts, no server.

## What's in this folder

```
index.html        the whole app
manifest.json     makes it installable
sw.js             offline support
icons/            app icons
```

Keep the folder structure exactly as-is (the `icons` folder must stay a subfolder).

---

## Try it locally first (optional)

Just double-click `index.html` to open it in your browser. Everything works except the "install to home screen" step, which needs a real web address (next section).

To see it populated, open it and tap **Load sample data**.

---

## Put it online with GitHub Pages (no terminal needed)

1. Go to **github.com** and sign in. Click the **+** (top right) → **New repository**.
2. Give it a name, e.g. `cadence`. Set it to **Public**. Click **Create repository**.
3. On the new repo page, click **uploading an existing file** (or **Add file → Upload files**).
4. Drag **all the contents of this folder** into the upload area — `index.html`, `manifest.json`, `sw.js`, and the **icons** folder. (Drag the icons folder in too; GitHub keeps the structure.)
5. Click **Commit changes**.
6. Go to the repo's **Settings → Pages** (left menu).
7. Under **Build and deployment → Source**, choose **Deploy from a branch**. Pick branch **main** and folder **/ (root)**. Click **Save**.
8. Wait ~1 minute, refresh. Pages shows your live link, like:
   `https://YOUR-USERNAME.github.io/cadence/`

That URL is your app.

---

## Install it on your iPhone

1. Open the GitHub Pages link in **Safari** (must be Safari, not Chrome, for install on iOS).
2. Tap the **Share** button → **Add to Home Screen** → **Add**.
3. Open it from your home screen. It now runs full-screen like a normal app.

---

## How reminders work

Because there's no server, the app can't push you a notification while it's closed. So it warns you three ways:

- **Due soon** — the dashboard always shows what's coming, with a countdown.
- **In-app alerts** — turn these on in Settings; they fire while the app is open.
- **Calendar reminder (the reliable one)** — on the **Calendar** tab, tap the calendar icon on any item, or **Calendar file** to export everything. This downloads a `.ics` file. Open it and your phone adds the payments (and trial "cancel by" dates) to your real calendar, which *does* alert you even when Cadence is closed. Set how many days before to warn per subscription.

Re-export the calendar file whenever you add or change subscriptions.

---

## Updating the app later

Edit the file(s), then on GitHub: **Add file → Upload files**, drop the changed file in, and commit. Your live URL updates in about a minute. (If an update doesn't show, close and reopen the app — the offline cache refreshes on next load.)

## Backups

Your data lives only in this browser/app. In **Settings**, use **Export backup (JSON)** now and then. If you ever clear the app or switch phones, **Import backup** restores everything.
