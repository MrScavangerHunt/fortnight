[README.md](https://github.com/user-attachments/files/34241029/README.md)
# FORTNIGHT

A single-file, browser-based battle royale in the style of the original Fortnite island. Everything (map, character, trees, fonts, sounds) is embedded in `index.html`, so it runs by opening the file or from any static host.

## Play
- Open `index.html` in Chrome, Edge or Safari (internet needed once for Three.js from the CDN).
- Press **READY** in the lobby. Matchmaking, spawn island, Battle Bus, glide down, loot chests, survive the storm.

| Key | Action |
| --- | --- |
| W A S D | Move |
| Shift | Run |
| C (hold) | Crouch |
| Space | Jump / leave bus / open glider |
| Left click | Fire / swing pickaxe |
| Right click (hold) | Aim down sights |
| E | Open chest |
| R | Reload |
| 1-4 | Pickaxe, pistol, shotgun, rifle |
| L | Leave match |

## What is in the file
- Menus: lobby (3D Steve rig), locker, item shop, battle pass, challenges. Progress saves in the browser.
- Map: heightfield + texture from the supplied OG island model, embedded and compressed (about 1.4 MB).
- Character: Steve rig from `Steve_riged.blend` (rigid parts on pivots), animated in code: walk, run, crouch, hold gun, aim.
- Trees: models from the supplied forest pack, planted on the dark-green patches of the map texture. Real models near the player, simple shapes far away. Trunks are solid.
- Gameplay: spawn island, Battle Bus, glider, 110 chests, 3 guns with rarities, 29 bots, shrinking storm, collision between players.
- Sounds: gun shots and reload embedded from the supplied clips.

## Code layout
Everything is in `index.html`:
1. CSS and the embedded font (`@font-face`).
2. Menu markup and menu script.
3. Data blocks: `<script type="text/plain" id="D_...">` (map heights, texture, sounds, Steve rig, skin, trees).
4. The game script (IIFE): audio, map, entities, combat, storm, camera, HUD, lobby 3D, trees, input.

## Not done yet
- Building and harvesting, vehicles, building interiors.
- 3D models for towns (see `poi_map.png`: 20 numbered points of interest). Without them towns are flat ground with a painted texture.
- Real challenge tracking (the challenges tab uses test buttons).

## Notes
- The Burbank font, the map, the forest models and the Steve model are third-party assets. Check their licenses before making this repo or the game public.
- Google Analytics is included in `index.html`.
