# DC Circuit Analysis: Fundamentals and Methods

## Introduction

Direct Current (DC) circuit analysis forms the foundation of electrical engineering. In DC circuits, current flows in one direction and voltages are constant with time. Understanding DC circuits is essential before progressing to AC circuits and more complex electrical systems.

## Learning Objectives

By the end of this lecture, students will be able to:
- Apply Ohm's law and understand its limitations
- Use Kirchhoff's current and voltage laws to analyze circuits
- Apply various circuit analysis techniques (nodal, mesh, loop)
- Understand and apply network theorems (Thevenin, Norton, Superposition)
- Analyze circuits with dependent sources
- Calculate power and energy in DC circuits
- Understand maximum power transfer theorem
- Solve complex circuit problems using multiple methods

## Part 1: Basic DC Circuit Elements

### Voltage Sources

**Ideal Voltage Source**:
- Maintains constant voltage regardless of current
- Internal resistance = 0
- Can supply unlimited current (theoretically)

**Practical Voltage Source**:
- Has internal resistance (Rs)
- Terminal voltage varies with load current
- Vt = Vs - IsRs

**Independent vs Dependent Sources**:
- **Independent**: Fixed value, not controlled by other circuit variables
- **Dependent**: Value depends on voltage or current elsewhere in circuit

### Current Sources

**Ideal Current Source**:
- Maintains constant current regardless of voltage
- Internal resistance = ∞
- Can develop unlimited voltage (theoretically)

**Practical Current Source**:
- Has finite internal resistance (parallel)
- Output current varies with load voltage

### Resistors

**Ohm's Law**: V = IR
- V = Voltage (Volts)
- I = Current (Amperes)  
- R = Resistance (Ohms)

**Power in Resistors**:
```
P = VI = I²R = V²/R
```

**Temperature Coefficient**:
```
R(T) = R₀[1 + α(T - T₀)]
```
Where α = temperature coefficient

### Capacitors (DC Behavior)

**In DC steady state**: Acts as open circuit
**During transients**: i = C(dv/dt)
**Energy stored**: W = ½CV²

### Inductors (DC Behavior)

**In DC steady state**: Acts as short circuit
**During transients**: v = L(di/dt)  
**Energy stored**: W = ½LI²

## Part 2: Kirchhoff's Laws

### Kirchhoff's Current Law (KCL)

**Statement**: The algebraic sum of currents entering a node equals zero.
```
ΣI = 0
```

**Alternative statement**: Current entering = Current leaving

**Applications**:
- Node analysis
- Finding unknown currents
- Current divider circuits

**Sign Convention**:
- Currents entering node: Positive
- Currents leaving node: Negative

### Kirchhoff's Voltage Law (KVL)

**Statement**: The algebraic sum of voltage drops around any closed loop equals zero.
```
ΣV = 0
```

**Alternative statement**: Sum of voltage rises = Sum of voltage drops

**Applications**:
- Mesh analysis
- Loop analysis
- Finding unknown voltages

**Sign Convention**:
- Voltage drop: Positive (direction of assumed current)
- Voltage rise: Negative

### Examples of Kirchhoff's Laws

**Example 1 - KCL at a Node**:
If currents I₁ = 5A (entering), I₂ = 3A (entering), I₃ = ? (leaving)
Then: I₁ + I₂ - I₃ = 0
Therefore: I₃ = 8A

**Example 2 - KVL around a Loop**:
For a series circuit with voltage source Vs and resistors R₁, R₂, R₃:
Vs - IR₁ - IR₂ - IR₃ = 0

## Part 3: Series and Parallel Circuits

### Series Circuits

**Characteristics**:
- Same current through all elements
- Voltage divides among elements
- Total resistance = Sum of individual resistances

**Series Resistance**:
```
Rtotal = R₁ + R₂ + R₃ + ... + Rn
```

**Voltage Division**:
```
V₁ = Vs × (R₁/Rtotal)
V₂ = Vs × (R₂/Rtotal)
```

**Current Calculation**:
```
I = Vs/Rtotal
```

### Parallel Circuits

**Characteristics**:
- Same voltage across all elements
- Current divides among branches
- Total resistance less than smallest individual resistance

**Parallel Resistance**:
```
1/Rtotal = 1/R₁ + 1/R₂ + 1/R₃ + ... + 1/Rn
```

For two resistors:
```
Rtotal = (R₁ × R₂)/(R₁ + R₂)
```

