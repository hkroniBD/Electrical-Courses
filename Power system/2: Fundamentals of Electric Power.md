# ⚡ Lecture 2: Fundamentals of Electric Power

### 👨‍🏫 Course Instructor
**Md. Hassanul Karim Roni**  
Assistant Professor, Department of Electrical and Electronic Engineering  
Hajee Mohammad Danesh Science and Technology University (HSTU)  
Dinajpur 5200, Bangladesh  
📞 01767052709  
✉️ hassanulkarim.roni@gmail.com

### 🎯 Learning Objectives
By the end of this lecture, students will be able to:
- Understand fundamental electrical concepts: voltage, current, power, and energy
- Differentiate between AC and DC systems and their applications
- Analyze single-phase and three-phase electrical systems
- Calculate power factor and understand its significance in power systems
- Apply three-phase system concepts to practical power system problems

---

## 1. 🔋 Basic Electrical Concepts

### 1.1 ⚡ Voltage (V)
**Definition**: Electric potential difference between two points in an electrical circuit

**Key Points**:
- **Unit**: Volt (V)
- **Symbol**: V or E
- **Physical meaning**: Work done per unit charge to move charge between two points
- **Mathematical expression**: V = W/Q (where W = work, Q = charge)

**In Bangladesh Power Systems**:
- Household voltage: 220V (single-phase)
- Industrial voltage: 380V (three-phase)
- Transmission voltages: 132kV, 230kV, 400kV

### 1.2 🔄 Current (I)
**Definition**: Rate of flow of electric charge through a conductor

**Key Points**:
- **Unit**: Ampere (A)
- **Symbol**: I
- **Physical meaning**: Amount of charge flowing per unit time
- **Mathematical expression**: I = Q/t (where Q = charge, t = time)

**Types**:
- **Direct Current (DC)**: Constant magnitude and direction
- **Alternating Current (AC)**: Magnitude and direction change periodically

### 1.3 ⚡ Power (P)
**Definition**: Rate of energy consumption or production

**Key Points**:
- **Unit**: Watt (W), Kilowatt (kW), Megawatt (MW)
- **Symbol**: P
- **Mathematical expressions**:
  - P = V × I (for DC circuits)
  - P = V × I × cos φ (for AC circuits, where φ is phase angle)
  - P = I²R = V²/R

**Power in Bangladesh Context**:
- Peak demand: ~15,500 MW
- Installed capacity: ~25,000 MW
- Per capita consumption: ~500 kWh/year

### 1.4 🔋 Energy (E)
**Definition**: Capacity to do work or amount of work done

**Key Points**:
- **Unit**: Joule (J), Kilowatt-hour (kWh)
- **Symbol**: E or W
- **Mathematical expression**: E = P × t (where P = power, t = time)
- **Relationship**: 1 kWh = 3.6 × 10⁶ J

---

## 2. 🔄 AC vs DC Systems

### 2.1 🔄 Alternating Current (AC) Systems

**Characteristics**:
- **Waveform**: Sinusoidal (typically)
- **Mathematical expression**: i(t) = I_m sin(ωt + φ)
- **Frequency**: 50 Hz (in Bangladesh), 60 Hz (in USA)
- **RMS Value**: I_rms = I_m/√2

**Advantages**:
- Easy voltage transformation using transformers
- Lower transmission losses at high voltages
- Simpler generation using rotating machines
- Better for long-distance transmission

**Applications**:
- Power generation and transmission
- Household and industrial supply
- Electric motors and appliances

### 2.2 🔋 Direct Current (DC) Systems

**Characteristics**:
- **Waveform**: Constant magnitude
- **Mathematical expression**: I = constant
- **No frequency concept**
- **No transformer operation**

**Advantages**:
- No reactive power issues
- Better for electronic devices
- Suitable for energy storage systems
- Lower losses in certain applications

**Applications**:
- Electronic devices
- Battery systems
- HVDC transmission
- Solar PV systems

