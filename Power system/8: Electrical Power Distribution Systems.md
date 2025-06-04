# Lecture 8: Electrical Power Distribution Systems

**Course Instructor:**
📚👨‍🏫 Md. Hassanul Karim Roni
🏫 Assistant Professor, EEE, HSTU, Dinajpur, BD
✉️ [hassanulkarim.roni@gmail.com](mailto:hassanulkarim.roni@gmail.com)
📞 01767052709 (WhatsApp)

---

## 💡 Fun Fact!

Did you know that the vast network of power lines that make up the electrical grid is often considered the largest and most complex machine ever built by humankind? It operates in real-time, balancing supply and demand across vast distances instantaneously!

---

## Key Points

* Electrical power distribution systems deliver electricity from substations to end-users with minimal losses.
* Components include feeders, transformers, and protective devices ensuring reliable power supply.
* Voltage levels in Bangladesh include 11 kV, 0.4 kV for distribution, with 33 kV for sub-transmission.
* Distribution systems are classified as radial, ring, or meshed, each balancing cost and reliability.
* Power quality issues like voltage sags or harmonics impact system performance and require mitigation.
* Safety and maintenance practices, such as earthing and regular inspections, ensure operational reliability.

---

## Introduction to Power Distribution Systems

Electrical power distribution systems transfer electricity from transmission substations to consumers, including residential, commercial, and industrial users. Operating at medium (11 kV, 33 kV) and low voltages (0.4 kV), they ensure efficient power delivery with minimal losses. In Bangladesh, the Bangladesh Rural Electrification Board (BREB) and Dhaka Power Distribution Company (DPDC) manage distribution networks, delivering power to over 20 million households.

---

## Components of Distribution Systems

* **Feeders:** Primary distribution lines (11 kV or 33 kV) carrying power from substations to load centers.
* **Distribution Transformers:** Step down voltage (e.g., 11/0.4 kV) for consumer use, typically 25–500 kVA.
* **Service Mains:** Connect transformers to consumer premises, usually at 400/230 V.
* **Protective Devices:** Fuses, circuit breakers, and reclosers protect against faults like short circuits.
* **Earthing Systems:** Ensure safety by grounding neutral and equipment, common in BREB’s 11 kV networks.
* **Metering Systems:** Measure consumer usage for billing, e.g., smart meters in Dhaka.

---

## Types of Distribution Systems

| Feature          | Radial System                  | Ring Main System                     | Meshed System                           |
| ---------------- | ------------------------------ | ------------------------------------ | --------------------------------------- |
| **Path**         | Single                         | Two (loop)                           | Multiple interconnected                 |
| **Reliability**  | Low                            | Medium to High                       | Very High                               |
| **Cost**         | Low                            | Moderate                             | High                                    |
| **Complexity**   | Simple                         | Moderate                             | Complex                                 |
| **Fault Impact** | High (entire section out)      | Low (isolatable)                     | Very Low (alternative paths)            |
| **Typical Use**  | Rural areas, low-density loads | Urban areas, residential, commercial | Dense urban, industrial, critical loads |
| **Example (BD)** | Rural Dinajpur (BREB)          | Urban Dhaka (DPDC)                   | Industrial Chittagong                   |

---

## Voltage Levels in Bangladesh

* **Primary Distribution:** 11 kV or 33 kV for feeders connecting substations to load centers.
* **Secondary Distribution:** 400/230 V for residential and commercial users.
* **Sub-transmission:** 33 kV for intermediate power transfer in semi-urban areas like Sylhet.

*Example:* BREB’s 11/0.4 kV transformers in Khulna serve rural households, while DPDC uses 33/11 kV for urban loads.

---

## Power Losses in Distribution

Losses include:

* **Technical Losses:** $I^2R$ losses in conductors, transformer losses.
* **Non-technical Losses:** Theft, metering errors.

Typical losses in Bangladesh are 10–15%, with BREB targeting less than 10% through amorphous core transformers.

**Loss Calculation:**

$$
P_{\text{loss}} = I^2 \times R
$$

*Example:*
For a 1 km 11 kV feeder conductor with 0.1 Ω/km resistance carrying 100 A:

$$
P_{\text{loss}} = 100^2 \times 0.1 = 10,000 \times 0.1 = 1,000 \text{ W} = 1 \text{ kW}
$$

*Note:* For a three-phase system, total losses would be higher, considering all conductors.

---

## Power Quality Issues

