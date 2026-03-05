# Dispersion

Simulation code for modeling biofilm cell ejection driven by self-generated hydrogel.

This repository contains the numerical model used in the study:

**Self-generated hydrogel locally ejects cells from a biofilm**,  
Chou et al. (2026)

---

## System requirements

Tested with:

- Python 3.11  
- Windows 11 

Optional hardware:

- NVIDIA GPU with CUDA support (for GPU acceleration using CuPy)

---

## Dependencies

### Python packages

- numpy  
- matplotlib  
- cupy-cuda12x  

`cupy-cuda12x` enables GPU acceleration but is optional.  
If it is not available, the simulation automatically falls back to a CPU implementation using NumPy.

### External dependency

FFmpeg is required to generate the simulation movies.

Download and install FFmpeg from:  
https://ffmpeg.org/

After installation, make sure `ffmpeg` is available in your system PATH.

---

## Installation

Clone the repository and install the Python dependencies:

git clone https://github.com/dsb-lab/dispersion  
cd dispersion  
pip install -r requirements.txt

Installation typically takes less than **5 minutes** on a standard desktop computer.

---

## Running the simulation

Open the notebook:

Dispersion.ipynb

Run all cells sequentially to reproduce the simulations.

---

## Expected output

The simulation produces:

- movies of the biofilm dynamics  
- RGB visualizations of cell populations  
- figure panels saved as PDF  

Output files are saved in the `movies/` directory created during execution.

---

## Typical runtime

Runtime depends on the hardware configuration.

- With GPU acceleration (CuPy + CUDA), simulations typically take about **10–20 minutes**.  
- On CPU, simulations may take **several hours up to one or more days**, depending on system performance and simulation parameters.

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
---

## License

This project is licensed under the **GNU General Public License v3.0 (GPL-3.0)**.



