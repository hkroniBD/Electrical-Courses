# ⚙️ Lecture 22: Power System Reliability

**Course Title:** Theoretical Electrical Power Systems
**Instructor:** HK Roni, Assistant Professor, EEE, HSTU
📧 [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com) | ☎️ 01767052709 (WhatsApp)

---

## ❄️ Ice-Breaker: Power Outage on Eid Night – A Reliability Dilemma ⚡🕌

On **Eid night of 2023**, parts of northern Bangladesh plunged into darkness due to unexpected faults in a substation transformer. Despite high generation capacity, **lack of redundancy and slow restoration plans** caused prolonged outages.

This raises a critical question:

> "How reliable is our power system when it matters the most?"

---

## 📘 Overview: What is Power System Reliability?

Power system reliability is the **ability of the electrical grid** to deliver continuous power **without failure**. It combines:

* **Adequacy** (enough capacity to meet demand)
* **Security** (ability to withstand disturbances)

### ✅ Key Focus Areas

* Frequency and duration of outages
* Impact on consumers and economy
* Redundancy and contingency planning

---

## 🧮 Common Reliability Indices

| Index | Full Form                                    | Unit               | Measures                                      |
| ----- | -------------------------------------------- | ------------------ | --------------------------------------------- |
| SAIFI | System Average Interruption Frequency Index  | Interruptions/year | Avg. number of interruptions per customer     |
| SAIDI | System Average Interruption Duration Index   | Minutes/year       | Avg. outage duration per customer             |
| CAIDI | Customer Average Interruption Duration Index | Minutes            | Avg. time to restore service per interruption |

---

### 🔢 Formulas:

1. **SAIFI**

   $$
   SAIFI = \frac{\sum \text{Total Number of Customer Interruptions}}{\text{Total Number of Customers Served}}
   $$

2. **SAIDI**

   $$
   SAIDI = \frac{\sum \text{Customer Interruption Durations}}{\text{Total Number of Customers Served}}
   $$

3. **CAIDI**

   $$
   CAIDI = \frac{SAIDI}{SAIFI}
   $$

---

## 🔎 Interpreting Reliability Metrics

| Scenario | SAIFI (Freq) | SAIDI (Duration)          | Reliability Inference                |
| -------- | ------------ | ------------------------- | ------------------------------------ |
| Low      | Low          | Low                       | Reliable system                      |
| High     | Low          | Medium                    | Frequent small outages               |
| Low      | High         | Long single outages       | Poor restoration time or contingency |
| High     | High         | Frequent and long outages | Serious reliability concerns         |

---

## 🛠️ Theoretical Principles of Reliability Evaluation

### 1. **Deterministic Methods**

* N-1 Contingency Rule: System must withstand loss of **any one major element**
* Used in planning and grid code compliance

### 2. **Probabilistic Methods**

* Use **failure probabilities**, **MTBF**, **MTTR**
* Provide **statistical estimates** of reliability performance

| Method        | Strength                       | Weakness                                 |
| ------------- | ------------------------------ | ---------------------------------------- |
| Deterministic | Simpler to implement           | May overlook real-world failure behavior |
| Probabilistic | More realistic and data-driven | Requires statistical data                |

---

## 🔄 Redundancy in Power Systems

Redundancy is the **provision of backup components** that can take over in case of a fault.

| Redundancy Type | Description                           | Example                           |
| --------------- | ------------------------------------- | --------------------------------- |
| Component-Level | Backup transformer, relay             | Standby transformer in substation |
| Network-Level   | Alternate power paths via extra lines | Ring feeder design                |

---

## 🧰 Contingency Planning

Contingency planning involves preparing for **unexpected events** like:

* **Loss of a generator**
* **Transmission line faults**
* **Sudden load increase**

### Steps in Planning:

1. Identify critical system components
2. Perform **N-1, N-2 studies**
3. Implement backup systems and rerouting strategies
4. Validate with **simulation and real-time SCADA monitoring**

---

## 🌐 Bangladesh Context: Real-World Reliability Concerns

| Event                         | Issue Identified                         | Learning Outcome                           |
| ----------------------------- | ---------------------------------------- | ------------------------------------------ |
| 2020 National Grid Failure    | Fault in transmission system             | Weak protection coordination and backup    |
| Rural Load Shedding (Summer)  | Poor grid penetration and feeder outages | Need for distributed backup and automation |
| Industrial Zones (e.g., DEPZ) | Voltage sags and shutdowns               | Require UPS + embedded redundancy          |

---

## 🌱 Enhancing Reliability in Bangladesh

* Smart Grids for **fault localization and self-healing**
* SCADA + PMU deployment for real-time reliability monitoring
* Better **feeder-level metering** for SAIDI/SAIFI calculation
* Microgrids as backup in **rural and islanded zones**

---

## ❓ Objective Viva Questions ❓

1. **Which index represents average outage frequency?**
   a) SAIDI
   b) SAIFI
   c) CAIDI
   d) MAIFI

2. **What does CAIDI indicate?**
   a) Number of interruptions per feeder
   b) Total energy lost during outage
   c) Average duration per interruption
   d) Cost of downtime

3. **N-1 contingency means:**
   a) No component failure allowed
   b) Only one fault per year is acceptable
   c) System should survive loss of one element
   d) One generator must be on standby

4. **Which method includes statistical modeling?**
   a) Deterministic
   b) Heuristic
   c) Probabilistic
   d) Static

5. **Which of the following is a redundancy strategy?**
   a) Load forecasting
   b) Feeder automation
   c) Backup transformer
   d) Time-of-day tariff

---

## ✅ Solutions to Viva Questions ✅

1. **b) SAIFI**
   *Explanation:* SAIFI measures the average number of times a customer experiences an outage in a year.

2. **c) Average duration per interruption**
   *Explanation:* CAIDI = SAIDI / SAIFI

3. **c) System should survive loss of one element**
   *Explanation:* N-1 means one component can fail without system-wide collapse.

4. **c) Probabilistic**
   *Explanation:* This approach uses failure probability and statistical data.

5. **c) Backup transformer**
   *Explanation:* Redundancy ensures continued operation during faults.

---
