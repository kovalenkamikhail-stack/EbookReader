# Book Reader Mini App

A Telegram-friendly EPUB reader that runs entirely on the client. Drop an EPUB file, keep your library in IndexedDB, and resume reading where you left off—inside Telegram Web Apps or any modern browser.

## Features
- EPUB rendering powered by `epub.js`
- Local library + last position stored in IndexedDB
- Works both inside Telegram Web Apps and regular browsers
- Friendly notice for FB2/MOBI (conversion not yet enabled)

## GitHub Pages setup
1. Push the `miniapp` branch to your GitHub repository.
2. In **Repository Settings → Pages**, set **Source** to **Deploy from a branch**.
3. Choose the branch you want to publish (e.g., `miniapp` or `main` after merging) and set the **folder** to `/app`.
4. Save. GitHub Pages will publish at `https://<your-username>.github.io/<repo-name>/app/` once the build finishes.

## Opening the mini app in Telegram
1. Make sure your bot has a domain that matches the GitHub Pages URL (e.g., `https://<username>.github.io/<repo>/app/`). For public Pages, Telegram accepts the `github.io` domain.
2. In **BotFather**:
   - Send `/setdomain` and provide the GitHub Pages URL (without query params).
   - Send `/setmenubutton` → choose **Web App** → paste the same URL.
3. Optional: set `/setdescription` and `/setabouttext` to describe the reader.
4. Open the bot in Telegram, tap the menu button, and the Book Reader mini app will load.

## Running outside Telegram
Open `/app/index.html` directly (e.g., via GitHub Pages). The app detects when Telegram’s SDK is unavailable and runs in standalone mode automatically.
