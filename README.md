# Diablo-Reign

A semi open world, low poly hack and slash RPG, built in **Unreal Engine 5.6** with **C++** for Windows.
Inspired by Diablo 3: fight through levelled zones out of a safe camp, collect loot, and work down to Diablo himself.

**📍 Roadmap:** see [ROADMAP.md](ROADMAP.md) for what's done, what's being play-tested and what's next.

---

## The game

### Camp hub
A safe camp in the middle of the world, with zone gates on every side.
- **Merchant:** an 8-item shelf, an Item of the Day, restocks every 5 minutes, and "Sell All Trash"
- **Blacksmith:** salvage, forge and reforge gear
- **Stash** for storing gear
- **Recall** (`H`) back to camp from anywhere; a Return Portal takes you back to the exact spot, with that zone as you left it

### Zones
| # | Zone | Levels |
|---|---|---|
| 1 | Slime Fen | 1-5 (Slime King boss) |
| 2 | Goblin Warrens | scales with the hero |
| 3 | Orc Badlands | scales with the hero |
| 4 | Ogre Crags | scales with the hero |
| 5 | Cinder Wastes | scales with the hero |
| 6 | Ashland Caverns | 21-25: a fiery cave of cracked ground and lava, and Diablo's throne room |

Each zone has its own enemies, a boss, secret chests and breakable props. Every zone can be edited in the Unreal editor: Spawn Points and Loot Nodes can be selected and moved, and each marker has its own enemy level, density and loot odds.

### Combat
- Third-person over-the-shoulder camera with WASD and mouse look (`V` switches to top-down)
- Directional attacks, hold to keep attacking, heavy-weapon slowdown, and parry
- Enemies include slimes, goblins, orcs, ogres, imps and skeletons, plus fire variants, Champions and a Treasure Goblin
- **Diablo:** a custom rigged model with Ground Slam, Fire Wall and a melee combo (more phases planned)

### Loot
- Rarities: Normal, Magic, Rare, Set and Legendary, plus prefixes and suffixes
- **Parts system:** weapons, armour and shields are built from parts (Grip, Guard, Blade, ...). Each part adds its own stats and style, and together they give the item its name, for example *"Swift Deadly Longsword"*
- Armour looks: Plate, Bone, Leather, Chain and Regal
- Inventory with drag-and-drop, a stats tab and favourites; the game saves automatically

### Progression
Level cap 70 from a custom XP table. Zones scale with your level.

---

## Tech
- Unreal Engine 5.6, C++ (MSVC)
- Data-driven: enemies, loot, zones, parts, affixes and the level system are all editable data assets
- Custom models are made in Blender and rigged to the Unreal mannequin skeleton
- Automated tests run through Unreal's Automation system
