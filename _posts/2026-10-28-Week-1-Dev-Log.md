## Dev Log – Week 1  ( 21-Oct-2026 to 28-Oct-2026 )

### Overview

This was the founding week of the project. Starting from an empty repository, the core end-to-end pipeline (Editor → Map Compiler → Game) was established, and the first playable systems came online extremely quickly.

### Major Progress

1. Project Bootstrap & Pipeline
	*	Initial commit and first working end-to-end flow: Editor → JSON → BSP/BVH → Game
	*	Replaced BSP with BVH early on
	*	Project directory reorganized
	*	Basic version stamping (git branch/commit) added
	*	Cross-platform compile & run path started (Windows + Linux considerations)
2. Editor Foundations
	*	Basic brush and entity editing with gizmos
	*	3D view + multiple 2D orthographic views
	*	Dockable layout + layout switching (default ↔ quad view)
	*	Orientation cube
	*	Entity select list and basic property editing
	*	Simple undo support
	*	Early graph/connection system for entities (foundation for later node editor)
	*	Compile-and-run workflow improvements
3. Core Gameplay Systems
	*	Player movement, jump, and crosshair
	*	Weapon firing + simple recoil animation
	*	func_door with “E” use interaction
	*	func_physbox / pushable physics objects (player can push boxes)
	*	Gravity gun implemented
	*	Explosive barrels (prop_physics based)
	*	Basic enemy (npc_zombie) spawning and AI chase logic
	*	Trigger system (trigger_multiple) and simple level control
	*	Early collision improvements between player, enemies, and physics objects
4. Navigation & AI Experiments
	*	Basic enemy chase logic
	*	Simple nav mesh attempt
	*	A* work-in-progress
	*	Node graph for enemy pathfinding introduced (worked on flat maps by end of week)
	*	Multiple iterations on pathfinding reliability
5. Audio & Visual Polish (Early)
	*	Basic SDL_Mixer sound effects (shoot, hit, door, explosion)
	*	Simple brush texturing
	*	Improved gun visual shape
	*	Better initial scene scale and spawn placement

### Notable Technical Decisions

* Early switch from BSP to BVH for collision
* Hybrid approach: custom BVH/ray tracing for player + Jolt Physics for dynamic objects
*	Entity connection system prepared for future visual graph editing
*	Map compiler split into more logical modules toward end of week

### State at End of Week

By 28 Oct the project already had:

*	A usable (if basic) level editor
*	A working map compile pipeline
*	Playable movement + shooting
*	Doors, physics boxes, gravity gun, explosive barrels
*	Enemies that could chase the player on flat geometry
*	Basic sound and visual feedback

This was a high-velocity foundation week. Most core pillars of the eventual Vertical Slice (physics interactions, gravity gun, enemies, editor toolchain) were already present in prototype form.

### Open / Known Issues at Week End

*	Enemy pathfinding only reliable on flat maps
*	Stairs / multi-level navigation still broken
*	Visuals and juice still very minimal
*	Code organization still early (would be heavily refactored in later weeks)
