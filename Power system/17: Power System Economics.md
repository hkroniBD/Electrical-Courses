# 🌞 Lecture 17: Power System Economics

**Course Title:** Theoretical Electrical Power Systems
**Instructor:** HK Roni, Assistant Professor, EEE, HSTU
📧 [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com) | ☎️ 01767052709 (WhatsApp)

---

## ❄️ Ice-Breaker: Why Electricity is Cheaper at Midnight Than Noon? ⚡

* In many countries, electricity costs drop drastically at night.
* Peak load pricing, marginal cost dispatching, and fuel type dependency all affect this.
  Understanding this dynamic leads us into the world of **power system economics** — where engineering meets money.

---

## 📘 Overview of Power System Economics

Power system economics focuses on the **planning, pricing, and operation** of electricity generation, transmission, and distribution in the **most cost-effective and reliable** manner.

### ✅ Key Goals

* Minimize total cost (CAPEX + OPEX)
* Maintain grid stability and reliability
* Encourage energy efficiency
* Ensure fair and transparent tariffs for all consumer classes

---

## 💰 Types of Costs in Power Systems

| 🏷️ **Cost Type**          | 📝 **Description**                                                |
| -------------------------- | ----------------------------------------------------------------- |
| 📦 Capital Cost (CAPEX)    | Cost of infrastructure (plants, lines, substations)               |
| 🔧 Operational Cost (OPEX) | Fuel, labor, maintenance, auxiliary power                         |
| 🔄 Start-up/Shut-down Cost | Cost of turning generators on/off                                 |
| 🛠️ Maintenance Cost       | Routine and emergency repairs, parts replacement                  |
| 🌿 External Costs          | Environmental, social, regulatory (e.g., carbon taxes, emissions) |

### 📌 Marginal Cost

The **cost of producing one more unit** (kWh) of electricity — crucial for dispatch and pricing decisions.

---

## 📊 Tariff Structures and Pricing Models

### 📋 What is a Tariff?

A tariff is a **structured pricing scheme** used to recover utility costs while influencing user behavior.

### ⚖️ Common Tariff Models

| Tariff Type         | Description                                                |
| ------------------- | ---------------------------------------------------------- |
| Flat Rate           | Constant price per kWh regardless of time or usage         |
| Time-of-Use (ToU)   | Higher prices during peak demand, lower at off-peak        |
| Block Rate          | Price increases/decreases in consumption slabs             |
| Two-Part Tariff     | Fixed monthly fee + variable energy charges                |
| Demand-Based Tariff | Based on maximum kW load drawn (especially for industries) |

---

## 🏛️ Deregulation and Market Models

### 🔓 What is Deregulation?

Deregulation involves **unbundling** vertically integrated power utilities into **competitive entities** that generate, transmit, and distribute electricity independently.

### 👥 Market Participants

* **GENCOs** – Generation companies
* **TRANSCOs** – Transmission companies
* **DISCOs** – Distribution companies
* **ISO/RTO** – Independent System/Regional Transmission Operators

### 🌍 Market Models

| Model           | Features                                             |
| --------------- | ---------------------------------------------------- |
| Pool Model      | Central operator dispatches based on least-cost bids |
| Bilateral Model | Direct buyer-seller contracts (long/short-term)      |
| Hybrid Model    | Combination of both pool and bilateral trading       |

---

## 🧮 Spot Pricing and Economic Dispatch

### 🧊 Spot Pricing

The **real-time price** of electricity at a specific location and time, based on current demand and supply balance.

### ⚙️ Economic Dispatch

Minimizes total generation cost under power balance constraint:

$$
\min \sum_{i=1}^{n} C_i(P_i) \quad \text{subject to} \quad \sum P_i = P_{\text{demand}}
$$

Where:

* $C_i(P_i)$: Generator cost function
* $P_i$: Power output of generator $i$

---

## 🌍 Real-World Application: Power Pricing in Bangladesh

| Sector            | Policy/Status                                                  |
| ----------------- | -------------------------------------------------------------- |
| Bulk Generation   | BPDB sells to utilities under regulated bulk tariff            |
| Retail Tariff     | Varies across residential, commercial, agricultural consumers  |
| Subsidy Mechanism | Government subsidizes retail tariffs to maintain affordability |
| Key Challenges    | High dependency on imported fuel, rising cost, low RES share   |

---

## ❓ Objective Viva Questions ❓

1. **Which of the following is not a capital cost?**
   a) Power transformer
   b) Land development
   c) Fuel purchase
   d) Switchgear installation

2. **Which entity manages transmission in a deregulated market?**
   a) IPP
   b) ISO
   c) DISCO
   d) GENCO

3. **What is the goal of economic dispatch?**
   a) Maximize generator output
   b) Minimize electricity bills
   c) Equal load sharing
   d) Minimize total generation cost

4. **Which tariff type charges based on maximum kW usage?**
   a) Flat Rate
   b) Time-of-Use
   c) Block Rate
   d) Demand-Based

5. **What does marginal cost represent in power economics?**
   a) Total cost of a plant
   b) Maintenance cost per year
   c) Cost of generating one additional unit
   d) Cost of purchasing fuel in bulk

---

## ✅ Solutions to Viva Questions ✅

1. **c) Fuel purchase**
   *Explanation:* Fuel is part of operational cost, not capital cost.

2. **b) ISO**
   *Explanation:* Independent System Operator manages transmission and dispatch in deregulated markets.

3. **d) Minimize total generation cost**
   *Explanation:* Economic dispatch allocates generation to minimize system cost while meeting demand.

4. **d) Demand-Based**
   *Explanation:* This tariff charges based on peak power draw, usually in kW.

5. **c) Cost of generating one additional unit**
   *Explanation:* Marginal cost is crucial for real-time pricing and dispatch strategies.

---

Next Lecture 18: Power Quality
