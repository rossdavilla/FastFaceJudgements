# FastFaceJudgements ⚡

A quick, engaging in-class game that shows students how rapidly the brain can judge facial attractiveness.

Each round flashes two faces in sequence — **Face 1 → static mask → Face 2 → static mask** — then asks which face was more attractive. The faces flash faster every round, from a full second down to just 60 milliseconds. Guess right and you get a one-second burst of confetti 🎉.

## How it works

- **7 rounds**, each getting faster:

  | Round | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
  |-------|-----|------|------|------|------|------|------|
  | Face time | 1.00s | 0.75s | 0.50s | 0.25s | 0.15s | 0.10s | 0.06s |

  (A 1-second static mask is shown between and after each face.)
- **Randomized order** — the pairs are shuffled each play-through, while the correct "more attractive" answer is tracked per pair.
- **All images preload up front** behind a loading screen, so there's zero lag once the flashing starts.
- After each answer, both faces are revealed side by side with the more attractive one crowned 👑.
- A results screen shows your score and a per-round breakdown.

## Running it

It's a single self-contained `index.html` (no build step, no dependencies). Because it loads local images, serve it over a simple local server rather than opening the file directly:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000> in your browser.

## Project structure

```
index.html   # the entire game (HTML + CSS + JS, self-contained)
img/         # 7 face pairs + static.jpg mask
```

Face image filenames label which one is the more attractive of each pair.
