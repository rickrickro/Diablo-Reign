# Roadmap

A Diablo-style action RPG in Unreal Engine 5.6 (C++). This roadmap is built from the project to-do list.
Legend: ✅ done · 🟡 in progress · ⬜ not started. Item codes (H1, M6, ...) match the to-do list.

## 🎯 Where we are

- Camp hub plus **6 zones**: Slime Fen, Goblin Warrens, Orc Badlands, Ogre Crags, Cinder Wastes and Ashland Caverns (level 21-25). Every zone can be edited with selectable Spawn Points and Loot Nodes.
- **Diablo** is in his Ashland throne room with his own rigged model and Phase 1 abilities (Ground Slam, Fire Wall, melee combo).
- Loot: Normal to Set rarity, weapon, armour and shield **parts**, editable affixes, merchant, blacksmith, stash, and save games.
- Level cap 70, driven by one file (`DA_LevelSystem`).

---

## 1. Play-testing now (high priority)

| | Item | What to check |
|---|---|---|
| ⬜ | **H3** Loot tuning | Change drop and rarity values in `Data/DA_LootTuning` |
| 🟡 | **H5** Paint tool and zone preview | Foliage mode (`Shift+3`), spawn preview indicators in the editor |
| ⬜ | **H8** Camera feedback | Settle the camera angle, zoom, distance and follow style before more camera code |
| 🟡 | **H9** Spawn Points and Loot Nodes | Move and tune markers; try Spawn/Loot Density on `DA_Zone_SlimeFen` |
| ⬜ | **H11** Prop loot and per-container override | Edit `Data/PropLoot/*`; override one chest without changing the others |
| ⬜ | **H14** Weapon parts | Part-based names ("Swift Deadly Longsword"), tooltips for each part, edit `Data/Parts/*` |
| ⬜ | **H18** Part styles, armour and shield parts | Standard, Broad, Slender, Jagged and Ornate model styles; 27 armour and shield part files; `DA_ItemAffixes` |
| ⬜ | **H19** Enemy weapon grip, 5 armour looks | Enemies hold weapons properly; Plate, Bone, Leather, Chain and Regal armour looks |
| ⬜ | **H15** Diablo's real fight | No gliding, his swings land, Fire Wall appears in front of him, check for stretching at shoulders and hips |
| ⬜ | **H17** Level system balance | Tune `DA_LevelSystem`; check how hard the fire zones hit |
| ⬜ | **H16** Every enemy walks | Watch packs after the anti-glide fix |

## 2. Next features (medium priority)

| | Item | Notes |
|---|---|---|
| 🟡 | **M6** Diablo's arena and boss | Arena (Zone 6) and Phase 1 are done. **Next:** Phase 2 *Infernal Mage*, Phase 3 *Cataclysm*, a lava damage effect. Abilities are designed with Rick. |
| ⬜ | **M6b** Skill tree and prestige system | |
| ⬜ | **M5** Combo swing system | Chained multi-attack weapon combos |
| ⬜ | **M9** Custom models for every enemy | Reuse the Diablo rig pipeline (`blender_rig_diablo2.py`, `build_diablo2_rigged.py`) |
| 🟡 | Skill visual effects | Every skill gets a distinctive animated effect; style guide in `Docs/SKILL-FX-STYLE.md` |

## 3. Later (low priority)

| | Item | Notes |
|---|---|---|
| ⬜ | **H4** Heavy swing timing | Re-check axe and halberd pacing |
| ⬜ | **H7** Dev map normal variant | Give `DA_Enemy_Elite` a Minion twin, then re-run `build_dev_markers.py` |
| ⬜ | **L1** Minimap | |
| ⬜ | **L2** Destructibles and hazards | Climbing and crawling enemy spawns |
| ⬜ | **L3** Additional classes | Archer, Summoner, ... |
| ⬜ | **L4** Followers | Companions with their own gear, skills and classes |
| ⬜ | **L5** Artisan progression | Artisans level up with use |
| ⬜ | **L6** Quality-of-life pickups | Health orbs, auto-collected gold |
| ⬜ | **L7** Documentation | `HANDOFF.txt`, `Docs/DATA-ASSETS.md`, `Docs/PROJECT-MAP.md` |
| 🟡 | **L9** Dev map clean-up | Bosses are done; ordinary enemy rows still need spacing or a grid |
| ⬜ | **L10** Treasure Goblin never appears | Add him to some zones' spawn tables |
| ⬜ | **M3** Enemy weapon drops | *Probably not coming* |

## 4. Backlog (later phase)

- ⬜ **P1** Gem sockets and runes
- ⬜ **P2** Hub jeweler
- ⬜ **P3** Legendary power extraction
- ⬜ **P4** Transmog
- ⬜ **P5** Gambling vendor
- ⬜ **P6** Weapon power rating (one number for quick comparisons)

---

## ✅ Done

<details>
<summary>Milestones already shipped (click to expand)</summary>

**World and zones**
- Camp hub (`L_Camp`) with merchant, blacksmith, stash, themed areas, torches and 50% faster movement in the hub (M4)
- Zone 1 Slime Fen: up to 90 monsters, depth-based variants, Slime King boss
- Zones 2-5 (Goblin Warrens, Orc Badlands, Ogre Crags, Cinder Wastes): 15 new enemies with their own maps, loot and bosses (M1, M2, H12)
- Zone 6 Ashland Caverns and the working Diablo hub portal (M6, M7)
- Camp gates and the merchant can be selected and moved in the editor (M8)
- Boss and way-back gate markers can be selected in every zone (H10)
- Recall and the Return Portal: zones keep their state when you recall and come back (H13)
- Selectable Spawn Points and Loot Nodes, density controls, paint tool, zone preview rings

**Combat and enemies**
- Four base enemy types plus visual gear grades; played and approved (H1)
- Diablo with Rick's own rigged model; walks, swings and lands hits; Fire Wall
- Enemies walk all the way in (no gliding); parry; "Resistant" combat text
- Directional attacks, one click per attack and hold to keep attacking, heavy-weapon slowdown
- Boss and enemy health bars with names and levels

**Loot and items**
- Weapon Parts system (Crude to Masterwork), trash tagging and "Sell All Trash"
- Merchant (8-item shelf, Item of the Day, restock every 5 minutes)
- Prop loot assets, and a loot override for a single container
- Inventory drag-and-drop, Stats tab, item weight and durability removed

**Progression and camera**
- Level cap 70 using Rick's XP table; zones scale with the hero
- Over-the-shoulder camera with WASD and mouse look (`V` switches to top-down), walls fade out when they block the view

</details>
