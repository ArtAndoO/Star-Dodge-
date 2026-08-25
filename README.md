# ✦ Star Dodger — Customizable Edition

A slick, fully customizable 2D browser game built with plain HTML5 Canvas + vanilla JavaScript. No frameworks, no build step, no dependencies — one file, drop it anywhere. Move your ship left and right to dodge falling hazards, catch bonus stars for combo points, grab power-ups, and survive as the game ramps up in intensity.

## Play it

Just open in any modern browser.

Or enable **GitHub Pages** on this repo (Settings → Pages → deploy from the branch/root) and share the live link with anyone.

## Controls

- **Desktop:** Arrow keys or `A` / `D` to move, `Space` to restart after game over
- **Mobile:** Drag your finger left/right anywhere on the canvas

## Customization panel

Everything is adjustable live from the side panel, and your picks are remembered between sessions via `localStorage`:

- **Ship Color** — 6 glowing color options
- **Ship Shape** — Fighter (triangle), Orb (disc), or Diamond
- **Difficulty** — Chill / Normal / Insane, each with its own fall speed, spawn rate, and ramp curve
- **Arena Theme** — Nebula (blue/purple), Sunset (orange/pink), Matrix (green) — each recolors the background gradient and starfield
- **Screen Shake** — toggle the hit-impact camera shake
- **Particle Trail** — toggle the glowing engine trail behind your ship
- **Power-ups** — toggle whether power-up drops spawn at all

## Gameplay features

- **Combo system** — chain bonus-star catches quickly for escalating point bonuses
- **Power-ups** (when enabled):
  - Shield — absorbs one hazard hit
  - Slow-mo — temporarily slows all falling objects
  - Extra life — up to a max of 5
- **Screen shake + particle bursts** on hits and pickups for impact
- **Parallax starfield** with two depth layers plus a glowing engine trail
- **Progressive difficulty** — fall speed and spawn rate increase the longer you survive
- **Persistent best score** and saved customization settings across sessions

## How it works

Everything lives in a single `index.html` file:
- A `<canvas>` element is the game surface, `requestAnimationFrame` drives the loop
- Falling shapes and power-ups spawn on timers that tighten over time
- Simple AABB collision detection between the ship, hazards, and power-ups
- All customization state lives in a plain JS object and persists via `localStorage`

## Ideas to extend it further

- Add sound effects / background music
- Add more ship shapes or unlockable skins tied to score milestones
- Add a leaderboard using a small backend (e.g. an n8n webhook + database)
- Add boss waves or patterned obstacle formations
- Add a pause menu

## License

MIT — do whatever you want with it.
