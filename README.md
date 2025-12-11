
# About

This repository presents a thermally-coupled, degradation-integrated Single-Particle Model (dSPM) designed to capture the structural evolution, gas generation, and performance degradation observed in high-energy NMC811 cathodes during CC–CV cycling.  
The model incorporates oxygen evolution, shrinking-core phase transition, passivation growth, and electrochemical degradation modes that collectively drive capacity fade and voltage decay.

The modeling framework and figures are based on the work presented at the **International Meeting of the Battery Research Society (IMBRS), Hilton Bangalore, Dec 06–09, 2025**.


## 2. Background

Ni-rich layered oxides such as **LiNi₀.₈Mn₀.₁Co₀.₁O₂ (NMC811)** enable high specific energy but are prone to degradation at elevated voltages and temperatures.  
Primary degradation processes include:

- Oxygen evolution and lattice oxygen loss  
- Rock-salt surface reconstruction  
- Loss of active material (LAM)  
- Loss of lithium inventory (LLI)  
- Parasitic reactions and passivation layer growth  
- Thermal instability and accelerated impedance rise  

These phenomena influence cyclability, voltage hysteresis, thermal behavior, and long-term performance.

The proposed **dSPM** augments the classical SPM with explicit degradation mechanisms and thermal coupling to predict these experimentally observed effects.


### 3.2 Degradation Sub-Models

#### A. Oxygen Evolution  

Oxygen release occurs when high SOC or high voltage destabilizes the layered lattice.  
Consequences include:

- Structural reconstruction  
- Gas generation  
- Increased internal resistance  
- Loss of transition-metal stability  

The model introduces an oxygen evolution rate term that directly impacts capacity and impedance.



#### B. Shrinking-Core Structural Reconstruction  

As cycling progresses, the particle transitions from:

- **Layered crystalline phase (intact)** →  
- **Passivated rock-salt shell (inactive)**

This mechanism explains:

- Loss of active material  
- Higher overpotential  
- Reduced lithium diffusivity  


## 4. Simulation and Performance Analysis

### 4.1 Stimulation Plots 
**Figure: Stimulation.png**

This figure presents the predicted dynamic voltage, concentration evolution, and internal degradation trends under CC–CV cycling.  
It validates that the dSPM reproduces time-domain responses similar to experimental behavior.


### 4.2 Capacity Fade Across Cycling
**Figure: Capacity Fade.png**

This figure shows voltage–capacity curves for:

- **0.5C at 25°C**  
- **1C at 25°C**  
- **1C at 45°C**

Key observations:

- High-temperature cycling triggers early rollover.  
- Higher C-rates reduce accessible capacity.  
- Predicted fade trends closely match expected degradation pathways.



### 4.3 Structural Transformation  
**Figure: Shrinking Core.png**

The surface-to-core transformation is modeled through a time-dependent reduction in active radius, explaining:

- Reduced diffusional volume  
- Increased mechanical stress  
- Decline in usable capacity  


### 4.4 Oxygen Evolution and Safety Considerations  
**Figure: Oxygen Evolution.png**

The oxygen evolution figure shows that oxygen release is strongly linked to:

- High SOC  
- Elevated temperature  
- Prolonged high-voltage operation  

This provides insight into thermal instability and cell safety concerns.



## 5. Significance

The dSPM framework provides a computationally tractable yet physically rich method to:

- Predict degradation trends under CC–CV cycling  
- Quantify phase transitions and oxygen evolution  
- Represent shrinking-core behavior in Ni-rich cathodes  
- Study the impact of temperature on long-term cyclability  
- Capture voltage fade and impedance growth  
- Support BMS-oriented health prediction models  

By integrating degradation directly into particle-scale transport equations, the model advances predictive understanding of high-energy cathode aging.


