[![DOI](https://zenodo.org/badge/1125026748.svg)](https://doi.org/10.5281/zenodo.18091406)

# Viscous Shear Cosmology (VSC) Simulations

### A Rheological Field Theory for Unified Dark Sector Physics

This repository contains the numerical simulations validating the **Viscous Shear Cosmology (VSC)** model. This framework treats spacetime not as an empty geometry, but as a physical superfluid condensate with non-zero viscosity.

By applying **Israel-Stewart causal thermodynamics** and **Non-Newtonian fluid dynamics** to the vacuum, these simulations demonstrate that "Dark Matter" and "Dark Energy" can be derived as mechanical effects of vacuum viscosity.

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
