# 🔋 Lecture 23: Advanced Power System Operation

**Course Title:** Theoretical Electrical Power Systems
**Instructor:** HK Roni Sir, Assistant Professor, EEE, HSTU
📧 [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com) | ☎️ 01767052709 (WhatsApp)

---

## ❄️ Ice-Breaker: Balancing Electricity in Real-Time ⚡🔄

Did you know?
On **April 4, 2024**, the Bangladesh Power Development Board (BPDB) had to shed 400 MW load within seconds due to a sudden generator outage. Maintaining supply-demand balance in **real time** is essential—and that is the realm of **Advanced Power System Operation**.

---

## 📘 Concept: Real-Time Operation & Control

Real‑time operation involves continuously monitoring grid conditions and **adjusting generation** and **load** to maintain:

* **Frequency** (50 Hz ± tolerance)
* **Voltage profile** across buses
* **Reserve margins** for contingencies

Core elements include:

* **Real-Time Monitoring** via SCADA/EMS
* **Automatic Generation Control (AGC)**
* **Contingency Analysis**
* **Reserve Management**

---

## 🛠️ Advanced Automatic Generation Control (AGC)

AGC autonomously adjusts generator outputs to correct **frequency deviations** and maintain **net interchange schedules**.

* **Control Area**: Controlled by a regulating authority (e.g., BPDB)
* **Error Calculation**: Area Control Error (ACE) = (Actual−Scheduled Interchange) + β × (Actual–Nominal Frequency)
* **Control Actions**: Regulating units follow **AGC signals** to eliminate ACE and restore balance

### Comparison: AGC vs. Manual Dispatch

| Feature             | Manual Dispatch            | AGC                        |
| ------------------- | -------------------------- | -------------------------- |
| Response Time       | Minutes to tens of minutes | Seconds to minutes         |
| Accuracy            | Operator-dependent         | High (closed-loop control) |
| Human Interaction   | Required                   | Minimal                    |
| Frequency Stability | Poor under sudden events   | Maintained via AGC-Steady  |

---

## 📉 Contingency Analysis

Contingency analysis simulates failures (N-1, N-2) to detect **violations** before they occur.

* **Security Constrained OPF (SCOPF)** ensures limits are not violated post-contingency
* **Alert Actions**: Re-dispatch, load shedding plan, islanding strategies

### Table: Severity Levels in Contingency

| Contingency Type            | Impact                        | Control Measure                          |
| --------------------------- | ----------------------------- | ---------------------------------------- |
| N-1 Line Outage             | Overloading of alternate path | Re-dispatch, RAS activation              |
| N-1 Generator Loss          | Frequency drop                | AGC ramp-up, spinning reserve activation |
| N-2 Major Equipment Failure | Widespread violation          | Load shedding, grid reconfiguration      |

---

## 🧠 Reserve Management

To handle uncertainties and failures, power systems maintain reserves:

| Reserve Type                     | Purpose                                   | Duration                 |
| -------------------------------- | ----------------------------------------- | ------------------------ |
| Primary (Governor)               | Immediate frequency support               | Seconds–minutes          |
| Secondary (AGC)                  | Correct residual errors, restore reserves | Minutes                  |
| Tertiary (Spinning/Non-Spinning) | Replenish used reserves                   | Tens of minutes to hours |

🟢 **Reserve Margin** (e.g., 15% of peak load) keeps system secure.

---

## 🌏 Bangladesh Context: Real-Time Operation

* **BPDB & NLDC** manage AGC across plants like Ghorashal, Kaptai, Meghnaghat
* SCADA-based **Real-Time Monitoring** implemented at grid and generator end
* **Contingency drills** monthly; loading reserve dispatch algorithms in testing
* Reserve levels: around **10–12%** spinning margin, emergency **5%**

---

## 🔁 Real-Time Operation Workflow

1. **Data Collection** via SCADA/PMUs
2. **State Estimation** for real-time grid model
3. **AGC & Dispatch Instructions** issued
4. **Contingency Scan** for N-1/N-2
5. **Reserve Deployment** and monitoring

---

## ❓ Objective Viva Questions ❓

1. **What is ACE in AGC used for?**
   a) Emergency control override
   b) Area Control Error calculation
   c) Automatic current expander
   d) Annual corrective evaluation

2. **Which reserve type supports seconds to minute response?**
   a) Primary (Governor)
   b) Secondary (AGC)
   c) Tertiary (Non-Spinning)
   d) Strategic backup

3. **Contingency ‘N-1’ typically simulates:**
   a) Two simultaneous failures
   b) Planned maintenance outage
   c) Single component failure (e.g. a line)
   d) Demand surge

4. **Which system performs real-time grid monitoring?**
   a) ADMS
   b) HMI
   c) SCADA
   d) DMS

5. **Which authority sets scheduled interchange?**
   a) GENCOS
   b) DISCOs
   c) NLDC/BPDB
   d) End consumers

---

## ✅ Solutions to Viva Questions ✅

1. **b) Area Control Error calculation**
   *Used to adjust generator output to correct frequency/interchange deviations.*

2. **a) Primary (Governor)**
   *Provides immediate frequency support within seconds.*

3. **c) Single component failure (e.g. a line)**
   *N-1 simulates single outage to test system robustness.*

4. **c) SCADA**
   *SCADA collects, processes, and displays real-time grid data.*

5. **c) NLDC/BPDB**
   *NLDC sets the scheduling and monitoring of power interchange.*

---
