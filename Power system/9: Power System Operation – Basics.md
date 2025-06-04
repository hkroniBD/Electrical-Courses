# 🎓 Lecture 9: Power System Operation – Basics

**Course Title:** Power Systems for Utility & Industry
**Instructor:** HK Roni Sir, Assistant Professor, EEE, HSTU
✉️ [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com) | ☎️ 01767052709 (WhatsApp)

---

## ❄️ Ice-Breaker: Fun Facts to Spark Curiosity 🌟

### ⏱️ Real-Time Matching

🔌 Power generation must **instantly balance demand**. Even a mismatch of 100 MW can disturb the grid frequency within seconds—this is why automation is key.

### 🛰️ NLDC's Smart Grid Role

The **National Load Dispatch Center (NLDC)** is the brain of Bangladesh's grid. With **SCADA systems**, it adjusts power flows in real-time to prevent overloading, blackouts, or brownouts.

### ⚖️ Frequency = Load Indicator

When system frequency drops from 50 Hz to 49.5 Hz, it's a signal that **load is exceeding generation**. Control systems act to either increase supply or shed some load.

---

## 📘 Overview of Power System Operation

Power system operation ensures electricity reaches consumers **reliably**, **safely**, and **economically**, even during sudden changes in load or faults.

🛠️ It includes:

* **Load scheduling**
* **Generator commitment**
* **Real-time frequency and voltage control**
* **Contingency management during faults**
* **Grid supervision by centralized control centers**

---

## 🔄 Load Dispatching and Unit Commitment

### 🔧 Load Dispatching (What to Generate & When)

This involves adjusting the power output of generators to match **demand patterns**, considering system constraints.

🔹 **Day-ahead dispatch:** Based on forecasts.
🔹 **Real-time dispatch:** Responds to actual demand fluctuations.
🔹 **Economic dispatch:** Minimizes cost by choosing cheaper generation.

🧠 Example: During summer afternoons, air conditioners cause peak loads. NLDC schedules additional generation from quick-start gas turbines.

### 🧮 Unit Commitment (Which Units to Run)

This planning decides:

* Which power plants should run at each hour
* Ensures **minimum up/down times**, fuel constraints, and startup costs
* Maintains **spinning reserve** to handle faults or sudden load rise

💡 Algorithms used: **Mixed Integer Programming**, **PSO**, and **GA**.

---

## 📈 Frequency and Voltage Control

### ⚙️ Frequency Control (Balance of Supply & Demand)

The frequency must stay close to **50 Hz**. Any deviation indicates a mismatch in generation and consumption.

**Control Levels:**

| Level     | Action Time    | Method                          |
| --------- | -------------- | ------------------------------- |
| Primary   | < 10 sec       | Governor action (droop control) |
| Secondary | \~30 sec–5 min | Automatic Generation Control    |
| Tertiary  | > 5 min        | Manual dispatch/load adjustment |

🧠 Example: In PGCB's control center, AGC ramps up generation automatically if frequency drops.

---

### 🔌 Voltage Control (Local Power Quality)

Voltage must remain within ±5% of nominal to protect devices. This is done by:

* **Shunt capacitors** to support voltage
* **Tap-changing transformers** to adjust line voltage
* **Synchronous condensers** for reactive power compensation

📍 Example: In Rajshahi, OLTCs at 33/11 kV substations manage voltage swings from irrigation pump loads.

---

## ⚖️ Frequency Stability & Load Shedding

### 🔄 Frequency Stability

Maintained by ensuring **generation = load** at all times. Loss of generation causes:

* Frequency drop
* Turbine governors respond automatically
* AGC supports frequency recovery
* UFLS kicks in if situation worsens

### 🔋 Load Shedding (UFLS Mechanism)

Used when **automatic recovery fails**. UFLS drops parts of the load to prevent system collapse.

💡 Example: Bangladesh’s under-frequency relays disconnect feeders when frequency drops below 49.0 Hz.

---

## 🧠 Role of Control Centers (NLDC, BPDB)

Control centers act as the **central nervous system** of the grid.

### 🛰️ Functions of NLDC (PGCB)

* Monitor real-time generation, load, frequency, voltage
* Balance power imports (India) and internal generation
* Schedule maintenance
* Respond to contingencies

📍 Technology Used:

* **SCADA**
* **Energy Management Systems (EMS)**
* **PMUs for dynamic grid monitoring**

🔍 Example: During Eid holidays, NLDC reduces base load plant usage and focuses on hydro + imports due to low demand.

---

## 📊 Summary Table of Key Operations

| Operation Area    | Objective                       | Tools Used                   |
| ----------------- | ------------------------------- | ---------------------------- |
| Load Dispatching  | Match demand with generation    | SCADA, Forecasting, OPF      |
| Unit Commitment   | Optimize generator schedules    | MIP, GA, PSO                 |
| Frequency Control | Maintain 50 Hz                  | Governor, AGC, Load Shedding |
| Voltage Control   | Maintain voltage within ±5%     | OLTC, Capacitors, Reactors   |
| Grid Supervision  | Real-time operation & stability | NLDC, EMS, PMU, SCADA        |

---

## ❓ Objective Viva Questions

1. **What is the standard frequency of Bangladesh’s power system?**
   a) 60 Hz
   b) 50 Hz
   c) 0 Hz
   d) 120 Hz

2. **Which authority oversees power generation in Bangladesh?**
   a) PGCB
   b) BPDB
   c) REB
   d) SREDA

3. **What is the typical generation voltage in Bangladesh?**
   a) 132–230 kV
   b) 11–25 kV
   c) 400 V
   d) ±500 kV

4. **True or False: The Power Grid Company of Bangladesh (PGCB) manages the national transmission grid.**
   a) True
   b) False

5. **What is the household distribution voltage in Bangladesh?**
   a) 230 V
   b) 120 V
   c) 11 kV
   d) 400 V

6. **What conductor is commonly used in Bangladesh’s transmission lines?**
   a) Copper Solid
   b) ACSR
   c) Iron Core
   d) Fiber Optic

7. **What is Bangladesh’s electrification rate as of 2022?**
   a) \~50%
   b) \~85%
   c) \~30%
   d) \~100%

---

## ✅ Solutions to Viva Questions

1. **b) 50 Hz**
   *Explanation:* Bangladesh’s grid operates at 50 Hz, common across Europe and Asia.

2. **b) BPDB**
   *Explanation:* Bangladesh Power Development Board is responsible for most generation assets.

3. **b) 11–25 kV**
   *Explanation:* Most power plants in Bangladesh generate in this voltage range for transmission compatibility.

4. **a) True**
   *Explanation:* PGCB manages and operates the 132 kV and 230 kV national transmission network.

5. **d) 400 V**
   *Explanation:* Household connections are 3-phase 400 V (230 V per phase to neutral).

6. **b) ACSR**
   *Explanation:* ACSR (Aluminum Conductor Steel Reinforced) is widely used in high-voltage transmission.

7. **b) \~85%**
   *Explanation:* As of 2022, Bangladesh had reached approximately 85% electrification nationwide.
