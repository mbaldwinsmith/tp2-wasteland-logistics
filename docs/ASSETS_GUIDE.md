# ASSETS_GUIDE.md  
Asset Creation Guide for **Wasteland Logistics**

This document defines standards, workflows, and requirements for all 3D models, textures, scenery props, terrain materials, and UI assets used in the overhaul mod.

It is intended for artists, asset creators, and technical contributors.

---

# 1. Overview

Wasteland Logistics requires a large number of custom assets:

- **Vehicles** (see VEHICLES.md)
- **Industries & Buildings**
- **Town Structures**
- **Environmental Props**
- **Ruin Sets**
- **Terrain Textures**
- **UI Icons & Overlays**

The goal is visual coherence: rust-punk → reconstruction → revival → post-post-apocalyptic.

Assets must balance performance with atmosphere.

---

# 2. Art Direction

### Aesthetic Phases
- **Era I:** scrap-built, rusted, mismatched, improvised  
- **Era II:** repaired, improving quality, functional  
- **Era III:** clean energy, lightweight alloys, neon accents  
- **Era IV:** sleek composites, embedded lights, smooth geometry  

### Colour Palette
- rust reds  
- oxidised turquoise  
- industrial blues  
- sand ochres  
- muted greens  
- neon cyan/purple (Era III–IV accents)

### Material Style
- PBR compatible  
- rough metals  
- matte plastics  
- weathered wood  
- dusty, gritty surfaces  
- optional emissive strips (Era III–IV)

---

# 3. File Structure
Assets should follow the folder conventions defined in `STRUCTURE.md`:
res/models/vehicle/
res/models/building/
res/models/asset/
res/textures/vehicles/
res/textures/assets/
res/textures/terrain/
res/config/models/

---

# 4. Naming Conventions

### General
<category><descriptor><variant>

### Examples
ruin_highrise_A
sign_reclaimers_small
scrapheap_01
tree_mutant_oak
terrain_cracked_earth

### Textures
asset_<name>_(albedo|metal|rough|ao|normal).dds

### Model files
<name>.mdl
lod_0.msh
lod_1.msh
lod_2.msh

---

# 5. Model Requirements

### File Format
- `.mdl` for model definition  
- `.msh` or `.msh.blob` for mesh  
- `.mtl.lua` for material metadata (optional)

### Geometry
- Clean topology  
- Avoid excessive triangles  
- Recommended polycounts:
  - Props: 300–3,000 tris  
  - Buildings: 1k–20k tris  
  - Large ruins: up to 40k tris (with good LODs)  

### LODs
Each asset must include:
- `lod_0` — full detail  
- `lod_1` — ~40–60% poly  
- `lod_2` — ~15–25% poly  

### Scale
Match TF2 metric scale:
- Human height ~1.8 m  
- Vehicles scale to vanilla equivalents  

---

# 6. Material Requirements

### PBR Channels
Required:
- Albedo  
- Metalness  
- Roughness  
- Ambient Occlusion  

Optional:
- Normal map  
- Emissive map (Era III–IV vehicles, neon props)

### File Formats
- `.dds` (recommended)  
- `.png` allowed during WIP  

### Texture Size Guidelines
- Props: 256–1024  
- Buildings: 1024–2048  
- Ruins: 2048–4096  
- Vehicles: 1024–4096  

---

# 7. Environmental Assets

These define the atmosphere and worldbuilding.

---

## 7.1 Ruins

### Description
Collapsed high-rises, scorched vehicles, crumbling roads, broken pipes.

### Variants
- highrise shells  
- skeletal towers  
- tilted highway slabs  
- broken monorail pylons  
- wrecked vehicles (cars, buses, freight)  
- rubble piles  

### Guidelines
- heavily weathered materials  
- jagged geometry  
- use decals for cracks/dust  

---

## 7.2 Vegetation (Mutant & Natural)

### Types
- twisted trees  
- fungus clusters  
- oversized leaves  
- burnt snags  
- irradiated grass patches  

