# 🎮 Game Ideas & Roadmap

A wishlist of small games to build into the offline arcade. Everything here is designed to be:

- **One self‑contained HTML file** (so it caches and runs with no signal),
- **Portrait + touch‑first** (one‑handed on an iPhone),
- **Endless or generated** (good for killing 5 hours, no "you finished it" wall),
- **Calm or satisfying**, not stressful.

Effort key: **S** = an afternoon · **M** = a day or two · **L** = a real project.

---

## The plan: one app, many games

Instead of a separate icon per game, the best move is a **hub**: a single PWA with a tropical menu screen, and each game is a screen inside it. One "Add to Home Screen," everything offline, easy to add to over time.

```
arcade/
├── index.html          ← hub / menu (links to each game)
├── sw.js               ← caches ALL games at once
├── manifest.webmanifest
├── icon-*.png
└── games/
    ├── tiki-merge.html
    ├── tiki-2048.html
    └── …
```

---

## Quick wins (build these first)

### 1. Tropical 2048 — "Tiki 2048"  ·  **S**
Swipe to slide tiles; equal tiles merge and double. Re‑skin the tiles as the same 8 cocktails so it feels like a sister game to Tiki Merge.

- *Why it fits:* dead‑simple to build, endless, deeply replayable, pure swipe control.
- *Controls:* swipe up/down/left/right.

### 2. Match‑3 — "Tiki Crush"  ·  **M**
Swap adjacent fruits to line up 3+; they pop, things cascade. Tropical fruit art, gentle chimes, no timer (relaxed mode).

- *Why it fits:* the classic "I'll just do one more" loop; endless board.
- *Controls:* tap‑swap or drag.

### 3. Memory Pairs — "Happy Hour Match"  ·  **S**
Flip cards to find matching cocktails. Scales from easy (3×4) to hard (6×6). Could secretly use **photos of you two** as some of the pairs. 💕

- *Why it fits:* tiny build, sweet, quick rounds.

### 4. Sudoku  ·  **M**
Offline puzzle generator + solver, infinite puzzles, 4 difficulties, pencil marks. The gold standard for quiet lecture‑time focus.

- *Why it fits:* truly infinite, calm, respected time‑killer.

### 5. Tiki Snake  ·  **S**
The classic, themed as a cocktail straw growing as it sips fruit. Swipe to steer, wrap‑around or walls mode.

- *Why it fits:* instant pick‑up‑and‑play, endless high‑score chase.

---

## Bigger but worth it

### 6. Solitaire (Klondike)  ·  **M/L**
Comfort‑food card game, perfect for long sessions. Add FreeCell / Spider later for variety. Smooth drag‑and‑drop, undo, auto‑complete.

### 7. Bubble Shooter — "Tiki Pop"  ·  **M**
Aim and fire fruit bubbles; match 3 to pop clusters. Trajectory‑line aiming (you already love that from Tiki Merge).

### 8. Flow Connect  ·  **M**
Connect matching colored dots with pipes that fill the grid. Generated levels = infinite. Very zen.

### 9. Tiki Bar Tycoon (idle/clicker)  ·  **M/L**
Tap to serve drinks, earn coins, buy upgrades and auto‑bartenders. Computes offline earnings from elapsed time when reopened. A natural thematic sequel to Tiki Merge — shares all the art.

### 10. Minesweeper  ·  **S/M**
Endless, generated boards, long‑press to flag. A compact logic classic.

---

## Cozy / zen

### 11. Color‑by‑tap / Mandala  ·  **S**
Tap regions to fill them from a palette; no fail state, no timer. Pure relaxation. Could include tropical / floral templates.

### 12. Jigsaw — from your own photos  ·  **M**
Slice a chosen image into pieces to reassemble. Load it with **your favorite photos of the two of you** — a puzzle that's also a little love letter. 💛

---

## Personal touches (make it *hers*)

These cost almost nothing to add and land big:

- Put **her name** on the menu / title screen.
- Hide tiny **love notes** that unlock as she hits score milestones ("you just beat my high score — miss you 😘").
- A **photo memory match** or **photo jigsaw** (ideas #3 and #12) using your pictures.
- A **"daily card"**: a different sweet message each calendar day (works offline — it's just the device date).
- Name the high‑score holder after you, so she has someone to beat.

---

## My recommended next 3

1. **Tiki 2048** (S) — biggest fun‑per‑effort, ships fast, matches the theme.
2. **Build the hub** so everything lives under one offline icon.
3. **Memory Pairs with your photos** (S) — quick to build, personal, she'll love it.

Then pick between **Match‑3** (satisfying) and **Sudoku** (calm focus) depending on her taste.

---

Want me to start on any of these? Say the word and I'll build it the same way — single file, offline‑ready, drop‑in to the hub.
