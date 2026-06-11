# Experimental Results and Discussion

This file details the experimental results obtained from the electrical and transient characterization of the investigated p-GaN/AlGaN/GaN HEMT structure[cite: 1]. The measurements encompass Current-Voltage (I-V), Current-Voltage-Temperature (IVT), and Current-based Deep Level Transient Spectroscopy (I-DLTS) performed under strictly controlled thermal and biasing ranges[cite: 1].

---

## 5.1 I-V Characteristics

The forward bias I-V characteristics exhibit a nonlinear, exponential current trend typical of Schottky barrier-controlled transport mechanisms[cite: 1]. At low forward voltages, the current is constrained by limited carrier injection across the potential barrier[cite: 1]. As the bias increases, the current increases significantly due to enhanced thermionic carrier transport through the heterostructure[cite: 1]. 

Under reverse bias, leakage current remains low at low electric fields but increases significantly at elevated reverse voltages[cite: 1]. This behavior points to field-assisted conduction pathways operating in the high-field domain, including Poole-Frenkel emission, trap-assisted tunneling, and thermionic field emission[cite: 1].

![Figure 5.1: Forward Bias I-V and C-V Characteristics](figures/2d_plots/figure_5_1.png)
> *Figure 5.1: Measured forward bias I-V characteristics and C-V sweep profiles of the investigated p-GaN HEMT structure[cite: 1].*

---

## 5.2 Temperature-Dependent IVT Analysis

Temperature-dependent IVT sweeps were evaluated across a controlled thermal environment (spanning 223 K to 473 K in 50 K steps) using the Semetrol cryogenic system[cite: 1]. Increasing the operating temperature shifts the forward current upward, confirming the thermally activated nature of the carrier transport over the Schottky barrier[cite: 1]. 

In the reverse bias regime, leakage current increases tracking the temperature growth[cite: 1]. This temperature dependence highlights the contribution of trap-assisted thermal emission mechanisms linked to active deep-level states[cite: 1]. The IVT data isolates three distinct transport regions:
* **Low-field region:** Dominated by low-level background leakage pathways[cite: 1].
* **Intermediate-field region:** Dominated by ideal thermionic emission over the barrier[cite: 1].
* **High-field region:** Governed by field-enhanced, trap-assisted carrier emission processes[cite: 1].

![Figure 5.2: Temperature-Dependent I-DLTS Spectrum Peak](figures/2d_plots/figure_5_2.png)
> *Figure 5.2: Temperature-dependent I-DLTS spectrum showing a prominent trap-assisted transient response peak situated around 420 K to 440 K[cite: 1].*

![Figure 5.3: Distributed Trap I-DLTS Spectrum](figures/2d_plots/figure_5_3.png)
> *Figure 5.3: I-DLTS spectrum captured under alternative transient timing conditions illustrating a distributed defect signature[cite: 1].*

---

## 5.3 Leakage Current Analysis

The reverse leakage current variation scales nonlinearly with both temperature and the applied electric field[cite: 1]. To verify the dominance of field-assisted thermal emission, the Poole-Frenkel (PF) emission model was applied[cite: 1]:

$$J = CE \exp\left[ -\frac{q(\Phi_t - \beta\sqrt{E})}{kT} \right]$$

A linear relationship observed between $\ln(J/E)$ and $\sqrt{E}$ confirms the presence of Poole-Frenkel conduction within the high-field domain[cite: 1]. These results strongly support the presence of deep acceptor-like states introduced within the carbon-doped GaN buffer layer, which dynamically modulate vertical isolation under high bias[cite: 1].

---

## 5.4 I-DLTS Spectra Analysis

Current-based Deep Level Transient Spectroscopy isolates specific defect centers by evaluating time-resolved transient current decay curves during carrier emission[cite: 1]. The extracted I-DLTS spectra display distinct temperature-activated peaks that materialize when the defect's characteristic emission rate matches the configured Rate Window (RW) sampling state[cite: 1].

The broad geometry of the identified peaks indicates that instead of an isolated single-energy point defect, the heterostructure possesses distributed trap states[cite: 1]. This broadening is characteristic of GaN material systems where defect non-uniformity, threading dislocations, and buffer-layer carbon impurities overlap[cite: 1].

