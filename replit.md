# Duck Defense 3D

## Overview
Duck Defense 3D is a browser-based 3D survival game built with Three.js. It's a twist on the classic Duck Hunt game - this time, you play as a duck defending yourself against waves of hunters in a murky Florida swamp!

## Project Structure
- `index.html` - Single-file game containing HTML, CSS, and JavaScript
- Simple static site served via Python HTTP server

## Main Menu
The game features a full menu system:
- **PLAY GAME** - Start a new game with selected difficulty and character
- **SETTINGS** - Adjust difficulty, input method, and select your character
- **STATISTICS** - View your gameplay stats and score history graph
- **SHOP** - In-game store to spend coins on lives, weapons, and premium bird variants

## How to Play
- **W/A/S/D** - Move forward/left/back/right
- **MOUSE** - Aim direction  
- **SPACE** - Jump (multi-jump varies by character!)
- **HOLD SPACE (while falling)** - Glide with wings outstretched
- **LEFT CLICK** - Attack/Shoot (also fires tank cannon when driving)
- **Q** - Activate special ability (character-specific)
- **G** - Throw grenade (3 second cooldown)
- **E** - Enter/Exit vehicles
- **Collect weapons** dropped by slain hunters
- **Steal hunter trucks** after eliminating the driver
- **Survive as long as possible!**

## Game Features

### Movement & Combat
- **Character-Specific Jumps**: Each bird has different jump counts
  - Titan Turkey: 1 jump (heavy)
  - Duck, Merica Mallard, Loonatic: 2 jumps
  - Chick 7: 3 jumps
  - Kung Pow Chicken: 4 jumps (most agile!)
  - Eggy Surprise: 1 jump (can't fly, it's an egg!)
- **Gliding**: Hold SPACE while falling to glide with wings outstretched
- **Chick 7's 67 Wing Pattern**: Unique wing animation when jumping
- **Enhanced Melee Combat**: 
  - Sword performs wide arc swing animation with improved hitbox
  - Hammer delivers powerful vertical chopping strikes
- **Improved Hitboxes**: Sword has 1.3x range multiplier for better arc coverage

### Weapons
- **Pistol** - Default starting weapon, weak but reliable ranged weapon
- Weapons drop from slain hunters (25% chance) based on your available weapon pool
- Purchased weapons from the shop add to your loot drop possibilities
- Weapon pickups despawn after 30 seconds (fade out warning in last 5 seconds)

**Available Weapons:**
- **Pistol** - Weak starting ranged weapon (15 damage)
- **Sword** - Enhanced melee with decorative crossguard. Wide sweeping attacks
- **Hammer** - Heavy melee with vertical chopping animation
- **Rifle** - Standard ranged weapon (80 damage)
- **Machine Gun** - Rapid fire ranged weapon
- **Catapult** - Fires large orange projectiles that pierce through multiple enemies
- **Cannon** - Most powerful weapon with massive piercing projectiles

### Environment - Floridian Marsh
- Murky marsh atmosphere with humid fog
- Cypress trees with hanging spanish moss
- Dark swamp water patches
- Darker ground vegetation
- Dynamic day/night cycle with marsh-appropriate colors

### Vehicles
- **Hunter Trucks** - Spawn every 15-25 seconds with armed drivers
- **Tanks** - Spawn after 6 minutes (late game), heavily armored with explosive shells
- Kill the driver to hijack the vehicle
- Drive with W/A/S/D, run over enemies for kills
- **Tanks fire explosive shells** - Click to shoot when driving a tank
- Press E to enter/exit vehicles

### Grenades
- Press **G** to throw a grenade in the direction you're facing
- Grenades bounce and explode after a short fuse or 3 bounces
- 8-unit explosion radius deals up to 80 damage
- Damages enemies and tanks (tanks take 50% grenade damage)
- 3 second cooldown between throws

### Statistics Tracking
- **Score History Graph** - Visual display of your scores over time
- **High Score & Average Score** - Track your best and typical performance
- **Total Hunters Killed** - Lifetime kill count
- **Time in Vehicles** - How long you've spent driving trucks
- **Favorite Weapon** - Your most-used weapon based on kills
- **Games Played** - Total number of games
- All stats persist across browser sessions using localStorage

