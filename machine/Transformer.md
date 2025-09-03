# Transformers: Principles, Construction, and Applications

## Introduction

A transformer is a static electrical device that transfers electrical energy from one AC circuit to another through electromagnetic induction. It can step up or step down voltage levels while maintaining the same frequency, making it essential for efficient power transmission and distribution systems.

## Learning Objectives

By the end of this lecture, students will be able to:
- Understand the fundamental principles of transformer operation
- Explain transformer construction and core types
- Analyze transformer equivalent circuits and phasor diagrams
- Calculate transformer parameters and perform various tests
- Understand different types of transformers and their applications
- Identify transformer losses, efficiency, and regulation
- Perform parallel operation analysis
- Understand protection and maintenance requirements

## Part 1: Fundamental Principles

### Electromagnetic Induction

Transformers operate on two fundamental laws:

**Faraday's Law of Electromagnetic Induction**:
```
e = -N(dΦ/dt)
```
Where:
- e = Induced EMF (Volts)
- N = Number of turns
- Φ = Magnetic flux (Weber)
- t = Time (seconds)

**Lenz's Law**: The direction of induced EMF opposes the change causing it.

### Mutual Induction

When alternating current flows in the primary winding, it creates an alternating magnetic flux in the core. This flux links with the secondary winding, inducing an EMF according to mutual induction principles.

### Basic Transformer Action

1. **Primary winding** connected to AC supply creates alternating flux
2. **Alternating flux** links with both primary and secondary windings
3. **EMF induced** in both windings proportional to number of turns
4. **Secondary EMF** causes current to flow when load is connected
5. **Secondary current** creates its own flux opposing primary flux
6. **Primary current** increases to maintain flux balance

## Part 2: Construction of Transformers

### Core Construction

**Core Materials**:
- **Silicon steel**: Low hysteresis and eddy current losses
- **Laminations**: 0.35-0.5mm thick, insulated to reduce eddy currents
- **Grain-oriented steel**: Superior magnetic properties
- **Amorphous steel**: Ultra-low losses for high-efficiency transformers

**Core Types**:

**1. Core Type**
- Windings surrounding the core limbs
- Rectangular core with two limbs
- Easy to manufacture and repair
- Used for small and medium transformers

**2. Shell Type**
- Core surrounding the windings
- Three limbs with central limb carrying windings
- Better mechanical protection
- Used for large power transformers

**3. Distributed Type**
- Multiple cores and windings
- Used for very large transformers
- Better cooling and reduced size

### Winding Construction

**Winding Materials**:
- **Copper**: Excellent conductivity, higher cost
- **Aluminum**: Lower cost, larger cross-section required
- **Insulation**: Paper, pressboard, oil, SF6 gas

**Winding Types**:

**1. Concentric Windings**
- Cylindrical windings, one inside the other
- Low voltage winding inside (easier insulation)
- High voltage winding outside
- Most common arrangement

**2. Interleaved Windings**
- Windings divided into sections
- Alternate sections of primary and secondary
- Better coupling, used in special applications

**3. Spiral Windings**
- Flat spiral conductors
- Used for very high current, low voltage applications

### Insulation System

**Solid Insulation**:
- Pressboard, paper, nomex
- Barriers between windings
- Lead insulation

**Liquid Insulation**:
- Mineral oil (most common)
- Synthetic fluids (fire-resistant)
- Natural esters (biodegradable)

**Gaseous Insulation**:
- SF6 gas for compact substations
- Dry air for dry-type transformers

## Part 3: Transformer Theory

### Ideal Transformer

**Assumptions**:
- No losses (100% efficient)
- No leakage flux
- Infinite permeability of core
- No resistance in windings

**Voltage Transformation**:
```
V₁/V₂ = N₁/N₂ = a (transformation ratio)
```

**Current Transformation**:
```
I₁/I₂ = N₂/N₁ = 1/a
```

**Power Balance**:
```
V₁I₁ = V₂I₂ (input power = output power)
```

**Impedance Transformation**:
```
Z₁ = a²Z₂
```

### EMF Equation

For sinusoidal flux: Φ = Φₘ sin ωt

**RMS value of induced EMF**:
```
E = 4.44 f N Φₘ
```
Where:
- E = RMS value of EMF (Volts)
- f = Frequency (Hz)
- N = Number of turns
- Φₘ = Maximum flux (Weber)

**Form Factor**: 4.44 relates RMS and maximum values for sinusoidal waveform

### Practical Transformer

**Losses present**:
- Core losses (hysteresis and eddy current)
- Copper losses (I²R losses in windings)
- Stray losses

**Impedances present**:
- Leakage reactances
- Winding resistances