### 2.3 🔄 Why AC Dominates Power Systems?

**Historical Reasons**:
- Tesla's polyphase system (1888)
- Easy voltage transformation
- Simpler generators and motors

**Technical Advantages**:
- Transformer operation enables voltage stepping
- Lower transmission losses at high voltages
- Easier synchronization of multiple generators
- Simpler protection and switching

---

## 3. 🔌 Single-Phase Systems

### 3.1 📊 Single-Phase AC Characteristics

**Basic Properties**:
- **Voltage**: v(t) = V_m sin(ωt)
- **Current**: i(t) = I_m sin(ωt - φ)
- **Power**: p(t) = v(t) × i(t)
- **Average Power**: P = V_rms × I_rms × cos φ

**Key Parameters**:
- **RMS Voltage**: V_rms = V_m/√2
- **RMS Current**: I_rms = I_m/√2
- **Phase Angle**: φ (between voltage and current)
- **Power Factor**: cos φ

### 3.2 🏠 Single-Phase Applications

**Residential Use**:
- Household appliances (220V in Bangladesh)
- Lighting systems
- Small motors (up to 3 HP typically)

**Limitations**:
- Power pulsation (varies with time)
- Lower efficiency for large loads
- Unbalanced magnetic fields in motors
- Limited power handling capacity

---

## 4. ⚡ Three-Phase Systems

### 4.1 🔄 Three-Phase Generation

**Principle**:
- Three separate windings displaced by 120° in space
- Three sinusoidal voltages 120° apart in time
- **Phase A**: v_a(t) = V_m sin(ωt)
- **Phase B**: v_b(t) = V_m sin(ωt - 120°)
- **Phase C**: v_c(t) = V_m sin(ωt - 240°)

**Advantages of Three-Phase Systems**:
1. **🔋 Constant Power**: Total instantaneous power is constant
2. **💰 Economic**: Less conductor material required
3. **⚙️ Better Motors**: Uniform torque, higher efficiency
4. **🔧 Easier Generation**: Balanced magnetic fields
5. **📊 Higher Power Density**: More power per unit weight

### 4.2 🌟 Balanced Three-Phase Systems

**Definition**: A three-phase system where:
- All phase voltages have equal magnitude
- Phase voltages are 120° apart
- Load impedances are equal in all phases

**Mathematical Properties**:
- **Voltage sum**: V_a + V_b + V_c = 0
- **Current sum**: I_a + I_b + I_c = 0
- **Power distribution**: Equal in all three phases

### 4.3 🔗 Three-Phase Connections

#### 4.3.1 ⭐ Star (Y) Connection

**Configuration**:
- Three phase windings connected to a common neutral point
- Four-wire system (3 phases + 1 neutral)
- Used in generation and distribution

**Key Relationships**:
- **Line Voltage**: V_L = √3 × V_ph
- **Line Current**: I_L = I_ph
- **Line voltages lead phase voltages by 30°**

**Applications in Bangladesh**:
- Generator connections at power plants
- Distribution transformers (11kV/0.4kV)
- Industrial three-phase supply (380V line-to-line)

#### 4.3.2 🔺 Delta (Δ) Connection

**Configuration**:
- Phase windings connected in a closed loop
- Three-wire system (no neutral)
- Common in motor connections

**Key Relationships**:
- **Line Voltage**: V_L = V_ph
- **Line Current**: I_L = √3 × I_ph
- **Line currents lag phase currents by 30°**

**Applications**:
- Transmission line configurations
- Large motor connections
- Some transformer configurations

### 4.4 📊 Phase and Line Quantities

#### In Star Connection:
| Quantity | Relationship |
|----------|-------------|
| **⚡ Voltage** | V_L = √3 × V_ph |
| **🔄 Current** | I_L = I_ph |
| **🔋 Power** | P = √3 × V_L × I_L × cos φ |

