# Literature Review: Fundamentals, Heterostructure Physics, and Defect Mechanistics in GaN HEMTs

This document presents a comprehensive review of the historical development, structural physics, gate junction configurations, and defect dynamics associated with Gallium Nitride (GaN) High Electron Mobility Transistors (HEMTs). [cite_start]It acts as the theoretical framework necessary to analyze the temperature-dependent electrical characteristics and deep-level trap dynamics explored in this work[cite: 476].

---

## 2.1 Fundamentals and Evolution of GaN HEMTs

### 2.1.1 Wide Bandgap Properties of Gallium Nitride
Gallium Nitride ($\text{GaN}$) is a prominent wide-bandgap semiconductor material belonging to the III-V family, exhibiting a direct energy bandgap of approximately 3.4 eV at room temperature[cite: 67, 93, 94, 205]. [cite_start]When contrasted with conventional semiconductor substrates like Silicon ($\text{Si}$) and Gallium Arsenide ($\text{GaAs}$), $\text{GaN}$ demonstrates distinct electro-physical advantages[cite: 68, 94, 206]:

* **Critical Breakdown Field:** A significantly high critical electric field allows devices to handle large voltage operations without experiencing premature breakdown[cite: 68, 98, 206, 208].
* **Saturation Velocity:** High electron saturation velocity supports ultra-fast carrier transport dynamics, making it optimal for high-speed operation in microwave and Radio Frequency ($\text{RF}$) systems[cite: 68, 99, 206, 209].
* **Thermal Stability:** Excellent thermal conductivity and chemical stability ensure low degradation rates when operating within high-power or high-temperature environments[cite: 68, 97, 206, 207, 210].
* **Commercial Landscapes:** These parameters make $\text{GaN}$-based components highly valuable across modern high-efficiency power management blocks, electric vehicles, radar systems, satellite transmitters, and 5G telecommunication infrastructure[cite: 69, 72, 102, 116, 211].

### 2.1.2 Polarization Mismatch and 2DEG Channel Formation
The exceptional current handling capacity of $\text{GaN}$ HEMTs relies on the formation of a high-density, high-mobility **Two-Dimensional Electron Gas (2DEG)** confined at the heterointerface[cite: 71, 100, 110, 213]. [cite_start]This electron channel accumulates naturally due to strong spontaneous and piezoelectric polarization fields present within III-Nitride heterostructures[cite: 100, 110, 214]. 

Unlike conventional $\text{Si}$ MOSFET channels, this inversion/accumulation layer is achieved without requiring intentional chemical impurity channel doping[cite: 101, 215]. [cite_start]This absence of dopants significantly isolates carriers from ionized impurity scattering mechanisms, yielding exceptional carrier mobility profiles[cite: 101, 215, 522]. [cite_start]Ibbetson et al. demonstrated that surface donor states acting in conjunction with polarization discontinuities dictate the electrostatic charge balance at the heterointerface[cite: 217, 524]:

$$\sigma_{\text{surface}} + \sigma_{\text{AlGaN}} - qn_s = 0$$ [cite: 220, 527]

Where:
* $\sigma_{\text{surface}}$ represents the surface donor state charge density[cite: 222, 528].
* $\sigma_{\text{AlGaN}}$ represents the net polarization-induced charge accumulation[cite: 223, 529].
* $q$ is the elementary charge of an electron[cite: 47, 224, 530].
* $n_s$ represents the resultant 2DEG sheet electron density[cite: 225, 531].

The physical sheet density is directly controlled by engineering parameters including the Aluminum ($\text{Al}$) mole fraction and structural thickness of the $\text{AlGaN}$ barrier layer[cite: 226, 532, 533, 534]. [cite_start]Higher $\text{Al}$ concentrations scale up the internal polarization fields, increasing carrier confinement within the triangular potential well formed at the interface[cite: 227, 520, 539, 546].

