# VEHICLES.md  
Vehicle Catalogue & Specifications for **Wasteland Logistics**

This document provides concept descriptions, naming conventions, and technical guidelines for all vehicles across the four technological eras of Wasteland Logistics.

---

# 1. Overview

Wasteland Logistics includes **40–60 vehicles** across:

- Road (buses, trucks)
- Rail (steam, diesel, electric, hybrid, lev-rail)
- Trams
- Aircraft (dirigibles, aerostats, VTOLs)
- Ships (barges, ferries)
- Monorail systems (Era IV)

Vehicles are designed to reflect the progression from desperate scavenging to advanced reconstruction-era engineering.

---

# 2. Vehicle Design Principles

### Aesthetic Principles
- rust-punk  
- welded plates  
- exposed components  
- patched metal and mismatched colours  
- scavenged plastics, cloth, neon  
- asymmetry acceptable in early eras  

### Gameplay Principles
- visible improvement per era  
- slow → reliable → efficient → futuristic  
- cargo capacities expand over time  
- maintenance decreases, speed increases  
- energy diversity: diesel, biofuel, electric, hybrid, nuclear  

### Technical Principles
- minimum **3 LODs**  
- shared materials where possible  
- adherence to TF2 scale  
- config files must use correct transport type definitions  

---

# 3. Vehicle Naming Convention
<category><era><name>

Examples:
bus_e1_dust_mule
train_e2_reclaimer_diesel
air_e3_aerostat_skywhale
rail_e4_levrail_strider


---

# 4. Vehicle Eras

---

# ERA I — SCAVENGER YEARS (2120–2170)

### Summary
Improvised, unstable, slow. Built from scrap heaps and reverse-engineered pre-war parts. High maintenance, low speed, high charm.

### Visual Style
- bolted metal plates  
- exposed pistons  
- faded paint, graffiti  
- mixed tyre/rim types  
- torn fabric canopies  

---

## ROAD VEHICLES (Era I)

### **Dust Mule Bus**
- old-school bus chassis + welded sheet metal  
- top speed: ~25–35 km/h  
- capacity: 8–12 passengers  
- runs on dirty biofuel  
- loud, smoky exhaust  

### **Rusthound Truck**
- scavenged pickup with extended scrap-bed  
- cargo: 4–8 units  
- terrible braking  
- iconic wasteland look  

---

## TRAINS (Era I)

### **Patchwork 0-4-0 Steamer**
- handmade boiler, rust patches  
- low torque  
- slow acceleration  
- used mainly for short salvage runs  

### **Makeshift Freight Wagon**
- open scrap frame  
- minimal suspension  
- ideal for scrap metal transport  

---

## AIR (Era I)

### **Wind-Skiff Dirigible**
- tiny balloon with fabric patches  
- very slow, very cheap  
- cargo: 2 units  
- used for scouting and isolated settlement supply  

---

## TRAMS (Era I)

### **Settlement Tram Mk.I**
- ancient tram skeleton reactivated  
- unstable wiring  
- slow but atmospheric  

---

# ERA II — RECONSTRUCTION DAWN (2170–2210)

### Summary
Communities stabilise; reliable engines return. Pre-war vehicles are restored. Biofuel and early electrics appear.

### Visual Style
- cleaner welds  
- more uniform colours  
- recovering industrial standards  
- visible solar panels on some vehicles  

---

## ROAD VEHICLES (Era II)

### **Twin-Turbine Freight Truck**
- hybrid biofuel turbofans assisting diesel engine  
- cargo: 10–16  
- decent acceleration  

### **Settlement Shuttle Bus**
- restored pre-war transit system  
- top speed: 50–60 km/h  
- capacity: ~20 passengers  

---

## TRAINS (Era II)

### **Reclaimer Class Diesel**
- restored long-body diesel engine  
- reliable and strong  
- forms backbone of mid-game rail networks  

### **Refit Boxcar / Tanker / Flatcar**
- improved capacities  
- cleaner industrial design  

---

## AIR (Era II)

### **Courier Blimp**
- fast, stable balloon  
- cargo: 6–10  
- medium-range inter-settlement delivery  

---

## TRAMS (Era II)

### **Solar Tram Lite**
- first-generation solar-electric tram  
- modest speed  
- elegant reclaimed look  

---

# ERA III — REVIVAL AGE (2210–2250)