## Part 4: Equivalent Circuit

### Exact Equivalent Circuit

**Primary side referred**:
- R₁ = Primary resistance
- X₁ = Primary leakage reactance
- R₂' = Secondary resistance referred to primary
- X₂' = Secondary leakage reactance referred to primary
- Rₒ = Core loss resistance
- Xₒ = Magnetizing reactance

### Approximate Equivalent Circuit

**Assumptions for simplification**:
- Shunt branch (Rₒ, Xₒ) moved to primary terminals
- Negligible voltage drop in shunt branch

**Equivalent impedance**:
```
Zeq = (R₁ + R₂') + j(X₁ + X₂')
Req = R₁ + R₂'
Xeq = X₁ + X₂'
```

### Phasor Diagram

**No-load condition**:
- Primary current has two components
- Magnetizing component (90° lagging)
- Core loss component (in phase with voltage)

**Load condition**:
- Secondary current reflected to primary
- Vector addition of no-load and load components
- Phase relationships depend on load power factor

## Part 5: Transformer Tests

### Open Circuit Test (No-Load Test)

**Purpose**: Determine core losses and magnetizing parameters

**Procedure**:
- Secondary open-circuited
- Rated voltage applied to primary
- Measure V₁, I₀, W₀

**Calculations**:
```
Core loss = W₀
Magnetizing current = I₀
Power factor = W₀/(V₁I₀)
Magnetizing reactance = V₁/Iμ
Core loss resistance = V₁/Ic
```

### Short Circuit Test

**Purpose**: Determine copper losses and equivalent impedance

**Procedure**:
- Secondary short-circuited
- Reduced voltage applied to primary (5-15% of rated)
- Measure Vsc, Isc, Wsc

**Calculations**:
```
Copper loss at full load = Wsc
Equivalent resistance = Wsc/Isc²
Equivalent impedance = Vsc/Isc
Equivalent reactance = √(Zeq² - Req²)
```

### Back-to-Back Test (Sumpner's Test)

**Purpose**: Determine losses in identical transformers efficiently

**Procedure**:
- Two identical transformers connected back-to-back
- Primary windings connected to supply
- Secondary windings connected with small voltage difference
- Circulating current adjusted to rated value

**Advantages**:
- Power consumed only for losses
- Economical for large transformers
- Both transformers tested simultaneously

## Part 6: Losses and Efficiency

### Types of Losses

**1. Core Losses (Iron Losses)**

**Hysteresis Loss**:
```
Ph = Kh × f × Bmax^n × Volume
```
Where n = 1.6 to 2.0 (Steinmetz constant)

**Eddy Current Loss**:
```
Pe = Ke × f² × Bmax² × t² × Volume
```
Where t = lamination thickness

**Total Core Loss**: Pi = Ph + Pe (constant at all loads)

**2. Copper Losses (I²R Losses)**
```
Pcu = I₁²R₁ + I₂²R₂ = I²Req
```
- Variable with load
- Proportional to square of current

**3. Stray Losses**
- Leakage flux losses in tank walls
- Additional losses due to harmonics
- Usually 0.5-1% of rating

### Efficiency

**Definition**:
```
η = Output Power / Input Power × 100%
η = Output Power / (Output Power + Losses) × 100%
```

**Alternative form**:
```
η = (1 - Losses/Input Power) × 100%
```

**Condition for Maximum Efficiency**:
Maximum efficiency occurs when variable losses equal fixed losses:
```
Copper losses = Core losses
I²Req = Pi
```

**All-day Efficiency**:
```
ηall-day = (Energy output in 24 hours) / (Energy input in 24 hours) × 100%
```

Important for distribution transformers with varying loads.

## Part 7: Voltage Regulation

### Definition
Voltage regulation is the change in secondary terminal voltage from no-load to full-load expressed as percentage of no-load voltage.

```
% Regulation = ((E₂ - V₂)/E₂) × 100%
```

### Approximate Formula
```
% Regulation ≈ (I₂Req cos φ₂ + I₂Xeq sin φ₂)/E₂ × 100%
```

Where φ₂ = load power factor angle

**For different power factors**:
- **Resistive load** (cos φ = 1): Minimum regulation
- **Inductive load** (cos φ lagging): Positive regulation
- **Capacitive load** (cos φ leading): May be negative regulation

### Exact Calculation
Using phasor diagram or:
```
V₁ = √[(E₂ cos φ₂ + I₂Req)² + (E₂ sin φ₂ + I₂Xeq)²]
```

## Part 8: Three-Phase Transformers

### Construction Types

**1. Core Type Three-Phase Transformer**
- Three separate cores with windings
- Larger and more expensive
- Easy maintenance
- Used where transportation is not limiting