### 2.1.3 Development of AlGaN/GaN Heterostructure Technology
Early hardware implementations of $\text{GaN}$ HEMTs prioritized Silicon Carbide ($\text{SiC}$) substrates because their close lattice matching and high thermal conductivity optimized heat dissipation during intensive $\text{RF}$ stress sequences[cite: 252]. [cite_start]However, the modern commercial market heavily favors **GaN-on-Silicon (GaN-on-Si)** systems[cite: 106, 253]. [cite_start]Silicon base substrates offer massive cost reductions, scalable wafer diameters, and seamless compatibility with established mass-production CMOS manufacturing lines[cite: 253].

### 2.1.4 Normally-ON vs. Normally-OFF Operational Architectures
Standard planar $\text{AlGaN/GaN}$ architectures are inherently depletion-mode (normally-ON) structures because the deep polarization quantum well remains completely filled with free electrons even at zero gate-to-source bias[cite: 284]. [cite_start]While highly effective for specific $\text{RF}$ amplification blocks, normally-ON devices present severe safety and power-sequencing challenges when integrated into commercial power electronics and general analog layouts[cite: 73, 285]. 

To achieve enhancement-mode (normally-OFF) operation—where the channel remains non-conductive until a positive threshold voltage is actively applied—multiple structural approaches have emerged, including recessed-gate configurations, plasma-assisted fluorine ion implantation, cascode layouts, and **p-GaN gate technology**[cite: 286, 287]. [cite_start]Among these, p-GaN gates are highly valued for providing operational safety and broad gate-drive circuit compatibility[cite: 73, 103, 288, 290].

### 2.1.5 Dominant Reliability Bottlenecks
Despite their high-efficiency metrics, $\text{GaN}$ hardware systems remain susceptible to unique reliability anomalies induced by deep-level trap dynamics[cite: 74, 104, 152, 327]. [cite_start]Chief among these is **current collapse**, an operational state characterized by a severe, transient reduction in maximum drain current capabilities following exposure to high off-state drain voltage stress[cite: 123, 329]. [cite_start]Bisi et al. confirmed that these structural instabilities map directly to active charge trapping centers distributed across unpassivated surface states or structural buffer interfaces[cite: 136, 330]. [cite_start]These trapping instabilities systematically lead to[cite: 77, 123, 139, 155, 167, 331]:
* Dynamic ON-resistance ($R_{\text{ON,dyn}}$) degradation[cite: 123, 155, 334].
* Uncontrolled threshold voltage ($V_{th}$) shifts and gate hysteresis loops[cite: 77, 139, 155, 167, 332, 336].
* Transconductance ($g_m$) suppression and accelerated $\text{RF}$ power gain compression[cite: 77, 123, 139, 155, 167, 335, 337].

---

## 2.2 p-GaN Gate HEMT Structure and Device Physics

### 2.2.1 Epitaxial Architecture and Stack Profile
The specific enhancement-mode p-GaN architecture configuration evaluated throughout this investigation consists of a meticulously engineered epitaxial stack built upon a commercial Silicon platform[cite: 106, 378, 479]:

* **Gate Cap Layer:** A 100 nm p-type GaN layer utilized to fully deplete the underlying 2DEG channel at zero gate bias to enforce normally-off operation[cite: 371, 379].
* **Barrier Layer:** A thin 15 nm $\text{Al}_{0.21}\text{Ga}_{0.79}\text{N}$ barrier layer that introduces the polarization mismatch necessary to sustain high sheet carrier density under forward bias[cite: 374, 381].
* **Channel Layer:** A 300 nm unintentionally doped ($\text{UID}$) $\text{GaN}$ channel region optimized for low impurity scattering and high electron mobility[cite: 375, 438, 442].
* **Isolation Buffer:** A 300 to 500 nm carbon-doped ($\text{C-doped}$) $\text{GaN}$ buffer layer designed to maximize vertical isolation and suppress substrate leakage current[cite: 107, 376, 381].
* **Transition Zone:** A graded Aluminum Gallium Nitride ($\text{Al}_x\text{Ga}_{1-x}\text{N}$) transition layer grown atop a standard Silicon substrate to manage thermal expansion mismatches and minimize structural cracking[cite: 377, 378, 496, 497].