**Current Division**:
```
I₁ = Is × (R₂/(R₁ + R₂))    [for two resistors]
I₂ = Is × (R₁/(R₁ + R₂))
```

**General current division**:
```
I₁ = Is × (Rtotal/R₁)
```

### Series-Parallel Combinations

**Analysis Steps**:
1. Identify series and parallel combinations
2. Simplify step by step
3. Work backwards to find individual values

**Delta-Wye Transformations**:

**Delta to Wye**:
```
R₁ = (RₐRc)/(Rₐ + Rb + Rc)
R₂ = (RₐRb)/(Rₐ + Rb + Rc)  
R₃ = (RbRc)/(Rₐ + Rb + Rc)
```

**Wye to Delta**:
```
Rₐ = (R₁R₂ + R₂R₃ + R₃R₁)/R₃
Rb = (R₁R₂ + R₂R₃ + R₃R₁)/R₁
Rc = (R₁R₂ + R₂R₃ + R₃R₁)/R₂
```

## Part 4: Circuit Analysis Methods

### Nodal Analysis

**Procedure**:
1. Select reference node (ground)
2. Assign node voltages (V₁, V₂, etc.)
3. Apply KCL at each non-reference node
4. Express currents in terms of node voltages
5. Solve simultaneous equations

**For node with voltage Vn**:
```
Σ(Vn - Vm)/Rmn = ΣIsources_connected_to_node
```

**Matrix Form**: [G][V] = [I]
Where [G] = conductance matrix

**Advantages**:
- Generally fewer equations than mesh analysis
- Systematic approach
- Easy to program

### Mesh Analysis

**Procedure**:
1. Identify independent meshes
2. Assign mesh currents (clockwise convention)
3. Apply KVL around each mesh
4. Express voltages in terms of mesh currents
5. Solve simultaneous equations

**For mesh with current Im**:
```
ΣRmn × In = ΣVsources_in_mesh
```

**Matrix Form**: [R][I] = [V]
Where [R] = resistance matrix

**Supermesh**: When current source is common to two meshes

### Loop Analysis

**Similar to mesh analysis but uses any set of independent loops**

**Steps**:
1. Select independent loops
2. Assign loop currents
3. Apply KVL to each loop
4. Solve equations

**Branch Current Method**:
1. Assign current to each branch
2. Apply KCL at nodes
3. Apply KVL to independent loops
4. Solve for branch currents

## Part 5: Network Theorems

### Superposition Theorem

**Statement**: In linear circuits with multiple sources, the response is the sum of responses due to each source acting alone.

**Procedure**:
1. Consider one source at a time
2. Replace other voltage sources with short circuits
3. Replace other current sources with open circuits
4. Calculate response due to active source
5. Repeat for all sources
6. Add all individual responses

**Limitations**:
- Applies only to linear circuits
- Cannot be used for power calculations directly
- Dependent sources remain active

### Thevenin's Theorem

**Statement**: Any linear two-terminal network can be replaced by an equivalent circuit consisting of a voltage source VTH in series with a resistance RTH.

**Finding Thevenin Equivalent**:

**Method 1 (Direct Method)**:
1. Find open-circuit voltage (VTH = Voc)
2. Find short-circuit current (Isc)
3. RTH = VTH/Isc

**Method 2 (Source Deactivation)**:
1. Find open-circuit voltage (VTH)
2. Deactivate all independent sources
3. Find equivalent resistance looking into terminals (RTH)

**Method 3 (Test Source Method)**:
1. Find VTH as above
2. Apply test voltage/current at terminals
3. Calculate RTH from test measurements

**Applications**:
- Simplifying complex networks
- Load analysis
- Maximum power transfer

### Norton's Theorem

**Statement**: Any linear two-terminal network can be replaced by an equivalent circuit consisting of a current source IN in parallel with a resistance RN.

**Finding Norton Equivalent**:
1. Find short-circuit current (IN = Isc)
2. Find equivalent resistance (RN = RTH)

**Thevenin-Norton Conversion**:
```
IN = VTH/RTH
RN = RTH
VTH = IN × RN
```

### Maximum Power Transfer Theorem

**Statement**: Maximum power is transferred to a load when the load resistance equals the source resistance.

**Condition**: RL = RS (for maximum power transfer)

**Maximum power**:
```
Pmax = VTH²/(4RTH)
```

**Efficiency at maximum power transfer**: η = 50%

**Applications**:
- Audio systems
- RF circuits
- Communication systems

