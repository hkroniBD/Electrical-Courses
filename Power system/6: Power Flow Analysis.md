# Lecture 6: Power Flow Analysis in Electrical Networks

**Course Instructor** 📚  
- 👨‍🏫 Md. Hassanul Karim Roni  
- 🏫 Assistant Professor, EEE, HSTU, Dinajpur, BD  
- ✉️ [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com)  
- 📞 01767052709 (WhatsApp)  

---

## Objective  
Understand the essentials of power flow analysis, classify bus types (PQ, PV, Slack), and apply the per-unit system to simplify calculations, with a focus on load flow studies for efficient planning and operation of the power grid in Bangladesh.

---

## Ice-Breaker: Fun Facts to Spark Curiosity 🌟  
- **River Flow Analogy** 🌊: Think of power flow as water moving through rivers in Bangladesh—voltage is the water level, and current is the flow rate, guiding power from Bhola to Bogra!  
- **Grid’s Hidden Dance** 💃: Electricity moves at near-light speed, but power flow patterns are like choreographed traffic on Dhaka’s highways—some lines carry heavy loads, others stay light!  
- **Slack Bus Superpower** 🦸: The slack bus is the grid’s unsung hero, balancing power mismatches to keep the system stable, like a conductor leading an orchestra.  
- **Per-Unit Magic** 🪄: The per-unit system turns a complex 230 kV grid into simple “1.0” values, making calculations as easy as summing apples and oranges!  

---

## 1. Concept of Power Flow in Networks 🔄  

Power flow analysis determines the steady-state behavior of electrical networks by calculating voltage magnitudes, phase angles, and power flows across buses and lines.

### Key Principles  
- **Power Balance**: Generated power equals consumed power plus losses at each bus.  
- **Kirchhoff’s Laws**: Govern current and voltage relationships in the network.  
- **AC Power Flow**: Active (P) and reactive (Q) power flow based on voltage differences and impedances.  

### Key Variables  
- **Voltage Magnitude (|V|)**: Drives reactive power flow.  
- **Voltage Angle (δ)**: Drives active power flow.  
- **Active Power (P)**: Measured in MW, powers loads.  
- **Reactive Power (Q)**: Measured in MVAR, supports voltage stability.  

### In Bangladesh  
Power flow studies are critical for PGCB to manage peak loads in Dhaka and Chittagong, ensuring stable voltage in Sylhet and preventing overloads in Ashuganj-Mymensingh lines.

---

## 2. Bus Types in Power Systems 🚌  

Buses are classified based on known and unknown quantities, forming the backbone of load flow analysis.

### Summary of Bus Types  

| Bus Type     | Known Variables | Unknown Variables | Typical Applications         | In Bangladesh                 |
|--------------|-----------------|-------------------|-----------------------------|-------------------------------|
| **PQ Bus**   | P, Q            | \|V\|, δ          | Load centers, substations   | Khulna 132 kV substation      |
| **PV Bus**   | P, \|V\|        | Q, δ              | Generators, power plants    | Barapukuria power station     |
| **Slack Bus**| \|V\|, δ        | P, Q              | Reference bus, grid anchor  | Dhaka East 230 kV substation  |

### 2.1 PQ Bus (Load Bus) 📊  
- **Known**: Active power (P) and reactive power (Q) demand.  
- **Unknown**: Voltage magnitude (|V|) and angle (δ).  
- **Role**: Represents load centers like cities or industries.  
- **In Bangladesh**: A Rajshahi substation with 60 MW and 40 MVAR demand is a PQ bus, with voltage determined by system conditions.  

### 2.2 PV Bus (Generator Bus) ⚡  
- **Known**: Active power (P) and voltage magnitude (|V|).  
- **Unknown**: Reactive power (Q) and angle (δ).  
- **Role**: Represents generators with voltage control.  
- **In Bangladesh**: Ghorashal power plant generating 150 MW at 1.03 pu voltage adjusts reactive power to maintain voltage stability.  

### 2.3 Slack Bus (Reference Bus) 🎯  
- **Known**: Voltage magnitude (|V|) and angle (δ = 0°).  
- **Unknown**: Active power (P) and reactive power (Q).  
- **Role**: Balances system losses and power mismatches; only one per system.  
- **In Bangladesh**: Dhaka East 230 kV substation, set at 1.0 pu voltage, adjusts P and Q to stabilize the grid.  

---

## 3. Theoretical Foundations of Load Flow Studies 📐  

Load flow studies solve nonlinear equations to model steady-state power system operation.

### Power Flow Equations (Simplified)  
For bus *i* connected to *n* buses:  
- **Active Power**: Balances real power based on voltage angles.  
- **Reactive Power**: Balances reactive power based on voltage magnitudes.  
- **Admittance Matrix**: Uses conductance (G) and susceptance (B) to model network connections.  

### Solution Methods  
- **Gauss-Seidel**: Simple, iterative, but slow for large grids.  
- **Newton-Raphson**: Fast, accurate, widely used by PGCB in PSS/E software.  
- **Fast-Decoupled**: Efficient for large systems, ideal for the grid in Bangladesh.  

### System Constraints  
- For *n* buses, there are *2n* unknowns (P, Q, |V|, δ).  
- PQ and PV buses provide known values; the slack bus resolves the rest.  
- **Convergence Criteria**: Power mismatch < 0.01 pu; voltages within 0.95–1.05 pu.  

---

