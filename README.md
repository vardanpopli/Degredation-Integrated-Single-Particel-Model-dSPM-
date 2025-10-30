# Integrating Degradation Mechanisms & Physics-Based Modeling for Predictive Battery Aging

This repository presents a physics-based Li-ion battery degradation model integrating electrochemical behaviour with oxygen-driven material degradation to predict long-term performance and lifetime across operating conditions.

---

## 📌 Research Objectives

- Build a degradation-integrated electrochemical model for Li-ion batteries
- Capture oxygen evolution, rock-salt formation, and interface shrinkage
- Accelerate battery lifetime prediction via physics-based simulation
- Reduce experimental cycles through pre-validation simulation analysis

---

## 🧠 Model Framework

### 🔬 Core Modeling Components
- **Electrochemical Model:** Single-Particle Model (SPM)
- **Degradation Physics:**
  - Oxygen evolution at cathode surface
  - Rock-salt shell growth (core-shell mechanism)
  - Interface passivation & capacity fade

### 🔗 Coupled Mechanisms
- Electrochemistry ↔ Oxygen diffusion ↔ Structural degradation

---

## 🎥 Simulation Visualisation

### 🔄 Positive Electrode Degradation Animation
> *Shrinking-core structure showing surface-initiated degradation driven by oxygen evolution*

<video src="Positive_Electrode_Degredation_GIF.mp4" width="400" controls></video>

---

## 📊 Key Results

### ✅ Capacity Fade at 0.5C
![Capacity Fade at 0.5C](Capacity%20Fade%20Figures/capacity_fade_0.5C.png)

### ✅ Capacity Fade at 0.1C
![Capacity Fade at 0.1C](Capacity%20Fade%20Figures/capacity_fade_01C.png)

---

## 🔎 Insights

- Higher **temperature** and **C-rate** accelerate oxygen release
- Faster oxygen-driven surface passivation → greater capacity loss
- Model trends match realistic voltage + capacity degradation behaviour

---

## ✅ Conclusion

> **Oxygen evolution drives particle surface degradation → rock-salt growth → shrinking active core → accelerated capacity fade.**

This model enables physics-driven lifetime prediction and supports simulation-first validation for battery ageing studies.

---

## 📁 Repository Structure

