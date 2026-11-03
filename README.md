# Church Confession Online

A quiet, browser-based virtual church. Pray a decade of Hail Marys, light a candle, and take a private moment to examine your conscience, alongside other worshippers. No dependencies, no build step, no external assets: everything is drawn in code on an HTML canvas.

> **Important:** this is a space for prayer and reflection. It does **not** replace the Sacrament of Reconciliation. Only a priest can grant absolution, so please visit a priest at your local parish.

## Features

- **Virtual church:** altar, stained glass, pews, and chibi-style worshippers with a golden halo while they pray.
- **Hail Mary counter:** tap the button (or press `Space`) to count ten beads and complete a decade. The whole chapel sees the notification.
- **Light a candle:** write a short intention, and your candle appears on the prayer-candle stand.
- **Examination of Conscience:** a guided checklist, a free-writing step, and an act of contrition. Your text is **never saved and never sent anywhere**.
- **Weekly leaderboard, live activity feed, and online count.**
- Your name and progress are stored only in your browser (`localStorage`).

## Demo note

The other worshippers are simulated. Real multiplayer needs a realtime server (WebSocket, Firebase, Supabase Realtime, or Colyseus).

## Run locally

Open `index.html` in any modern browser.

## Publish with GitHub Pages

1. Create a new GitHub repository and upload `index.html` and `README.md`.
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and the `/ (root)` folder, then save.
4. After a minute, the game is live at `https://<your-username>.github.io/<repo-name>/`.

## Customize

Everything is in `index.html`:

- `NAMES`, `INTS`: simulated worshipper names and prayer intentions
- `EX`: the examination-of-conscience questions
- `scene()`, `chibi()`: the chapel and character drawings
- `doPray()`, `candle()`, `conf1()` to `conf3()`: the main interactions