**2. Shell Type Three-Phase Transformer**
- Five-limb core construction
- More compact
- Complex construction
- Better magnetic circuit

### Connection Types

**1. Star (Y) Connection**
- Line voltage = √3 × Phase voltage
- Line current = Phase current
- Neutral point available

**2. Delta (Δ) Connection**
- Line voltage = Phase voltage
- Line current = √3 × Phase current
- No neutral point

**3. Zigzag Connection**
- Each phase winding split into two halves
- Better for unbalanced loads
- Used in grounding transformers

### Common Connection Groups

**Yy0**: Star-Star, 0° phase shift
**Dd0**: Delta-Delta, 0° phase shift
**Yd11**: Star-Delta, -30° phase shift (330°)
**Dy11**: Delta-Star, -30° phase shift

## Part 9: Special Transformers

### Auto Transformers

**Construction**:
- Single winding with tapped connections
- Primary and secondary share common winding
- More economical for voltage ratios close to 1:1

**Advantages**:
- Smaller size and cost
- Higher efficiency
- Better regulation

**Disadvantages**:
- No electrical isolation
- Transferred power = Transformed power + Conducted power

**Applications**:
- Starting of induction motors
- Voltage regulation
- Interconnecting different voltage systems

### Instrument Transformers

**Current Transformers (CT)**:
- Step down current to standard values (1A or 5A)
- Secondary must never be open-circuited
- Used for measurement and protection

**Voltage Transformers (VT/PT)**:
- Step down voltage to standard values (110V)
- Primary connected across lines
- Used for measurement and protection

### Isolation Transformers

**Purpose**: Provide electrical isolation between circuits
**Applications**:
- Medical equipment
- Laboratory instruments
- Sensitive electronic equipment

### Pulse Transformers

**Applications**:
- Digital circuits
- Radar systems
- Gate drive circuits for power electronics

## Part 10: Parallel Operation

### Conditions for Parallel Operation

1. **Same voltage ratios**
2. **Same percentage impedances**
3. **Same impedance ratios (X/R)**
4. **Same phase sequence** (for 3-phase)
5. **Same frequency rating**

### Load Sharing

**For transformers with different ratings**:
```
I₁/I₂ = (kVA₂ × Z₂)/(kVA₁ × Z₁)
```

**Equal percentage impedances**: Load shared in proportion to kVA ratings

**Unequal percentage impedances**: Transformer with lower impedance carries more load

### Circulating Current

When transformers with unequal voltage ratios are paralleled:
```
Icir = (E₁ - E₂)/(Z₁ + Z₂)
```

This circulating current causes:
- Additional I²R losses
- Reduced load carrying capacity
- Poor regulation

## Part 11: Testing and Condition Monitoring

### Routine Tests

**1. Resistance Measurement**
- DC resistance of windings
- Temperature correction required
- Detects loose connections, broken strands

**2. Insulation Resistance Test**
- Megger test between windings and earth
- Polarization index measurement
- Minimum values specified in standards

**3. Ratio Test**
- Verify turns ratio
- TTR (Transformer Turns Ratio) tester
- Important for parallel operation

### Diagnostic Tests

**1. Dissolved Gas Analysis (DGA)**
- Gases dissolved in oil indicate faults
- Different gas ratios identify fault types
- Early warning of developing problems

**2. Oil Quality Tests**
- Dielectric strength (breakdown voltage)
- Moisture content
- Acidity and oxidation products
- Furanic compounds (paper degradation)

**3. Frequency Response Analysis (FRA)**
- Detects mechanical deformation
- Compares frequency response with fingerprint
- Sensitive to winding movement

**4. Partial Discharge Testing**
- Detects insulation degradation
- Online and offline measurements
- Important for aging assessment

### Temperature Monitoring

**Hot Spot Temperature**:
- Critical parameter for insulation life
- Fiber optic sensors for direct measurement
- Thermal models for estimation

**Oil Temperature**:
- Top oil and bottom oil temperatures
- Cooling system performance indication
- Load capability determination

## Part 12: Protection Systems

### Protection Schemes

**1. Overcurrent Protection**
- Primary protection for distribution transformers
- Time-graded coordination
- Fuses or circuit breakers

**2. Differential Protection**
- Compares primary and secondary currents
- Fast operation for internal faults
- Restrained differential for large transformers

**3. Restricted Earth Fault (REF)**
- Protects against earth faults in star-connected windings
- High sensitivity
- Used with differential protection

**4. Buchholz Relay**
- Gas accumulation and oil flow detection
- Two-stage operation (alarm and trip)
- Only for oil-filled transformers with conservator