#### In Delta Connection:
| Quantity | Relationship |
|----------|-------------|
| **⚡ Voltage** | V_L = V_ph |
| **🔄 Current** | I_L = √3 × I_ph |
| **🔋 Power** | P = √3 × V_L × I_L × cos φ |

---

## 5. 📊 Power Factor and Its Significance

### 5.1 📐 Power Factor Definition

**Power Factor (PF)**: Cosine of the phase angle between voltage and current
- **Mathematical expression**: PF = cos φ
- **Range**: 0 to 1 (or 0% to 100%)
- **Types**: Leading, lagging, unity

### 5.2 ⚡ Types of Power in AC Systems

#### 5.2.1 🔋 Active Power (P)
- **Definition**: Actual power consumed or produced
- **Unit**: Watt (W), Kilowatt (kW), Megawatt (MW)
- **Formula**: P = V × I × cos φ
- **Physical meaning**: Power that does useful work

#### 5.2.2 🔄 Reactive Power (Q)
- **Definition**: Power that oscillates between source and load
- **Unit**: VAR (Volt-Ampere Reactive), kVAR, MVAR
- **Formula**: Q = V × I × sin φ
- **Physical meaning**: Power required for magnetic/electric fields

#### 5.2.3 ⚡ Apparent Power (S)
- **Definition**: Total power in AC circuit
- **Unit**: VA (Volt-Ampere), kVA, MVA
- **Formula**: S = V × I
- **Relationship**: S² = P² + Q²

### 5.3 📊 Power Triangle

```
    S (Apparent Power)
    |\
    | \
    |  \
 Q  |   \ 
    |    \
    |φ    \
    |______\
        P (Active Power)
```

**Relationships**:
- **Power Factor**: cos φ = P/S
- **Reactive Factor**: sin φ = Q/S
- **Power Triangle**: S² = P² + Q²

### 5.4 🎯 Importance of Power Factor

#### 5.4.1 💰 Economic Impact
- **Higher Current**: Low PF → Higher current for same power
- **Increased Losses**: I²R losses in transmission/distribution
- **Larger Equipment**: Transformers, cables, switchgear
- **Penalty Charges**: Utilities charge for low power factor

#### 5.4.2 🔧 Technical Impact
- **Voltage Drop**: Higher current causes more voltage drop
- **System Capacity**: Reduces system power-carrying capacity
- **Generator Loading**: Generators must supply reactive power
- **Stability Issues**: Can affect system voltage stability

### 5.5 🏭 Power Factor in Bangladesh Industries

**Typical Power Factors**:
- **Resistive loads** (heaters): PF = 1.0
- **Incandescent lighting**: PF = 1.0
- **Fluorescent lighting**: PF = 0.5-0.6
- **Induction motors** (loaded): PF = 0.8-0.9
- **Induction motors** (no-load): PF = 0.2-0.3
- **Welding equipment**: PF = 0.5-0.7

**Bangladesh Regulations**:
- Industrial consumers: Maintain PF ≥ 0.85
- Penalty for PF < 0.85
- Incentives for PF > 0.95

### 5.6 🔧 Power Factor Improvement

#### Methods:
1. **🔋 Capacitor Banks**: Most common method
2. **🔄 Synchronous Motors**: Over-excited operation
3. **⚡ Static VAR Compensators**: Advanced control
4. **🔧 Equipment Replacement**: High-efficiency motors

#### Benefits:
- Reduced electricity bills
- Lower transmission losses
- Improved voltage regulation
- Increased system capacity
- Better equipment utilization

---

## 6. 🧮 Practical Calculations

### 6.1 📊 Three-Phase Power Calculations

#### For Balanced Systems:
**Active Power**: P = √3 × V_L × I_L × cos φ
**Reactive Power**: Q = √3 × V_L × I_L × sin φ
**Apparent Power**: S = √3 × V_L × I_L

#### Example Problem:
A three-phase motor operates at:
- Line voltage: 380V
- Line current: 50A  
- Power factor: 0.8 lagging

