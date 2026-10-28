# SpaceJong

A free Mahjong solitaire game where every tile is a slab of refractive crystal glass. The nebula behind the board bends and shimmers through each tile, matches shatter into glass shards and lightning, and the faces are glowing sci-fi glyphs instead of bamboo and bones. Twelve boards, a relaxed Zen mode and a Timed mode with combos.

**Play it in your browser:** https://nbwillcox.github.io/spacejong/

Everything is generated in code: the nebulae, the glass tiles, the glyphs and all sound effects and music (Web Audio synthesis). There are no image or audio files and no build step. A sibling of [SpaceTris](https://github.com/nbwillcox/SpaceTris) and the rest of the Space series, and one of the cabinets in [Nic's Arcade](https://github.com/nbwillcox/arcades).

## How to play

Clear the board by matching pairs of identical **free** tiles. A tile is free when nothing sits on top of it and its left **or** right side is open. Blocked tiles are dimmed, and clicking one flashes the tiles that block it.

- **Flowers and seasons:** any nebula flower matches any other flower, and any season matches any season (the gold-rimmed tiles).
- **Combos:** matches within 3.6 seconds of each other chain a combo that multiplies points up to x8, with bigger shatter effects as it climbs.
- **Every deal is solvable.** Boards are built backwards from a finished state, so a clean clear always exists. If you paint yourself into a corner the board reshuffles itself.

### Tile set

| Group | Faces |
| --- | --- |
| Orbs (1-9) | glowing energy spheres, counted like dots |
| Rods (1-9) | light rods, counted like bamboo |
| Numerals (1-9) | glowing digits in a hex medallion |
| Winds (4) | compass roses: N, E, S, W |
| Guardians (3) | Nova (burst star), Bio (hex lattice), Void (portal frames) |
| Flowers (4) and Seasons (4) | nebula blossoms; sun, snowflake, storm, terra |

## Modes

- **Zen:** no clock, no penalties, unlimited hint / undo / shuffle. Your best clear time per board is remembered.
- **Timed:** you start with a time budget based on the board size. Every match adds seconds (more on a combo). **Hint** costs 10 s, **Undo** 8 s and **Shuffle** 15 s (10 s if the board is stuck and reshuffles itself). Run out of time and it is over; clear the board and the leftover seconds become bonus score. Top 5 scores per board are kept in your browser.

### The twelve boards

Classic Turtle, Ziggurat, Crystal Diamond, Ringed Planet, Pixel Invader (66 tiles, the short one), Galaxy Core, Comet Tail, Ring Station, Twin Towers, Hourglass Nebula, Nova Cross and Starfighter, or pick Random.

## Controls

| Action | Mouse / touch | Keyboard | Gamepad |
| --- | --- | --- | --- |
| Pick a tile | click / tap a free tile, then its twin | `←↑↓→` hop between free tiles, `Enter` / `Space` pick | D-pad / left stick hop, `A` pick |
| Drop selection | right-click or tap empty space | `Q` | `B` |
| Hint | HINT button | `H` | `X` |
| Undo | UNDO button | `U` / `Z` / `Backspace` | `Y` |
| Shuffle | SHUFFLE button | `S` / `X` | `RB` / `LB` |
| Pause / new deal | pause button | `P` or `Esc` / `R` | `Start` |

In menus the arrow keys / D-pad move the highlight, `Enter` / `A` selects and `Esc` / `B` goes back. The board tilts a little with your mouse for a parallax glass effect (Settings can turn that off, along with screen shake, dimming and the glass refraction for slower machines).

### On a phone or tablet

Tap to play. Tall screens turn the board on its side so the tiles come out bigger, but landscape is still roomier. Use your browser's *Add to Home Screen* to install it as a full-screen app.

## Run locally

It is plain HTML/CSS/JS. Either open `index.html` directly, or serve the folder:

```bash
python -m http.server 8000
```

then visit http://localhost:8000. Handy URL parameter: `?play=<board>&mode=timed` skips the menu (boards: `turtle`, `ziggurat`, `diamond`, `saturn`, `invader`, `galaxy`, `comet`, `ring`, `towers`, `hourglass`, `cross`, `fighter`).

## License and attribution

Licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/): free to play, share and remix **non-commercially**, as long as you give credit and **link back to this repository**: https://github.com/nbwillcox/spacejong

This is an original game inspired by the traditional tile-matching solitaire. It uses no assets, names or code from any existing game.
