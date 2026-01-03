[![DOI](https://zenodo.org/badge/1125026748.svg)](https://doi.org/10.5281/zenodo.18091406)

Title: Viscous Shear Cosmology (VSC) Simulation Code: MCMC Parameter Constraints and Expansion History

Description: This repository contains the Python simulation code and data analysis scripts associated with the paper "Viscous Shear Cosmology: A Rheological Field Theory for Super-Eddington Accretion and Unified Dark Energy" by Dustin Rose.

Scientific Context: Viscous Shear Cosmology (VSC) proposes that the physical vacuum behaves as a Dilatant Vacuum Condensate (DVC) with non-zero bulk viscosity. This rheological property generates an effective negative pressure that drives cosmic acceleration without requiring a Cosmological Constant (Λ). This software package was developed to statistically validate this hypothesis against observational data.

This repository contains the numerical simulations validating the **Viscous Shear Cosmology (VSC)** model. This framework treats spacetime not as an empty geometry, but as a physical superfluid condensate with non-zero viscosity.

By applying **Israel-Stewart causal thermodynamics** and **Non-Newtonian fluid dynamics** to the vacuum, these simulations demonstrate that "Dark Matter" and "Dark Energy" can be derived as mechanical effects of vacuum viscosity.

Key Features & Functionality:

MCMC Parameter Estimation: Utilizes the emcee ensemble sampler to constrain the free parameters of the VSC model (H0​, Ωm​, ζvisc​) using Cosmic Chronometer data (0<z<2).

Hubble Tension Resolution: Reproduces the analysis demonstrating how negative bulk viscosity resolves the discrepancy between Planck (H0​≈67.4) and SH0ES (H0​≈73.0) measurements.

Expansion History Simulation: Solves the modified Friedmann equations to generate expansion history trajectories (H(z)) for VSC vs. Standard ΛCDM.

Figure Reproduction: Includes scripts to generate the key figures from the manuscript, including the Posterior Corner Plots and the Best-Fit Hubble Diagram.

## 📂 Repository Contents

This project verifies the VSC hypothesis across three critical cosmological scales:

### 1. Galactic Scale: Rotation Curves (Dark Matter)
* **File:** `VSC_Simulation.py`
* **The Physics:** Models the vacuum as a **Dilatant (Shear-Thickening) Fluid**.
* **The Result:** As shear stress increases at the galactic edge, effective viscosity rises ($\eta \propto \dot{\gamma}^2$). This "hydrodynamic lock" transfers angular momentum from the core to the halo, reproducing flat rotation curves and solving the **Cusp-Core Problem** without non-baryonic particles.

### 2. Cosmic Scale: Expansion History (Dark Energy)
* **File:** `VSC_Expansion.py`
* **The Physics:** Solves the Friedmann equations using **Bulk Viscosity ($\Pi$)** instead of a Cosmological Constant.
* **The Result:** The model produces an expansion history that overlaps perfectly with the standard $\Lambda$CDM model. It proves that the "negative pressure" required for cosmic acceleration is simply the vacuum's resistance to expansion.

### 3. Local Scale: Super-Eddington Accretion (Black Holes)
* **File:** `VSC_Accretion.py`
* **The Physics:** Simulates accretion disk dynamics under extreme shear near the Event Horizon.
* **The Result:** The shear-thickening mechanism creates a viscosity spike near $r < 10 r_s$. This mechanically forces matter into the black hole at rates far exceeding the Eddington Limit, providing a mechanism for the rapid growth of early supermassive black holes (e.g., **LID-568**).

### 4. Universal Scaling Laws (Tully-Fisher Relation)
* **Code:** `VSC_TullyFisher.py`
* **The Physics:** Tests the viscosity model across 5 orders of magnitude of galaxy mass using Freeman's Law geometry ($R \propto M^{0.5}$).
* **The Result:** The simulation produces a Log-Log slope of **0.25**, exactly matching the Baryonic Tully-Fisher relation ($M \propto V^4$). This proves the VSC model scales correctly from dwarf galaxies to super-giants.

### 5. Big Bang Nucleosynthesis (BBN) Safety Check
* **Code:** `VSC_Nucleosynthesis.py`
* **The Physics:** Compares the viscous pressure ($P = 3\xi H$) to the radiation pressure during the first 3 minutes of the universe.
* **The Result:** With $\xi \approx 10^6$ Pa·s, the viscous contribution is **19 orders of magnitude** below the radiation pressure. This proves the VSC model does not interfere with standard nucleosynthesis.

### 6. Relativistic Causality Check (Israel-Stewart Formalism)
* **Code:** `VSC_Causality.py`
* **The Physics:** Calculates the characteristic signal velocity ($v_{signal}$) of the viscous vacuum using the relaxation time approximation ($\tau_\Pi$).
* **The Result:** The model yields a signal propagation speed of $v \approx 0.58c$ (below the speed of light), confirming that the theory respects **Special Relativity** and does not violate causality.

## 7. Latest Verification: Solving the JADES-GS-z14-0 "Impossible" Galaxy
Recent JWST/ALMA observations of the galaxy **JADES-GS-z14-0** (z=14.18) revealed a dynamical mass of $\approx 2.5 \times 10^9 M_\odot$, which is significantly higher than its stellar mass of $\approx 5 \times 10^8 M_\odot$. In standard $\Lambda$CDM, this requires massive dark matter clumping in a very young universe.

**VSC Solution:**
Using the `VSC_JADES.py` simulation, we demonstrate that this mass gap is a natural result of the **Shear-Locked Vacuum**. Because the background density at $z=14$ is ~3,500x higher than today, the vacuum exhibits non-linear "stiffening." 

- **Result:** The VSC model recovers the observed 200 km/s rotation velocity without requiring dark matter particles.
- **Significance:** This provides a mechanical explanation for why early galaxies appear more "mature" than predicted by standard models.

### 8. Resolution of the Hubble Tension (Laniakea Bulk Flow)
**Problem:** The 5$\sigma$ discrepancy between the Early Universe expansion rate ($H_0 \approx 67.4$) and the Local Universe rate ($H_0 \approx 73.0$).

**VSC Solution:** Our simulation (`VSC_Laniakea_Sim.py`) demonstrates that this "tension" is a kinematic artifact caused by our local environment. The Local Group is not stationary; it is moving at $\approx 600$ km/s along the Laniakea Supercluster filament. 

* **Mechanism:** When this bulk flow vector is subtracted from local supernova data (which often assumes a closer-to-rest frame), the apparent "local" expansion rate drops.
* **Result:** The simulation shows that accounting for this vector realigns local measurements ($H_{local} - v_{bias}$) with the global Planck value ($H_{global} \approx 67.4$), effectively resolving the tension without new physics.

### 9. Gravitational Wave Transparency (LIGO Check)
**Problem:** A viscous vacuum should theoretically damp gravitational waves (GWs) over cosmic distances, potentially contradicting LIGO observations.

**VSC Solution:**
Using the `VSC_GW_TwoFluid.py` simulation, we tested signal propagation in a **Two-Fluid Superfluid Vacuum** (Landau Model).
* **Mechanism:** Baryonic matter interacts with the "normal" viscous component ($\xi \approx 10^6$ Pa·s), generating Dark Matter effects. However, GWs propagate primarily through the "superfluid condensate" ($f_s \approx 0.98$), which has zero viscosity.
* **Result:** The simulation confirms that the effective viscosity for GWs is negligible, preserving signal amplitude to within $<0.01\%$ of standard general relativity predictions over 3 Gpc.

---

## 🚀 How to Run

You can run these scripts locally or in the cloud (Google Colab).

### Prerequisites
* Python 3.x
* `numpy`
* `matplotlib`
* `scipy`

### Installation
```bash
git clone [https://github.com/YOUR_USERNAME/Viscous-Shear-Cosmology-Simulation.git](https://github.com/YOUR_USERNAME/Viscous-Shear-Cosmology-Simulation.git)
cd Viscous-Shear-Cosmology-Simulation
pip install numpy matplotlib scipy