### 2.2.2 Threshold Voltage Engineering Dynamics
Establishing a stable, positive threshold voltage requires precise stabilization of the structural bands under the gate area[cite: 401, 402]. [cite_start]The exact $V_{th}$ alignment is a function of the $\text{p-GaN}$ layer thickness, the concentration of active Magnesium acceptors, the baseline thickness of the $\text{AlGaN}$ barrier, and fixed interface charge states[cite: 402, 403, 405, 406, 407, 408]. [cite_start]While increasing the acceptor level shifts $V_{th}$ positively, excessive doping profiles introduce a high density of local defect states that can compromise gate control and trigger high leakage profiles under forward bias[cite: 409, 410, 411, 458].

### 2.2.3 Schottky Metal / p-GaN Control Junction Electrostatics
The electrical control interface is established by depositing a Schottky metal contact terminal directly over the $\text{p-GaN}$ cap layer[cite: 413]. [cite_start]At standard operational temperatures and moderate bias sweeps, the baseline carrier transport across this boundary behaves as an ideal Schottky junction governed by Thermionic Emission ($\text{TE}$) theory[cite: 416]:

$$I = AA^*T^2 \exp\left(-\frac{q\Phi_B}{kT}\right)$$ [cite: 419, 762]

Where $A$ evaluates the true layout contact area [cite: 421][cite_start], $A^*$ is the effective Richardson constant for Gallium Nitride [cite: 422][cite_start], and $\Phi_B$ isolates the underlying Schottky barrier height[cite: 423]. [cite_start]Deviations from this baseline relationship track the activation of localized, defect-assisted leakage paths[cite: 424].

### 2.2.4 The Two-Junction Capacitor Model
To interpret the non-linear capacitance-voltage ($C-V$) trends observed during testing, the p-GaN gate configuration is treated as an equivalent **two-junction capacitor network**[cite: 425, 426]. [cite_start]This model splits the gate stack into two discrete capacitive impedances operating in a series configuration[cite: 426]:
1. The metal/p-GaN Schottky depletion capacitance zone ($C_{\text{Sch}}$)[cite: 427, 435].
2. The fundamental heterojunction dielectric barrier capacitance zone ($C_{\text{AlGaN}}$)[cite: 427, 436].

$$\frac{1}{C_{\text{total}}} = \frac{1}{C_{\text{Sch}}} + \frac{1}{C_{\text{AlGaN}}}$$ [cite: 429]

This structural coupling explains the sharp step transitions observed in $C-V$ sweeps as the internal bias shifts the depletion boundaries from the metal boundary down to the 2DEG plane[cite: 430].

### 2.2.5 Magnesium Acceptor Activation and Incomplete Ionization Mechanics
Magnesium ($\text{Mg}$) serves as the standard dopant used to induce p-type conductivity within the GaN crystal lattice[cite: 454]. [cite_start]However, $\text{Mg}$ activates deeply within the bandgap, resulting in incomplete ionization at room temperature[cite: 455]. [cite_start]Consequently, only a small fraction of the total incorporated Magnesium atoms activate into free holes[cite: 456]. [cite_start]This behavior introduces a strong temperature dependence into the gate depletion depth and transient threshold voltage tracking profiles[cite: 457].

### 2.2.6 Forward Gate Leakage Pathways
When subjected to positive forward gate stress, current leakage across the gate structure scales non-linearly due to the activation of multiple concurrent transport phenomena[cite: 461, 462]. [cite_start]These include direct Thermionic Emission ($\text{TE}$) over the metal interface, Trap-Assisted Tunneling ($\text{TAT}$) across thin localized barriers, and field-enhanced Poole-Frenkel ($\text{PF}$) emission through defect states in the barrier layer[cite: 464, 466]. [cite_start]Deep-level traps present near the gate region dynamically capture and emit carriers, driving threshold voltage instability and analog linearity degradation[cite: 468].

---

## 2.3 Deep-Level Traps and Defect Physics in GaN Devices

