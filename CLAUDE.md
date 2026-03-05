# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Single-file browser game — no build tools, no dependencies, no package manager. Everything lives in `index.html` (HTML + embedded `<style>` + embedded `<script>`).

## Running the project

Open `index.html` directly in a browser:

```bash
start index.html        # Windows
open index.html         # macOS
xdg-open index.html     # Linux
```

## Architecture

All game logic is in the `<script>` block at the bottom of `index.html`:

- `board` — flat 9-element array representing the grid (`''`, `'X'`, or `'O'`)
- `current` — whose turn it is (`'X'` or `'O'`)
- `WINS` — hardcoded array of all 8 winning index triples used by `checkWin()`
- `scores` — object `{ X, O, D }` tracking wins and draws across rounds; persists until page reload
- `init()` — resets board and UI for a new round without clearing scores
- Cell clicks are handled via individual `addEventListener` on each `.cell` element

## Git workflow

Every change should be committed and pushed to GitHub:

```bash
git add <file>
git commit -m "<type>: <short description>

<optional body>"
git push
```

Remote: `https://github.com/Didilan75/tictactoe`
