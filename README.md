# Truth or Dare

A standalone party game (Truth or Dare) that runs in any browser and installs to your iPad home screen. No app store, no accounts, works offline once installed.

---

## Files in this folder

| File | What it is |
|---|---|
| `index.html` | The whole game |
| `sw.js` | Service worker (makes it work offline) |
| `manifest.webmanifest` | Home-screen install info |
| `icon-180.png` / `icon-192.png` / `icon-512.png` | App icons |

Upload all of these **loose** (not zipped) to GitHub.

---

## Part 1 — Put it online with GitHub Pages

Do this once. Later updates only repeat Part 3.

1. Go to **github.com** and sign in.
2. Click **+** (top right) then **New repository**.
3. Name it `truthordare`. Set it to **Public**. Click **Create repository**.
4. On the new page, click the **uploading an existing file** link.
5. Drag all the files from this folder onto the upload box. Wait for every file to appear in the list.
6. Click **Commit changes**.
7. Click the **Settings** tab, then **Pages** in the left sidebar.
8. Under **Source**, choose **Deploy from a branch**. Set branch to **main** and folder to **/ (root)**. Click **Save**.
9. Wait about 2 minutes, refresh the page. It shows: **Your site is live at** `https://YOUR-USERNAME.github.io/truthordare/`

That link is your game. It works on any device.

---

## Part 2 — Install on the iPad

1. Open the live link in **Safari** on the iPad.
2. Tap the **Share** button (square with an up arrow).
3. Tap **Add to Home Screen**, then **Add**.
4. **Close the Safari tab.** From now on, always open the game from the **home screen icon**, never from Safari.

Why: Safari erases website data after about 7 days. The home screen app does not. They also do not share data, so anything you import in Safari will not show up in the home screen app. Do everything in the home screen app.

Android: open the link in Chrome, tap the three-dot menu, **Add to Home screen** / **Install app**.

---

## Part 3 — Update the game later

When there is a new `index.html` (or any file):

1. Go to your `truthordare` repo on GitHub.
2. Click the file you want to replace (e.g. `index.html`).
3. Click the **pencil** (Edit) icon, or click **Add file → Upload files** and drop the new version in to overwrite.
4. Click **Commit changes**.
5. Wait 1 to 2 minutes. On the iPad, close the app fully (swipe it away) and reopen it from the home screen icon. The service worker pulls the new version.

If the update does not show, remove the home screen icon and re-add it (Part 2).

---

## Editing your Truths and Dares

Everything lives on your device, not on GitHub. The public link only holds the empty game shell. Your custom list never leaves the iPad.

1. Open the game from the home screen icon.
2. Tap the **pencil** icon (top right).
3. **Add / edit / delete** any item inline, or:
   - **Import** a spreadsheet exported as CSV. Columns: `Type, Level, Timer, Text` (Type = Truth/Dare, Level = Wimpy/Easy/Medium/Hard/Extreme, Timer = seconds or blank). A header row is optional.
   - On import you choose **Replace** the whole list or **Add** to it.
   - **Export** writes your current list back out as a `.txt` you can keep as a backup.

---

## Playing

- Pick number of players (2 to 5), then a face for each.
- Tap **Spin**. The reel scrolls and lands on a player.
- Tap **Truth** or **Dare**.
- Timed dares: tap the play button, the last 5 seconds beep, a buzzer ends it.
- **Punishment** gives that player a dare as a penalty; tap **Back to original** to return to their first card. **Done** moves to the next spin.
- **Difficulty** (top bar) switches Wimpy / Easy / Medium / Hard / Extreme at any time.
- Dares and truths never repeat until the whole set for that level has been used.

---

## Version

The current version shows in the top-left corner (e.g. `v3`). When I send an update, check that the corner number changed after you reload to confirm the new build loaded.
