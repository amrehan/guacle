# Guacle 🥑

**Play: https://amrehan.github.io/guacle/**

A daily guac speedrun. Swipe to chop an avocado, tomato, onion, jalapeño and lime as fast as you can, then share your time.

- Swipe like Fruit Ninja: hold and drag, with no lift needed between cuts.
- An ingredient is done once most of it is diced small. Then the next one drops in.
- Ranks: **Guac god** < 12s · Taqueria pro < 16s · Line cook < 22s · Home cook < 35s.
- Your streak, daily best and personal best are saved in your browser.

## Beat the AI

I trained a neural network plus beam-search planner to speedrun Guacle under human-speed swipe limits:

| Player | Best time |
|---|---|
| Random swiping | 21.7s |
| Greedy bot | 17.9s |
| Neural net | 13.6s |
| Neural net + search | **11.8s** |
| Theoretical human floor | ~9.5s |

Tip from the AI: never lift your finger. Zig-zag long straight lines at whatever big pieces are left, and start your first swipe while the ingredient is still dropping in.

## Tech

One HTML file, with no build step and no dependencies. It uses canvas 2D polygon slicing (Sutherland–Hodgman), a small rigid-body physics step, and sprite-cached pieces, so it stays smooth with hundreds of pieces. MIT licensed.
