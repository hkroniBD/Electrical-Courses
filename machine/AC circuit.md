# AC Circuit Analysis: Principles and Methods

## Introduction

Alternating Current (AC) circuit analysis is fundamental to electrical engineering, as most electrical power systems operate with AC. Unlike DC circuits where current and voltage are constant, AC circuits involve time-varying quantities that require special mathematical tools and concepts for analysis.

## Learning Objectives

By the end of this lecture, students will be able to:
- Understand the fundamental concepts of AC waveforms and their parameters
- Apply phasor analysis to solve AC circuits
- Calculate impedance and admittance in AC circuits
- Analyze power relationships in AC circuits
- Understand and apply resonance concepts
- Solve complex AC circuits using various network theorems
- Analyze three-phase AC circuits
- Use frequency response concepts in circuit analysis

## Part 1: AC Waveform Fundamentals

### Sinusoidal Waveforms

**General form of AC voltage**:
```
v(t) = Vm sin(ωt + φ)
```
Where:
- v(t) = Instantaneous voltage
- Vm = Peak or maximum value
- ω = Angular frequency (rad/s)
- t = Time (seconds)
- φ = Phase angle (radians or degrees)

**Key Parameters**:

**1. Peak Value (Vm)**: Maximum value of the waveform

**2. Peak-to-Peak Value**: Vpp = 2Vm

**3. RMS (Root Mean Square) Value**:
```
Vrms = Vm/√2 = 0.707Vm
```

**4. Average Value**: For sinusoidal waveform over complete cycle = 0
   For half cycle: Vavg = 2Vm/π = 0.637Vm

**5. Form Factor**: FF = RMS value / Average value = π/(2√2) = 1.11

**6. Crest Factor**: CF = Peak value / RMS value = √2 = 1.414

### Frequency and Period

**Angular Frequency**: ω = 2πf (rad/s)

**Frequency**: f = 1/T (Hz)

**Period**: T = 2π/ω = 1/f (seconds)

### Phase Relationships

**Leading**: When one waveform reaches its maximum before another
**Lagging**: When one waveform reaches its maximum after another
**In Phase**: When two waveforms have the same phase angle (φ = 0°)
**Out of Phase**: When phase difference is 180° (φ = 180°)
**Quadrature**: When phase difference is 90° (φ = 90°)

## Part 2: Phasor Representation

### Complex Numbers Review

**Rectangular Form**: A + jB
- A = Real part
- B = Imaginary part
- j = √(-1)

**Polar Form**: |Z|∠θ
- |Z| = Magnitude = √(A² + B²)
- θ = Angle = tan⁻¹(B/A)

**Euler's Formula**: e^(jθ) = cos θ + j sin θ

### Phasor Concept

A phasor is a complex number representing the magnitude and phase of a sinusoidal quantity.

**Time domain**: v(t) = Vm sin(ωt + φ)
**Phasor domain**: V = Vm∠φ (peak phasor)
                   or V = Vrms∠φ (RMS phasor)

**Phasor Operations**:
- **Addition/Subtraction**: Convert to rectangular form
- **Multiplication/Division**: Use polar form
- **Differentiation**: jω × phasor
- **Integration**: phasor / (jω)

### Converting Between Domains

**From phasor to time domain**:
If V = Vm∠φ, then v(t) = Vm sin(ωt + φ)

**From time domain to phasor**:
If v(t) = Vm sin(ωt + φ), then V = Vm∠φ

## Part 3: AC Circuit Elements

### Resistor in AC Circuit

**Voltage-Current Relationship**: v(t) = R × i(t)
**Phasor Form**: V = R × I
**Power**: P = I²R = V²/R (always positive - consumed)
**Phase Relationship**: Voltage and current are in phase

### Inductor in AC Circuit

**Voltage-Current Relationship**: v(t) = L(di/dt)
**Phasor Form**: V = jωL × I = jXL × I
**Inductive Reactance**: XL = ωL = 2πfL (Ω)
**Power**: Average power = 0 (reactive power = I²XL)
**Phase Relationship**: Voltage leads current by 90°

### Capacitor in AC Circuit

**Voltage-Current Relationship**: i(t) = C(dv/dt)
**Phasor Form**: I = jωC × V, so V = I/(jωC) = -jXC × I
**Capacitive Reactance**: XC = 1/(ωC) = 1/(2πfC) (Ω)
**Power**: Average power = 0 (reactive power = I²XC)
**Phase Relationship**: Current leads voltage by 90°

### Reactance Summary

**Inductive Reactance**:
- XL = ωL
- Increases with frequency
- Voltage leads current

**Capacitive Reactance**:
- XC = 1/(ωC)
- Decreases with frequency
- Current leads voltage

## Part 4: Impedance and Admittance

### Impedance (Z)

**Definition**: The total opposition to AC current flow
```
Z = V/I (complex quantity)
```

**Rectangular Form**: Z = R + jX
- R = Resistance (real part)
- X = Reactance (imaginary part)

**Polar Form**: Z = |Z|∠θ
- |Z| = √(R² + X²) = Magnitude
- θ = tan⁻¹(X/R) = Phase angle

### Types of Impedance

**For Series R-L Circuit**:
Z = R + jXL = R + jωL

**For Series R-C Circuit**:
Z = R - jXC = R - j/(ωC)

**For Series R-L-C Circuit**:
Z = R + j(XL - XC) = R + j(ωL - 1/(ωC))

### Admittance (Y)

**Definition**: The reciprocal of impedance
```
Y = 1/Z = I/V
```

**Unit**: Siemens (S)

**Rectangular Form**: Y = G + jB
- G = Conductance = R/(R² + X²)
- B = Susceptance = -X/(R² + X²)

### Parallel Circuit Analysis

For parallel circuits, admittances add:
```
Ytotal = Y1 + Y2 + Y3 + ...
```

**For Parallel R-L Circuit**:
Y = 1/R - j/(ωL) = G - jBL

**For Parallel R-C Circuit**:
Y = 1/R + jωC = G + jBC

## Part 5: AC Circuit Analysis Methods

### Kirchhoff's Laws in AC Circuits

