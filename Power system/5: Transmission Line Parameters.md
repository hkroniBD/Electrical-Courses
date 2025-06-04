# Lecture 5: Transmission Line Parameters

**Course Instructor** 📚  
- **Name**: Md. Hassanul Karim Roni 👨‍🏫  
- **Position**: Assistant Professor, EEE, HSTU, Dinajpur, BD 🏫  
- **Email**: hassanulkarim.roni@gmail.com ✉️  
- **Contact**: 01767052709 (WhatsApp) 📞  

## Objective  
Master the fundamental electrical parameters of transmission lines (resistance, inductance, capacitance) and understand how line length determines modeling approaches for accurate power system analysis.

## Ice-Breaker: Fun Facts to Spark Curiosity 🌟  
- **Invisible Enemy** ⚡: The 230 kV Ghorashal-Siddhirganj line loses ~2-3% power due to resistance alone – that's enough to power 1,000 homes!  
- **Magnetic Mystery** 🧲: PGCB's 132 kV lines store magnetic energy equivalent to lifting a 10-ton truck 100 meters high, all invisible in the air around conductors!  
- **Capacitive Surprise** 🔋: Even when disconnected, transmission lines act like giant capacitors, storing enough charge to light LED bulbs through electromagnetic induction!  
- **Length Matters** 📏: A 50 km line behaves like a simple resistor, but a 500 km line becomes a complex electromagnetic wave transmission medium!

## 1. Resistance (R) of Transmission Lines 🔥  
Resistance causes power losses and voltage drops, directly impacting transmission efficiency in Bangladesh's grid.

### DC Resistance  
- **Formula**: $$R_{dc} = \rho \frac{l}{A}$$  
  - Where: ρ = resistivity (Ω⋅m), l = length (m), A = cross-sectional area (m²)  
- **ACSR Example**: For aluminum conductor with ρ = 2.83×10⁻⁸ Ω⋅m, 300 mm² area, 100 km length:  
  $$R_{dc} = 2.83×10^{-8} \times \frac{100,000}{300×10^{-6}} = 9.43 \text{ Ω}$$