**Calculate**:
- **Active Power**: P = √3 × 380 × 50 × 0.8 = 26.3 kW
- **Reactive Power**: Q = √3 × 380 × 50 × 0.6 = 19.7 kVAR
- **Apparent Power**: S = √3 × 380 × 50 = 32.9 kVA

### 6.2 🔄 Power Factor Correction Example

**Problem**: A factory has a load of 100 kW at 0.7 power factor lagging. Calculate the capacitor size needed to improve power factor to 0.9.

**Solution**:
- **Initial Q₁**: Q₁ = P × tan(cos⁻¹(0.7)) = 100 × 1.02 = 102 kVAR
- **Final Q₂**: Q₂ = P × tan(cos⁻¹(0.9)) = 100 × 0.484 = 48.4 kVAR
- **Capacitor Size**: Q_c = Q₁ - Q₂ = 102 - 48.4 = 53.6 kVAR

---

## 7. 🏭 Applications in Bangladesh Power Systems

### 7.1 ⚡ Generation Level
- **Three-phase generators** in all power plants
- **Typical voltage**: 11kV (generator terminal voltage)
- **Power factor control** through excitation systems
- **Synchronization** of multiple generators

### 7.2 🔌 Transmission Level
- **Three-phase transmission** at 132kV, 230kV, 400kV
- **Power factor** affects transmission capacity
- **Reactive power management** through:
  - Shunt capacitors/reactors
  - Static VAR compensators
  - Synchronous condensers

### 7.3 🏠 Distribution Level
- **Three-phase primary distribution**: 33kV, 11kV
- **Single-phase secondary**: 220V for residential
- **Three-phase secondary**: 380V for commercial/industrial
- **Power factor improvement** mandatory for large consumers

### 7.4 🏭 Industrial Applications
- **Textile industry**: Large induction motors
- **Steel industry**: Arc furnaces (low power factor)
- **Cement industry**: High power factor requirements
- **Pharmaceutical**: Clean power requirements

---

## 📝 Summary

**🔑 Key takeaways:**

1. **Basic electrical concepts** (voltage, current, power, energy) form the foundation of power system analysis
2. **AC systems dominate** power systems due to easy voltage transformation and efficient transmission
3. **Three-phase systems** offer significant advantages over single-phase systems in terms of economy, efficiency, and performance
4. **Star and Delta connections** have specific applications with different voltage-current relationships
5. **Power factor** is crucial for economic and efficient operation of power systems
6. **Power factor improvement** is essential for industrial consumers and system efficiency

**Practical Applications:**
- Understanding these fundamentals is essential for power system design and operation
- Power factor management is critical for economic operation
- Three-phase calculations are fundamental for power system analysis
- Knowledge of AC/DC systems helps in understanding modern power electronics applications

---

## 📝 Quiz Questions

### 🔤 Multiple Choice Questions (MCQ)

**1. In a balanced three-phase star-connected system, the relationship between line and phase voltage is:**
a) V_L = V_ph
b) V_L = √3 × V_ph  
c) V_L = 3 × V_ph
d) V_L = V_ph/√3

**2. The power factor of a purely resistive load is:**
a) 0
b) 0.5
c) 0.707
d) 1.0

**3. In Bangladesh, the standard frequency for AC power systems is:**
a) 50 Hz
b) 60 Hz
c) 25 Hz
d) 100 Hz

**4. The unit of reactive power is:**
a) Watt (W)
b) Volt-Ampere (VA)
c) VAR
d) Joule (J)

**5. In a delta-connected system, the relationship between line and phase current is:**
a) I_L = I_ph
b) I_L = √3 × I_ph
c) I_L = 3 × I_ph
d) I_L = I_ph/√3

**6. The RMS value of a sinusoidal AC voltage with peak value V_m is:**
a) V_m
b) V_m/2
c) V_m/√2
d) V_m/√3

