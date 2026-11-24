# MTG Action Logger

A phone-friendly web app for logging what happens in our Commander games: damage, heals, kills, commander casts and more. Every action is saved to a Google Sheet so we can track stats over time.

**Open the app:** https://walvox.github.io/mtg-logger

## What it does

- **Tap or talk to log.** Pick who did it, what they did and who it hit, or use voice input and say it.
- **Hit several players at once.** Choose multiple targets and one action is logged for each.
- **Instant logging.** Actions save on your phone right away and sync to the sheet in the background.
- **Works with a bad connection.** If the connection drops, actions wait on your phone and sync when it comes back. The status dot turns gold while anything is waiting.
- **Pick up where you left off.** "Load Latest Game" reloads the current game, its players and the turn number.
- **Fix mistakes.** Edit or delete entries from the session log.

## Getting connected

1. Open the app on your phone.
2. Enter the group password (ask Walter).
3. That's it. The app remembers you on that device.

No Google account is needed to log games.

## How it works

- **The app** is a single `index.html` file hosted for free on GitHub Pages.
- **The data** lives in a Google Sheet with tabs for Player Stats, Deck List, Game Log, Play Log and Action Log.
- **In between** is a Google Apps Script web app. The app sends actions to it with the group password, and the script writes them to the sheet. The script runs under Walter's Google account, so nobody else needs access to the sheet itself.

The Apps Script can be slow to respond after it's been idle for a while. The app wakes it up when you open it and doesn't wait for it when you log, so you shouldn't notice.

## Making changes

Edit `index.html` and commit it to `main`. GitHub Pages updates the live app within a minute or two. After that, refresh the page on your phone.

## Players

Bianca, Ezra, James, Josh, Justine, Kingston, Nate, Victor and Walter.
