## Dev Log – Week 2 ( 29-Oct-2026 – 4-Nov-2026 )

### Overview
Week 2 shifted from pure foundation-building into gameplay deepening and the start of a major architectural cleanup. Core interactions became more interesting (traps, gravity-gun combat, enemy states), while the codebase began moving toward proper modular libraries and real texture support.

### Major Progress
1. Gameplay & Enemy Systems
   * Simple Finite State Machine (FSM) for enemies (Idle / Chase / Attack / etc.)
   * Fixed player passing through enemies
   * Trap system implemented (early falling / crush style traps)
   * Gravity gun can now launch physics objects to kill enemies
   * Camera shake added for impact feedback
   * Attempted fix for enemies pushing the player under stairs
2. Level Flow
   * Basic map switching support
   * Simple level state machine started (foundation for multi-map progression)
3. Architecture Refactor (Major) Began extracting systems into proper shared libraries:
   * libcore
   * libgeometry
   * libphysics (pulled out of the game executable)
   * Preparation for libassets
   * Game executable moved out of the old game/ folder
   * Multi-part refactoring commits (parts 2–4)
This was the start of the modular structure that later became src/core, src/geometry, src/physics, src/assets, etc.
4. Map Format & Assets Pipeline
   * Map format evolved (v6 added materials lump, v7 introduced stride-11 vertices + real UVs)
   * Texture loading experiments (PNG support)
   * Texture cache introduced
   * light_spot support added
5. Conversion tooling:
   * Quake source map → custom JSON/MBVH format
   * Early VMF → JSON conversion scripts
   * WIP Half-Life 2 related extraction experiments
6. Tooling & Quality of Life
   * Safer MapIO loading in the editor for converted maps
   * Various cleanup and stride/UV fixes

### State at End of Week
By early November the project had:
* Enemies with basic state-driven behavior
* Functional traps and gravity-gun combat utility
* Camera feedback
* Working (if simple) map transitions
* A clear direction toward modular libraries
* First real steps into textured geometry and material support
The game was no longer just a tech demo of movement + shooting — interactions were becoming more intentional.

### Notable Themes
* Gameplay first, then structure: New features (traps, FSM, gravity gun kills) landed before the big refactor.
* Asset readiness: Heavy focus on map format and texture pipeline in the second half of the week.
* Technical debt awareness: The multi-part refactor shows recognition that the early rapid prototype needed better boundaries.

### Open Issues / Focus Going Forward
* Stairs / multi-level pathfinding still problematic
* Trap and enemy interaction still incomplete in places
* Texture / material system still early
* Refactor not yet fully settled
