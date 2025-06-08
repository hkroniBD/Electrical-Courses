# 🎓 Lecture 10: Power System Control – Fundamentals

**Course Title:** Power Systems for Utility & Industry
**Instructor:** HK Roni Sir, Assistant Professor, EEE, HSTU
✉️ [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com) | ☎️ 01767052709 (WhatsApp)

---

## ❄️ Ice-Breaker: Control That Never Sleeps ⚙️🔋

### 🎯 A 0.1 Hz Frequency Drop = 500 MW Imbalance!

Even a small drop from 50 Hz to 49.9 Hz means a severe **generation-load mismatch**. Grid operators must react within seconds to avoid cascading blackouts.

### 🧠 AGC – The Invisible Hand

**Automatic Generation Control (AGC)** automatically signals power plants to ramp up/down generation – faster than human operators can act.

### 🛡️ Voltage = Local Hero

While frequency is global, voltage is **highly localized**. You may have perfect frequency but poor voltage quality at your neighborhood if local control fails.

---

## 📘 Overview of Power System Control

Power system control is the **central nervous system** of modern electrical grids. Its main role is to keep:

* ⚖️ **Supply = Demand**
* ⚡ **Voltage = Stable**
* 🔁 **Power flow = Balanced & Safe**

Control actions occur **at multiple time scales**—from milliseconds (local response) to minutes (system-wide coordination).

---

## 🎯 Core Control Objectives

| Objective            | Why it Matters                       | Controlled By                 |
| -------------------- | ------------------------------------ | ----------------------------- |
| 🕒 Frequency Control | Reflects balance of power in system  | Governors, AGC, Load Shedding |
| 🔌 Voltage Control   | Ensures power quality, device safety | Exciters, OLTCs, Capacitors   |
| 🔁 Power Flow Mgmt   | Prevents line overloads, blackouts   | Load Dispatch, FACTS devices  |

---

## 🔄 Automatic Generation Control (AGC)

### 🧠 What is AGC?

AGC is a **secondary frequency control mechanism** that adjusts generator outputs automatically to:

* Maintain **scheduled frequency (50 Hz)**
* Maintain **tie-line interchange**
* Balance **interconnected control areas**

### 📐 Key Term: Area Control Error (ACE)

$$
ACE = \Delta P_{\text{tie-line}} + B \cdot \Delta f
$$

Where:

* $\Delta P_{\text{tie-line}}$ = deviation in inter-area power
* $B$ = frequency bias factor
* $\Delta f$ = frequency deviation

### 🚦 AGC in Action

If frequency drops:

* AGC commands generators to **increase output**
* Brings frequency and tie-line flow **back to setpoint**

🛡️ Acts as a **"closed-loop" control** system, constantly sensing and correcting.

---

## 🧰 Key Control Devices

### ⚙️ 1. Governors – The Fast Responders

* Maintain **frequency** by regulating **turbine speed**
* Act **within seconds** using droop characteristics

📌 Types:

* Mechanical Governors (older)
* Digital/Electronic Governors (modern)

### ⚡ 2. Exciters – The Voltage Doctors

* Control the **field current** of synchronous generators
* Maintain **terminal voltage** and **reactive power**

📌 Systems:

* Static Excitation (common now)
* Brushless AC Exciters

### 🧮 3. AVRs (Automatic Voltage Regulators)

* Work with exciters to regulate **voltage dynamically**
* Keep voltage **within ±5%**

---

## 🧱 Control Levels in Practice

| Control Level   | Action Time    | Objective                     | Devices Used                 |
| --------------- | -------------- | ----------------------------- | ---------------------------- |
| Primary         | < 10 sec       | Arrest frequency deviations   | Governors                    |
| Secondary (AGC) | 10 sec – 5 min | Restore nominal frequency     | Centralized AGC              |
| Tertiary        | > 5 min        | Re-dispatch and balance areas | Load dispatch centers (NLDC) |

🧠 Example: NLDC uses AGC to coordinate multiple plants during a sudden load change on the grid.

---

## 🧠 Local vs Centralized Control

| Parameter     | Local Control       | Centralized Control         |
| ------------- | ------------------- | --------------------------- |
| Scope         | Generator/Bus level | Inter-area/System level     |
| Example       | AVR, Governor       | AGC, Load Dispatch via NLDC |
| Reaction Time | Fast (ms–s)         | Moderate (s–min)            |

---

## 🧪 Real-Life Example: PGCB & Frequency Control

* During Eid load drop, PGCB’s AGC **ramps down thermal generation**
* **Saves fuel** and avoids **over-frequency**
* **Tie-line exchange with India** adjusted in real-time

---

## 📊 Summary Table of Key Control Concepts

| Control Element | Primary Function      | Responds To             | Control Type       |
| --------------- | --------------------- | ----------------------- | ------------------ |
| Governor        | Frequency control     | Speed/Frequency error   | Mechanical/Digital |
| Exciter         | Voltage control       | Terminal voltage        | Electronic         |
| AGC             | Area-wide balance     | Frequency + ACE         | Digital/SCADA      |
| AVR             | Local voltage support | Reactive load variation | Fast Electronics   |

---

## ❓ Objective Viva Questions

1. **What is the main purpose of AGC?**
   a) Improve power factor
   b) Load forecasting
   c) Frequency and tie-line control
   d) Billing estimation

2. **Which device regulates the generator's terminal voltage?**
   a) AVR
   b) Governor
   c) Transformer
   d) Load Tap Changer

3. **What is droop control used for?**
   a) Voltage stability
   b) Excitation damping
   c) Primary frequency response
   d) Reactive power compensation

4. **True or False: Exciters are used for controlling mechanical input to the generator.**
   a) True
   b) False

5. **Which parameter does ACE depend on?**
   a) Voltage and power factor
   b) Power loss and temperature
   c) Tie-line deviation and frequency deviation
   d) Load shedding and generator inertia

---

## ✅ Solutions to Viva Questions

1. **c) Frequency and tie-line control**
   *AGC ensures system frequency and inter-area exchange are within limits.*

2. **a) AVR**
   *AVR, working with the exciter, maintains terminal voltage.*

3. **c) Primary frequency response**
   *Droop control adjusts generator output based on frequency deviation.*

4. **b) False**
   *Exciters control voltage, not mechanical input.*

5. **c) Tie-line deviation and frequency deviation**
   *ACE = tie-line error + frequency bias term.*
