# 🎓 Lecture 13: Power System Protection – Fundamentals and Coordination

**Course Title:** Theoretical Electrical Power Systems
**Instructor:** HK Roni Sir, Assistant Professor, EEE, HSTU
✉️ [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com) | ☎️ 01767052709 (WhatsApp)

---

## ❄️ Ice-Breaker: “The Nervous System” of Power Networks 🧠⚡

Just as the human body needs **nerves to detect pain and react**, power systems require **protection schemes** to identify faults and isolate them immediately. Without protection, even a **minor short circuit** can lead to **grid collapse** or **equipment destruction**.

> “Protection systems don’t prevent faults — they **prevent disasters**.”

---

## 🛡️ Why Power System Protection is Necessary

Power systems operate under high voltages and currents. Faults must be cleared:

* Quickly 🕒
* Selectively 🎯
* Automatically ⚙️

### 🎯 Protection Objectives:

* Protect life and property
* Prevent equipment damage
* Ensure system stability
* Minimize power outage durations

---

## ⚙️ Key Protective Devices

| Device                         | Function                                          |
| ------------------------------ | ------------------------------------------------- |
| **Relays**                     | Detect abnormal conditions and send trip signals  |
| **Circuit Breakers**           | Disconnect faulty sections                        |
| **Fuses**                      | Provide overcurrent protection for small circuits |
| **Current Transformers (CTs)** | Step down current for relays                      |
| **Voltage Transformers (VTs)** | Step down voltage for relays                      |

---

## 🔄 Protection System Architecture

```
[Primary Protection] — [Backup Protection]  
       |                    |  
  (Fast, localized)    (Slower, broader scope)
```

* **Primary Protection**: Closest to the fault, acts first
* **Backup Protection**: Operates if primary fails
* **Zones of Protection**: Defined by CT locations and relay reach

---

## ⚡ Common Protection Schemes

| Scheme                      | Application              | Principle                                 |
| --------------------------- | ------------------------ | ----------------------------------------- |
| **Overcurrent Protection**  | Feeders, transformers    | Exceeds set current value                 |
| **Differential Protection** | Transformers, generators | Difference between input & output current |
| **Distance Protection**     | Transmission lines       | Measures impedance to fault               |
| **Directional Protection**  | Radial systems           | Current direction awareness               |

---

### 📌 Overcurrent Protection

* Trip when current exceeds a preset threshold
* **Types:**

  * Instantaneous (no delay)
  * Inverse-time (trip time decreases with increased current)

$$
t = \frac{K}{(I/I_{pickup})^n - 1}
$$

---

### 🧮 Differential Protection

* Based on **Kirchhoff’s Current Law**
* If $I_{in} \ne I_{out}$, fault is present
* Widely used in **transformer and generator protection**

$$
I_{diff} = I_{in} - I_{out}
$$

---

### 🔍 Distance Protection

* Calculates **impedance** from relay to fault point
* Suitable for long transmission lines
* Uses **impedance relays** that operate when:

$$
Z_{measured} = \frac{V}{I} < Z_{set}
$$

---

## 🕸️ Zones of Protection

* Zones are **overlapping** to ensure complete coverage
* Each zone is protected by a **set of relays and CTs**
* **Zone Overlap** ensures redundancy in case of failure

---

## 🧩 Selectivity and Coordination

* **Selectivity:** Only the **faulted section** is isolated
* **Coordination:** Ensures backup operates if primary fails
* Achieved by **time grading**, **current grading**, or **zone grading**

---

## 🛑 Fuse and Relay Coordination

In distribution systems, fuses and relays must coordinate such that:

* Fuses protect **individual loads**
* Relays protect **feeders or zones**

---

## 🧠 Protection Design Considerations

* **Sensitivity:** Detect small faults
* **Speed:** Operate quickly to prevent escalation
* **Selectivity:** Isolate only faulted areas
* **Reliability:** Always work when needed
* **Simplicity & Economy:** Cost-effective system

---

## 💡 Real-Life Example

📍 A transformer has differential protection. During internal fault:

* Relay measures $I_{in} = 500 \, \text{A}, I_{out} = 0$
* Fault current $I_{diff} = 500 \, \text{A}$ → Relay trips

---

## ❓ Objective Viva Questions ❓

1. **Which of the following detects abnormal conditions in a power system?**
   a) Circuit breaker
   b) CT
   c) Relay
   d) Fuse

2. **The main function of a differential relay is to:**
   a) Detect direction of fault
   b) Measure voltage
   c) Compare incoming and outgoing currents
   d) Detect overvoltage

3. **Which of the following protection schemes is best suited for transmission lines?**
   a) Overcurrent
   b) Differential
   c) Distance
   d) Directional

4. **Primary protection should be:**
   a) Slower than backup
   b) More sensitive and faster
   c) Delayed to coordinate
   d) Optional in modern systems

5. **Zones of protection are mainly defined by:**
   a) Voltage transformers
   b) Substation buses
   c) CT and relay locations
   d) Number of feeders

---

## ✅ Solutions to Viva Questions

1. **c) Relay**
   *Explanation:* Relays monitor system conditions and trigger circuit breakers.

2. **c) Compare incoming and outgoing currents**
   *Explanation:* This is the core principle of differential protection.

3. **c) Distance**
   *Explanation:* Distance protection is ideal for long transmission lines where fault location varies.

4. **b) More sensitive and faster**
   *Explanation:* Primary protection must act quickly and accurately to isolate the fault.

5. **c) CT and relay locations**
   *Explanation:* Zones of protection are physically limited by the placement of CTs and associated relays.

---

Next Lecture 14: *Load Forecasting and Demand Management*
