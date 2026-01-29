# Duck Defense 3D

## Overview
Duck Defense 3D is a browser-based 3D survival game built with Three.js. Players control a duck defending against waves of hunters in a Florida swamp, offering a unique twist on the classic Duck Hunt. The project aims to deliver an engaging, feature-rich 3D experience directly in the browser, featuring diverse characters, weapons, vehicles, and a dynamic environment.

## User Preferences
I prefer iterative development, with clear communication before major changes.

## System Architecture

### UI/UX Decisions
- **Main Menu System**: Features PLAY GAME, SETTINGS, STATISTICS, and SHOP options.
- **Dynamic Environment**: Floridian Marsh theme with murky atmosphere, cypress trees, Spanish moss, dark swamp water, and a dynamic day/night cycle.
- **Mobile Controls**: Virtual joystick for movement and action buttons for touch devices.

### Technical Implementations
- **Core Technology**: Three.js (r128) for 3D graphics, Vanilla JavaScript for game logic, HTML5/CSS3 for UI.
- **Game Structure**: Single-file game (`index.html`) containing HTML, CSS, and JavaScript.
- **Movement & Combat**:
    - Character-specific jump counts and gliding mechanics.
    - Enhanced melee combat with unique animations and improved hitboxes for sword and hammer.
    - Projectile collision detection with environment elements.
    - Piercing projectiles for certain weapons (cannon, catapult).
- **Weapon System**:
    - Starting pistol, with additional weapons dropping from slain hunters (25% chance).
    - Purchased weapons expand the loot pool.
    - Weapons despawn after 30 seconds.
    - Special weapon types: Flamethrower (stream particles), Tesla Coil (chain lightning jumps between enemies), Boomerang (returns to player).
- **Stat Upgrades**: Permanent, stackable upgrades like Speed Boost, Quick Draw, Jump Height, and Lucky Feather, persisting across games.
- **Coin System & Shop**:
    - Earn coins from defeating hunters.
    - In-game shop (`Duck Mart`) for purchasing lives, full heals, shields, premium characters, and weapons.
    - Coins and character unlocks persist across sessions.
- **Special Orb System**: Orbs drop from hunters (25% chance) to charge character-specific special abilities.
- **Statistics Tracking**: Comprehensive tracking of high score, average score, total kills, time in vehicles, favorite weapon, and game count, all persisting via `localStorage`.

### Feature Specifications
- **Game Modes**: Survival, Endless Horde, Boss Rush, Time Attack.
- **Vehicles**: Pilotable Hunter Trucks and Tanks, hijackable after defeating drivers. Tanks fire explosive shells.
- **Grenades**: Throwable grenades with AOE damage and a 3-second cooldown.
- **Playable Characters**:
    - **Default**: Duck (classic), Titan Turkey (charge, stomp), Kung Pow Chicken (combo, invisibility), Merica Mallard (AOE, bombs), Chick 7 (tornado), Loonatic (berserker rage), Eggy Surprise (rolling egg, explosion on death).
    - **Premium (Unlockable)**: Golden Duck (2x coins), Phoenix Fowl (explosion immunity, fire aura), Robot Rooster (faster attack, laser eyes), Poultrygeist (haunt, doppelganger), Duck Norris (roundhouse kick, chuck flurry), Quackula (lifesteal, bat swarm).
    - Each character has unique visual designs, primary (Q key) and special (orb-powered) abilities.
- **Enemy Types**: Basic Hunter, Catapult Hunter (explosive projectiles), Hulk Hunter (melee-only, multiple lives). Progressive difficulty with Easy/Normal/Hard modes.
- **Gore Effects**: Blood particles on enemy defeat.

## External Dependencies
- **Three.js**: Used for 3D graphics rendering.
- **Python's built-in HTTP server**: Used for serving the static game files locally on port 5000.
- **localStorage**: Utilized for persistent storage of game statistics, settings, coins, and character unlocks across browser sessions.