### Advanced Mechanics
- Enemy AI hunters that shoot at the player
- Projectile collision with trees and hut (both player and enemy projectiles blocked)
- Piercing projectiles for cannon/catapult (go through multiple enemies)
- Catapult ground blast radius - explosions damage nearby enemies
- Improved projectile accuracy with larger hit detection
- Weapon pickup system
- Score and lives tracking
- Progressive difficulty with Easy/Normal/Hard modes
- Gore effects and blood particles
- Mobile controls with virtual joystick for movement and action buttons

### Playable Characters
Each character has unique colors, features, a primary ability (Q key), and a special ability (orb-powered):

- **Duck** (Classic yellow) - No abilities, balanced gameplay
- **Titan Turkey** (Brown/red with wattle)
  - Primary (Q): Helmet Charge - doubles speed, rams through enemies for 10s
  - Special: Turkey Stomp - massive ground pound AOE attack
- **Kung Pow Chicken** (White with red headband)
  - Primary (Q): Martial Arts - 5s of combo attacks with increasing damage
  - Special: Ninja Vanish - become invisible for 8s, enemies can't target you
- **Merica Mallard** (Patriotic blue with Uncle Sam hat)
  - Primary (Q): Eagle Strike - instant AOE damage to nearby enemies
  - Special: Freedom Bombs - rain 6 explosive bombs from the sky
- **Chick 7** (Fluffy yellow baby chick)
  - Special: 67 Windy Wing - creates tornado that pushes enemies away, invulnerable during use
  - Wings animate in the signature 67 offset pattern
- **Loonatic** (Dark berserker loon with crazy red eyes)
  - Special: Berserker Rage - 80% faster weapon recharge for 10 seconds
  - Features red rage aura while active
