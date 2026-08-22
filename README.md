# Commander Tracker

A life tracker and dungeon reference built for playing Commander/EDH, designed to run flat on a tablet placed in the middle of the group.

No installs, no accounts, no ads — just two static HTML pages you open in a browser.

## What's in here

### `commander-tracker.html`
The main life tracker. Supports 2–6 players, arranged around a central hub so every seat's controls are reachable and correctly oriented no matter where someone's sitting.

- Life totals with a floating running-total indicator while you tap or hold +/-
- Poison, Storm, and Commander Tax counters, plus a renamable custom counter for anything else you need to track
- A full WUBRG + colorless mana pool tracker
- Commander damage per opponent, including partner commanders, which correctly reduces life as it's dealt
- Monarch and Initiative, each a single-holder status you tap to pass between players
- A "Dungeons" button per player opening a browsable, tappable tracker for all four official Magic dungeon cards (Lost Mine of Phandelver, Tomb of Annihilation, Dungeon of the Mad Mage, and Undercity)
- A "random opponent" picker and a "who goes first" randomizer, both with an animated selection
- Autosaves to the browser's local storage, so a reload or closed tab doesn't lose the game in progress
- A running "time elapsed" display for the current game
- Optional screen wake-lock so the tablet doesn't dim mid-game (works when the page is served over `https`; opening the file directly from disk doesn't support this due to browser restrictions)

### `dungeon-gallery.html`
A standalone reference/browser for the same four dungeon cards, navigable with on-screen arrows. Each card shows the full room text and lets you tap through a run the same way the in-tracker dungeon window does, independently of any live game.

## Using it

Nothing to install. Either:
- Open the `.html` file directly in a browser (works fully offline; screen wake-lock won't work in this mode), or
- Host it somewhere with `https` (e.g. GitHub Pages) so wake-lock works and it's reachable from any device by URL. On a tablet, using the browser's "Add to Home Screen" option after opening it gives a more app-like, full-screen feel.

## Tech notes

Each page is a single self-contained HTML file — HTML, CSS, and JavaScript all in one, no build step, no external dependencies or CDN calls, no frameworks. Written in plain JS (`let`/`const`, no bundler needed). This was a deliberate choice to keep the whole thing easy to copy, host, or hand to someone else as one file.

## Disclaimer

This is an unofficial, fan-made tool. It is not produced, sponsored, or endorsed by Wizards of the Coast. *Magic: The Gathering*, the dungeon cards referenced, their room names, effect text, and mana symbols are all the property of Wizards of the Coast LLC. Dungeon room text is reproduced here for reference/utility purposes, matching common practice among fan-made deckbuilding and companion tools.

Commander tracker is unofficial Fan Content permitted under the Fan Content Policy. Not approved/endorsed by Wizards. Portions of the materials used are property of Wizards of the Coast. ©Wizards of the Coast LLC.

## License

The code in this repository may be reused, modified, and shared freely. This license covers the HTML/CSS/JS only — it does not and cannot extend to Magic: The Gathering's card text, names, or imagery, which remain the intellectual property of Wizards of the Coast regardless of how the code itself is licensed.
