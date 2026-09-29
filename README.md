# Diablo's Reign

A semi open world, low poly hack and slash RPG, built in **Unreal Engine 5.6** with **C++** for Windows.
Inspired by Diablo 3: pick a class, fight through levelled lands out of a safe camp, collect loot, and work down to Diablo himself.

**📍 Roadmap:** see [ROADMAP.md](ROADMAP.md) for what's done, what's being play-tested and what's next.

---

## The story

Long ago the Lord of Terror, **Diablo**, burned this land from a throne beneath the Ashland. Eight **Wardens** brought him down, tore out
his burning heart - the **Heart of Cinders** - and broke it into **eight Cinder Shards**, each hidden at a far corner of the realm.

Now the shards are burning again. Diablo is waking, and every shard twists whatever holds it into a tyrant: a slime becomes a king, a
goblin a warchief, a dead Warden a king of bones. From the last free camp at the crossroads, the hero takes the shards back, lord by lord -
until the heart is whole, the sealed Ashland gate opens, and there is only one road left: down.

**Act I** is ten chapters, from a first word with the camp's Knight Captain to Diablo's throne room, with offers, turn-ins and a
different greeting for every class. Side quests come from the camp's people, and every land has repeatable bounties.

---

## The game

### Eight classes
Pick a class for each new hero: **Hemomancer** (a blood knight who spends his own life), **Barbarian**, **Crusader**, **Demon Hunter**,
**Monk**, **Necromancer**, **Witch Doctor** and **Wizard**. Each has its own skills, its own resource (Fury, Wrath, Hatred, Spirit,
Essence, Mana, Arcane Power...), its own left-click attack, its own look and its own reason to be here.

### Skills
- A skill screen (`K`): unlock skills as you level, drag them onto the bar
- **169 skills**, each with **5 runes** that change what it does
- Elements: physical, fire, cold, lightning, poison, wind, arcane, holy and shadow
- Every skill has its own animated visual effect

### Camp hub
A safe camp in the middle of the world, with gates to every land.
- **Camp people:** Brother Aldric (healer), His Holiness Benedict (blessings), Captain Roderic Vane (bounties) and Grisla the
  Beastmaster (a wolf companion) - and the story's quest-givers
- **Merchant:** an 8-item shelf, an Item of the Day, restocks every 5 minutes, and "Sell All Trash"
- **Blacksmith:** salvage, forge and reforge gear
- **Stash** for storing gear
- **Recall** (`H`) back to camp from anywhere; a Return Portal takes you back to the exact spot, with that land as you left it

### Lands
| # | Land | Lord |
|---|---|---|
| 1 | Slime Fen | Slime King |
| 2 | Goblin Warrens | Goblin Warchief |
| 3 | Orc Badlands | Blood Warlord |
| 4 | Ogre Crags | Ogre Chieftain |
| 5 | Cinder Wastes | Cinder Lord |
| 6 | Bone Crypt | Bone King |
| 7 | Frozen Peaks | Frost Giant |
| 8 | Blighted Swamp | Bog Horror |
| 9 | Ashland Caverns | **Diablo**, in his throne room |

The Slime Fen is levels 1-5; the other lands scale with the hero. Each land has its own monsters, a lord, secret chests, breakable props
and its own set of zone gear. Every land can be edited in the Unreal editor: Spawn Points, Loot Nodes and quest markers can be selected
and moved, and each marker has its own enemy level, density and loot odds.

### Quests
- A quest tracker, a quest log (`J`), and Accept / Turn In in the camp people's talk screens, with "!" and "?" over them
- Story chapters, side quests and per-land bounties (finish them all for a bonus chest)
- No arrows pointing the way - the words tell you where to look

### Combat
- Third-person over-the-shoulder camera with WASD and mouse look (`V` switches to top-down)
- Directional attacks, hold to keep attacking, heavy-weapon slowdown, and parry
- Slimes, goblins, orcs, ogres, imps, skeletons, wraiths, giants and more, plus Champions
- **Diablo:** a custom rigged model with Ground Slam, Fire Wall and a melee combo (more phases planned)

### Loot
- Rarities: Normal, Magic, Rare, Set and Legendary, plus prefixes and suffixes
- **Parts system:** weapons, armour and shields are built from parts (Grip, Guard, Blade, ...). Each part adds its own stats and style,
  and together they give the item its name, for example *"Swift Deadly Longsword"*
- **Class weapons:** Mighty Weapons, Flails, Hand Crossbows, Fist Weapons, Daibos, Scythes, Ceremonial Knives, Wands and Orbs - 27
  designs, each with its own model, and stronger for their class's skills
- Zone gear sets from each land, and every ordinary weapon, shield and jewel modelled in Blender
- Inventory with drag-and-drop, a stats tab and favourites; the game saves automatically

### Progression
Level cap 70 from a custom XP table. Lands scale with your level.

---

## Tech
- Unreal Engine 5.6, C++ (MSVC)
- Data-driven: classes, skills, enemies, loot, class weapons, zones, parts, affixes, quests and the level system are all editable data assets
- Custom models are made in Blender (built by scripts) and rigged to the Unreal mannequin skeleton
- Automated tests run through Unreal's Automation system (111 tests)
