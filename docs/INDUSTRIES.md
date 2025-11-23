# INDUSTRIES.md  
Industry Chains & Systems for **Wasteland Logistics**

This document defines all cargo chains, industry types, production logic, balancing targets, and technical implementation for the post-war reconstruction economy.

---

# 1. Overview

Wasteland Logistics replaces the vanilla Transport Fever 2 economic system with a salvage-driven reconstruction economy consisting of:

- **9 new cargo types**
- **13–18 new industries**
- **3 economy tiers** (Early, Mid, Late)
- **dynamic settlement demand**
- **optional hazard modifiers**

Each industry is designed to reflect scarcity, rebuilding, and technological rediscovery.

---

# 2. Cargo Types

| Cargo | Era | Description |
|-------|------|-------------|
| **Scrap Metal** | Early | Rusted debris from ruins and vehicles |
| **Dirty Water** | Early | Unpurified water from wells/coast marsh |
| **Raw Organics** | Early | Fungus, mutated crops, scavenged food |
| **Refined Scrap** | Mid | Processed scrap usable for machinery |
| **Clean Water** | Mid | Purified water from filters/chem plants |
| **Biofuel** | Mid | Processed organics for engines |
| **Tech Fragments** | Mid | Salvaged pre-war circuitry |
| **Energy Cells** | Late | Stabilised power storage units |
| **Archaeotech Components** | Late | High-tech recovered artefacts |

All cargo types require icons, colour sets, and Lua config entries.

---

# 3. Industry Chain Overview

A high-level view of all material flows:

[ Ruins ] → Scrap → Refined Scrap → Components → Construction Materials

[ Wells / Coast ] → Dirty Water → Clean Water

[ Mutant Farms ] → Raw Organics → Food / Bio-Mash → Biofuel

[ Ruins ] → Tech Fragments → Schematics → Archaeotech Components

[ Solar / Wind ] → Raw Energy → Energy Cells


---

# 4. Early-Game Industries (Scavenger Years)

These industries define survival-level logistics. Production is low and unreliable.

---

## 4.1 Ruined District  
**Type:** Extractor  
**Inputs:** None  
**Outputs:** Scrap Metal  
**Description:** Wrecked buildings and collapsed highways. Salvagers recover usable metal.  
**File:** `industry/ruins.lua`

---

## 4.2 Vehicle Grave  
**Type:** Extractor  
**Inputs:** None  
**Outputs:** Scrap Metal (higher yield)  
**Description:** Sun-baked graveyard of rusted cars, buses, and convoys.  
**File:** `industry/vehicle_grave.lua`

---

## 4.3 Dirty Well  
**Type:** Extractor  
**Inputs:** None  
**Outputs:** Dirty Water  
**Description:** Unfiltered groundwater from contaminated aquifers.  
**File:** `industry/dirty_well.lua`

---

## 4.4 Mutant Orchard / Rad-Farm / Fungus Pit  
**Type:** Extractor  
**Inputs:** None  
**Outputs:** Raw Organics  
**Variants:** 3 visual types  
**Description:** Mutated crops and fungal beds cultivated by settlements.  
**File:** `industry/radfarm.lua`

---

# 5. Mid-Game Industries (Reconstruction Dawn)

These industries unlock stability, refining, and industry-level productivity.

---

## 5.1 Scrapyard Processor  
**Type:** Processor  
**Inputs:** Scrap Metal  
**Outputs:** Refined Scrap  
**Description:** Heavy crushers and magnetic separators refine metal for reuse.  
**File:** `industry/scrapyard_processor.lua`

---

## 5.2 Assembly Yard  
**Type:** Processor  
**Inputs:** Refined Scrap  
**Outputs:** Basic Components / Construction Materials  
**Description:** Produces critical parts needed for rebuilding towns.  
**File:** `industry/assembly_yard.lua`

---

## 5.3 Purification Plant  
**Type:** Processor  
**Inputs:** Dirty Water  
**Outputs:** Clean Water  
**Description:** Uses charcoal filters and early chem rigs to make water potable.  
**File:** `industry/purification_plant.lua`

---

