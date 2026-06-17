# World Cup 2026 Wallchart

An interactive, browser-based wallchart for the **FIFA World Cup 2026** (USA · Canada · Mexico).
Everything lives in a single self-contained `index.html` — no build, no server, no dependencies.
Just open the file in a browser.

## Features

- **All 12 groups** (A–L), 48 teams, every round-robin fixture with editable score boxes.
- **Live standings** that recompute as you type, using FIFA tiebreakers
  (points → goal difference → goals for → head-to-head mini-league).
- **Third-place ranking** across all groups, highlighting the best 8 that qualify.
- **Auto-filling knockout bracket** — Round of 32 → Final + third-place play-off.
  - The Round of 32 always reflects the **current** group standings (winner, runner-up and the
    eight best third-placed teams), with provisional slots marked `*` until each group finishes.
  - Third-placed teams are slotted into FIFA's official Round-of-32 group pools.
  - Enter a knockout score to advance a team; draws reveal penalty boxes to decide the winner.
  - Results propagate all the way to crowning a champion.
- **Persists to `localStorage`** — fully client-side. Your edits survive a refresh.
- Pre-loaded with the real group draw and the results played so far.

## Usage

Open `index.html` in any modern browser.

- **Reset to live results** — restore the real results played so far (clears your edits).
- **Clear all** — empty every result, including the ones already played.

## Note

Where FIFA's third-place allocation table allows more than one valid arrangement, a deterministic
valid one is chosen. It always respects the official group pools, but in rare combinations the exact
slotting could differ from FIFA's published matchups.
