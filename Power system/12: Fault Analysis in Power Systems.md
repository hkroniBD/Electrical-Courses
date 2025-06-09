# 🎓 Lecture 12: Fault Analysis in Power Systems – Theory & Methods

**Course Title:** Theoretical Electrical Power Systems
**Instructor:** HK Roni Sir, Assistant Professor, EEE, HSTU
✉️ [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com) | ☎️ 01767052709 (WhatsApp)

---

## ❄️ Ice-Breaker: The “Silent Killers” of Power Systems ⚡🚨

🔌 Faults in power systems are like **silent heart attacks** — they occur suddenly and can cripple entire networks if not diagnosed properly.
📉 A simple **line-to-ground fault** in a remote part of the system may cause a cascade of **generator trips and blackouts** if not detected swiftly.

🔥 Ice-Breaker: The 2020 National Grid Blackout in Bangladesh
On October 4, 2020, Bangladesh suffered a massive blackout due to a fault in the transmission line system. Over 80% of the country lost power — highlighting the importance of fault detection, analysis, and protection systems in power grids.
This case reminds us how critical it is to understand fault types and their theoretical analysis to ensure stable power systems.

---

## 🔍 What is Fault Analysis?

Fault analysis is the process of **determining the electrical conditions** (currents and voltages) in a power system during abnormal conditions like short circuits.

⚡ Objectives:

* Ensure **protective devices** respond correctly
* Design and **rate system components** safely
* Understand system **stability under faults**

---

## 🔥 Types of Faults

| Fault Type            | Description                       | % Occurrence |
| --------------------- | --------------------------------- | ------------ |
| Three-Phase Fault     | All three conductors shorted      | < 5%         |
| Line-to-Ground (L–G)  | One conductor touches ground      | \~70%        |
| Line-to-Line (L–L)    | Two conductors shorted            | \~15%        |
| Double Line-to-Ground | Two conductors and ground shorted | \~10%        |
| Open Circuit Faults   | One or more conductors open       | Rare         |

🔌 **Symmetrical Fault:**

* Balanced in all phases (e.g., three-phase fault)
* Simplest to analyze
* High magnitude but low probability

⚡ **Unsymmetrical Faults:**

* Involve imbalance (e.g., L–G, L–L)
* More complex and more common

---

## 📏 Assumptions in Fault Calculations

To simplify theoretical analysis:

* Network is operating under **balanced load conditions** before fault
* Faults are **bolted** (zero impedance)
* System impedance is known
* **Transient effects** may be neglected for initial estimation

---

## ⚙️ Symmetrical Components Method

Introduced by Charles Fortescue, it decomposes **unbalanced 3-phase systems** into:

$$
\text{Original System} = \text{Positive Seq.} + \text{Negative Seq.} + \text{Zero Seq.}
$$

| Sequence Type | Meaning                            | Behavior                 |
| ------------- | ---------------------------------- | ------------------------ |
| Positive      | Balanced system (normal operation) | Rotates forward          |
| Negative      | Imbalance due to faults            | Rotates backward         |
| Zero          | Ground return paths involved       | In-phase, same magnitude |

This simplifies **unsymmetrical fault analysis** by turning it into a set of **balanced problems**.

---

## 📌 Fault Current Calculations: A Brief Flow

### Step-by-Step Process:

1. **Convert system** to per-unit
2. **Draw equivalent reactance diagram**
3. **Apply fault at location**
4. Use **Thevenin’s equivalent** at fault point
5. Compute **fault current** using:

   $$
   I_f = \frac{V_{pre-fault}}{Z_{th} + Z_{fault}}
   $$

---

## ⚡ Example: Single Line-to-Ground (L–G) Fault

For a fault on phase A, the current in phase A is:

$$
I_A = \frac{3V}{Z_1 + Z_2 + Z_0}
$$

Where:

* $V$: Pre-fault voltage (1∠0° pu)
* $Z_1$: Positive sequence impedance
* $Z_2$: Negative sequence impedance
* $Z_0$: Zero sequence impedance

---

## 🔄 Comparison of Fault Currents

| Fault Type         | Current Formula (simplified)      | Relative Magnitude |
| ------------------ | --------------------------------- | ------------------ |
| 3-Phase            | $I = \frac{V}{Z_1}$               | High               |
| Line-to-Line (L–L) | $I = \frac{\sqrt{3}V}{Z_1 + Z_2}$ | Medium             |
| Single Line-Ground | $I = \frac{3V}{Z_1 + Z_2 + Z_0}$  | Medium to High     |
| Double Line-Ground | More complex – uses all sequences | High               |

---

## 🛡️ Applications of Fault Analysis

* Designing **protective relay settings**
* **Sizing** of circuit breakers
* **Identifying weak points** in the network
* Enhancing **system stability and selectivity**

---

## 🧪 Short Case Example

📍 A 100 MVA, 13.8 kV generator with 0.2 pu reactance is connected to a 10 km line. A three-phase fault occurs at the end of the line. Calculate fault current assuming system base of 100 MVA.

$$
I_{fault} = \frac{V_{base}}{Z_{total}} = \frac{1.0}{0.2} = 5.0\text{ pu}
$$

$$
I_{actual} = 5.0 \times \frac{100 \times 10^6}{\sqrt{3} \times 13.8 \times 10^3} \approx 2092 \text{ A}
$$

---

## ❓ Objective Viva Questions ❓

1. **Which of the following is a symmetrical fault?**
   a) Line-to-Ground
   b) Double Line-to-Ground
   c) Three-phase fault
   d) Line-to-Line

2. **The most common type of fault in power systems is:**
   a) Line-to-Line
   b) Line-to-Ground
   c) Three-phase
   d) Open circuit

3. **Symmetrical components are used for:**
   a) Balanced loads only
   b) Symmetrical faults
   c) Unsymmetrical faults
   d) Overcurrent protection

4. **What is the formula for L–G fault current?**
   a) $\frac{V}{Z_1}$
   b) $\frac{3V}{Z_1 + Z_2 + Z_0}$
   c) $\frac{\sqrt{3}V}{Z_1 + Z_2}$
   d) $\frac{V}{Z_0}$

5. **Which sequence component is in-phase in all three phases?**
   a) Positive sequence
   b) Negative sequence
   c) Zero sequence
   d) Mixed sequence

---

## ✅ Solutions to Viva Questions

1. **c) Three-phase fault**
   *Explanation:* Only three-phase faults are symmetrical with balanced conditions.

2. **b) Line-to-Ground**
   *Explanation:* Over 70% of faults in power systems are single line-to-ground.

3. **c) Unsymmetrical faults**
   *Explanation:* Symmetrical components simplify analysis of unbalanced conditions.

4. **b) $\frac{3V}{Z_1 + Z_2 + Z_0}$**
   *Explanation:* This is the standard per-unit formula for L–G faults.

5. **c) Zero sequence**
   *Explanation:* Zero sequence currents are equal in magnitude and phase in all conductors.

---

Next Lecture 13: Power System Protection
