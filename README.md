# Dispersion

Simulation code for modeling biofilm cell ejection driven by self-generated hydrogel.

This repository contains the numerical model used in the study:

**_Self-generated hydrogel locally ejects cells from a biofilm_**,  
Chou et al. (2026)

The code simulates the coupled dynamics of:

- motile cells  
- non-motile cells  
- hydrogel  
- nutrient field  
- pressure-driven flow  

and reproduces the mechanical ejection (dispersion) of cells from a growing biofilm.

Run `Dispersion.ipynb` to reproduce the simulations.

---

## Model overview

The simulation describes a growing biofilm as a compressible active mixture where:

- Cells grow depending on nutrient availability  
- Motile cells produce hydrogel  
- Hydrogel and growth generate pressure  
- Pressure drives flows that advect cells and matrix  
- These flows can eject cells from the colony  

The model solves coupled PDEs for:

| Field | Meaning |
|------|--------|
| ρₘ | motile cell density |
| ρₙ | non-motile cell density |
| h | γ-PGA hydrogel density |
| c | nutrient concentration |
| p | pressure field |

<br>

<img width="324" height="256" alt="Fig5v3 (1)" src="https://github.com/user-attachments/assets/00385e5f-06a6-407a-93a3-e0969cd65c4f" />