### 2.3.1 Microstructural Origins of Trapping Sites
The structural defects present within the device layer stem from the lattice mismatch and thermal expansion variance existing between the $\text{GaN}$ epitaxy and the host Silicon substrate[cite: 131, 586]. [cite_start]These stresses generate macroscopic threading dislocations, point vacancies, interface irregularities, and process-induced damage across critical junction planes[cite: 75, 130, 135, 576, 578, 580, 581, 582, 584]. [cite_start]These states introduce localized energy levels deep within the wider bandgap, capturing or emitting free channel carriers dynamically depending on the local electric field, applied electrical stress, and ambient temperature[cite: 78, 133, 587, 588].

### 2.3.2 Point Defects, Dislocations, and Impurity Centers
While incorporating Carbon atoms ($\text{C}$) into the underlying buffer layer is necessary to achieve high breakdown vertical isolation, it inevitably introduces deep acceptor-like states that capture free channel carriers under stress[cite: 107, 147, 148, 589, 590]. [cite_start]These carbon-related defects, interface states, and threading dislocations are prominent drivers of transient trapping phenomena and dynamic device degradation[cite: 149, 469, 590, 1351].

### 2.3.3 Conduction Models and Field-Enhanced Release Mechanisms
Trapped carriers escape back into the active bands via thermal or electrical field excitation[cite: 595, 838]. [cite_start]The electron emission rate ($e_n$) of an electron escaping from a thermally activated deep defect back into the active conduction band follows a fundamental relation[cite: 597]:

$$e_n = \sigma_n v_{\text{th}} N_c \exp\left(-\frac{E_a}{kT}\right)$$ [cite: 599, 992]

Where:
* $e_n$ is the electron emission rate[cite: 601, 994].
* $\sigma_n$ is the trap capture cross-section[cite: 602, 603, 995, 996].
* $v_{\text{th}}$ represents the thermal carrier velocity[cite: 604, 997].
* $N_c$ is the effective conduction band density of states[cite: 605, 998].
* $E_a$ represents the activation energy (trap depth) relative to the band edge[cite: 606, 607, 999].

When the HEMT operates under high-field stress, multiple field-assisted conduction mechanisms coexist alongside standard drift-diffusion transport[cite: 667, 668]. [cite_start]Under the influence of a strong electric field, the **Poole-Frenkel Effect** lowers the Coulombic potential barrier surrounding a charged trap center, allowing trapped carriers to escape more easily into the conduction band[cite: 838, 840, 841]. [cite_start]This field-assisted emission increases the leakage current density ($J$) as a linear function of the square root of the applied electric field ($\sqrt{E}$)[cite: 840, 841, 850, 851, 861, 862]:

$$\ln\left(\frac{J}{E}\right) \propto \sqrt{E}$$ [cite: 862, 1377, 1378, 1379]

In highly defective regions, alternative mechanisms such as Space-Charge-Limited Conduction ($\text{SCLC}$) occur when the injected carrier concentration exceeds the thermally generated carrier concentration[cite: 703]. [cite_start]The SCLC current density follows the relation $J = \left(\frac{9}{8}\right)\epsilon\mu\left(\frac{V^2}{L^3}\right)$[cite: 704, 705].

---

## 2.4 Current Collapse and Transient Phenomena

### 2.4.1 Drain Lag and Gate Lag Mechanisms
The time-resolved response of a $\text{GaN}$ HEMT operating under switching profiles is constrained by dynamic lag phenomena[cite: 149]:
* **Gate Lag:** A transient delay in drain current recovery observed when the gate terminal is switched rapidly, typically linked to active surface state trapping configurations[cite: 136, 241].
* **Drain Lag:** A current suppression effect that occurs when the drain terminal transitions from high-voltage stress back to a low-bias state, driven by slow carrier emission from deep buffer states[cite: 136, 241].

