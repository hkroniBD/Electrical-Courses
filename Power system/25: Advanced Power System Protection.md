# 🎓 Lecture 25: Advanced Power System Protection

**Course Title:** Theoretical Electrical Power Systems  
**Instructor:** HK Roni Sir, Assistant Professor, EEE, HSTU  
✉️ [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com) | ☎️ 01767052709 (WhatsApp)

---

## ❄️ Ice-Breaker: From Fuses to AI-Enabled Relays 🚀

🔧 In the early days, **fuses** were our only protection tool. Fast forward to today, and we have **digital relays** that communicate in real time, **analyze power system data**, and adapt to changing network conditions dynamically.

📍 In Bangladesh, **PGCB's digital substation initiatives** and the **Smart Grid Roadmap** are already adopting intelligent electronic devices (IEDs) and wide-area protection for high-voltage networks.

---

## 📌 Lecture Focus

- Digital Relays and IEDs  
- Wide-Area Protection Systems  
- Adaptive Protection Techniques  

---

## 🛡️ Digital Relays and Intelligent Electronic Devices (IEDs)

### 🔷 What are Digital Relays?

Digital relays are **microprocessor-based protection devices** that process voltage, current, and frequency inputs to detect and isolate faults.

| Feature              | Digital Relays              | Electromechanical Relays     |
|----------------------|-----------------------------|-------------------------------|
| Speed                | Fast (in ms)                | Slower (in cycles)           |
| Accuracy             | High                        | Moderate                     |
| Communication        | Yes (Ethernet, IEC 61850)   | No                           |
| Programmable Logic   | Yes                         | No                           |
| Self-diagnostics     | Yes                         | No                           |

### 🔷 What are IEDs?

IEDs combine **multiple functions** such as:

- Protection (overcurrent, differential, distance)
- Control (breaker operation)
- Monitoring (data logging, event reporting)
- Communication (SCADA, IEC 61850)

➡️ Widely used in **Digital Substations** (e.g., PGCB’s Ghorashal GIS Substation project)

---

## 🌐 Wide-Area Protection Systems (WAPS)

### 🔸 Why Wide-Area Protection?

As power systems grow complex, localized protection is not enough. **WAPS** uses **system-wide data** from Phasor Measurement Units (PMUs) for **coordinated protection**.

### 🔸 Key Components:

- **PMUs:** Measure time-synchronized voltage and current phasors
- **WAMS (Wide-Area Monitoring Systems):** Real-time situational awareness
- **Central Protection Coordinator:** Decides fast, intelligent tripping logic

### 🔸 Advantages:

- Detect inter-area oscillations
- Prevent system-wide blackouts (like the 2020 Bangladesh blackout)
- Enhanced situational awareness

---

## 🧠 Adaptive Protection Techniques

### 🛠️ What is Adaptive Protection?

Adaptive protection involves **real-time modification of relay settings** based on:

- Load changes
- Network topology
- Renewable integration
- Fault history

### 🔄 Techniques:

- **Online re-coordination of relays**
- **Adaptive distance settings**
- **Self-healing networks**

| Scenario                    | Traditional Relay | Adaptive Relay |
|-----------------------------|-------------------|----------------|
| Line outage                 | Static settings   | Settings update in real-time |
| DG Integration (Solar)      | Misoperation risk | Auto-adjust pickup levels     |
| Topology changes            | Manual intervention | Autonomous adjustment       |

### 🌱 Example: Integration with Solar Plants

In grids like those in rural Bangladesh where **solar mini-grids** are connected, adaptive relays help manage **intermittency** and avoid **nuisance tripping**.

---

## 🔬 Case: PGCB’s Protection Automation Efforts

🔹 PGCB and BPDB have begun implementing **digital substations** with **SCADA-integrated protection** and **GPS-synchronized PMUs**.  
🔹 The goal is to establish **adaptive islanding schemes** and protect against cascading failures, especially during high-loading periods (e.g., Eid seasons).

---

## 🔄 Summary Table

| Feature                 | Digital Relay          | WAPS                    | Adaptive Protection      |
|-------------------------|------------------------|--------------------------|---------------------------|
| Technology Basis        | Microprocessors        | PMUs, GPS                | Real-time logic updates   |
| Coverage                | Local Substation       | Entire Grid              | Context-aware nodes       |
| Main Benefit            | Speed, Accuracy        | System-Wide Coordination | Flexibility & Intelligence|

---

## ❓ Objective Viva Questions ❓

1. **Which protocol is widely used for IED communication?**  
   a) TCP/IP  
   b) Modbus  
   c) IEC 61850  
   d) SCADA

2. **Which device provides synchronized phasor data?**  
   a) RTU  
   b) PMU  
   c) PLC  
   d) IED

3. **WAPS is primarily used to:**  
   a) Control generators  
   b) Monitor breaker health  
   c) Provide wide-area protection  
   d) Replace relays

4. **Adaptive protection changes settings based on:**  
   a) Manufacturer specs  
   b) Environmental temperature  
   c) System conditions  
   d) Operator's manual setting

5. **A key feature of digital relays is:**  
   a) Mechanical tripping  
   b) Fixed delay logic  
   c) Programmability  
   d) Absence of communication

---

## ✅ Solutions to Viva Questions

1. **c) IEC 61850**  
   _It’s the standard for substation communication protocols._

2. **b) PMU**  
   _PMUs provide time-synchronized phasor data using GPS._

3. **c) Provide wide-area protection**  
   _WAPS ensures coordination across large grid regions._

4. **c) System conditions**  
   _Adaptive protection adjusts dynamically based on operating conditions._

5. **c) Programmability**  
   _Digital relays offer logic customization and remote updates._

---

📘 **Next Lecture:** Lecture 26 – Energy Management Systems (EMS)