## 5.4 Food Still / Smokehouse  
**Type:** Processor  
**Inputs:** Raw Organics  
**Outputs:** Processed Food  
**Description:** Essential early food production for towns.  
**File:** `industry/food_still.lua`

---

## 5.5 Biofuel Refinery  
**Type:** Processor  
**Inputs:** Raw Organics  
**Outputs:** Biofuel  
**Description:** Converts organics into basic fuel for vehicles.  
**File:** `industry/biofuel_refinery.lua`

---

## 5.6 Archaeotech Depot  
**Type:** Extractor  
**Inputs:** None  
**Outputs:** Tech Fragments  
**Description:** Excavation site recovering pre-war circuitry from deep rubble.  
**File:** `industry/archaeotech_depot.lua`

---

# 6. Late-Game Industries (Revival Age → New World Era)

High-level technologies produce advanced components, energy, and final goods.

---

## 6.1 Archivist Lab  
**Type:** Processor  
**Inputs:** Tech Fragments  
**Outputs:** Recovered Schematics  
**Description:** Scholars and engineers restoring pre-war knowledge.  
**File:** `industry/archivist_lab.lua`

---

## 6.2 Archaeotech Lab  
**Type:** Processor  
**Inputs:** Recovered Schematics  
**Outputs:** Archaeotech Components  
**Description:** Combines recovered knowledge with advanced machinery.  
**File:** `industry/archaeotech_lab.lua`

---

## 6.3 Solar Field / Wind Scavenger  
**Type:** Energy Extractor  
**Inputs:** None  
**Outputs:** Raw Energy  
**Description:** Restored renewable fields powering settlements.  
**File:** `industry/solar_field.lua`

---

## 6.4 Energy Stabiliser Plant  
**Type:** Processor  
**Inputs:** Raw Energy  
**Outputs:** Energy Cells  
**Description:** Stabilised power for advanced vehicles and town expansion.  
**File:** `industry/energy_stabiliser.lua`

---

## 6.5 Reconstruction Mill  
**Type:** Final Processor  
**Inputs:** Components + Construction Materials  
**Outputs:** Settlement Growth  
**Description:** Drives building upgrades and late-game city development.  
**File:** `industry/reconstruction_mill.lua`

---

# 7. Town Growth Integration

Towns require:

- Clean Water  
- Processed Food  
- Construction Materials  
- Energy Cells (late game)

Delivery of these drives:

- population growth  
- building upgrades  
- economy expansion  
- unlocking advanced vehicle demand  

Town definitions modified in:  
`config/town/*.lua`

---

# 8. Balancing Guidelines

## 8.1 Early Game
- small production (10–20 units)  
- inconsistent supply  
- high vehicle maintenance  

## 8.2 Mid Game
- stable production (20–40 units)  
- more efficient chains  
- water + food sustain towns  

## 8.3 Late Game
- high output (40–80 units)  
- multi-input industries  
- unlock Era IV vehicles  
- towns visibly expand  

---

# 9. Hazard Zone Modifiers (Optional)

Hazard zones increase:

- industry breakdown rate  
- maintenance costs  
- reduce production efficiency  

Script-driven via:  
`/res/scripts/hazard/*.lua`

---

# 10. Industry File Template (`.lua`)

A minimal template for new industries:

```lua
function data()
  return {
    type = "INDUSTRY",
    id = "scrapyard_processor",
    name = _("Scrapyard Processor"),
    description = _("Processes raw scrap into refined metal."),
    inputs = { "scrap_metal" },
    outputs = { "refined_scrap" },
    production = {
      initial = 20,
      rate = 40,
    },
    terrainAlignment = "SLOPE",
    cost = 200000,
  }
end
```

# 11. Asset Requirements (Per Industry)
* Each industry requires:
* .mdl building model
* collision mesh
* material folder
* effect definitions (smoke, sparks, steam)
* custom ground decal (recommended)
* UI icon
* balancing profile

# 12. Future Expansions
* Potential future additions:
* geothermal plants
* desert water siphons
* biodome farms
* rail scrapyards
* advanced excavation rigs
* caravan hubs


A high-level view of all material flows:

