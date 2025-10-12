# Duck Defense 3D

## Overview
Duck Defense 3D is a browser-based 3D survival game built with Three.js. It's a twist on the classic Duck Hunt game - this time, you play as a duck defending yourself against waves of hunters!

## Project Structure
- `index.html` - Single-file game containing HTML, CSS, and JavaScript
- Simple static site served via Python HTTP server

## How to Play
- **W/A/S/D** - Move forward/left/back/right
- **MOUSE** - Aim direction  
- **SPACE** - Jump
- **LEFT CLICK** - Attack/Shoot
- **Collect weapons** to increase firepower against hunters
- **Survive as long as possible!**

## Game Features
- 3D terrain with hills, trees, water, and bushes
- Dynamic day/night cycle
- Multiple weapons: Fists, Sword, Hammer, Rifle, Machine Gun, Catapult, Cannon
- Enemy AI hunters that shoot at the player
- Weapon pickup system
- Score and lives tracking
- Progressive difficulty

## Technology Stack
- **Three.js** (r128) - 3D graphics rendering
- **Vanilla JavaScript** - Game logic
- **HTML5/CSS3** - UI and styling

## Development
The game runs on port 5000 via Python's built-in HTTP server. No build process or dependencies are required.

## Recent Changes
- **2025-10-12**: Fixed JavaScript bug in weapon model creation (handleMat variable scope issue in hammer case)
- **2025-10-12**: Initial import and setup in Replit environment

## Deployment
The game is configured for autoscale deployment using Python's HTTP server on port 5000.
