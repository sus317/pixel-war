# Pixel War

A pixel art wave-survival game in a single HTML file. Play as a mage against enemies that shoot projectiles from their own biome, beat a boss every 5 waves and survive random events.

*Riassunto in italiano in fondo.*

## Play

| Way | How |
|---|---|
| **Online** | Open https://sus317.github.io/games/ |
| **Debug** | Open https://sus317.github.io/games/debug.html · press **F6** for wave 25 or **F7** for the final boss |
| **Windows / macOS (browser)** | Download the repository and double-click `index.html` (Chrome, Edge, Firefox, Safari) |
| **Windows / macOS (app)** | Download the file from [Releases](../../releases): `.exe` for Windows, `.dmg` for Mac |

No installation and no internet connection needed to play locally.

## Controls

**Keyboard and mouse**

| Action | Key |
|---|---|
| Move | A / D |
| Jump (double jump) | Space or W |
| Dash | Shift |
| Fire | Left click or J |
| Slash | C |
| Lightning | Right click or K |
| Powers | Q shield · E black hole · R ice · F holy light · T poison · G beam · V fire |
| Pause | P or Esc |
| Full screen | Click ⛶ in the game |

**Gamepad** (Xbox, PlayStation, Switch Pro; press any button to activate it)

| Action | Button |
|---|---|
| Move / Aim | Left stick / Right stick |
| Jump | A |
| Fire | X or RT (hold) |
| Dash / Slash | L1 / R1 |
| Lightning | LT |
| Shield / Black hole | B / Y |
| Ice / Holy light / Poison / Fire | D-pad left / up / down / right |
| Beam | L3 (press left stick) |
| Pause | Start |

Powers unlock as you progress (lightning wave 1, shield 2, black hole 3, ice 4, holy light 6, poison 7, beam 8, fire 9). The game pauses automatically if you unplug the gamepad or switch tabs. Your best score is saved in the browser.

Use the **♪** button to select an MP3 from your device for background music. The **↺** button restores the game's music, which changes with the biome and boss. The speaker button mutes or unmutes the audio.

## Features

- 5 biomes (Forest, Tundra, Swamp, Autumn, Volcano) that change after each boss, each with its own enemies and projectiles.
- A final boss phase after wave 25, with two health bars, golden laser rings and helpers.
- Checkpoints at the start of every boss and when reaching a new biome.
- Enemies: slimes, bats, shooters, brutes and elites. Bosses: stone golem and spiked beast, in a different version for each biome.
- Random events: meteor shower, lightning storm, Blood Moon.
- Biome and boss music, sound effects, selectable MP3 soundtrack, combo score, drops (heart, star, bomb), particles and gamepad rumble.
- English and Italian.

## Publishing on GitHub

```bash
git init -b main
git add .
git commit -m "Pixel War"
git remote add origin https://github.com/sus317/games.git
git push -u origin main
```

1. **Online playable page:** on GitHub go to *Settings → Pages → Build and deployment → Source: GitHub Actions*. After the first push the game is live at `https://sus317.github.io/games/`.
2. **Windows and Mac apps:** create a tag and GitHub builds the files and puts them in *Releases*:
   ```bash
   git tag v1.0.0
   git push origin v1.0.0
   ```

### Warnings the first time you open the apps

The apps are not signed with a paid certificate, so your system may warn you:
- **Windows:** SmartScreen → *More info* → *Run anyway*.
- **macOS:** right-click the app → *Open* → *Open*. If it says the app is damaged: `xattr -cr "/Applications/Pixel War.app"`.

## Development

[Node.js 20+](https://nodejs.org) is only needed for the desktop apps:

```bash
npm install
npm start        # opens the game window
npm run dist     # builds the installer for your system into dist/
```

The game itself is `index.html`: edit it and open it in the browser. `debug.html` is the separate debug copy (F6: wave 25, F7: final boss). Audio files are in `audio/`.

## Credits and licenses

- Game: © sus317, MIT license (see `LICENSE`).
- **Visual effects (explosions, lightning, ice, rain, etc.): [Pixel Art VFX by Sprite Fusion](https://www.spritefusion.com/pixel-art-vfx)** by Hugo Duprez, open source under the MIT license. Details in `THIRD_PARTY_NOTICES.md`.
- **Sound effects:** 8-Bit Sound Effect Pack Vol. 001 by Deva / @Shades, CC0; see `audio/CREDITS.txt`. The player explosion MP3 was supplied by the project owner.

## Italiano

**Pixel War** è un gioco pixel art di sopravvivenza a ondate in un solo file HTML. Gioca online con GitHub Pages, apri `index.html` nel browser su Windows o macOS, oppure scarica `.exe` / `.dmg` da Releases. Supporta tastiera, mouse e controller (comandi nelle tabelle sopra) e ha la pausa (P / Esc / Start). Effetti visivi di [Sprite Fusion Pixel Art VFX](https://www.spritefusion.com/pixel-art-vfx) (MIT).

# Third-party notices

## Pixel Art VFX – Sprite Fusion

The visual effects (explosions, impacts, slash, blood, muzzle flash, lightning,
ice, poison, energy, shield, black hole, holy light, heal, power-up, pickup,
sparkle, dash, fire, rain, snow, fog, embers, fireflies, falling leaves,
bubbles) come from the free, open source **Pixel Art VFX** library by
**Hugo Duprez / Sprite Fusion**.

- Source: https://www.spritefusion.com/pixel-art-vfx
- License: MIT (free and commercial use, modification allowed)
- Copyright (c) Sprite Fusion (Hugo Duprez)

In `index.html` this code is the first `<script>` block (minified, exposed as
`window.FX`). The game logic in the second `<script>` block is original work.

The MIT license requires that the copyright notice and the license text stay
with the code. The full MIT text is in the `LICENSE` file of this repository;
if the effects ZIP you downloaded contains its own license file, copy its
exact copyright line here.
