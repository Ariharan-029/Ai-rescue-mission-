# AI RESCUE MACHINE — Round 1 Quiz

A single self-contained file: `index.html`. No build step, no dependencies, no backend.

## Host it on GitHub Pages (free)

1. Create a new GitHub repo (e.g. `ai-rescue-machine`).
2. Upload `index.html` to the root of the repo (rename it from `ai-rescue-machine.html` to exactly `index.html` so GitHub Pages serves it at the root URL).
3. Go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
5. Wait a minute, then your quiz is live at:
   `https://<your-username>.github.io/ai-rescue-machine/`
6. The admin panel is the same URL with `?admin=1` on the end:
   `https://<your-username>.github.io/ai-rescue-machine/?admin=1`

## How results get to you (no database needed)

This page runs entirely in each participant's browser — there's no server, so it can't automatically send you every team's score. Instead:

1. When a team finishes, they see a **"Download My Result"** button that saves a small `.json` file (e.g. `arm-result-team-alpha.json`).
2. Ask teams to send you that file (WhatsApp, email, a shared Drive folder — whatever's easiest to collect at your event).
3. Open the admin panel (`?admin=1`), and use the file picker to select **all** the `.json` files at once.
4. The panel builds a sortable leaderboard (by score or time) and lets you **Export CSV** for your records.

## If you want live/automatic result syncing instead

That requires a real backend (e.g. a Google Sheet + Apps Script, or Firebase) to receive submissions from every participant's device in real time. The current file doesn't include that, but I can build it if you'd like — just ask.

## Anti-cheating notes

Tab-switch detection, right-click disabling, and the fullscreen prompt are all client-side JavaScript, which a technically determined participant could bypass (e.g. via browser dev tools). They're included as a reasonable deterrent, not a guarantee — there's no fully secure way to do this without a proctoring service.
