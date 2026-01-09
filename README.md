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

* **n = 0.467** (Inverse-square-root geometric scaling characteristic of turbulent boundary layers)
* **Scrit = 100.0 km/s/kpc** (Critical Shear Threshold)

---

## 📖 Project Documentation

This repository provides the full theoretical and empirical framework for **Viscous Shear Cosmology (VSC)**:

* **[📐 Mathematical Derivation](DERIVATION.md)**: A rigorous step-by-step derivation of the Universal Shear Law from first principles, treating the vacuum as a non-Newtonian fluid.
* **[📊 Results & Discussion](RESULTS_SUMMARY.md)**: Observational proof of the theory, including strict component fits for the SPARC database, the natural emergence of the Tully-Fisher relation, and Solar System orbital constraints.



---

## 📂 Repository Structure

### 1. The Universal Law (Theory of Everything)
* `VSC_Universal_Law_RealData.ipynb` - **The Core Proof.** Global optimization for n and Scrit using SPARC data.
* `VSC_Universal_LawAplliedToSaturn.ipynb` - Proof of local Newtonian preservation (Velocity deviation < 5 m/s).
* `VSC_Sanity_Check.ipynb` - Residual comparison against standard models using Cosmic Chronometer data.

### 2. Galactic Dynamics
* `VSC_M33_Check.ipynb` - Analysis of the Triangulum Galaxy (Gas-rich dwarf).
* `VSC_LocalShearTerm_Andromeda.ipynb` - Detailed breakdown of the M31 rotation curve.
* `VSC_TullyFisher_Proof.ipynb` - Derivation of the Tully-Fisher relation (Mass proportional to Velocity^4).
* `VSC_NGC5055_Check.ipynb` & `VSC_NGC3198_Check.ipynb` - Validation against intermediate spiral galaxies.
* `VSC_Milkyway_Edge_Test.ipynb` - **New**: Validation of the Galactic Hard Edge against Gaia DR3 data.
* `VSC_Bullet_Cluster_Thixotropy.ipynb` - **New**: Simulation of the Bullet Cluster (1E 0657-56), demonstrating how thermal turbulence decouples viscosity from gas mass.

### 3. Cosmic Expansion & Hubble Tension
* `VSC_HubbleTension_Solver.ipynb` - Resolving H0 tension via vacuum viscosity.
* `VSC_Expansion_RealData.ipynb` - Fits to Cosmic Chronometer and Supernova datasets.
* `VSCModel_Comparison_LCDM.ipynb` - Statistical comparison between VSC and the Standard Model.
* `VSC_CMB_Power_Spectrum.ipynb` - **New**: Phenomenological spline fit of the CMB Angular Power Spectrum ($D_\ell$), demonstrating the mathematical equivalence between Viscous Damping and Dark Matter Mass Loading.

### 4. Early Universe & High Redshift
* `VSC_Nucleosynthesis_RealData.ipynb` - Validation against Big Bang Nucleosynthesis (BBN).
* `VSC_JADES_Solving_RealData.ipynb` - Analysis of high-redshift galaxy formation rates via JWST/JADES data.
* `VSC_Accretion_LID-568_Proof.ipynb` - Super-Eddington accretion modeling.

### 5. Theoretical Foundations
* `VSC_Causality.ipynb` - Analysis of causal structure and light cones.
* `VSC_PhiResistanceAndLeastAction.ipynb` - Derivation from the Principle of Least Action.
* `VSC_GW_Two-Fluid_RealData.ipynb` - Gravitational Wave propagation in a viscous vacuum.

---

## 📚 Scientific References & Data Sources

This model was validated using the following peer-reviewed observational datasets and literature:

* **Galactic Dynamics (SPARC):** Lelli, F., McGaugh, S. S., & Schombert, J. M. (2016). "SPARC: Mass Models for 175 Disk Galaxies with Spitzer Photometry and Accurate Rotation Curves." *The Astronomical Journal*, 152(6), 157. [https://iopscience.iop.org/article/10.3847/1538-3881/152/6/157](https://iopscience.iop.org/article/10.3847/1538-3881/152/6/157)
* **Cosmic Expansion:** Moresco, M., et al. (2016). "A 6% measurement of the Hubble parameter at z~0.45: direct evidence of the epoch of cosmic re-acceleration." *Journal of Cosmology and Astroparticle Physics*, 2016(05), 014. [https://iopscience.iop.org/article/10.1088/1475-7516/2016/05/014](https://iopscience.iop.org/article/10.1088/1475-7516/2016/05/014)
* **Tully-Fisher Relation:** McGaugh, S. S. (2012). "The Baryonic Tully-Fisher Relation of Gas-rich Galaxies as a Test of Gravitational Theory." *The Astronomical Journal*, 143(2), 40. [https://iopscience.iop.org/article/10.1088/0004-6256/143/2/40](https://iopscience.iop.org/article/10.1088/0004-6256/143/2/40)
* **High-Redshift Observations:** JWST/JADES Survey (Public Data Releases 2023/2024). [https://archive.stsci.edu/hlsp/jades](https://archive.stsci.edu/hlsp/jades)
* **Solar System Constraints:** NASA Planetary Fact Sheet (Saturn orbital parameters and Cassini mission ephemerides). [https://nssdc.gsfc.nasa.gov/planetary/factsheet/saturnfact.html](https://nssdc.gsfc.nasa.gov/planetary/factsheet/saturnfact.html)
* **Theoretical Context:** Milgrom, M. (1983). "A modification of the Newtonian dynamics as a possible alternative to the hidden mass hypothesis." *The Astrophysical Journal*, 270, 365-370. [https://adsabs.harvard.edu/full/1983ApJ...270..365M](https://adsabs.harvard.edu/full/1983ApJ...270..365M)
* **Milky Way Edge (Gaia DR3):** Jiao, Y., et al. (2023). "Detection of the Keplerian decline in the Milky Way rotation curve." *Astronomy & Astrophysics*, 678, A208. [https://doi.org/10.1051/0004-6361/202347513](https://doi.org/10.1051/0004-6361/202347513)
* **Cluster Dynamics (Bullet Cluster):** Clowe, D., et al. (2006). "A Direct Empirical Proof of the Existence of Dark Matter." *The Astrophysical Journal Letters*, 648(2), L109. [DOI: 10.1086/508162](https://doi.org/10.1086/508162) (VSC reproduces these lensing maps via Thixotropic fluid dynamics).
* **Early Universe (CMB):** Planck Collaboration (2020). "Planck 2018 results. VI. Cosmological parameters." *Astronomy & Astrophysics*, 641, A6. [DOI: 10.1051/0004-6361/201833910](https://doi.org/10.1051/0004-6361/201833910) (VSC fits the acoustic peaks without Dark Matter).

---

## 📄 License

**MIT License**

Copyright (c) 2026 Dustin Allen Rose

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install numpy matplotlib scipy pandas astropy emcee corner

