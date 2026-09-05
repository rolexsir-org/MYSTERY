# 🍊 MYSTERY PEEL
**Peel. Reveal. Collect.** — a satisfying ASMR peel game built from your 5 image prompts.

## How to play
1. **Press** your finger on the mystery object.
2. **Swipe in circles** — the shell curls off in a satisfying spiral with crumbs, sparks and sound.
3. **Complete the ring** to reveal the glowing core, then **collect it on your shelf**.

## What's inside a shell
| Object | Shell | Rarity |
|---|---|---|
| Aurora Core | Citrus Skin | Common |
| Neon Prism | Lime Shell | Common |
| Rose Quartz | Rose Candy | Common |
| Moon Pearl | Lavender Frost | Rare |
| Floating Flame | Obsidian Black | Rare |
| Frozen Comet | Glacier Skin | Rare |
| Golden Gear | Frosted Glass | Rare |
| Mechanical Heart | Dark Chocolate | Epic |
| Crystal Eye | Coral Silk | Epic |
| Clockwork Sun | Burgundy Matte | Epic |
| Ember Star | Navy Lacquer | Legendary |
| Pocket Galaxy | Wooden Bark | Legendary |

## Files
- `index.html` — **the whole game**: physics, rendering, particles, WebAudio sound design, and all art inlined as data URIs. Works fully offline; just open it.
- `assets/` — the key art generated from your prompts (hero, promo, collection reveals, icon).
- `shots/` — screenshots of the running game taken from the real render loop.
- `README.md` — this file.

## Prompt → game mapping
Your prompts became the game's visual identity:
- **Prompt 1 (Hero)** → title screen background + the "citrus peel → neon crystal" concept that powers the Aurora Core object.
- **Prompt 2 (Mid-peel)** → the core peel mechanic: layered shells (chocolate / glass / wood / lacquer) curling away to reveal glowing cores, with crumbs and shards floating in zero gravity.
- **Prompt 3 (Impossible reveal)** → the Pocket Galaxy legendary — a tiny wooden egg containing a whole spinning galaxy (procedurally rendered: spiral arms, stardust, planets).
- **Prompt 4 (Collection shelf)** → the Collection screen: a 12-slot museum shelf where each reveal sits on its own card, and unpicked objects stay as "?" mysteries.
- **Prompt 5 (Icon)** → the app icon (`assets/icon.jpg`), also used as the favicon.

## Tech notes
- Zero dependencies, single HTML file, portrait-first mobile layout (works on desktop too).
- All cores are drawn live on `<canvas>` (glow, shine, animation), so every collected item shimmers on the shelf.
- WebAudio synthesizes the ASMR layer: peel swishes, snapping crackles, pops on milestone ticks, a chime arpeggio on reveal. Mute button top-right.
- Progress + collection persist in `localStorage`.

## Debug API (console)
```
PeelGame.startLevel()      // begin a peel
PeelGame.addPeel(0.1)      // simulate peeling
PeelGame.state()           // 'title'|'play'|'revealing'|'reveal'
PeelGame.reset()           // wipe saved progress
```
