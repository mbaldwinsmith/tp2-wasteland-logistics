# STRUCTURE.md  
Directory & File Structure for **Wasteland Logistics**

This document defines the recommended folder layout and file organisation for the Transport Fever 2 overhaul mod **Wasteland Logistics**.  
It ensures consistency, clarity, and maintainability across all contributions.

---

# 1. Overview

The mod follows standard Transport Fever 2 conventions:

- All functional content resides under `/res/`
- Documentation lives under `/docs/`
- Root folder contains `mod.lua`, `LICENSE`, and metadata files

wasteland_logistics/
│
├── mod.lua
├── LICENSE
├── README.md
│
├── docs/
│ ├── CONCEPT.md
│ ├── DESIGN.md
│ └── STRUCTURE.md
│
└── res/
├── config/
├── models/
├── scripts/
└── textures/


---

# 2. /res/config/

Contains configuration files for cargo, industries, vehicles, UI, and maps.

res/config/
│
├── cargo/ # cargo type definitions
│ ├── scrap_metal.lua
│ ├── dirty_water.lua
│ ├── raw_organics.lua
│ ├── refined_scrap.lua
│ ├── clean_water.lua
│ ├── biofuel.lua
│ ├── tech_fragments.lua
│ ├── energy_cells.lua
│ └── archaeotech_components.lua
│
├── industry/ # industry definitions & placement rules
│ ├── scrapyard_processor.lua
│ ├── purification_plant.lua
│ ├── radfarm.lua
│ ├── archivist_lab.lua
│ ├── energy_stabiliser.lua
│ └── reconstruction_mill.lua
│
├── models/
│ ├── vehicle/ # model metadata (.mdl)
│ ├── building/ # industry & town buildings
│ └── asset/ # props, decorations, ruins
│
├── map/ # custom map themes, climates
│ ├── wasteland_coast_theme.lua
│ ├── ash_plains_theme.lua
│ ├── verdant_fringe_theme.lua
│ ├── high_barrens_theme.lua
│ └── deadlines_theme.lua
│
├── ui/ # UI replacement icons, colours, layouts
│ ├── icons/
│ ├── styles/
│ └── colours.lua
│
└── strings/ # localisation files
├── en.lua
├── de.lua
└── fr.lua


---

# 3. /res/models/

Contains 3D models, collisions, and animation files.

res/models/
│
├── vehicle/
│ ├── era1/
│ │ ├── bus_dust_mule/
│ │ │ ├── bus_dust_mule.mdl
│ │ │ ├── lod_0.msh
│ │ │ ├── lod_1.msh
│ │ │ ├── lod_2.msh
│ │ │ └── materials/
│ │ └── truck_rusthound/
│ │ ├── truck_rusthound.mdl
│ │ └── ...
│ │
│ ├── era2/
│ ├── era3/
│ └── era4/
│
├── building/
│ ├── industries/
│ ├── town/
│ └── infrastructure/
│
└── asset/
├── ruins/
├── debris/
├── signage/
├── vegetation/
├── props_misc/
└── fx/ # smoke, sparks, light meshes

---

# 4. /res/textures/

All custom textures, terrain materials, UI icons, and vehicle skins.

res/textures/
│
├── vehicles/
│ ├── dust_mule/
│ │ ├── albedo.dds
│ │ ├── rough.dds
│ │ ├── metal.dds
│ │ └── ao.dds
│ └── ...
│
├── buildings/
│
├── assets/
│
├── terrain/
│ ├── cracked_earth.dds
│ ├── rust_asphalt.dds
│ ├── mutated_grass.dds
│ └── irradiated_accent.dds
│
└── ui/
├── cargo_icons/
├── vehicle_icons/
├── map_overlay/
└── ui_theme.dds


---

# 5. /res/scripts/

Lua scripts governing hazard zones, industry logic, and utility functions.

res/scripts/
│
├── hazard/
│ ├── hazard_controller.lua
│ ├── region_markers.lua
│ └── maintenance_modifiers.lua
│
├── industry_logic/
│ ├── chain_balancing.lua
│ ├── economy_events.lua
│ └── production_overhaul.lua
│
└── utils/
├── math_helpers.lua
├── table_helpers.lua
└── debug.lua


---

# 6. docs/

All major documentation for contributors.

docs/
│
├── CONCEPT.md
├── DESIGN.md
└── STRUCTURE.md


Future docs may include:
- `ASSETS_GUIDE.md`
- `VEHICLE_GUIDE.md`
- `INDUSTRIES.md`
- `CONTRIBUTING.md`

---

# 7. Root Files

### mod.lua
Defines the mod metadata:
- title
- description
- version
- author
- dependencies

### LICENSE
The MIT license (default).

### README.md
The public-facing description of the mod for GitHub & Steam Workshop.

---

# 8. Naming Conventions

### Files
- lowercase, underscores
- avoid spaces
- descriptive but concise

Examples:
scrapyard_processor.lua
dust_mule_bus.mdl
levrail_strider_albedo.dds

### Vehicles
vehicle_<era><type><name>

### Industries
industry_<function>_<descriptor>


---

# 9. GitHub Branch Structure

Optional but recommended:

- `main` — stable release-ready branch  
- `dev` — active development  
- `assets` — raw art assets and blend files  
- `scripts` — experimental Lua changes  
- `vehicles` — 3D asset development  
- `industry` — data-driven industry and cargo files  

---

# 10. Packaging for Release

Packages include:

- `/res/` folder  
- `mod.lua`  
- `LICENSE`  
- `README.md`  

All unnecessary source files (e.g., `.blend`, `.psd`, raw exports) remain excluded.

---

# 11. Future Extensions

Possible future directories:
/res/sound/ # ambient audio, vehicle loops
/res/particles/ # custom particle effects
/docs/WIKI/ # expanded GitHub wiki pages


---

# 12. Summary

This structure ensures:
- modular development  
- easy onboarding for contributors  
- clean separation between models, textures, scripts, and config  
- straightforward packaging for Steam Workshop  

Wasteland Logistics is designed to scale into a fully modular overhaul while remaining readable and maintainable for long-term development.