| Issue             | Description                                                                                                  | Common Causes                                                                       | Typical Effects                                                         | Mitigation in BD                                                            |
| ----------------- | ------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| **Voltage Sag**   | Temporary reduction in RMS voltage (0.1–0.9 pu for 0.5 cycles to 1 min)                                      | System faults, motor starting, sudden large load increase                           | Equipment malfunction/trip, data loss, lighting flicker                 | Voltage regulators, UPS, STATCOMs                                           |
| **Voltage Swell** | Temporary increase in RMS voltage (1.1–1.8 pu for 0.5 cycles to 1 min)                                       | Sudden large load reduction, capacitor bank switching, single line-to-ground faults | Equipment damage (insulation breakdown), reduced lifespan               | Surge arresters, voltage regulators, proper grounding                       |
| **Harmonics**     | Sinusoidal voltage/current components at frequencies that are integer multiples of the fundamental frequency | Non-linear loads (rectifiers, SMPS, VFDs, arc furnaces), inverters                  | Increased losses, equipment heating, metering errors, relay malfunction | Harmonic filters (passive/active), K-rated transformers (DPDC's Dhaka grid) |
| **Power Factor**  | Ratio of real power to apparent power                                                                        | Inductive loads (motors, transformers)                                              | Increased $I^2R$ losses, voltage drops, reduced system capacity         | Capacitor banks (Gazipur industries), synchronous condensers                |
| **Outages**       | Complete loss of power                                                                                       | Faults, equipment failure, maintenance, severe weather                              | Disruption of all activities, economic losses                           | Reclosers, sectionalizers, redundant supply (ring/meshed systems)           |

---

## Protection and Safety Measures

| Device                 | Primary Function                          | Operation Principle                                   | Reset Mechanism      | Typical Application (BD)               |
| ---------------------- | ----------------------------------------- | ----------------------------------------------------- | -------------------- | -------------------------------------- |
| **Fuse**               | Overcurrent protection (sacrificial)      | Melts when current exceeds rating, breaking circuit   | Manual (replacement) | Distribution transformers, LV circuits |
| **Circuit Breaker**    | Overcurrent & short-circuit protection    | Detects fault, mechanically opens contacts            | Manual or Automatic  | Substations, feeders, consumer units   |
| **Recloser**           | Interrupt transient faults, restore power | Opens on fault, attempts reclosing after set delay(s) | Automatic            | Overhead 11 kV rural feeders (BREB)    |
| **Lightning Arrester** | Protect from voltage surges (lightning)   | Diverts surge current to ground, clamps voltage       | Self-resetting       | Overhead lines, transformers (Sylhet)  |

---

## Maintenance Practices

* **Line Inspections:** Monthly checks for damaged insulators or sagging conductors.
* **Transformer Maintenance:** Oil testing (dielectric strength ≥30 kV/2.5 mm), Dissolved Gas Analysis (DGA), and bushing checks.
* **Vegetation Management:** Clear tree branches near 11 kV lines to prevent faults, practiced by BREB.
* **Meter Calibration:** Ensure accurate billing, conducted annually by DPDC.

*Example:* BREB’s quarterly maintenance in Khulna reduces outages by 20%.

---

## Distribution System Design Considerations

* **Load Forecasting:** Predict demand using historical data, e.g., Dhaka’s 5% annual load growth.
* **Conductor Selection:** Use ACSR (Aluminum Conductor Steel Reinforced) for 11 kV feeders due to strength.
* **Reliability Indices:** SAIDI (System Average Interruption Duration Index) and SAIFI (System Average Interruption Frequency Index) guide improvements. BREB targets SAIDI < 50 hours/year.
* **Smart Grids:** DPDC’s smart meters in Dhaka enable real-time monitoring and loss reduction.

---

## Practical Applications in Bangladesh

* **Rural Electrification:** BREB’s 11/0.4 kV networks power 80% of rural households.
* **Urban Distribution:** DPDC’s 33/11 kV ring systems ensure reliable power in Dhaka.
* **Industrial Supply:** Meshed 33 kV systems in Chittagong support textile factories.
* **Renewable Integration:** Solar farms in Feni feed 11 kV grids via step-up transformers.
* **Loss Reduction:** Capacitor banks in Sylhet improve power factor, saving 5–10 MW annually.

---

## Key Takeaways

* Distribution systems deliver power efficiently from substations to consumers.
* Radial, ring, and meshed systems balance cost and reliability.
* Voltage levels (11 kV, 0.4 kV) cater to diverse loads in Bangladesh.
* Power quality and loss reduction are critical for system efficiency.
* Regular maintenance and safety measures ensure reliability and worker safety.

---

## References 📚

1. Grainger, J. J., & Stevenson, W. D. (1994). *Power System Analysis*. McGraw-Hill.
2. Glover, J. D., Sarma, M. S., & Overbye, T. J. (2017). *Power System Analysis and Design*. Cengage.
3. Kothari, D. P., & Nagrath, I. J. (2011). *Modern Power System Analysis*. Tata McGraw-Hill.
4. IEEE Std 141-1993, *Recommended Practice for Electric Power Distribution for Industrial Plants*.
5. BREB and DPDC Annual Reports.
6. Electrical4U, “Electrical Power Distribution System” (Electrical4U).

---

## Objective Viva Questions ❓

1. **What is the typical voltage for primary distribution in Bangladesh?**
   a) 400 V
   b) 11 kV
   c) 132 kV
   d) 230 kV

2. **Which system offers the highest reliability?**
   a) Radial
   b) Ring
