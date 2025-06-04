# Lecture 6: Power Flow Analysis

**Course Instructor** 📚

* 👨‍🏫 Md. Hassanul Karim Roni
* 🏫 Assistant Professor, EEE, HSTU, Dinajpur, BD
* ✉️ [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com)
* 📞 01767052709 (WhatsApp)

---

## Objective

Understand how electrical power flows in transmission networks using mathematical models, recognize bus classifications (PQ, PV, Slack), apply per-unit (p.u.) systems to simplify calculations, and establish the theoretical basis of load flow studies crucial for planning, operation, and control of Bangladesh’s national grid.

---

## Ice-Breaker: Fun Facts to Spark Curiosity 🌟

* **Invisible Conductor Negotiations** ⚡: At every moment, power in our grid is adjusting itself like a negotiation among buses—some control voltage, others control power!
* **Slack Bus Magic** 🧙: Without a slack bus, your power flow equations become unsolvable—it's like trying to balance a seesaw with both ends fixed!
* **Per-Unit Trickery** 🎩: The per-unit system transforms messy multi-unit equations into clean, dimensionless expressions. A 132 kV system becomes just “1.0”!
* **Grid Harmony** 🎼: Load flow studies ensure that voltage, phase, and power remain in sync across the vast transmission network—just like conducting an orchestra.

---

## 1. Concept of Power Flow in Electrical Networks 🔁

### What is Power Flow?

Power flow (or load flow) refers to the study of how active (P) and reactive (Q) power moves across a network of buses through transmission lines.

### Key Objectives of Power Flow Studies

* Determine voltage magnitude and phase at each bus
* Calculate active and reactive power flow on transmission lines
* Ensure voltage and power limits are within safe bounds
* Design efficient operation strategies, e.g., load dispatch or voltage regulation

### Bangladesh Context 🇧🇩

PGCB performs routine load flow studies to manage peak loads in Dhaka-Chittagong and North-West corridors. Faulty power flow may lead to undervoltage in Rajshahi or overload in Meghnaghat lines.

---

## 2. Bus Types in Power System 🚌

### 1. **PQ Bus (Load Bus)**

* **Known**: Active power demand $P$, reactive power demand $Q$
* **Unknown**: Voltage magnitude $|V|$, phase angle $\delta$
* **Common Usage**: Consumer substations, residential feeders
* **Example**: Rajshahi 132 kV substation

### 2. **PV Bus (Generator Bus)**

* **Known**: Active power generation $P$, voltage magnitude $|V|$
* **Unknown**: Reactive power $Q$, phase angle $\delta$
* **Common Usage**: Grid-connected generators
* **Example**: Ghorashal power station

### 3. **Slack Bus (Swing Bus)**

* **Known**: Voltage magnitude $|V|$, phase angle $\delta = 0°$
* **Unknown**: Active $P$ and reactive $Q$ generated
* **Purpose**: Balances active/reactive losses in system
* **Common Usage**: Reference or anchor bus for system solution
* **Example**: PGCB Dhaka East 230 kV substation

---

## 3. Theoretical Foundations of Load Flow Studies 🧠

### Governing Equations (in Polar Form):

For bus *i*,

* **Active Power**:
  $P_i = \sum_{j=1}^{n} |V_i||V_j|(G_{ij} \cos\theta_{ij} + B_{ij} \sin\theta_{ij})$
* **Reactive Power**:
  $Q_i = \sum_{j=1}^{n} |V_i||V_j|(G_{ij} \sin\theta_{ij} - B_{ij} \cos\theta_{ij})$
  Where:
* $G_{ij}, B_{ij}$: Real and imaginary parts of admittance
* $\theta_{ij} = \delta_i - \delta_j$: Phase angle difference

### Number of Unknowns and Equations

* **n buses → 2n unknowns** (|V|, δ at each bus)
* Slack bus provides reference; other buses follow PQ or PV conditions

### Iterative Techniques for Solving

* **Gauss-Seidel**: Simple but slow
* **Newton-Raphson**: Fast and accurate (used in PGCB/PSSE)
* **Fast-Decoupled Load Flow**: Memory efficient, used in large networks

