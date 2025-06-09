# 🎓 Lecture 24: Advanced Power System Control

**Course Title:** Theoretical Electrical Power Systems
**Instructor:** HK Roni Sir, Assistant Professor, EEE, HSTU
✉️ [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com) | ☎️ 01767052709 (WhatsApp)

---

## ❄️ Ice-Breaker: “Who Controls the Grid?” 🧠⚡

Imagine a sudden drop in solar generation due to cloud cover over northern Bangladesh. The grid frequency dips. Within seconds, an **automated control system** dispatches spinning reserves from gas generators and restores balance — no manual action needed.
This is **Advanced Power System Control** in action — the brain behind real-time decisions in smart grids.

---

## 🎯 Lecture Objectives

After completing this lecture, students will be able to:

* Understand **optimal and predictive control** strategies in power systems
* Explain the role of **wide-area control systems**
* Explore **control integration of renewables and microgrids**
* Analyze challenges and strategies in dynamic control environments

---

## ⚙️ 1. Advanced Control Strategies

### 🔹 Optimal Control

Optimal control aims to operate the power system **at minimum cost or maximum efficiency**, subject to system constraints.

#### Key Features:

* Objective: Minimize cost or loss, or maximize reliability
* Constraints: Voltage limits, power balance, generator limits
* Techniques: Lagrangian methods, Pontryagin’s principle, dynamic programming

### 🔹 Model Predictive Control (MPC)

MPC uses a **model of the system to predict future states** and optimize control actions over a prediction horizon.

| Aspect           | Model Predictive Control (MPC)            |
| ---------------- | ----------------------------------------- |
| Forecasting      | Predicts future states of system          |
| Decision Horizon | Finite (e.g., next 5–15 mins)             |
| Updates          | Re-optimizes at every time step           |
| Applications     | Voltage control, wind & solar integration |

> ⚠️ **In Bangladesh context:** MPC is gaining importance in **solar-battery hybrid microgrids**, such as projects implemented in **Sundarbans solar islands**.

---

## 🌐 2. Wide-Area Control Systems (WACS)

Traditional control systems operate **locally**, but wide-area control involves **global visibility of the grid** using communication networks.

### 🧠 Key Concepts:

* Utilizes PMUs (Phasor Measurement Units)
* Centralized or distributed control
* Enables **real-time dynamic stability control**

### 📊 WACS vs. Traditional SCADA

| Feature                | SCADA Control           | Wide-Area Control       |
| ---------------------- | ----------------------- | ----------------------- |
| Data Refresh Rate      | 2–10 seconds            | 30–60 times/second      |
| Communication          | Slow (legacy protocols) | Fast (IP/MPLS)          |
| Dynamic Event Response | Delayed                 | Near-instant            |
| Coverage               | Local/Regional          | National/Interconnected |

> ✅ **Bangladesh Example:** The **Bangladesh Power Grid Company (PGCB)** has initiated **PMU deployment** in key substations under the Power Grid Expansion Project for better visibility and wide-area control.

---

## ☀️ 3. Control Concepts for Renewable Integration and Microgrids

Integration of variable renewable energy (VRE) and microgrids presents new challenges in control and coordination.

### 🔧 Challenges:

* Variability and intermittency of renewables
* Voltage fluctuations and reverse power flow
* Grid synchronization in islanded operation

### 🔌 Grid-Connected vs Islanded Control in Microgrids

| Feature                  | Grid-Connected Mode              | Islanded Mode                  |
| ------------------------ | -------------------------------- | ------------------------------ |
| Control Objective        | Voltage regulation, power export | Voltage/frequency stability    |
| Frequency Source         | Main grid                        | Local inverter or generator    |
| Energy Management        | Based on price/load forecast     | Based on storage & load demand |
| Resynchronization Needed | No                               | Yes (before reconnecting)      |

> 🏝️ **Bangladesh Projects:** The **Solar Mini-Grids in Hatiya, Sandwip**, and **Monpura islands** operate in islanded mode at night using battery-DG hybrids, switching to grid mode when available.

---

## 🛠️ 4. Control Tools and Emerging Trends

| Control Area        | Tools/Techniques                           |
| ------------------- | ------------------------------------------ |
| Frequency Control   | Droop control, AGC, MPC                    |
| Voltage Regulation  | AVR, OLTCs, STATCOM, reactive dispatch     |
| Stability Control   | WACS, FACTS, SSSC                          |
| Renewable Smoothing | Battery Energy Storage Systems (BESS), MPC |
| Grid Flexibility    | Demand Response, Dynamic pricing           |

---

## 🧪 Case Study Example: MPC in PV-Battery Microgrid

A 100 kW PV system with 200 kWh battery is used in a rural off-grid microgrid in Khulna.
**Problem:** Manage battery charging/discharging to ensure nighttime availability.
**MPC Control Logic:**

* Forecast PV for next 3 hours
* Optimize charge during peak solar hours
* Ensure minimum battery SoC (state-of-charge) at sunset

✅ Result: Improved reliability & minimized diesel usage

---

## ❓ Objective Viva Questions ❓

1. **What is the main goal of optimal control in power systems?**
   a) Reduce emissions
   b) Minimize costs under constraints
   c) Improve voltage quality
   d) Store energy

2. **Model Predictive Control works by:**
   a) Real-time rule-based logic
   b) Forecasting future states and optimizing actions
   c) Fixed setpoint control
   d) AI only

3. **Which of the following enhances dynamic response using global data?**
   a) SCADA
   b) AVR
   c) WACS
   d) OLTC

4. **In islanded mode, microgrids require:**
   a) No control
   b) Constant power supply from the grid
   c) Local frequency regulation
   d) Always-on solar

5. **Which technology is key to enabling WACS?**
   a) Relays
   b) PMUs
   c) Circuit breakers
   d) Capacitor banks

---

## ✅ Solutions to Viva Questions

1. **b) Minimize costs under constraints**
   *Optimal control seeks cost-effective and constraint-aware operation.*

2. **b) Forecasting future states and optimizing actions**
   *MPC uses predictive models to plan ahead and adjust dynamically.*

3. **c) WACS**
   *Wide-area systems integrate data across the network for real-time control.*

4. **c) Local frequency regulation**
   *Islanded microgrids must maintain voltage and frequency independently.*

5. **b) PMUs**
   *Phasor Measurement Units are critical sensors for wide-area control.*

---
