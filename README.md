# About

This repository presents an extended physics-based Single-Particle Model (SPM) integrated with degradation mechanisms to predict phase transitions, gas evolution, and performance decay in Ni-rich NMC811 electrodes under various operating conditions.  
The model is thermally coupled and validated against CC–CV cycling behavior to capture structural breakdown, oxygen release, and capacity fade phenomena.

The work is based on the study presented at the **International Meeting of the Battery Research Society (IMBRS)**, The Hilton, Bangalore, Dec 06–09, 2025.  
All poster figures and plots are available in the `/Figures` directory.


## 1. Project Overview

Ni-rich layered oxides such as **NMC811** exhibit high specific capacity but suffer from accelerated degradation when cycled at high voltage.  
Key degradation pathways include:

- **Oxygen evolution** from the cathode lattice  
- **Rock-salt layer formation** and structural reconstruction  
- **Loss of Active Material (LAM)**  
- **Loss of Lithium Inventory (LLI)**  
- **Passivation layer growth**  
- **Impedance rise and thermal instability**

To address this, a **Thermally-Coupled Degradation-Integrated Single-Particle Model (CC-CV-T-dSPM)** is developed.  
The model combines:

- Classical SPM for electrode diffusion
- Temperature coupling during CC–CV cycling
- Explicit degradation sub-models representing oxygen evolution, shrinking-core transformation, and passivation growth
- Voltage and capacity fade prediction across cycling and temperature windows


The `/Figures` folder contains all plots extracted from the research poster, including degradation pathways, shrinking-core diagrams, oxygen evolution analysis, and capacity fade curves.

---

## 3. Modelling Framework

### 3.1 Classical SPM Foundation
The base SPM describes Li-ion diffusion within a representative spherical cathode particle:

\[
\frac{\partial c_s}{\partial t} = \frac{D_s}{r^2}\frac{\partial}{\partial r}\left( r^2 \frac{\partial c_s}{\partial r} \right)
\]

Boundary condition at particle surface:

\[
-D_s \left.\frac{\partial c_s}{\partial r}\right|_{r=R} = j
\]

where \( j \) is the interfacial flux governed by Butler–Volmer kinetics.

---

### 3.2 Degradation Sub-models

#### A. **Oxygen Evolution Model**
Based on Figure *Oxygen Evolution.png*, oxygen release is triggered under high voltage and high SOC conditions, resulting in:

- Lattice oxygen loss  
- Transition metal migration  
- Gas generation  
- Thermal acceleration  

The model includes an oxygen evolution rate term modifying the cathode activity and effective capacity.

---

#### B. **Shrinking-Core Structural Reconstruction**
Figure *Shrinking Core.png* shows the conversion of the crystalline layered structure into a rock-salt or disordered core upon cycling.  
The degradation is expressed as a shrinking active radius \( R_a(t) \):

\[
R_a(t) = R_0 (1 - k_{sc} \, t)
\]

This directly reduces LAM and increases impedance.

---

#### C. **Passivation Layer Growth**
Based on *Degredations.png*, a surface passivation film forms due to electrolyte reactions and oxygen-triggered transition metal dissolution.

Impedance grows following:

\[
R_{\text{film}}(t) = R_0 + k_f t^\alpha
\]

---

### 3.3 Thermal Coupling (CC–CV–T-dSPM)
Temperature influences:

- Diffusivity  
- Kinetic rate constants  
- Degradation rates (oxygen evolution, passivation growth)  
- Voltage hysteresis  

The model incorporates Joule heating and entropic heat:

\[
C_p \frac{dT}{dt} = I^2 R + I T \frac{\partial U}{\partial T}
\]

---

## 4. Simulation Conditions and Case Studies

The model is evaluated at:

- **0.5C and 25°C**  
- **1C and 25°C**  
- **1C and 45°C**

These cases correspond to the performance curves displayed in *Capacity Fade.png* and the cycling analyses in the poster (page 1 of PDF):contentReference[oaicite:1]{index=1}.

Key observations:

- Higher temperature accelerates oxygen evolution.  
- Increased C-rate causes deeper structural degradation.  
- Combined thermal + electrochemical stress leads to early capacity rollover and severe voltage drop.

---

## 5. Results Summary

### 5.1 Voltage–Capacity Characteristics
(Figure: *Capacity Fade.png*)

- Early cycles show stable behavior at moderate C-rates.  
- At elevated temperature (45°C), the voltage drops faster with increasing cycle number.  
- dSPM captures this rollover behavior consistent with experimental literature.

### 5.2 Oxygen Evolution and Gas Generation
(Figure: *Oxygen Evolution.png*)

- Oxygen evolution increases sharply above a critical SOC.  
- The resulting lattice instability triggers degradation cascades.

### 5.3 Shrinking-Core Transformation
(Figure: *Shrinking Core.png*)

- Active radius decreases with cycling.  
- Model predicts transition from crystalline phase to rock-salt surface.  

### 5.4 Combined Degradation Modes
(Figure: *Degredations.png*)

- LAM, LLI, passivation growth, and thermal instability emerge simultaneously at high voltage.  

## 6. Scientific Significance

The model provides a framework to:

- Predict voltage fade trajectories  
- Quantify active-material loss and impedance rise  
- Capture phase transitions and structural collapse  
- Model gas evolution and thermal runaway precursors  
- Integrate degradation physics into SPM-based control and BMS algorithms  

This contributes toward accurate state-of-health (SOH) and state-of-safety (SOS) estimation for next-generation NMC-based Lithium-ion batteries.


## 7. Author Contributions

- Developed CC–CV–T-dSPM modelling framework.  
- Implemented degradation sub-models: oxygen evolution, shrinking-core transformation, and passivation growth.  
- Performed multi-temperature, multi-C-rate simulations.  
- Generated all analytical plots used in the poster.  
- Contributed to model validation and interpretation of degradation physics.  


## 8. References

1. Ghosh, A., et al. *J. Electrochem. Soc.*, 2021, 168, 020509.  
2. Chen, C., et al. *J. Electrochem. Soc.*, 2020, 167, 080534.  
3. Guo, M., et al. *J. Electrochem. Soc.*, 2011, 158, A122.  
4. Zhuo, M., et al. *J. Power Sources*, 2023, 556, 232461.  
5. O’Regan, K., et al. *Electrochim. Acta*, 2022, 425, 140700.


## 9. Acknowledgements

The work was carried out at the **Fluids & Interfaces for Next-generation Devices (FIND) Laboratory**,  
Department of Chemical Engineering & Technology, IIT BHU.