### Reciprocity Theorem

**Statement**: In linear bilateral networks, the current at one point due to voltage at another point is the same as current at the second point when the same voltage is applied at the first point.

**Mathematically**: If voltage V at point A causes current I at point B, then voltage V at point B causes current I at point A.

### Millman's Theorem

**Used for circuits with multiple voltage sources in parallel**:
```
V = (V₁/R₁ + V₂/R₂ + ... + Vn/Rn)/(1/R₁ + 1/R₂ + ... + 1/Rn)
```

## Part 6: Dependent Sources

### Types of Dependent Sources

**Voltage-Controlled Voltage Source (VCVS)**:
```
V₂ = μV₁
```
μ = voltage gain (dimensionless)

**Current-Controlled Voltage Source (CCVS)**:
```
V₂ = rI₁
```
r = transresistance (Ohms)

**Voltage-Controlled Current Source (VCCS)**:
```
I₂ = gV₁
```
g = transconductance (Siemens)

**Current-Controlled Current Source (CCCS)**:
```
I₂ = βI₁
```
β = current gain (dimensionless)

### Analysis with Dependent Sources

**Key points**:
- Dependent sources are not deactivated during Thevenin/Norton analysis
- Controlling variable must be expressed in terms of circuit variables
- May require additional equations

**Modified nodal analysis**: Include controlling equations

## Part 7: Power and Energy in DC Circuits

### Power Calculations

**Basic power formula**: P = VI

**For resistors**:
```
P = I²R = V²/R = VI
```

**Power absorbed vs supplied**:
- **Absorbed**: Current enters positive terminal
- **Supplied**: Current leaves positive terminal

**Conservation of power**: Total power supplied = Total power absorbed

### Efficiency

**Definition**:
```
η = (Power delivered to load/Total power supplied) × 100%
```

**For circuits with source resistance**:
```
η = RL/(RS + RL) × 100%
```

### Energy Storage Elements

**Capacitors**:
```
Energy = ½CV²
```

**Inductors**:
```
Energy = ½LI²
```

## Part 8: Advanced DC Circuit Analysis

### Circuits with Operational Amplifiers

**Ideal Op-Amp assumptions**:
- Infinite input impedance
- Zero output impedance
- Infinite gain
- Zero input current
- Virtual short between inputs

**Analysis techniques**:
- Virtual short concept
- Current summing at inputs
- Feedback analysis

### Bridge Circuits

**Wheatstone Bridge**:
- Used for precise resistance measurement
- Balanced when R₁/R₂ = R₃/R₄
- Null detector shows balance condition

**Applications**:
- Resistance measurement
- Sensor circuits
- Precision measurements

### Nonlinear Elements

**Diodes**: Exponential I-V characteristic
**Analysis methods**:
- Graphical analysis
- Piecewise linear models
- Iterative techniques

## Part 9: Computer-Aided Analysis

### SPICE Simulation

**Basic elements**:
- Resistors: R
- Voltage sources: V
- Current sources: I

**Analysis types**:
- .OP: Operating point
- .DC: DC sweep
- .TRAN: Transient analysis

### Matrix Methods

**Nodal admittance matrix**:
```
[Y][V] = [I]
```

**Modified nodal analysis (MNA)**:
- Includes voltage sources directly
- Industry standard method

### Programming Approaches

**MATLAB/Python**:
- Matrix operations
- Symbolic analysis
- Graphical results

## Part 10: Practical Considerations

### Real Components

**Resistor tolerances**: ±1%, ±5%, ±10%
**Temperature effects**: Resistance varies with temperature
**Power ratings**: Must not exceed maximum dissipation
**Frequency effects**: Parasitic inductance and capacitance

### Measurement Techniques

**Multimeters**:
- Voltage measurement
- Current measurement
- Resistance measurement

**Loading effects**:
- Voltmeter loading
- Ammeter insertion resistance
- Measurement accuracy

### Safety Considerations

**Current effects on human body**:
- 1 mA: Barely perceptible
- 5 mA: Maximum safe current
- 10-20 mA: Muscular control lost
- 50+ mA: Ventricular fibrillation

**Voltage safety levels**:
- Below 50V: Generally safe
- Above 50V: Hazardous voltage

## Part 11: Problem-Solving Strategies

### Systematic Approach