### Summary
Energy tech accelerates; hybrid systems dominate. Aerostats and lightweight composites appear. Vehicles look cleaner, more aerodynamic.

### Visual Style
- green-energy panels  
- smooth lines  
- lightweight alloys  
- neon accents  

---

## ROAD VEHICLES (Era III)

### **Glider-Caravan Bus**
- ultra-light chassis  
- biofuel-electric hybrid  
- graceful curves  
- capacity: 28–32 passengers  

### **Wind-Harvest Truck**
- integrates small turbine systems  
- excellent range  
- mid-high cargo  

---

## TRAINS (Era III)

### **Sunline EMU**
- solar-boosted electric multiple unit  
- fast acceleration  
- reliable and clean  

### **BioHybrid Freight Engine**
- runs partly on biofuel, partly electric grid  
- strong mid-game hauler  

---

## AIR (Era III)

### **Airstream Aerostat**
- large, long-range cargo balloon  
- capacity: 12–18  
- efficient, stable  
- iconic silhouette  

### **Aeropack VTOL Hauler**
- repurposed military VTOL  
- medium cargo capacity  
- expensive but versatile  

---

## TRAMS (Era III)

### **Revival Linear Tram**
- lightweight, high-speed bogies  
- neon-lit front panel  
- sleek and modern  

---

# ERA IV — NEW WORLD ERA (2250–2300)

### Summary
Archaeotech breakthroughs enable advanced vehicles: lev-rail hybrids, nuclear monorails, VTOL megatransports, hyper-efficient freight haulers.

### Visual Style
- sleek panels  
- glowing accents  
- polished composites  
- clean geometry  
- hints of recovered high science  

---

## ROAD VEHICLES (Era IV)

### **Nanocell Courier**
- micro-reactor + electric drive  
- extremely fast  
- low cargo, perfect for high-value goods  

### **Reconstruction Megatruck**
- modular cargo compartments  
- capacity: 30–40 units  
- state-of-the-art stability  

---

## TRAINS (Era IV)

### **LevRail Strider**
- hybrid levitation + standard track compatibility  
- extremely high speed  
- visually iconic  

### **Horizon Nuclear Monorail**
- powered by stabilized micro-reactor  
- glides silently  
- best for long passenger routes  

### **MagHaul Freight Engine**
- heavy lev-rail cargo carrier  
- massive hauling capacity  

---

## AIR (Era IV)

### **Skybridge VTOL Lifter**
- colossal multi-rotor VTOL  
- heavy cargo  
- used for remote settlements  

### **AeroDome Cruiser**
- ultra-long-range airship  
- cargo: 24–30  
- elegant future aesthetic  

---

## SHIPS (Era IV)

### **Reclamation Hydrofoil**
- hydrofoil with advanced stabilisers  
- very high speed  
- used for coastal megacities  

---

# 5. Technical Specs (Per Vehicle Class)

### Road
- scale: standard TF2  
- materials: rust → clean → composite per era  
- physics: set realistic torque & braking  

### Rail
- animations: wheels, bogies, water/steam for early eras  
- effects: smoke, sparks, energy glow for Era IV  
- LODs critical for long consists  

### Air
- buoyancy config for airships  
- VTOL hover effect simulated via thrust scripting  
- rotors: animated with blurred prop textures  

### Ships
- water wake effects  
- proper collision masks  
- low poly hull bottoms for performance  

---

# 6. Balancing Guidelines

### Era Progression
- speed increases steadily  
- cost increases per technological level  
- maintenance decreases from Era I → III, increases slightly in Era IV (complexity)  
- capacity scales with technology  

### Performance Targets
- Era I: slow and fragile  
- Era II: reliable backbone  
- Era III: efficient and clean  
- Era IV: premium, futuristic, expensive  

---

# 7. Asset Checklist (Per Vehicle)

Every new vehicle must include:

- `.mdl` file  
- LOD0, LOD1, LOD2 meshes  
- materials folder  
- icons (UI)  
- smoke/light/fx definitions  
- sound assignments  
- seat/cargo node definitions  

---

# 8. Future Expansion Ideas

- faction livery variants  
- weather-specific modifications (sand filters, cold plating)  
- special mission vehicles (research drones, expedition crawlers)  
- experimental pre-era prototypes  

---

# 9. Licensing
All vehicles created for Wasteland Logistics are original works and released under the MIT License.



# 3. Vehicle Naming Convention