### 2.4.2 Dynamic ON-Resistance Degradation
During high-voltage off-state stress, hot electrons escape the 2DEG channel and become trapped within active defect sites in the buffer layer or gate edges[cite: 123, 1558]. [cite_start]When the device is switched back to the conductive on-state, these trapped negative charges remain localized due to their slow, temperature-dependent emission time constants[cite: 1088, 1566]. [cite_start]The localized negative charge acts as an internal depletion region that reduces the local carrier concentration in the 2DEG, causing a severe spike in the dynamic ON-resistance ($R_{\text{ON,dyn}}$) and causing current collapse phenomena[cite: 123, 1557, 1559].

---

## 2.5 Deep-Level Characterization Frameworks

### 2.5.1 Capacitance-Based DLTS (C-DLTS)
Capacitance-Based Deep Level Transient Spectroscopy ($\text{C-DLTS}$) monitors changes in the high-frequency junction capacitance ($C$) as trapped carriers undergo thermal emission following a voltage filling pulse[cite: 251, 141]. [cite_start]While highly effective for characterizing wide depletion regions in traditional diodes, standard $\text{C-DLTS}$ faces practical limitations when applied to thin HEMT channels due to high series resistance, small absolute active areas, and structural limitations in tracking high-frequency signals across thin heterojunction barriers[cite: 256].

### 2.5.2 Current-Based DLTS (I-DLTS)
Current-Based Deep Level Transient Spectroscopy ($\text{I-DLTS}$) overcomes these operational constraints by directly monitoring time-resolved current transients ($I(t)$) during the carrier emission phase[cite: 81, 1069]. This current-transient tracking approach offers multiple advantages for HEMT characterization:
* Exceptional sensitivity within ultra-thin channel structures[cite: 1069].
* Direct compatibility with planar multi-terminal layout geometries[cite: 1070].
* Accurate tracking of field-dependent trapping dynamics across active buffer layers and gate interfaces[cite: 1090].

### 2.5.3 The Rate Window Sampling Protocol
To isolate individual trap signatures from complex, overlapping current decay signals, the transient output is processed using the **Rate Window (RW) method**[cite: 1093]. [cite_start]The current transient curve is sampled at two discrete time instants ($t_1$ and $t_2$) following the removal of the filling pulse[cite: 1095]. [cite_start]The differential output defines the filtered DLTS signal[cite: 1096]:

$$S(T) = I(t_1) - I(t_2)$$ [cite: 1099]

Plotting $S(T)$ across a controlled temperature sweep generates a clean spectral peak[cite: 1105, 1395]. [cite_start]This maximum emerges at the exact temperature where the shifting internal emission rate ($e_n$) of the defect aligns with the configured rate window[cite: 1105, 1396]:

$$e_n = \frac{\ln(t_2/t_1)}{t_2 - t_1}$$ [cite: 1104]

By systematically adjusting the chosen sampling windows ($t_1, t_2$), the spectral peak shifts across the temperature axis, tracking the thermal activation of the defect[cite: 1109, 1512].

### 2.5.4 Arrhenius Regression Extraction Theory
Because carrier emission from deep levels is a thermally activated process, the relationship between the peak emission temperature ($T$) and its corresponding emission rate ($e_n$) can be mapped via an Arrhenius regression model[cite: 1137, 1138]. [cite_start]Accounting for the temperature dependence of the thermal velocity ($v_{\text{th}} \propto T^{1/2}$) and the effective density of states ($N_c \propto T^{3/2}$), the baseline expression is rewritten as[cite: 1139, 1140, 1141, 1142]:

$$\ln\left(\frac{e_n}{T^2}\right) = \ln(C) - \frac{E_a}{kT}$$ [cite: 1144, 1146]

Plotting $\ln(e_n/T^2)$ against $1/kT$ yields a straight line[cite: 1147, 1150]. [cite_start]The slope of this fit isolates the activation energy ($E_a$), confirming the physical depth of the defect center below the band edge[cite: 1153, 1155, 1156]. [cite_start]Concurrently, the intercept extracts the capture cross-section ($\sigma_n$), establishing a reliable method to identify and fingerprint distinct deep-level trap signatures within the device architecture[cite: 1154].
