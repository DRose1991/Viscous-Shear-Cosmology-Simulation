[![DOI](https://zenodo.org/badge/1125026748.svg)](https://doi.org/10.5281/zenodo.18091406)

# Viscous Shear Cosmology (VSC) Simulation

### A Rheological Approach to Galactic Dynamics

This repository contains the Python simulation code associated with the paper **"Viscous Shear Cosmology: A Rheological Field Theory for Super-Eddington Accretion and Unified Dark Energy."** (Available on Zenodo).

## 🔬 Project Overview
Standard cosmological models require Dark Matter to explain why the outer edges of galaxies spin as fast as their centers (the "Flat Rotation Curve" problem). This project tests an alternative hypothesis: **Viscous Shear Cosmology (VSC).**

The VSC model treats spacetime as a relativistic superfluid with **non-Newtonian (dilatant) viscosity**. This simulation demonstrates that when shear stress increases, the effective viscosity of the vacuum increases, creating a "hydrodynamic lock" that transfers angular momentum to the galaxy's edge.

## 📊 Key Results
Running this simulation reproduces two critical observational phenomena without invoking invisible particles:
1.  **Solid Body Rotation (Core):** Solves the "Cusp-Core Problem" by preventing the velocity singularity at the center ($r \to 0$).
2.  **Flat Rotation Curves (Halo):** Generates a high-velocity plateau at the galactic edge ($r > 20$ kpc) purely through viscous coupling.

## 🚀 How to Run
You can run this simulation in your browser via Google Colab or locally on your machine.

### Option 1: Google Colab (Recommended)
1. Open the file `VSC_Simulation.ipynb` (or copy the script).
2. Click "Run All".
3. View the generated Rotation Curve comparison plot.


### Option 2: Local Python
Requires `numpy` and `matplotlib`.
```bash
pip install numpy matplotlib
python simulation.py