1. **Identify the problem**: What is asked?
2. **Sketch the circuit**: Clear diagram with labels
3. **Choose analysis method**: Nodal, mesh, theorems
4. **Apply fundamental laws**: KVL, KCL, Ohm's law
5. **Solve equations**: Algebraic or matrix methods
6. **Check results**: Power balance, reasonable values

### Common Mistakes

- **Sign errors**: Consistent sign conventions
- **Unit errors**: Consistent units throughout
- **Calculation errors**: Double-check arithmetic
- **Conceptual errors**: Understanding of basic laws

### Verification Methods

- **Power balance check**: ΣP supplied = ΣP absorbed
- **Alternative method**: Solve using different technique
- **Limiting cases**: Check extreme values
- **Units check**: Dimensional analysis

## Part 12: Applications

### Power Systems

**DC transmission (HVDC)**:
- Long-distance transmission
- Underwater cables
- Grid interconnections

**Battery systems**:
- Energy storage
- Electric vehicles
- Backup power

### Electronic Circuits

**DC power supplies**:
- Voltage regulation
- Current limiting
- Filtering circuits

**Biasing circuits**:
- Transistor biasing
- Op-amp circuits
- Reference voltages

### Control Systems

**Sensor circuits**:
- Bridge configurations
- Signal conditioning
- Measurement systems

**Actuator circuits**:
- Motor drives
- Solenoid controls
- Relay circuits

## Conclusion

DC circuit analysis provides the fundamental tools for understanding all electrical circuits. The laws and theorems covered form the basis for more advanced topics in electrical engineering, including AC circuits, electronics, and power systems.

**Key Takeaways**:
- Ohm's law and Kirchhoff's laws are fundamental
- Multiple analysis methods are available for complex circuits
- Network theorems simplify analysis of complicated networks
- Power and energy calculations are essential for practical designs
- Computer tools enhance analysis capabilities
- Safety considerations are paramount in all electrical work

## Review Questions

1. State and explain Ohm's law. What are its limitations?
2. Explain Kirchhoff's current and voltage laws with examples.
3. Derive the voltage divider and current divider formulas.
4. Compare nodal analysis and mesh analysis methods.
5. Explain Thevenin's theorem and its applications.
6. What is the maximum power transfer theorem? When is it applicable?
7. How do dependent sources differ from independent sources?
8. Explain the superposition theorem and its limitations.
9. What is the difference between power and energy?
10. How do you analyze circuits with nonlinear elements?

## Numerical Problems

**Problem 1**: In the circuit below, find the current through each resistor using nodal analysis:
- Voltage source: 12V
- Resistors: R₁ = 4Ω, R₂ = 6Ω, R₃ = 3Ω
- Configuration: R₁ and R₂ in series, parallel with R₃, connected to voltage source

**Problem 2**: Find the Thevenin equivalent of a circuit containing:
- 10V voltage source in series with 2Ω resistor
- 5A current source in parallel with 4Ω resistor
- Both branches connected in parallel

**Problem 3**: A battery with internal resistance 0.5Ω supplies current to a variable load. If the terminal voltage is 11.5V when supplying 5A, find:
(a) EMF of the battery
(b) Load resistance for maximum power transfer
(c) Maximum power delivered to load

**Problem 4**: Using superposition theorem, find the current through 6Ω resistor in a circuit with:
- 12V voltage source
- 2A current source  
- Resistors: 3Ω, 6Ω, 4Ω in appropriate configuration

## Laboratory Exercises

1. **Ohm's Law Verification**: Measure V-I characteristics of resistors
2. **Series-Parallel Circuits**: Verify voltage and current division
3. **Kirchhoff's Laws**: Experimental verification in simple circuits
4. **Thevenin Equivalent**: Measure open-circuit voltage and short-circuit current
5. **Maximum Power Transfer**: Plot power vs load resistance
6. **Bridge Circuits**: Balance condition and sensitivity measurements
7. **Op-Amp Circuits**: Basic configurations and analysis
8. **Power Measurements**: Efficiency calculations in loaded circuits

## Further Reading

- "Fundamentals of Electric Circuits" by Alexander & Sadiku
- "Electric Circuits" by Nilsson & Riedel  
- "Engineering Circuit Analysis" by Hayt, Kemmerly & Durbin
- "Linear Circuit Analysis" by R.A. DeCarlo & P.M. Lin
- "Introduction to Electric Circuits" by Dorf & Svoboda
- IEEE Standards for electrical measurements
- SPICE circuit simulation tutorials
- National Electrical Code (NEC) for safety standards