**5. Sudden Pressure Relay**
- Detects rapid pressure rise
- Fast operation for severe internal faults
- Backup to Buchholz relay

### Magnetizing Inrush Current

**Characteristics**:
- High magnitude (up to 20 times rated current)
- Rich in second harmonic (15-50%)
- Decays exponentially
- Occurs during energization

**Effects on Protection**:
- May cause unwanted operation of overcurrent relays
- Differential relays need second harmonic restraint
- Special algorithms required

## Part 13: Maintenance

### Preventive Maintenance

**Oil Maintenance**:
- Regular oil sampling and testing
- Oil filtration and reconditioning
- Moisture removal
- Oxidation inhibitor addition

**Cooling System**:
- Radiator cleaning
- Fan and pump maintenance
- Thermostatic controls checking
- Oil flow verification

**Electrical Maintenance**:
- Tap changer maintenance
- Contact cleaning and adjustment
- Insulation system monitoring
- Bushing maintenance

### Condition-Based Maintenance

**Online Monitoring**:
- Continuous parameter monitoring
- Automatic alarms and diagnostics
- Trend analysis
- Predictive maintenance scheduling

**Thermal Monitoring**:
- Hot spot temperature tracking
- Load capability assessment
- Insulation aging models
- Life assessment

## Part 14: Applications

### Power System Applications

**1. Generation Transformers**
- Step up generator voltage to transmission level
- Typically 15-25 kV to 115-765 kV
- Large ratings (100-1500 MVA)
- Special design for generator terminals

**2. Transmission Transformers**
- Interconnect different voltage levels
- 115 kV to 765 kV systems
- Auto transformers common for close ratios
- Critical for system reliability

**3. Distribution Transformers**
- Step down to utilization voltages
- 4-35 kV to 120-480 V
- Pole-mounted or pad-mounted
- High reliability requirements

### Industrial Applications

**1. Rectifier Transformers**
- Supply DC rectifier systems
- Special design for harmonic currents
- Aluminum smelters, steel mills
- Multiple secondary windings

**2. Furnace Transformers**
- Arc furnace applications
- High secondary current capability
- Frequent tap changing
- Robust mechanical design

**3. Traction Transformers**
- Railway applications
- 25 kV to 750/1500 V DC
- Compact design
- Special protection requirements

### Emerging Applications

**1. Renewable Energy**
- Wind farm collector transformers
- Solar farm step-up transformers
- Grid integration requirements
- Smart grid compatibility

**2. HVDC Systems**
- Converter transformers
- Special insulation requirements
- Harmonic considerations
- Valve winding design

## Conclusion

Transformers are fundamental components of electrical power systems, enabling efficient transmission and distribution of electrical energy. Understanding their principles, construction, testing, and maintenance is crucial for electrical engineers working in power systems.

**Key Takeaways**:
- Transformers operate on electromagnetic induction principles
- Proper testing and maintenance ensure reliable operation
- Different types serve specific applications
- Efficiency and regulation are key performance parameters
- Protection systems are essential for safe operation
- Modern monitoring techniques enable predictive maintenance

## Review Questions

1. Derive the EMF equation of a transformer and explain each term.
2. Explain the equivalent circuit of a transformer and draw the phasor diagram on load.
3. Describe the open circuit and short circuit tests of a transformer. How are the parameters determined?
4. What is voltage regulation? Derive the condition for maximum efficiency.
5. Explain the construction differences between core type and shell type transformers.
6. Discuss the parallel operation of transformers and conditions required.
7. Explain different types of losses in transformers and methods to minimize them.
8. Describe the protection schemes used for power transformers.
9. What is magnetizing inrush current? How does it affect transformer protection?
10. Explain the principle and applications of auto transformers.

## Numerical Problems

**Problem 1**: A 50 kVA, 2400/240 V transformer has the following test results:
- OC Test: 240 V, 5.41 A, 186 W
- SC Test: 75 V, 20.8 A, 810 W

Calculate: (a) Equivalent circuit parameters (b) Efficiency at full load, 0.8 pf lagging (c) Voltage regulation

**Problem 2**: Two transformers A and B are operated in parallel. A is rated 500 kVA with 5% impedance, B is rated 250 kVA with 4% impedance. If the total load is 600 kVA at 0.8 pf lagging, find the load shared by each transformer.

## Further Reading

- "Electrical Power Transformer Engineering" by James H. Harlow
- "Transformer Engineering: Design, Technology, and Diagnostics" by S.V. Kulkarni
- IEEE Standards C57 series for transformers
- IEC 60076 series for power transformers
- "Electric Machinery" by A.E. Fitzgerald
- Manufacturer technical guides and handbooks