---

## 4. Per-Unit System for Simplified Analysis 🔄

### Why Use Per-Unit (p.u.) System?

* Normalizes voltage, current, power, and impedance
* Eliminates unit conversion
* Enables easier comparison between components of different ratings

### Base Quantities

1. **Base Power (Sbase)**: Typically 100 MVA
2. **Base Voltage (Vbase)**: Line-to-line RMS voltage
3. **Derived Quantities**:

   * Current: $I_{base} = \frac{S_{base}}{\sqrt{3} V_{base}}$
   * Impedance: $Z_{base} = \frac{V_{base}^2}{S_{base}}$
   * Admittance: $Y_{base} = \frac{1}{Z_{base}}$

### Per-Unit Value Formula

$\text{p.u. value} = \frac{\text{Actual value}}{\text{Base value}}$

### Example

A 230 kV line has impedance of 30 Ω:

* $Z_{base} = \frac{(230×10^3)^2}{100×10^6} = 529 \, \Omega$
* $Z_{pu} = \frac{30}{529} = 0.0567 \, \text{p.u.}$

---

## 5. Practical Applications in Bangladesh 🇧🇩

### Load Dispatch Optimization

* Power flow results help PGCB decide economic dispatch from multiple plants (e.g., Sirajganj vs. Meghnaghat)

### Voltage Regulation

* Voltage profiles are adjusted via tap-changing transformers or reactive power compensation at key buses (e.g., Comilla, Rangpur)

### Contingency Analysis

* Simulates line outage scenarios (e.g., 230 kV Bogra-Bheramara failure) to ensure system stability under fault conditions

---

## 6. Key Takeaways 📝

* Power flow analysis reveals how voltage and power vary across the grid
* Bus types determine known/unknown variables in power flow equations
* The slack bus balances the system, acting as a mathematical anchor
* Per-unit system simplifies large-scale, multi-voltage level calculations
* Load flow tools like Newton-Raphson method and PSSE are standard in PGCB

---

## References 📚

* Stevenson, W. D., & Grainger, J. J. (1994). *Power System Analysis*. McGraw-Hill.
* Glover, J. D., Sarma, M. S., & Overbye, T. J. (2017). *Power System Analysis and Design*. Cengage.
* Bergen, A. R., & Vittal, V. (2000). *Power Systems Analysis*. Prentice Hall.
* PGCB Reports and PSSE Load Flow Manuals
* IEEE Std 399-1997, *IEEE Recommended Practice for Industrial and Commercial Power Systems Analysis*

---

## Objective Viva Questions ❓

1. **Which of the following is NOT a bus type in power flow analysis?**
   a) PQ Bus
   b) PV Bus
   c) Z Bus
   d) Slack Bus

2. **The slack bus is needed in power flow analysis to:**
   a) Provide voltage support
   b) Control frequency
   c) Balance system losses
   d) Supply reactive power

3. **Which variable is always known for a PV bus?**
   a) Reactive power Q
   b) Voltage phase angle
   c) Voltage magnitude
   d) Complex power

4. **In per-unit system, what is the base impedance if Vbase = 132 kV and Sbase = 100 MVA?**
   a) 1.32 Ω
   b) 174.24 Ω
   c) 100 Ω
   d) 2.25 Ω

5. **Which method is most commonly used in large-scale load flow studies due to its accuracy and robustness?**
   a) Gauss-Seidel
   b) Newton-Raphson
   c) Crout Method
   d) Gradient Descent

---

## Solutions to Viva Questions ✅

1. **c) Z Bus**
   *Explanation*: Only PQ, PV, and Slack buses are standard classifications.

2. **c) Balance system losses**
   *Explanation*: Slack bus absorbs mismatch in power flow solution.

3. **c) Voltage magnitude**
   *Explanation*: PV bus has fixed voltage magnitude and active power.

4. **b) 174.24 Ω**
   *Explanation*:
   $Z_{base} = \frac{(132×10^3)^2}{100×10^6} = 174.24 \, \Omega$

5. **b) Newton-Raphson**
   *Explanation*: Offers fast convergence and high accuracy in nonlinear power flow problems.

---
