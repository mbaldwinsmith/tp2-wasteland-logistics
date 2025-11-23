# ECONOMY_DIAGRAM.md  
### Complete Economy Flowcharts for **Wasteland Logistics**

This document provides a unified, clear, and professionally structured overview of the entire Wasteland Logistics economy, including early-, mid-, and late-game industry chains, town-growth dependencies, and cross-era relationships.

---

# 1. High-Level Economy Flow

```
[ EARLY ] →→→ SURVIVAL ECONOMY  
[ MID ]   →→→ RECONSTRUCTION ECONOMY  
[ LATE ]  →→→ REVIVAL / NEW WORLD ECONOMY
```

```
 SCRAP METAL ──▶ REFINED SCRAP ──▶ COMPONENTS ──▶ CONSTRUCTION MATERIALS ──▶ CITY GROWTH
        │
        ▼
  TECH FRAGMENTS ──▶ SCHEMATICS ──▶ ARCHAEOTECH COMPONENTS ──▶ ERA IV VEHICLES

 DIRTY WATER ──▶ CLEAN WATER ──▶ TOWNS

 RAW ORGANICS ──▶ FOOD / BIO-MASH ──▶ BIOFUEL ──▶ VEHICLES

 RAW ENERGY ──▶ ENERGY CELLS ──▶ TOWN GROWTH / ADVANCED INDUSTRIES
```

---

# 2. Early Game — *Scavenger Years*

Survival-level logistics with low output and unstable production.

```
 RUINS / VEHICLE GRAVES ───▶ SCRAP METAL

 DIRTY WELL ───────────────▶ DIRTY WATER

 RAD-FARMS / FUNGUS PITS ─▶ RAW ORGANICS

 ARCHAEO-DEPOT ───────────▶ TECH FRAGMENTS
```

---

# 3. Mid Game — *Reconstruction Dawn*

Cities stabilise; purification, refining, and consistent supply chains emerge.

### 3.1 Scrap → Construction

```
SCRAP METAL
    │
    ▼
[ SCRAPYARD PROCESSOR ]
    │
    ▼
REFINED SCRAP
    │
    ▼
[ ASSEMBLY YARD ]
    ├────────▶ COMPONENTS
    └────────▶ CONSTRUCTION MATERIALS
```

### 3.2 Water Chain

```
DIRTY WATER
    │
    ▼
[ PURIFICATION PLANT ]
    │
    ▼
CLEAN WATER ───▶ TOWNS
```

### 3.3 Food & Fuel

```
RAW ORGANICS
    ├─────▶ [ FOOD STILL ] ───▶ PROCESSED FOOD ─▶ TOWNS
    └─────▶ [ BIOFUEL REFINERY ] ─▶ BIOFUEL ─────▶ VEHICLES
```

### 3.4 Tech Recovery

```
TECH FRAGMENTS ───▶ [ ARCHIVIST LAB ] ───▶ SCHEMATICS
```

---

# 4. Late Game — *Revival Age → New World Era*

Advanced industry, high-tech components, and multi-input production.

### 4.1 Archaeotech Chain

```
TECH FRAGMENTS
    │
    ▼
[ ARCHIVIST LAB ]
    │
    ▼
SCHEMATICS
    │
    ▼
[ ARCHAEOTECH LAB ]
    │
    ▼
ARCHAEOTECH COMPONENTS ───▶ ERA IV VEHICLES
```

### 4.2 Energy Chain

```
SOLAR / WIND
    │
    ▼
RAW ENERGY
    │
    ▼
[ ENERGY STABILISER PLANT ]
    │
    ▼
ENERGY CELLS ──▶ TOWN GROWTH  
               └▶ HIGH-TECH INDUSTRY
```

### 4.3 Settlement Reconstruction

```
COMPONENTS + CONSTRUCTION MATERIALS
                  │
                  ▼
         [ RECONSTRUCTION MILL ]
                  │
                  ▼
             CITY UPGRADE
```

---

# 5. Town Growth Inputs

```
EARLY  — Food + Clean Water  
MID    — Construction Materials  
LATE   — Energy Cells  
```

---

# 6. Full Master Diagram (Compact Form)

```
                     EARLY GAME
 ┌─────────────────────────────────────────────────────────┐
 │ Ruins → Scrap Metal                                     │
 │ Wells → Dirty Water                                     │
 │ Rad-Farms → Raw Organics                                │
 │ Archaeotech Depot → Tech Fragments                      │
 └─────────────────────────────────────────────────────────┘

                     MID GAME
 ┌─────────────────────────────────────────────────────────┐
 │ Scrap → Processor → Refined Scrap → Assembly →          │
 │        ├→ Components                                    │
 │        └→ Construction Materials                        │
 │                                                         │
 │ Dirty Water → Purification → Clean Water → Towns       │
 │ Raw Organics → Food/Biofuel                            │
 │ Tech Fragments → Archivist Lab → Schematics            │
 └─────────────────────────────────────────────────────────┘

                    LATE GAME
 ┌─────────────────────────────────────────────────────────┐
 │ Schematics → Archaeotech Lab → Archaeotech Components →│
 │                                   Advanced Vehicles     │
 │                                                         │
 │ Solar/Wind → Raw Energy → Stabiliser → Energy Cells →  │
 │                                   Town Growth           │
 │                                                         │
 │ Components + Construction Materials → Recon Mill →      │
 │                                   City Upgrade          │
 └─────────────────────────────────────────────────────────┘
```

---

# 7. Dependency Summary

### Vehicles depend on:
- Biofuel (Era II–III)  
- Electricity (Era II–IV)  
- Archaeotech Components (Era IV)  

### Towns depend on:
- Clean Water  
- Processed Food  
- Construction Materials  
- Energy Cells  

### Late-game industries depend on:
- Schematics  
- Energy Cells  

---

# 8. Visual Key

```
[ INDUSTRY ]   = Processing building  
CAPS           = Cargo  
▶              = Flow  
├/└            = Branching chain  
```

---

# 9. License

This document is released under the MIT License as part of Wasteland Logistics.