### AC Resistance  
- **Skin Effect**: AC current concentrates near conductor surface, increasing effective resistance  
- **Formula**: $$R_{ac} = R_{dc} \times k_s$$  
  - Where: ks = skin effect factor (1.02-1.05 for PGCB's 50 Hz system)  
- **Temperature Effect**: $$R_T = R_{20°C} [1 + α(T - 20)]$$  
  - For aluminum: α = 0.004/°C  
  - Bangladesh's 35°C average increases R by ~6%

In Bangladesh, PGCB standards specify maximum resistance for 132 kV lines at 0.3 Ω/km and 230 kV lines at 0.15 Ω/km. The 3% resistance loss on Dhaka-Chittagong corridor (~300 km) equals 30 MW power loss – enough for 24,000 households!

## 2. Inductance (L) of Transmission Lines 🧲  
Inductance opposes current changes, affecting voltage regulation and reactive power flow.

### Self-Inductance  
- **Formula**: $$L = 2×10^{-7} \ln\left(\frac{D}{r}\right) \text{ H/m}$$  
  - Where: D = geometric mean distance between phases, r = conductor radius  
- **Typical Values**: 0.9-1.3 mH/km for PGCB's transmission lines

### Mutual Inductance  
- **Between Phases**: Creates coupling between conductors in 3-phase systems  
- **Effect**: Influences current distribution and voltage balance

### Reactance Calculation  
- **Inductive Reactance**: $$X_L = 2πfL = ωL$$  
- **At 50 Hz**: XL ≈ 0.3-0.4 Ω/km for typical PGCB lines  
- **Example**: 100 km, 132 kV line with L = 1.2 mH/km:  
  $$X_L = 2π × 50 × 1.2×10^{-3} × 100 = 37.7 \text{ Ω}$$

In Bangladesh, inductive reactance causes 5-8% voltage drop on long 230 kV lines and consumes 20-30 MVAR per 100 km of 132 kV line under full load.

## 3. Capacitance (C) of Transmission Lines 🔋  
Capacitance between conductors and ground generates reactive power and affects voltage regulation.

### Line-to-Neutral Capacitance  
- **Formula**: $$C = \frac{2πε_0}{\ln(D/r)} \text{ F/m}$$  
  - Where: ε₀ = 8.854×10⁻¹² F/m (free space permittivity)  
- **Typical Values**: 8-12 nF/km for PGCB's overhead lines

### Capacitive Reactance  
- **Formula**: $$X_C = \frac{1}{2πfC} = \frac{1}{ωC}$$  
- **At 50 Hz**: XC ≈ 250-350 kΩ⋅km for typical lines  
- **Per Unit Length**: 0.3-0.4 MΩ/km

### Charging Current  
- **Formula**: $$I_c = \frac{V}{X_C} = V × ωC$$  
- **Example**: 230 kV line, 100 km, C = 10 nF/km:  
  $$I_c = \frac{230,000}{\sqrt{3}} × 2π × 50 × 10×10^{-9} × 100 = 41.8 \text{ A}$$

In Bangladesh, capacitive charging causes voltage rise on lightly loaded long lines, and 100 km of 230 kV line generates ~20 MVAR when energized but unloaded.

## 4. Line Models: Short, Medium, and Long Lines 📏  

### Short Lines (Length < 80 km) 🔗  
- **Model**: Resistance and inductance lumped, capacitance neglected  
- **Circuit**: Simple R-L series connection  
- **Equations**:  
  - $$V_s = V_r + I_r Z$$  
  - $$I_s = I_r$$  
  - Where: Z = R + jXL (series impedance)

In Bangladesh, Dhaka suburban 33 kV feeders and local 132 kV connections are typical examples.

### Medium Lines (80 km < Length < 250 km) 🔗🔗  
- **Model**: Nominal π (pi) circuit or T circuit  
- **π Circuit**: Capacitance split equally at both ends  
- **Equations**:  
  - $$V_s = AV_r + BI_r$$  
  - $$I_s = CV_r + DI_r$$  
  - ABCD parameters: A = D = 1 + YZ/2, B = Z, C = Y(1 + YZ/4)

In Bangladesh, Dhaka-Comilla 132 kV line and Bogra-Rangpur 230 kV connection are typical examples.

### Long Lines (Length > 250 km) 🔗🔗🔗  
- **Model**: Distributed parameter model with hyperbolic functions  
- **Propagation Constant**: $$γ = α + jβ = \sqrt{ZY}$$  
- **Characteristic Impedance**: $$Z_c = \sqrt{\frac{Z}{Y}}$$  
- **Equations**:  
  - $$V_s = V_r \cosh(γl) + I_r Z_c \sinh(γl)$$  
  - $$I_s = I_r \cosh(γl) + \frac{V_r}{Z_c} \sinh(γl)$$

In Bangladesh, the planned Dhaka-Chittagong 765 kV line (~300 km) and cross-border interconnections are typical examples.

## 5. Theoretical Basis for Parameter Calculations 🧮  

### Electromagnetic Field Theory  
- **Maxwell's Equations**: Govern electromagnetic behavior in transmission lines  
- **TEM Mode**: Transverse electromagnetic wave propagation  
- **Boundary Conditions**: Conductor surfaces and ground plane effects

### Geometric Considerations  
- **Conductor Bundling**: Reduces inductance and increases capacitance  
- **Ground Effect**: Uses method of images for accurate capacitance calculation  
- **Phase Spacing**: Optimized for minimum inductance (typically 4-6 meters for 132 kV)

### Environmental Factors  
- **Weather Impact**: Rain increases leakage, temperature affects resistance  
- **Conductor Sag**: Changes geometry and affects parameters  
- **Corona Effect**: Modifies effective conductor radius at high voltages

For 132 kV lines in Bangladesh, typical parameters include:
- **Resistance**: 0.25 Ω/km (ACSR 300 mm²)  
- **Inductance**: 1.1 mH/km  
- **Capacitance**: 9.5 nF/km  
- **Surge Impedance**: $$Z_c = \sqrt{L/C} = \sqrt{1.1×10^{-3}/9.5×10^{-9}} = 340 \text{ Ω}$$

## 6. Practical Applications in Bangladesh 🇧🇩  

### PGCB Design Standards  
- **Parameter Limits**: Maximum Z = 1.0 Ω/km for 132 kV lines  
- **Voltage Regulation**: <5% for transmission, <10% for sub-transmission  
- **Thermal Limits**: ACSR conductors rated for 75°C continuous operation

### System Studies  
- **Load Flow**: Uses π-model for medium lines, distributed model for long lines  
- **Short Circuit**: Resistance and inductance determine fault current magnitude  
- **Stability**: Line charging and series impedance affect power transfer limits

### Technical Data: Bangladesh Transmission Parameters  
| Voltage Level | R (Ω/km) | XL (Ω/km) | XC (MΩ⋅km) | Model Type |  
|---------------|----------|-----------|------------|------------|  
| **66 kV** | 0.4-0.5 | 0.35-0.40 | 0.25-0.30 | Short/Medium |  
| **132 kV** | 0.25-0.3 | 0.30-0.35 | 0.28-0.32 | Medium |  
| **230 kV** | 0.12-0.18 | 0.28-0.32 | 0.30-0.35 | Medium/Long |  
| **400 kV** | 0.08-0.12 | 0.25-0.30 | 0.32-0.38 | Long |

## 7. Key Takeaways 📝  
- Resistance causes I²R losses; skin effect increases AC resistance by 2-5%  
- Inductance creates reactive voltage drop; typically 0.3-0.4 Ω/km at 50 Hz  
- Capacitance generates reactive power; causes voltage rise on light-loaded lines  
- Line length determines model complexity: lumped (short), π-circuit (medium), distributed (long)  
- PGCB uses medium-line models for most 132-230 kV analysis  

## References 📚  
- Stevenson, W. D., & Grainger, J. J. (1994). *Power System Analysis*. McGraw-Hill Education.  
- Glover, J. D., Sarma, M. S., & Overbye, T. J. (2017). *Power System Analysis and Design*. Cengage Learning.  
- Bergen, A. R., & Vittal, V. (2000). *Power Systems Analysis*. Prentice Hall.  
- Power Grid Company of Bangladesh [PGCB](https://www.pgcb.gov.bd).  
- IEEE Standard 738-2012. *IEEE Standard for Calculating the Current-Temperature Relationship of Bare Overhead Conductors*.

## Objective Viva Questions ❓  
1. **What causes skin effect in AC transmission lines?**  
   a) High voltage  
   b) Magnetic field concentration  
   c) Current density variation with frequency  
   d) Temperature increase  

