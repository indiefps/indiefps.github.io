## Dev Log – Week 3  ( 5-Nov-2026 to 11-Nov-2026 )

### Overview
Week 3 marked the clear transition from pure white-box mechanics into the placeholder assets phase. Skeletal animation, real models, textures, and stronger editor/authoring tools landed, while the modular library structure continued to solidify and cross-platform builds improved.

### Major Progress
1. Assets & Rendering
    * Assimp integrated
    * Zombie NPC model loading and rendering
    * Skeletal bones + animation support
    * Basic animation switching driven by enemy state (idle / walk / etc.)
    * Temporary skybox added
    * Lighting adjustments for placeholder scenes
    * Alpha test fixes
    * Old procedural gun replaced with glTF weapon model
    * Texture cache and UV axis fixes continued from previous week
2. Modular Refactor Continues
    * MapLoader and Audio moved into libassets
    * Further cleanup of DLL exports
    * Header standardization (#pragma once)
    * Accidental ignore of src/assets restored
    * Overall structure becoming more stable
3. Editor Improvements
    * Textures now drawn in the editor
    * Per-face texture selection
    * Texture select UI added
    * Brush selection improvements
    *  Map loading / exporting kept in sync between editor, map compiler, and game
    * Auto-append of .json / .bvh extensions for convenience
    * Various MapIO and export bug fixes
4. Physics & AI
    * Enemy physics switched toward CharacterVirtual (Jolt)
    * Pathfinding adjustments
    * Script work for maps with displacements
5. Build & Platform
    * Portable MSVC build support improved
    * Linux build fixes
    * Build documentation updated
    * Project logo added

### State at End of Week
By mid-November the project had:
* Walking / animated zombies (placeholder models)
* Real glTF weapon
* Working texture pipeline in both editor and game
* Significantly more usable editor for textured brushwork
* Cleaner modular libraries
* Better cross-platform (especially Windows/MSVC) build story
The visual identity of the game started to emerge. It no longer looked like pure white-box geometry.

### Notable Themes
* Placeholder assets era begins in earnest — models, animations, textures, skybox
* Editor becoming a real content tool rather than just a prototype
* Build robustness receiving serious attention (portable MSVC, Linux fixes, docs)
* Continued tension between new features and keeping the modular structure clean

### Open / Ongoing
* Stairs / multi-level pathfinding still not fully solved
* Animation and model pipeline still early (but functional)
* Some temporary systems (skybox noted as temporary)
* Vertical Slice map still not the primary focus yet
