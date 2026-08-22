# Tally

A live workout companion. Log sets, rest between them — nothing else. No history, no stats, no tracking. Built for personal use.

## Deploying to GitHub Pages

1. **Create a repo.** On GitHub, create a new repository (e.g. `tally`). Public or private both work with GitHub Pages, though private repos need a paid plan for Pages.
2. **Upload these files** to the root of the repo (or push via git):
   - `index.html`
   - `manifest.json`
   - `favicon.ico`
   - `favicon-16x16.png`
   - `favicon-32x32.png`
   - `apple-touch-icon.png`
   - `icon-192.png`
   - `icon-512.png`
3. **Enable Pages.** In the repo, go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, pick `main` (or whichever branch you pushed to) and `/ (root)`, then Save.
4. **Wait a minute or two.** GitHub will give you a URL like `https://yourusername.github.io/tally/`. That's your live app.
5. **Add it to your home screen.** Open that URL on your phone in Safari (iOS) or Chrome (Android), then use "Add to Home Screen." Because of the manifest, it'll open full-screen without browser chrome, like a real app.

## About your data

The app saves your routine to your browser's `localStorage`, scoped to whatever URL you're using. A few things follow from that:

- Your routine lives in *that specific browser, on that specific device*. It won't sync between your phone and laptop automatically.
- Clearing your browser's site data/cache for that URL will erase it — same as it would for any site.
- If you ever want cross-device sync, that would need a small backend (or something like Firebase) — a bigger change, not something this static setup does on its own.

If you were using this inside claude.ai as an Artifact before, note that its sync used a different, Anthropic-hosted storage system — this GitHub-hosted version is fully independent and doesn't share data with that.

## Making changes later

It's a single `index.html` file — all the HTML, CSS, and JS are in one place, no build step. Edit it directly and push to update the live site (Pages usually redeploys within a minute of a push).
