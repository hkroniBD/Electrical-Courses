# 🎓 Lecture 11: Power System Stability – Concepts & Theoretical Foundations

**Course Title:** Theoretical Electrical Power Systems
**Instructor:** HK Roni Sir, Assistant Professor, EEE, HSTU
✉️ [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com) | ☎️ 01767052709 (WhatsApp)

---

## ❄️ Ice-Breaker: Power Systems Can “Swing”! ⚖️🌀

🔄 Ever wondered what happens when two generators go slightly out of sync? Their **rotors swing**—like a seesaw—trying to match phase. If not controlled, this swing can throw the entire system into instability!

💥 In 2003, a chain reaction in the US power grid—triggered by instability—left **50 million people without electricity**. That’s the **power of stability** (or the lack of it)!

---

## 📘 What is Power System Stability?

Power system stability refers to the **ability of the power grid to return to normal operation after a disturbance** like a fault, sudden load change, or loss of a generator.

💡 It’s about maintaining:

* **Synchronism** among generators
* **Voltage levels** within safe limits
* **Controlled power flow**

---

## 🧭 Types of Power System Stability

| Stability Type         | Focus Area               | Typical Time Scale         | Concerned With                         |
| ---------------------- | ------------------------ | -------------------------- | -------------------------------------- |
| Transient Stability    | Rotor angle (mechanical) | Seconds (0–10s)            | Large disturbances (faults, switching) |
| Dynamic Stability      | Rotor + system dynamics  | Several seconds to minutes | Small disturbances over time           |
| Steady-State Stability | Continuous operation     | Long-term (min–hrs)        | Small gradual load changes             |

---

## 🔄 Rotor Angle Stability

This deals with the **mechanical dynamics** of the rotor and whether generators stay in synchronism.

⚙️ **Swing Equation:**

$$
M \frac{d^2\delta}{dt^2} = P_m - P_e
$$

Where:

* $\delta$: Rotor angle
* $P_m$: Mechanical input power
* $P_e$: Electrical output power
* $M$: Inertia constant

💬 When power mismatch causes the rotor angle to change too fast, synchronism is lost.

---

## ⚖️ Equal Area Criterion (For Transient Stability)

A quick visual method to determine if the system will remain stable after a disturbance.

🟩 **Stability Condition:**
The area **gained** (accelerating) = area **lost** (decelerating)

📈 On a power-angle curve:

* Fault disturbs power output
* Post-fault clearing defines new curve
* Compare accelerating and decelerating areas

---

## ⚡ Voltage Stability

Concerns the **ability of the system to maintain acceptable voltage levels** during disturbances.

🔻 Voltage instability can lead to:

* Gradual voltage drop
* Equipment shutdown
* **Voltage collapse** in weak systems

🧪 Often studied using **PV curves** or continuation power flow analysis.

---

## 🔄 Dynamic Stability

Focuses on **oscillations in the rotor angle** and system states after small disturbances.

🧠 Requires advanced analysis with:

* **Linearized system models**
* **State-space representations**
* **Damping ratio assessments**

Used to evaluate **low-frequency oscillations** (0.1–2.0 Hz), especially in interconnected systems.

---

## 🧪 Case Study: Generator Out-of-Step

A generator at a gas plant suddenly loses synchronism after a lightning strike-induced fault. The protective relay isolates it quickly, but the event analysis showed that **inertia and poor damping** were the root causes.

💡 Solution: Add **Power System Stabilizers (PSS)** to improve dynamic damping.

---

## 🔍 Stability Enhancement Techniques

| Method                    | Objective                        |
| ------------------------- | -------------------------------- |
| Fast Fault Clearing       | Improve transient response       |
| High-Speed Relays         | Minimize system disturbance      |
| Excitation System Control | Stabilize voltage                |
| Power System Stabilizer   | Damp rotor oscillations          |
| HVDC Links & FACTS        | Manage power flows and support   |
| Load Shedding Schemes     | Avoid voltage/frequency collapse |

---

## 📊 Summary Table of Stability Types

| Type         | Time Scale   | Dominant Mechanism             | Analysis Tool               |
| ------------ | ------------ | ------------------------------ | --------------------------- |
| Transient    | 0–10 seconds | Rotor angle dynamics           | Swing equation, equal area  |
| Dynamic      | 10s–min      | Electromechanical oscillations | State-space, Eigen analysis |
| Steady-State | Minutes+     | Small signal disturbances      | Power flow methods          |
| Voltage      | Any          | Voltage/reactive instability   | PV curve, CPF analysis      |

---

## ❓ Objective Viva Questions ❓

1. **What is the swing equation used to study?**
   a) Voltage collapse
   b) Rotor angle stability
   c) Load forecasting
   d) Tariff design

2. **Which type of stability is associated with small disturbances and long-term behavior?**
   a) Transient
   b) Dynamic
   c) Steady-state
   d) Voltage

3. **Equal Area Criterion is used for analyzing:**
   a) Steady-state stability
   b) Voltage control
   c) Transient stability
   d) Frequency control

4. **Which tool is commonly used to study voltage stability?**
   a) Swing Equation
   b) Load Flow Analysis
   c) PV Curve
   d) Equal Area Criterion

5. **What does a Power System Stabilizer (PSS) do?**
   a) Excites generators
   b) Reduces load
   c) Improves frequency
   d) Damps rotor oscillations

---

## ✅ Solutions to Viva Questions

1. **b) Rotor angle stability**
   *Explanation:* The swing equation models the mechanical dynamics of the rotor angle.

2. **c) Steady-state**
   *Explanation:* Steady-state stability considers small, long-term changes.

3. **c) Transient stability**
   *Explanation:* The Equal Area Criterion helps assess transient rotor angle stability.

4. **c) PV Curve**
   *Explanation:* Voltage stability is assessed using PV curves and continuation flow.

5. **d) Damps rotor oscillations**
   *Explanation:* PSS helps reduce oscillations in rotor angle after disturbances.

---
Next Lecture: 
Lecture 12: Fault Analysis in Power Systems – Theory & Methods
