# Characterization of Deep-Level Traps in the C-Doped Buffer in GaN HEMTs with DLTS Techniques

This repository contains the data, analysis scripts, and documentation for the characterization of trap states in p-GaN/AlGaN/GaN High Electron Mobility Transistors (HEMTs). The research was conducted during an internship project at the **Department of Electronic Systems Engineering (DESE), Indian Institute of Science (IISc), Bengaluru**[cite: 1].


---

## Project Overview

Gallium Nitride (GaN) HEMTs are critical for high-frequency, high-power, and high-efficiency analog/RF applications[cite: 1]. However, deep-level traps and defect states heavily impact device reliability, threshold voltage stability, and leakage current behavior[cite: 1]. 

This project focuses on identifying thermally activated trap states using **Current-Voltage-Temperature (IVT)** analysis and **Current-based Deep Level Transient Spectroscopy (I-DLTS)**[cite: 1]. Rate Window (RW) analysis and Arrhenius plots were utilized to extract key trap parameters, specifically activation energy ($E_a$) and capture cross-section ($\sigma_n$)[cite: 1].

---

## Experimental Setup & Lab Equipment

All physical measurements and experimental characterizations were performed at the **SoC / Device Characterization Lab, DESE, IISc Bangalore** using a highly controlled cryogenic environment[cite: 1].

| Equipment / System | Description |
| :--- | :--- |
| **Semetrol Cryogenic Characterization System** | Used for precise temperature-dependent electrical and transient current acquisition[cite: 1]. |
| **Lake Shore Model 335 Temperature Controller** | Maintained exact thermal stabilization and feedback control across a wide temperature range[cite: 1]. |
| **Vacuum Pump System** | Generated a low-pressure vacuum environment to eliminate moisture, surface contamination, and ambient electrical noise[cite: 1]. |
| **Microprobe Station** | Positioned precision microprobe needles on the source, gate, and drain pads under microscope assistance[cite: 1]. |

---

## Key Results & Extracted Parameters

Through Rate Window sampling and Arrhenius plotting, two dominant deep-level trap states were successfully isolated and identified within the carbon-doped buffer layer/heterostructure interface[cite: 1]:

| Trap Label | Peak Temperature (K) | Activation Energy ($E_a$) | Capture Cross-Section ($\sigma_n$) | Possible Physical Origin |
| :---: | :---: | :---: | :---: | :--- |
| **T1** | 485 K[cite: 1] | $0.397 \pm 0.016 \text{ eV}$[cite: 1] | $4\times 10^{-19} \pm 1.6 \text{ cm}^2$[cite: 1] | Interface states / structural defect-assisted carrier trapping[cite: 1]. |
| **T2** | 440 K[cite: 1] | $0.520 \pm 0.058 \text{ eV}$[cite: 1] | $6.0\times 10^{-18} \pm 5.5 \text{ cm}^2$[cite: 1] | Deep carbon-related acceptor states in the GaN buffer layer[cite: 1]. |

### Summary of Conduction Mechanisms
* **Low-Field / Forward Bias:** Dominantly controlled by Thermionic Emission (TE) over the Schottky barrier[cite: 1].
* **High-Field / Reverse Bias:** Field-assisted leakage current driven by Poole-Frenkel (PF) emission and trap-assisted tunneling[cite: 1].

---

## Repository Structure

```text
├── docs/                 # Full Project Report copy and presentation materials
├── figures/              
├── literature-reviews/
├── results/               
├── LICENSE               # MIT License
└── README.md             # Project Documentation
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgements
We express our deepest gratitude to the Department of Electronic Systems Engineering (DESE), IISc Bengaluru for providing access to advanced experimental characterization infrastructure and laboratory support staff[cite: 1].
