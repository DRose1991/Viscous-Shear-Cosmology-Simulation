[![DOI](https://zenodo.org/badge/1125026748.svg)](https://doi.org/10.5281/zenodo.18091406)

# Viscous Shear Cosmology (VSC) Simulation Library

### A Scale-Invariant Solution to the Dark Matter Problem via Vacuum Viscosity

## 🌌 Overview

This repository contains the source code, simulation engines, and validation suites for the **Viscous Shear Cosmology (VSC)** model.

VSC hypothesizes that the vacuum of space behaves as a **non-Newtonian, shear-thinning fluid**. Instead of requiring dark matter particles or modifying the fundamental laws of gravity (MOND), VSC proposes that the vacuum "stiffens" in regions of low shear (galactic outskirts) and "thins" in regions of high shear (solar systems).

This library provides the rigorous mathematical proofs and data audits demonstrating that a single universal viscosity law can unify:

1. **Galactic Rotation Curves** (without rescaling gas mass).
2. **Cosmic Expansion History** (resolving the Hubble Tension).
3. **Solar System Dynamics** (passing the Saturn/Cassini constraint).

---

## 📐 The Universal Law of VSC

The core finding of this repository is the derivation of the **Universal Shear Equation**. Through global optimization across gas-rich dwarfs and stellar giants, we identified specific universal constants that satisfy observational data across all scales:

<div align="center">
  <img src="https://latex.codecogs.com/svg.image?\pagecolor{white}v_{obs}=v_{newt}\sqrt{1+\left(\frac{\Sigma_{shear}}{S_{crit}}\right)^{-n}}" title="Universal VSC Equation" />
</div>

Where optimization against SPARC and Cosmic Chronometer data yields:

* **$n = 0.467$** (Inverse-square-root geometric scaling)
* **$S_{crit} = 100.0 \text{ km s}^{-1} \text{kpc}^{-1}$** (Critical Shear Threshold)

---

## 📖 Project Documentation

This repository provides the full theoretical and empirical framework for **Viscous Shear Cosmology (VSC)**:

* **[📐 Mathematical Derivation](DERIVATION.md)**: A rigorous step-by-step derivation of the Universal Shear Law from first principles, treating the vacuum as a non-Newtonian fluid.
* **[📊 Results & Discussion](RESULTS_SUMMARY.md)**: Observational proof of the theory, including strict component fits for the SPARC database, the natural emergence of the Tully-Fisher relation ($\alpha \approx 3.35$), and Solar System orbital constraints.



---

## 📂 Repository Structure

The codebase is organized by astrophysical scale and testing regime.

### 1. The Universal Law (Theory of Everything)
* `VSC_Universal_Law_RealData.ipynb` - **The Core Proof.** Global optimization for $n$ and $S_{crit}$.
* `VSC_Universal_LawAplliedToSaturn.ipynb` - Proof of local Newtonian preservation ($\Delta v < 5$ m/s).
* `VSC_Sanity_Check.ipynb` - Residual comparison against $\Lambda$CDM.

### 2. Galactic Dynamics (Dark Matter Alternative)
* `VSC_M33_Check.ipynb` - Analysis of the Triangulum Galaxy (Gas-rich dwarf).
* `VSC_LocalShearTerm_Andromeda.ipynb` - Detailed breakdown of the M31 rotation curve.
* `VSC_TullyFisher_Proof.ipynb` - Derivation of the Tully-Fisher relation from viscous principles.

### 3. Cosmic Expansion & Hubble Tension
* `VSC_HubbleTension_Solver.ipynb` - Resolving $H_0$ tension via vacuum viscosity.
* `VSC_Expansion_RealData.ipynb` - Fits to Cosmic Chronometer and Supernova datasets.

### 4. Early Universe & High Redshift
* `VSC_Nucleosynthesis_RealData.ipynb` - Validation against Big Bang Nucleosynthesis (BBN).
* `VSC_JADES_Solving_RealData.ipynb` - Analysis of high-redshift galaxy formation.

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install numpy matplotlib scipy pandas astropy emcee corner