![Figure 5.4: 3D Visualization of Transient Current Response](figures/3d_visualizations/figure_5_4.png)
> *Figure 5.4: Three-dimensional map showing current transient amplitude tracking simultaneously against the temperature and time domain axes, highlighting peak activation near 420 K[cite: 1].*

---

## 5.5 & 5.6 Trap Property Extraction

Arrhenius analysis was completed by plotting the shifting coordinates of the transient peak maxima as a function of the emission rate and temperature[cite: 1]:

$$\ln\left(\frac{e_n}{T^2}\right) = \ln(C) - \frac{E_a}{kT}$$

The slope of the linear fit yields the trap activation energy ($E_a$), while the intercept determines the capture cross-section ($\sigma_n$)[cite: 1]. 

![Figure 5.5: Arrhenius Plot for Trap T1](figures/2d_plots/figure_5_5.png)
> *Figure 5.5: Arrhenius regression plot extracting a moderately deep trap activation energy for the T1 center[cite: 1].*

![Figure 5.6: Arrhenius Plot for Trap T2](figures/2d_plots/figure_5_6.png)
> *Figure 5.6: Arrhenius regression plot extracting a deeper trap state configuration corresponding to the T2 center[cite: 1].*

### Extracted Deep-Level Trap Parameters

The final physical parameters computed from the Arrhenius experimental sequences are summarized in the table below:

| Trap Label | Peak Temperature (K) | Activation Energy ($E_a$) | Capture Cross-Section ($\sigma_n$) | Probable Physical Context |
| :---: | :---: | :---: | :---: | :--- |
| **T1** | 465 K[cite: 1] | $0.397 \pm 0.016 \text{ eV}$[cite: 1] | $4.46\times10^{-19} \pm 1.6 \text{ cm}^2$[cite: 1] | Heterostructure interface states / defect-assisted structural trapping[cite: 1]. |
| **T2** | 440 K[cite: 1] | $0.520 \pm 0.058 \text{ eV}$[cite: 1] | $6.06\times10^{-18} \pm 5.5 \text{ cm}^2$[cite: 1] | Deep carbon-related acceptor complexes localized inside the GaN buffer[cite: 1]. |

---

## 5.7 Rate Window Analysis Results

Altering the rate window parameters causes a systematic shift in the temperature at which the maximum DLTS signal occurs[cite: 1]. Smaller rate windows emphasize slower emission dynamics, moving the peak positions toward lower temperature bands[cite: 1]. Conversely, larger rate windows evaluate fast carrier dynamics, forcing the transient peaks toward higher temperature regimes[cite: 1].

![Figure 5.7: Rate Window Peak Shifting Behavior](figures/2d_plots/figure_5_7.png)
> *Figure 5.7: Multi-rate-window overlay of the DLTS spectra illustrating systematic peak temperature translation with varying observation timing windows[cite: 1].*

---

## 5.8 Impact on Analog Performance

The dynamic capture and release of carriers within these isolated deep levels change the sheet charge density of the Two-Dimensional Electron Gas (2DEG) channel, degrading multiple analog metrics[cite: 1]:

* **Threshold Voltage Stability:** Trapped charges near the gate interface directly alter the local flat-band potential, introducing unwanted shifts in threshold voltage ($V_{th}$)[cite: 1]:
  $$V_{th} = V_{FB} + 2\phi_F + \frac{Q_{trap}}{C_{ox}}$$
* **Transconductance Degradation:** Trapping centers present near the active channel scattering paths cause localized mobility degradation, resulting in a reduction of the device transconductance ($g_m$) and overall operational linearity[cite: 1]:
  $$g_m = \frac{\partial I_D}{\partial V_{GS}}$$
* **Current Collapse & Dynamic On-Resistance:** High electric fields trap hot channel electrons in adjacent buffer states[cite: 1]. Slow de-trapping rates restrict channel conduction post-stress, driving up the dynamic on-resistance ($R_{ON,dyn}$) and leading to current collapse phenomena[cite: 1]:
  $$R_{ON,dyn} = \frac{V_{DS}}{I_D}$$