- **Eggy Surprise** (Large rolling egg - can't attack!)
  - Can only roll around, no combat abilities
  - Gets cracked and leaks yolk as it takes damage
  - On death: Eggsplosion deals massive AOE damage, then transforms into random bird at full health!

### Premium Shop Characters (Unlockable)
- **Golden Duck** (Shiny golden with crown) - 500 coins
  - Earn 2x coins from kills!
  - Royal crown with gem
- **Phoenix Fowl** (Fiery orange with flames) - 750 coins  
  - Immune to explosions!
  - Fire aura damages nearby enemies (Q ability)
  - 3 jumps
- **Robot Rooster** (Metallic gray with LEDs) - 1000 coins
  - 50% faster attack speed!
  - Laser eyes ability (Q)
  - Glowing cyan eyes and antenna
- **Poultrygeist** (Spectral ghost chicken) - 850 coins
  - Primary (Q): Haunt - releases ghostly wave that damages and confuses enemies
  - Special: Doppelganger Duo - summons a ghost clone that mirrors you and attacks enemies!
  - Clone can be killed by enemies but lasts 20 seconds
  - Semi-transparent ghostly appearance with floating chains
  - 3 jumps

### Coin System & Shop
- **Earn coins** by defeating hunters (5 coins normal, 10 catapult, 15 hulk)
- **Golden Duck** earns 2x coins from all kills
- **Open the Shop** during gameplay to spend coins on:
  - Extra lives, full heals, and shields
  - Premium bird variants (permanent unlocks)
  - Weapons for the current game session
  - **Side Chick** companion that fights at your side!
- **Shields** block incoming damage (max 3 stacks)
- Coins persist across game sessions

### Special Orb System
- **Orbs drop** from slain hunters (25% chance)
- **Collect orbs** to charge your special ability
- **Click the special button** (bottom right) to activate
- Each orb gives you one special charge
- Special button shows your current charge count

### Enemy Types
- **Basic Hunter** (0-2 min) - Standard rifle-wielding hunter
- **Catapult Hunter** (2+ min) - Fires explosive projectiles, wears military helmet
- **Hulk Hunter** (4+ min) - Massive green brute with spiked club, multiple lives, melee only

## Technology Stack
- **Three.js** (r128) - 3D graphics rendering
- **Vanilla JavaScript** - Game logic
- **HTML5/CSS3** - UI and styling

## Development
The game runs on port 5000 via Python's built-in HTTP server. No build process or dependencies are required.

## Recent Changes
- **2026-01-29**: Weapon loot system overhaul
  - Added weak pistol as default starting weapon
  - Weapons only drop from slain hunters (25% chance)
  - Dropped weapons are randomly selected from the player's available pool
  - Purchased weapons from shop add to the loot drop possibilities
  - Weapon pickups despawn after 30 seconds with fade-out warning
- **2026-01-27**: Tanks and grenades
  - Added tanks that spawn after 6 minutes with armored drivers
  - Tanks have 300 health and fire explosive shells at players
  - Players can hijack tanks and fire explosive shells by clicking
  - Added grenade throw system (G key) with 3 second cooldown
  - Grenades bounce, explode after fuse, deal AOE damage with knockback
- **2026-01-27**: In-game shop system
  - Added coin currency earned from defeating hunters (5/10/15 based on enemy type)
  - Duck Mart shop for purchasing extra lives, weapons, and premium characters
  - Added 3 premium unlockable characters: Golden Duck, Phoenix Fowl, Robot Rooster
  - Golden Duck earns 2x coins, Phoenix Fowl immune to explosions, Robot Rooster attacks 50% faster
  - Coins and character unlocks persist across sessions
- **2026-01-27**: Movement and weapon improvements
  - Character-specific jump counts (Titan Turkey: 1, Kung Pow Chicken: 4, etc.)
  - Added gliding mechanic - hold SPACE while falling to glide
  - Chick 7 uses unique 67 wing pattern when jumping
  - Weapons now drop from slain hunters (20% chance) instead of spawning randomly
  - Enhanced visual appearances for all bird variants
- **2026-01-23**: New bird variants
  - Added Chick 7 with 67 Windy Wing tornado special (pushes enemies, invulnerable)
  - Added Loonatic berserker loon with 80% weapon recharge boost
  - Added Eggy Surprise - rolling egg that eggsplosions on death and transforms into random bird
  - Centralized player damage handling with invulnerability support
- **2026-01-23**: Enemy behavior improvements
  - Centralized enemy death handling with handleEnemyDeath function for consistent behavior
  - Hulk hunters now have proper multi-life system (loses a life, regenerates health, rage flash effect)
  - Catapult hunters shoot explosive projectiles with AOE damage on ground impact
  - Hulk hunters use melee-only attacks with knockback effect on player
  - Enemy movement speeds differentiated by type (hulks faster, catapults slower)
- **2026-01-23**: Special orb system and new enemy types
  - Added special orb pickups that drop from slain enemies (25% chance)
  - Each character now has both primary (Q key) and special (orb-powered) abilities
  - Titan Turkey: Turkey Stomp ground pound AOE
  - Kung Pow Chicken: Ninja Vanish invisibility (enemies can't target you)
  - Merica Mallard: Freedom Bombs aerial bombardment
  - Added special button UI showing charge count
  - Added Catapult Hunter (spawns after 2 min) - fires explosive projectiles
  - Added Hulk Hunter (spawns after 4 min) - giant with spiked club, multiple lives
- **2026-01-23**: Character selection system
  - Added 4 playable characters: Duck, Titan Turkey, Kung Pow Chicken, Merica Mallard
  - Each character has unique visual design and colors
  - Character-specific primary abilities activated with Q key
  - Ability cooldown and duration system with UI indicators
  - Character selection persists to localStorage
- **2026-01-23**: Menu system and stats tracking
  - Created dedicated main menu with PLAY/SETTINGS/STATISTICS options
  - Added settings page with difficulty selection (Easy/Normal/Hard)
  - Added input method selection (Computer/Mobile)
  - Implemented comprehensive statistics page with score history graph
  - Stats include: high score, average score, total kills, time played, vehicle time, favorite weapon
  - All settings and stats persist to localStorage
- **2026-01-23**: Vehicles and combat improvements
  - Added pilotable hunter trucks that spawn with armed drivers
  - Players can hijack vehicles after killing the driver
  - Added catapult ground blast radius with explosion particles
  - Improved projectile accuracy with larger hit detection radii
  - Added mobile controls support (jump/attack buttons in settings)
  - Added E key for vehicle entry/exit
- **2025-10-12**: Major gameplay enhancements
  - Added double jump mechanic with wing flapping animation
  - Enhanced sword with hilt, pommel, and arc swing animation
  - Improved hammer with larger head and vertical chop animation
  - Enlarged catapult and cannon weapon models
  - Made cannon/catapult projectiles larger and able to pierce multiple enemies
  - Added projectile collision with obstacles (trees and hut)
  - Transformed environment to floridian marsh theme
  - Improved combat hitboxes
  - Fixed projectile system bug preventing enemy projectiles from inheriting player weapon properties
- **2025-10-12**: Fixed JavaScript bug in weapon model creation (handleMat variable scope issue in hammer case)
- **2025-10-12**: Initial import and setup in Replit environment

## Deployment
The game is configured for autoscale deployment using Python's HTTP server on port 5000.