2. **Which parameter is neglected in short line models?**  
   a) Resistance  
   b) Inductance  
   c) Capacitance  
   d) All parameters  

3. **What is the typical surge impedance of 132 kV transmission lines?**  
   a) 50 Ω  
   b) 150 Ω  
   c) 340 Ω  
   d) 500 Ω  

4. **For a 150 km, 230 kV line, which model should be used?**  
   a) Short line model  
   b) Medium line (π-circuit)  
   c) Long line (distributed)  
   d) Any model  

5. **What happens to line capacitance when conductor spacing increases?**  
   a) Increases  
   b) Decreases  
   c) Remains constant  
   d) Becomes zero  

6. **The charging current of a transmission line is proportional to:**  
   a) Line resistance  
   b) Line voltage  
   c) Line inductance  
   d) Load current  

7. **In Bangladesh's 50 Hz system, skin effect factor for aluminum is approximately:**  
   a) 0.95  
   b) 1.00  
   c) 1.03  
   d) 1.10  

## Solutions to Viva Questions ✅  
1. **c) Current density variation with frequency**  
   *Explanation*: AC current concentrates near conductor surface due to electromagnetic effects, increasing effective resistance.  

2. **c) Capacitance**  
   *Explanation*: Short lines (<80 km) neglect capacitance effects due to minimal charging current impact.  

3. **c) 340 Ω**  
   *Explanation*: Surge impedance Zc = √(L/C) ≈ 340 Ω for typical overhead transmission lines.  

4. **b) Medium line (π-circuit)**  
   *Explanation*: 150 km falls in medium line range (80-250 km), requiring π-circuit or T-circuit model.  

5. **b) Decreases**  
   *Explanation*: Capacitance C = 2πε₀/ln(D/r); increased spacing D reduces capacitance.  

6. **b) Line voltage**  
   *Explanation*: Charging current Ic = V×ωC is directly proportional to applied voltage.  

7. **c) 1.03**  
   *Explanation*: Skin effect factor for aluminum at 50 Hz is typically 1.02-1.05, with 1.03 being representative.