## 4. Per-Unit System: Simplifying Analysis 📏  

The per-unit system normalizes electrical quantities to dimensionless values, simplifying calculations across the multi-voltage grid in Bangladesh.

### 4.1 Base Quantities  
- **Base Power (Sbase)**: Typically 100 MVA.  
- **Base Voltage (Vbase)**: Nominal voltage, e.g., 230 kV or 132 kV.  
- **Derived**:  
  - Base Current: $I_{base} = \frac{S_{base}}{\sqrt{3} V_{base}}$  
  - Base Impedance: $Z_{base} = \frac{V_{base}^2}{S_{base}}$  

### 4.2 Per-Unit Calculations  
$\text{Per-unit value} = \frac{\text{Actual value}}{\text{Base value}}$  

**Example**:  
A 230 kV line with 35 Ω impedance:  
- $Z_{base} = \frac{(230×10^3)^2}{100×10^6} = 529 \, \Omega$  
- $Z_{pu} = \frac{35}{529} = 0.0662 \, \text{p.u.}$  

### 4.3 Advantages of Per-Unit  
- Simplifies calculations by eliminating voltage ratios.  
- Standardizes analysis across 132 kV, 230 kV, and 400 kV systems.  
- Reduces errors in three-phase calculations.  
- Enables direct comparison of equipment ratings.  

### 4.4 Change of Base  
When components use different bases:  
$Z_{pu,new} = Z_{pu,old} \times \frac{S_{base,new}}{S_{base,old}} \times \left(\frac{V_{base,old}}{V_{base,new}}\right)^2$  
**Example**: A 0.1 pu impedance on 25 MVA, 132 kV base converts to 100 MVA, 132 kV:  
$Z_{pu,new} = 0.1 \times \frac{100}{25} = 0.4 \, \text{p.u.}$  

---

## 5. Load Flow Study Procedure 🔄  

### Steps for Analysis  
1. **Collect Data**: Line impedances, bus loads, and generation data.  
2. **Classify Buses**: Identify PQ, PV, and slack buses.  
3. **Convert to Per-Unit**: Use common base (e.g., 100 MVA).  
4. **Form Y-Bus Matrix**: Model network topology.  
5. **Set Initial Conditions**: Assume flat start (1.0 pu, 0° for unknowns).  
6. **Solve Iteratively**: Use Newton-Raphson for fast convergence.  
7. **Analyze Results**: Check voltages, line flows, and losses.  

### In Bangladesh  
- **Load Dispatch**: Optimizes power from Sirajganj to Dhaka during peak hours.  
- **Voltage Regulation**: Uses capacitors at Comilla to maintain stable voltages.  
- **Contingency Planning**: Simulates outages (e.g., 230 kV Bogra-Barisal line) to ensure grid stability.  

---

## 6. Key Takeaways 📝  
- Power flow analysis ensures stable voltage and power distribution in the grid in Bangladesh.  
- PQ buses represent loads, PV buses represent generators, and the slack bus balances the system.  
- Per-unit system simplifies calculations across 132 kV, 230 kV, and 400 kV levels.  
- Newton-Raphson is the go-to method for fast, accurate load flow solutions.  
- Load flow studies are critical for PGCB to manage peak loads and plan grid expansion.  

---

## References 📚  
- Grainger, J. J., & Stevenson, W. D. (1994). *Power System Analysis*. McGraw-Hill.  
- Glover, J. D., Sarma, M. S., & Overbye, T. J. (2017). *Power System Analysis and Design*. Cengage.  
- Saadat, H. (2010). *Power System Analysis*. McGraw-Hill.  
- PGCB Load Flow Reports and PSS/E Manuals.  
- IEEE Std 399-1997, *Recommended Practice for Power Systems Analysis*.  

---

## Objective Viva Questions ❓  
1. **Which bus type has fixed voltage magnitude and angle?**  
   a) PQ Bus  
   b) PV Bus  
   c) Slack Bus  
   d) Load Bus  

2. **What is the base impedance for Sbase = 100 MVA, Vbase = 230 kV?**  
   a) 529 Ω  
   b) 230 Ω  
   c) 100 Ω  
   d) 23 Ω  

3. **Why is Newton-Raphson preferred for load flow studies?**  
   a) Simpler implementation  
   b) Faster convergence  
   c) Less accurate  
   d) Requires fewer inputs  

4. **Which quantities are unknown for a PV bus?**  
   a) P and Q  
   b) |V| and δ  
   c) Q and δ  
   d) P and |V|  

5. **What does a flat start assume in load flow studies?**  
   a) All voltages are zero  
   b) All voltages are 1.0 pu at 0°  
   c) All powers are equal  
   d) All angles are 90°  

---

## Solutions to Viva Questions ✅  
1. **c) Slack Bus**  
   *Explanation*: The slack bus has fixed |V| and δ to balance system losses.  

2. **a) 529 Ω**  
   *Explanation*: $Z_{base} = \frac{(230×10^3)^2}{100×10^6} = 529 \, \Omega$.  

3. **b) Faster convergence**  
   *Explanation*: Newton-Raphson converges in 3–5 iterations, unlike Gauss-Seidel’s 10–50.  

4. **c) Q and δ**  
   *Explanation*: PV bus has known P and |V|, with Q and δ calculated.  

5. **b) All voltages are 1.0 pu at 0°**  
   *Explanation*: Flat start assumes 1.0 pu voltage and 0° angle for unknown buses.