**7. Low power factor results in:**
a) Lower current for same power
b) Higher current for same power
c) No change in current
d) Lower voltage drop

**8. The standard household voltage in Bangladesh is:**
a) 110V
b) 220V
c) 380V
d) 440V

### ✏️ Short Answer Questions

**9. Define power factor and explain its significance in power systems.**

**10. List three advantages of three-phase systems over single-phase systems.**

**11. What is the relationship between active power, reactive power, and apparent power?**

**12. Why is AC preferred over DC for power transmission?**

### 🧠 Analytical Questions

**13. A three-phase motor draws 30A line current at 380V line voltage with a power factor of 0.85 lagging. Calculate the active power, reactive power, and apparent power consumed by the motor.**

**14. Explain why power factor correction is economically beneficial for industrial consumers in Bangladesh.**

**15. Compare star and delta connections in terms of voltage, current relationships, and typical applications.**

---

## ✅ Quiz Solutions

### 🔤 MCQ Answers
1. **b) V_L = √3 × V_ph** - Standard relationship in star connection
2. **d) 1.0** - No phase difference between voltage and current in resistive loads
3. **a) 50 Hz** - Standard frequency in Bangladesh and most countries
4. **c) VAR** - Volt-Ampere Reactive is the unit of reactive power
5. **b) I_L = √3 × I_ph** - Standard relationship in delta connection
6. **c) V_m/√2** - RMS value relationship for sinusoidal waveforms
7. **b) Higher current for same power** - I = P/(V×cos φ), lower cos φ means higher I
8. **b) 220V** - Standard single-phase household voltage in Bangladesh

### ✏️ Short Answer Solutions

**9. Power factor definition and significance:**
Power factor is the cosine of the phase angle between voltage and current (cos φ). Its significance includes: economic impact (higher current and losses with low PF), equipment sizing requirements, utility penalty charges, and system capacity limitations.

**10. Three advantages of three-phase systems:**
- Constant instantaneous power (no pulsation)
- More economical (less conductor material required)
- Better motor performance (uniform torque, higher efficiency)

**11. Power relationship:**
S² = P² + Q², where S is apparent power, P is active power, and Q is reactive power. This forms the power triangle with power factor cos φ = P/S.

**12. AC preferred over DC:**
AC allows easy voltage transformation using transformers, enabling high-voltage transmission with lower losses. AC generators are simpler to construct and multiple AC sources can be easily synchronized.

### 🧠 Analytical Solutions

**13. Three-phase motor calculation:**
Given: I_L = 30A, V_L = 380V, cos φ = 0.85
- Active Power: P = √3 × 380 × 30 × 0.85 = 16.8 kW
- sin φ = √(1 - 0.85²) = 0.527
- Reactive Power: Q = √3 × 380 × 30 × 0.527 = 10.4 kVAR  
- Apparent Power: S = √3 × 380 × 30 = 19.8 kVA

**14. Economic benefits of power factor correction:**
- Reduced electricity bills due to lower kVA demand charges
- Elimination of power factor penalty charges
- Lower transmission losses (I²R losses reduce with lower current)
- Increased system capacity utilization
- Reduced voltage drop and improved equipment performance

**15. Star vs Delta comparison:**

| Parameter | Star Connection | Delta Connection |
|-----------|----------------|------------------|
| **Voltage** | V_L = √3 × V_ph | V_L = V_ph |
| **Current** | I_L = I_ph | I_L = √3 × I_ph |
| **Neutral** | Available | Not available |
| **Applications** | Generation, Distribution | Transmission, Motors |
| **Starting** | Lower starting current | Higher starting current |
| **Fault Current** | Lower | Higher |

---

## 👀 Next Lecture Preview
**⚡ Lecture 3**: Power Generation Technologies
- 🏭 Types of power plants: thermal, hydro, nuclear, renewable
- ⚙️ Working principles of different generators
- 🌍 Efficiency and environmental considerations
- 🔋 Renewable energy integration challenges
