# Duck Defense 3D

## Overview
Duck Defense 3D is a browser-based 3D survival game built with Three.js. It's a twist on the classic Duck Hunt game - this time, you play as a duck defending yourself against waves of hunters in a murky Florida swamp!

## Project Structure
- `index.html` - Single-file game containing HTML, CSS, and JavaScript
- Simple static site served via Python HTTP server

## How to Play
- **W/A/S/D** - Move forward/left/back/right
- **MOUSE** - Aim direction  
- **SPACE** - Jump (press twice for double jump with wing flapping!)
- **LEFT CLICK** - Attack/Shoot
- **E** - Enter/Exit vehicles
- **Collect weapons** to increase firepower against hunters
- **Steal hunter trucks** after eliminating the driver
- **Survive as long as possible!**

## Game Features

### Movement & Combat
- **Double Jump**: Jump twice in mid-air with animated wing flapping
- **Enhanced Melee Combat**: 
  - Sword performs wide arc swing animation with improved hitbox
  - Hammer delivers powerful vertical chopping strikes
- **Improved Hitboxes**: Sword has 1.3x range multiplier for better arc coverage

### Weapons
- **Fists** - Basic melee
- **Sword** - Enhanced with decorative crossguard, pommel, and blade edge. Wide sweeping attacks
- **Hammer** - Larger head, longer handle, vertical chopping animation
- **Rifle** - Standard ranged weapon
- **Machine Gun** - Rapid fire
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
- Kill the driver to hijack the vehicle
- Drive with W/A/S/D, run over enemies for kills
- Press E to enter/exit vehicles

### Advanced Mechanics
- Enemy AI hunters that shoot at the player
- Projectile collision with trees and hut (both player and enemy projectiles blocked)
- Piercing projectiles for cannon/catapult (go through multiple enemies)
- Catapult ground blast radius - explosions damage nearby enemies
- Improved projectile accuracy with larger hit detection
- Weapon pickup system
- Score and lives tracking
- Progressive difficulty
- Gore effects and blood particles
- Mobile controls support (toggle in settings)

## Technology Stack
- **Three.js** (r128) - 3D graphics rendering
- **Vanilla JavaScript** - Game logic
- **HTML5/CSS3** - UI and styling

## Development
The game runs on port 5000 via Python's built-in HTTP server. No build process or dependencies are required.

## Recent Changes
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
