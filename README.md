# AA228V/CS238V lecture slides

Static site for the lecture decks, served by GitHub Pages.

```
index.html                      lecture list (edit to add lectures)
shared/deck-ink.js              Apple Pencil ink layer (used by every lecture)
shared/present.js               present mode: P or the top-right button
lectures/01-introduction/       one folder per lecture
  index.html                    the deck (exported from Claude Design, renamed)
  support.js, deck-stage.js,    deck runtime from the export
  image-slot.js
  uploads/, images/             media the deck uses
  ink.json                      published ink (created by the deck's Publish button)
```

## Adding a lecture

1. Export the deck from Claude Design as multiple files.
2. Make `lectures/NN-short-name/`, copy the export in, and rename `Lecture NN.dc.html` to `index.html`.
3. In that `index.html`, set `<meta name="deck-id" content="aa228v-lectureNN">` so each lecture keeps its own ink,
   delete the export's own `deck-ink.js`, and point the script tags at the shared copies:
   `<script src="../../shared/deck-ink.js"></script>` and `<script src="../../shared/present.js"></script>`.
4. Add a line for it in the top-level `index.html`.

## Publishing ink from the iPad (one-time setup per device)

1. On GitHub: Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token.
   - Repository access: **only this repository**.
   - Permissions: **Contents: Read and write**. Nothing else.
   - Pick an expiry (for example, the end of the quarter).
2. Open a lecture on the iPad, tap the gear in the ink toolbar and fill in:
   - Repository: `OWNER/REPO` (this repository)
   - Branch: `main`
   - Folder path: leave blank (each deck publishes into its own folder)
   - Token: the token from step 1
3. After writing, tap **Publish**. Students see the ink about a minute later.

The token is stored only in that device's browser. "Forget token" in the same panel removes it.

## Presenting

- **P** (or the Present button that appears near the top-right corner) goes full screen and hides the thumbnails; **P** or **Esc** leaves.
- Laser pointer: the target button in the ink toolbar, or **L**. It follows the Pencil (and its hover on iPads that support Pencil hover) or the mouse in draw mode, fades when lifted, and is never saved. **L** again returns to the pen.
- The ink toolbar's pin button switches between "always on screen" (dimmed when idle) and "auto-hide". It starts pinned on a device where publishing is set up.
- Palm rejection: a hand resting on the iPad never selects images or changes slides; only short, clean finger taps and swipes navigate.

## Notes

- Ink is keyed by slide number, so inserting or reordering slides after publishing shifts existing ink.
- The decks load React from unpkg.com and fonts from Google Fonts when they open, so they need an internet connection.
