# CONTRIBUTING.md  
Guidelines for contributing to **Wasteland Logistics**

Thank you for your interest in contributing!  
Wasteland Logistics is a community-friendly Transport Fever 2 overhaul mod built on open collaboration, original assets, and shared creativity.  
This document explains how to contribute, what standards to follow, and how we keep the project organised.

---

# 1. Code of Conduct

By participating in this project, you agree to:

- be respectful and constructive  
- collaborate openly  
- avoid harassment or hostile behaviour  
- keep discussions about ideas, not people  

Everyone is welcome — artists, scripters, modders, writers, and testers.

---

# 2. Project Structure

The project follows a clear directory and documentation structure:  
See `STRUCTURE.md` for the full layout.

Key directories:

- `/res/` — all Transport Fever 2 mod content  
- `/docs/` — documentation (CONCEPT, DESIGN, STRUCTURE, etc.)  
- `/res/models/` — 3D models  
- `/res/config/` — industries, cargo, vehicle metadata  
- `/res/scripts/` — Lua logic for hazards, economy, utilities  

---

# 3. Types of Contributions

You can contribute in many ways:

### ✔ 3D Models  
Vehicles, buildings, ruins, props, terrain detail assets.

### ✔ Textures & Materials  
PBR textures, albedo maps, terrain tiles, UI icons.

### ✔ Lua Scripting  
Industry logic, hazard systems, balancing tools.

### ✔ Documentation  
Improving guides, clarifying systems, expanding wikis.

### ✔ Playtesting & Balancing  
Helping refine pacing, costs, production chains, era progression.

### ✔ Audio & Music (Optional)  
Original soundscapes, ambient loops, radio snippets.

### ✔ Feedback & Suggestions  
Raising issues, proposing new ideas, analysing scope.

---

# 4. Getting Started

1. **Fork the repository**  
2. **Clone your fork locally**  
3. Create a new feature branch:  
git checkout -b feature/my-contribution
4. Make your changes  
5. Commit with clear messages  
6. Push your branch  
7. Open a Pull Request (PR) to `dev`

All pull requests must target the **`dev` branch**, not `main`.

---

# 5. Branching Strategy

The project uses a simple, stable workflow:
* main → stable releases
* dev → active development
* assets → raw 3D files, .blend, .psd
* scripts → experimental Lua features
* vehicles → new vehicle sets
* industry → new industry chains

Always branch from **`dev`**, never from `main`.

---

# 6. Standards & Quality Requirements

### 6.1 Naming Conventions  
Refer to `STRUCTURE.md`. Use lowercase, underscores, descriptive names.

Examples:
* bus_e1_dust_mule/
* ruin_highrise_A/
* archaeotech_lab.lua
* biofuel.dds


### 6.2 Model Requirements  
Refer to `ASSETS_GUIDE.md`.

- 3 LODs required  
- clean, efficient topology  
- correct scale  
- PBR materials  
- `.mdl` file tested in-game  

### 6.3 Texture Requirements  
- `.dds` preferred  
- use appropriate resolution  
- avoid texture stretching  
- maintain era-appropriate style  

### 6.4 Lua Standards  
- descriptive variable names  
- no infinite loops  
- do not override vanilla globals  
- follow TF2 modding conventions  
- keep logic lightweight for performance  

### 6.5 Balance & Tuning  
- avoid extreme production values  
- test industry chains end-to-end  
- keep vehicle stats internally consistent  

---

# 7. Pull Request Guidelines

Before submitting a PR:

- [ ] confirm your code builds/runs in-game  
- [ ] check your asset scale, LODs, materials  
- [ ] follow naming conventions  
- [ ] include screenshots if adding assets  
- [ ] update documentation if needed  
- [ ] ensure no copyrighted content is used  
- [ ] merge latest `dev` into your branch  

PRs should contain **one logical feature**.  
Avoid bundling multiple unrelated changes.

---

# 8. Testing Your Contribution

Always test your changes in Transport Fever 2:

- spawn the industry/vehicle/asset  
- check for errors in `stdout.txt`  
- verify texture paths  
- test collision meshes  
- confirm performance on large maps  
- try breakpoints (remove input supply, full queues, etc.)  

For Lua:
- add `print()` debugging  
- check for nil references  
- test on new ± late-game saves  

---

# 9. Submitting Issues

Issues should include:

- short title  
- clear description  
- reproduction steps  
- screenshots/logs if possible  
- suggested solution (optional)

Types of issues:
- bug reports  
- balancing problems  
- asset glitches  
- documentation errors  
- enhancement requests  

---

# 10. Prohibited Content

To protect the project legally and artistically:

- **no copyrighted, extracted, or ripped assets**  
  (Fallout, Mad Max, Metro, etc.)
- **no copyrighted sound effects or music**  
- **no direct IP references**  
- **no naming or design elements implying usage of protected franchises**  
- **no AI-generated copyrighted character likenesses**

All work must be original or CC0.

---

# 11. Licensing

All contributions are accepted under the project's license:

**MIT License**

This ensures:
- free reuse  
- free modification  
- free distribution  
- commercial and non-commercial freedom  

By submitting a PR, you agree that your contributions are licensed under MIT.

---

# 12. Communication

You may discuss development:

- in GitHub Issues  
- in PR comment threads  
- in the (future) project Discord  
- via structured feedback documents  

Constructive communication is valued.

---

# 13. Roadmap Awareness

Before creating large features, review:

- `CONCEPT.md`  
- `DESIGN.md`  
- `STRUCTURE.md`  

This ensures new contributions fit the overall vision.

---

# 14. Contributor Recognition

Contributors will be credited in:

- the mod’s GitHub repo  
- the Steam Workshop release page  
- the in-game credits asset (optional)  

Your art, scripting, and design work will be acknowledged.

---

# 15. Final Notes

Thank you for helping build Wasteland Logistics — an entire post-war economy, rebuilt from scrap, one contribution at a time.

Your creativity drives this world.