**KVL (Kirchhoff's Voltage Law)**:
∑V = 0 (algebraic sum of voltage drops in a closed loop)
In phasor form: ∑V⃗ = 0

**KCL (Kirchhoff's Current Law)**:
∑I = 0 (algebraic sum of currents at a node)
In phasor form: ∑I⃗ = 0

### Voltage Divider Rule

For series impedances Z₁ and Z₂:
```
V₁ = Vs × Z₁/(Z₁ + Z₂)
V₂ = Vs × Z₂/(Z₁ + Z₂)
```

### Current Divider Rule

For parallel impedances Z₁ and Z₂:
```
I₁ = Is × Z₂/(Z₁ + Z₂)
I₂ = Is × Z₁/(Z₁ + Z₂)
```

### Network Theorems

**Thevenin's Theorem**:
Any linear AC circuit can be replaced by an equivalent circuit consisting of a voltage source VTH in series with impedance ZTH.

**Norton's Theorem**:
Any linear AC circuit can be replaced by an equivalent circuit consisting of a current source IN in parallel with impedance ZN.

**Superposition Theorem**:
In circuits with multiple sources, the response is the sum of responses due to each source acting alone.

**Maximum Power Transfer Theorem**:
Maximum power is transferred when load impedance ZL = ZTH* (complex conjugate of source impedance).

## Part 6: Power in AC Circuits

### Instantaneous Power

```
p(t) = v(t) × i(t)
```

For sinusoidal voltage and current:
```
p(t) = VI cos φ + VI cos(2ωt + φv + φi)
```

### Average Power (Real Power)

**Definition**: Average value of instantaneous power over one complete cycle
```
P = VI cos φ (Watts)
```
Where φ = θv - θi (phase difference between voltage and current)

**Alternative forms**:
- P = I²R = V²R/Z²
- P = VrmsIrms cos φ

### Reactive Power

**Definition**: Power that oscillates between source and load
```
Q = VI sin φ (VAR - Volt-Ampere Reactive)
```

**Physical significance**: 
- Represents energy storage and release in reactive elements
- Does not contribute to useful work
- Causes additional current flow in power systems

### Apparent Power

**Definition**: Product of RMS voltage and RMS current
```
S = VI (VA - Volt-Ampere)
```

**Relationship**: S² = P² + Q²

### Power Factor

**Definition**: Ratio of real power to apparent power
```
pf = P/S = cos φ
```

**Types**:
- **Leading power factor**: Current leads voltage (capacitive load)
- **Lagging power factor**: Current lags voltage (inductive load)
- **Unity power factor**: Current and voltage in phase (resistive load)

### Power Triangle

**Representation**: Right triangle showing relationship between P, Q, and S
- Horizontal side: Real power (P)
- Vertical side: Reactive power (Q)
- Hypotenuse: Apparent power (S)
- Angle: Power factor angle (φ)

### Complex Power

**Definition**: S⃗ = P + jQ = VI*
Where I* is the complex conjugate of current phasor

**Magnitude**: |S⃗| = √(P² + Q²) = Apparent power
**Angle**: ∠S⃗ = φ = Power factor angle

## Part 7: Resonance in AC Circuits

### Series Resonance

**Condition**: XL = XC
```
ωL = 1/(ωC)
ωr = 1/√(LC) (resonant frequency)
fr = 1/(2π√(LC))
```

**Characteristics at resonance**:
- Impedance is minimum (Z = R)
- Current is maximum
- Power factor = 1 (unity)
- Voltage across L and C can exceed supply voltage
- Phase angle = 0°

**Quality Factor (Q)**:
```
Q = ωrL/R = 1/(ωrRC) = (1/R)√(L/C)
```

**Bandwidth**: BW = fr/Q

**Half-power frequencies**:
- f₁ = fr - BW/2
- f₂ = fr + BW/2

### Parallel Resonance

**Condition**: BL = BC (susceptances are equal)
```
1/(ωL) = ωC
ωr = 1/√(LC)
```

**Characteristics at resonance**:
- Admittance is minimum
- Impedance is maximum
- Line current is minimum
- Power factor = 1 (unity)
- Circulating current between L and C
- Often called "anti-resonance"

### Practical Resonance

**Series circuit with resistance**:
- Resonant frequency slightly affected by resistance
- Sharper resonance with lower resistance (higher Q)

**Parallel circuit with resistance**:
- Different expressions for resonant frequency
- Tank circuit behavior in practical applications

### Applications of Resonance

**Series Resonance**:
- Voltage amplification
- Frequency selection
- Filter circuits

**Parallel Resonance**:
- Current amplification
- Impedance transformation
- Oscillator circuits
- RF amplifiers

## Part 8: Frequency Response

### Transfer Functions

**Definition**: H(jω) = Output/Input

**Magnitude**: |H(jω)|
**Phase**: ∠H(jω)

### Bode Plots

**Magnitude Plot**: 20 log|H(jω)| vs log ω (dB vs frequency)
**Phase Plot**: ∠H(jω) vs log ω (degrees vs frequency)

### Filter Circuits

**Low-Pass Filter (RC)**:
```
H(jω) = 1/(1 + jωRC)
fc = 1/(2πRC) (cutoff frequency)
```

**High-Pass Filter (RC)**:
```
H(jω) = jωRC/(1 + jωRC)
fc = 1/(2πRC)
```

**Band-Pass Filter (RLC)**:
- Passes frequencies near resonant frequency
- Rejects frequencies far from resonance

**Band-Stop Filter (RLC)**:
- Rejects frequencies near resonant frequency
- Passes frequencies far from resonance

### Decibel Scale

**Power ratio**: dB = 10 log₁₀(P₂/P₁)
**Voltage ratio**: dB = 20 log₁₀(V₂/V₁)
**Current ratio**: dB = 20 log₁₀(I₂/I₁)

## Part 9: Three-Phase AC Circuits

### Three-Phase Generation

**Advantages of three-phase systems**:
- Constant power delivery
- More economical transmission
- Balanced magnetic fields in machines
- Smaller conductor requirements

**Phase relationships**:
- Three sinusoidal voltages
- 120° phase difference
- Same magnitude and frequency

### Three-Phase Connections

**Wye (Y) Connection**:
- Line voltage = √3 × Phase voltage
- Line current = Phase current
- VL = √3 × Vph
- IL = Iph

**Delta (Δ) Connection**:
- Line voltage = Phase voltage
- Line current = √3 × Phase current
- VL = Vph
- IL = √3 × Iph

### Three-Phase Power

**Balanced Load**:
```
P = √3 VL IL cos φ
Q = √3 VL IL sin φ
S = √3 VL IL
```

**Per-phase analysis**: Analyze one phase and multiply by 3

### Sequence Components

**Positive Sequence**: Normal balanced system
**Negative Sequence**: Reverse phase rotation
**Zero Sequence**: All phases in phase

Used for analyzing unbalanced systems.

## Part 10: Advanced AC Circuit Analysis

### Nodal Analysis

**Steps**:
1. Choose reference node (ground)
2. Assign node voltages
3. Apply KCL at each node
4. Solve simultaneous equations

**Admittance matrix method**: [Y][V] = [I]

### Mesh Analysis

**Steps**:
1. Identify independent loops
2. Assign mesh currents
3. Apply KVL around each mesh
4. Solve simultaneous equations

**Impedance matrix method**: [Z][I] = [V]

### AC Bridge Circuits

**Maxwell Bridge**: Measures inductance
**Hay Bridge**: Measures high Q inductance
**Schering Bridge**: Measures capacitance
**Wien Bridge**: Measures frequency

**Balance condition**: Z₁Z₃ = Z₂Z₄

### Coupled Circuits

**Mutual Inductance**: M = k√(L₁L₂)
Where k = coupling coefficient (0 ≤ k ≤ 1)

**Voltage equations**:
```
V₁ = jωL₁I₁ ± jωMI₂ + R₁I₁
V₂ = jωL₂I₂ ± jωMI₁ + R₂I₂
```

Sign depends on dot convention.

## Part 11: Computer-Aided Analysis

### SPICE Simulation

**AC Analysis commands**:
- .AC: Frequency response analysis
- .TRAN: Transient analysis
- .OP: Operating point analysis

### MATLAB Analysis

**Functions for AC analysis**:
- freqs(): Frequency response
- bode(): Bode plot
- nyquist(): Nyquist plot
- step(): Step response

### Symbolic Analysis

**Using complex algebra**:
- Define impedances as complex numbers
- Apply circuit laws
- Solve algebraically

## Part 12: Practical Considerations

### Non-Sinusoidal Waveforms

**Fourier Series**: Any periodic waveform can be represented as sum of sinusoids
```
f(t) = A₀ + Σ[An cos(nωt) + Bn sin(nωt)]
```

**Harmonic Analysis**: Study of individual frequency components
**Total Harmonic Distortion (THD)**: Measure of waveform distortion

### Power Quality

**Issues**:
- Harmonics
- Voltage sags and swells
- Flicker
- Unbalance

**Effects on AC circuit analysis**:
- Multiple frequency components
- Modified impedance calculations
- Increased losses

### Measurement in AC Circuits

**RMS Meters**: Measure true RMS values
**Power Meters**: Measure real power
**Power Factor Meters**: Measure cos φ
**Oscilloscopes**: Observe waveforms and phase relationships

## Part 13: Applications

### Power Systems

**Transmission lines**: Modeled as distributed R, L, C
**Transformers**: Ideal and practical models
**Generators**: Equivalent circuits and phasor diagrams
**Motors**: Equivalent circuits and power analysis

### Electronic Circuits

**Amplifiers**: Frequency response analysis
**Filters**: Design and analysis
**Oscillators**: Resonance applications
**Power supplies**: Rectification and filtering

### Communication Systems

**Antenna analysis**: Impedance matching
**Filter design**: Frequency selectivity
**Transmission lines**: Characteristic impedance
**Modulation**: Frequency domain analysis

## Conclusion

AC circuit analysis is fundamental to understanding electrical and electronic systems. The concepts of phasors, impedance, power, and resonance form the foundation for more advanced topics in power systems, electronics, and communications.

**Key Takeaways**:
- Phasor representation simplifies AC analysis
- Impedance and admittance are complex quantities
- Power in AC circuits has real, reactive, and apparent components
- Resonance provides frequency selectivity
- Three-phase systems are more efficient for power transmission
- Computer tools enhance analysis capabilities

## Review Questions

1. Explain the relationship between RMS and peak values for sinusoidal waveforms.
2. How do you convert between rectangular and polar forms of complex numbers?
3. Derive the impedance of series and parallel RLC circuits.
4. What is the significance of power factor in AC circuits?
5. Explain the conditions for series and parallel resonance.
6. How do you analyze three-phase balanced circuits?
7. Compare nodal and mesh analysis for AC circuits.
8. Explain the concept of quality factor in resonant circuits.
9. What are the advantages of phasor analysis over time-domain analysis?
10. How do harmonics affect AC circuit analysis?

## Numerical Problems

**Problem 1**: A series RLC circuit has R = 10Ω, L = 0.1H, C = 100μF. If the supply voltage is 100V at 50Hz, find:
(a) Impedance (b) Current (c) Power factor (d) Power consumed

**Problem 2**: Two impedances Z₁ = 8 + j6Ω and Z₂ = 10 - j8Ω are connected in parallel across a 200V, 60Hz supply. Find:
(a) Total current (b) Power consumed (c) Reactive power

**Problem 3**: A series RLC circuit resonates at 1kHz. If L = 10mH and the bandwidth is 100Hz, find:
(a) Capacitance (b) Resistance (c) Quality factor

## Laboratory Exercises

1. **Phasor Measurement**: Use oscilloscope to measure phase relationships
2. **Impedance vs Frequency**: Plot impedance characteristics of RLC circuits
3. **Resonance Investigation**: Find resonant frequency and Q factor
4. **Power Measurement**: Measure real, reactive, and apparent power
5. **Three-Phase Circuits**: Analyze balanced and unbalanced loads

## Further Reading

- "Fundamentals of Electric Circuits" by Alexander & Sadiku
- "Electric Circuits" by Nilsson & Riedel
- "Network Analysis" by M.E. Van Valkenburg
- "Linear Circuit Analysis" by R.A. DeCarlo & P.M. Lin
- IEEE Standards for electrical measurements
- SPICE circuit simulation guides