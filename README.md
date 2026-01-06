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

Where optimization against SPARC and Cosmic Chronometer data yields:

* **** (Inverse-square-root geometric scaling)
* **** (Critical Shear Threshold)

---

## 📂 Repository Structure

The codebase is organized by astrophysical scale and testing regime.

### 1. The Universal Law (Theory of Everything)

*These notebooks combine all scales to test the unified model.*

* `VSC_Universal_Law_RealData.ipynb` - **The Core Proof.** Runs a global optimization to find the single  and  that fits M31, M33, and NGC galaxies simultaneously without "cheating" on gas mass.
* `VSC_Universal_LawAplliedToSaturn.ipynb` - Applies the Universal Law to the Solar System, proving the effect vanishes at high shear (Saturn deviation < 5 m/s).
* `VSC_Sanity_Check.ipynb` - A quick-check script comparing VSC residuals against standard CDM.

### 2. Galactic Dynamics (Dark Matter Alternative)

*Tests VSC against rotation curves of specific galaxies, ranging from baryon-dominated to dark-matter-dominated.*

* `VSC_M33_Check.ipynb` - Analysis of the Triangulum Galaxy (Dwarf/Gas-rich).
* `VSC_LocalShearTerm_Andromeda.ipynb` & `VSC_Local_Shear_Proof.ipynb` - Detailed breakdown of the M31 rotation curve.
* `VSC_NGC5055_Check.ipynb` & `VSC_NGC3198_Check.ipynb` - Validation against intermediate and "dark matter poster child" galaxies.
* `VSC_GalaxyRotationCurveAudit.ipynb` - Broader audit of rotation curve phenomenology.
* `VSC_TullyFisher_Proof.ipynb` - Derivation of the Tully-Fisher relation from viscous principles.

### 3. Cosmic Expansion & Hubble Tension

*Tests VSC against the expansion history of the universe (H(z)) and CMB data.*

* `VSC_HubbleTension_Solver.ipynb` - Demonstrates how viscosity naturally resolves the  tension between early and late universe measurements.
* `VSC_Expansion_RealData.ipynb` - Fits the model to Cosmic Chronometer and Supernova datasets.
* `VSCModel_Comparison_LCDM.ipynb` - Statistical comparison (χ2) between VSC and the Standard Model.
* `VSC_MCMC_Constraints_H0_Prior.ipynb` - Bayesian analysis and parameter constraints.

### 4. Early Universe & High Redshift

*Validates the model against Big Bang Nucleosynthesis (BBN) and JWST/JADES data.*

* `VSC_Nucleosynthesis_RealData.ipynb` - Proves that viscosity is negligible at , preserving standard element abundance predictions.
* `VSC_JADES_Solving_RealData.ipynb` - Analysis of high-redshift galaxy formation rates.
* `VSC_Accretion_LID-568_Proof.ipynb` - Super-Eddington accretion modeling.

### 5. Theoretical Foundations

* `VSC_Causality.ipynb` - Analysis of causal structure and light cones in a viscous medium.
* `VSC_PhiResistanceAndLeastAction.ipynb` - Derivation of the viscous term from the Principle of Least Action.
* `VSC_GW_Two-Fluid_RealData.ipynb` - Gravitational Wave propagation in a two-fluid viscous vacuum.

---

## 🚀 Getting Started

### Prerequisites

The simulations rely on standard scientific Python libraries.

```bash
pip install numpy matplotlib scipy pandas astropy emcee corner

```

### Running the Proofs

To reproduce the **Universal Law** finding:

1. Open `VSC_Universal_Law_RealData.ipynb`.
2. Run all cells.
3. The notebook will output the optimization results for  and generate the "Universal Relation" plot matching physical observations.

---

## 📖 Project Documentation

This repository provides the full theoretical and empirical framework for **Viscous Shear Cosmology (VSC)**, a unified model for galactic dynamics and cosmic expansion:

* **[📐 Mathematical Derivation](DERIVATION.md)**: A rigorous step-by-step derivation of the Universal Shear Law from first principles, treating the vacuum as a non-Newtonian fluid.
* **[📊 Results & Discussion](RESULTS_SUMMARY.md)**: Observational proof of the theory, including strict component fits for the SPARC database, the natural emergence of the Tully-Fisher relation ($\alpha \approx 3.35$), and Solar System orbital constraints.

---


## 📜 Citation

If you use this code or the VSC model in your research, please cite the repository using the provided `CITATION.cff` file or the following format:

> [Dustin Allen Rose]. (2025). *Viscous Shear Cosmology Simulation Library*. GitHub. [https://github.com/DRose1991/Viscous-Shear-Cosmology-Simulation]

## 📄 License

This project is licensed under the MIT License - see the `LICENSE` file for details.