### Technical
- alpha masking for leaves  
- wind effect optional  
- low-poly trunks preferred  

---

## 7.3 Settlement Props

### Examples
- tents  
- water barrels  
- scrap walls  
- neon signs  
- tarps  
- solar rigs  
- generator units  
- watchtowers  

### Notes
- small assets should use atlased textures  
- match faction colour schemes where applicable  

---

## 7.4 Industrial Props

### Examples
- pipes, valves, tanks  
- nuclear warning beacons (generic, non-IP)  
- cables, vents, conduits  
- salvage robots / cranes (non-humanoid)  
- conveyor belts  

---

## 7.5 Roadside & Infrastructure

### Examples
- broken streetlamps  
- cracked pavement  
- rusted guardrails  
- debris piles  
- power-line towers  
- rail remnants  

---

# 8. Terrain Textures
Terrain textures live in:
res/textures/terrain/


### Types Needed
- cracked earth  
- ash dust  
- desert sand  
- rust-stained asphalt  
- mutated grass  
- overgrown dirt  
- irradiated accents (subtle only)  

### Texture Style
- gritty, high-frequency patterns  
- seamless tiling required  
- pairs with normal + rough maps  

---

# 9. Town Buildings

Towns grow visually in three phases:

### Tier 1 — Scrap Settlement
- metal huts  
- rusted fences  
- tarp awnings  
- makeshift market  

### Tier 2 — Reconstructed Community
- hardened shelters  
- reclaimed wood buildings  
- early solar panels  
- water towers  

### Tier 3 — Revival Town
- neon shopfronts  
- rebuilt streets  
- clean-energy rooftops  
- small monorail/station hubs  

Each tier uses progressively cleaner materials.

---

# 10. Industry Buildings

Each industry needs:

- main building model  
- optional sub-buildings  
- ground decal (dirt, scrap, concrete pad)  
- props (piles, machinery, lights)  
- smoke/steam emitters  
- terrain alignment rules  

Buildings should reflect era:
- early → scrap & welded  
- mid → repaired, industrial  
- late → clean technical structures  

---

# 11. UI & Iconography

### Cargo Icons
Size: **64×64** or **128×128**  
Style:
- bold silhouettes  
- rust-punk outlines  
- subtle texture grain  

### UI Colours
- dusty oranges  
- steel blues  
- sand neutrals  
- neon highlights  

### Map Overlay
- monochrome amber-green  
- pip-boy-like but original design  

Icons live in:
res/textures/ui/icons/

---

# 12. FX & Lighting

### Effects
- smoke plumes (steam, scrap smelters)  
- sparks (scrapyards)  
- dust clouds (vehicles in Ash Plains)  
- soft glows (Era III–IV emissives)  

### Light Props
- flickering neon  
- lanterns  
- solar lamps  
- engine glow  

Effects must be low-impact and use TF2’s built-in particle systems.

---

# 13. Performance Guidelines

- prefer atlased textures  
- LOD distances tuned to vehicle size  
- avoid too many light sources per scene  
- background ruins should have simple collisions  
- use triangle-efficient meshes  
- use shared materials where possible  

---

# 14. Exporting Instructions

### Workflow
- Model → UV unwrap → Texture → Export → Create `.mdl`  

### Export Format
- `.fbx` → converted via ModelEditor  
- ensure smoothing groups preserved  
- align pivot to centre-bottom  

### Testing
After export:
- check LOD transitions  
- verify materials  
- test collisions  
- test performance in a 200–500 asset scene  

---

# 15. Contribution Checklist

Before committing an asset:

- [ ] model scaled correctly  
- [ ] 3 LODs included  
- [ ] textures exported `.dds`  
- [ ] consistent naming  
- [ ] materials correct  
- [ ] `.mdl` file tested  
- [ ] no IP-locked designs  
- [ ] fits aesthetic of its era  

---

# 16. Licensing

All assets created for Wasteland Logistics are licensed under the MIT License.  
Contributors must ensure all materials are fully original or CC0.

