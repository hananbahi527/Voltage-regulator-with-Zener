# Zener Diode Voltage Regulator (220V AC to 5V DC)

This project demonstrates a simple yet effective **DC Voltage Regulator** circuit using a Zener diode. It converts a high-voltage AC input (220V mains) into a stable, regulated 5.1V DC output suitable for low-power electronic devices.

## Table of Contents
- [Circuit Diagram](#-circuit-diagram)
- [Components List](#-components-list)
- [How It Works](#-how-it-works)
- [Technical Specifications](#-technical-specifications)
- [Safety Warning](#-safety-warning)

---

##  Circuit Diagram

The circuit follows a classic linear power supply architecture:
**1. Transformer** ➔ **2. Bridge Rectifier** ➔ **3. Filter Capacitor** ➔ **4. Zener Regulator**

![Voltage Regulator with Zener Diagram](Voltage%20regulator%20with%20Zener%20p.jpeg)


---

##  Components List

| Component | Identifier | Description |
| :--- | :--- | :--- |
| **Transformer** | TR1 | Steps down 220V AC to ~12V AC. |
| **Diodes** | D1–D4 | 1N4001 Silicon Diodes (Bridge Rectifier). |
| **Capacitor** | C1 | 1000µF Electrolytic (Smoothing filter). |
| **Resistor** | R1 | 1kΩ Current Limiter for the Zener diode. |
| **Zener Diode** | D5 | 1N4733A (5.1V Zener) for regulation. |
| **LED Resistor** | R2 | 330Ω Current Limiter for the indicator LED. |
| **Indicator LED** | D6 | Green LED to signal output power. |



---

##  How It Works

1. **Step Down:** The **TR1 Transformer** reduces the dangerous 220V AC mains to a safer 12V AC level.
2. **Rectification:** The **Full-Bridge Rectifier (D1-D4)** converts the AC sine wave into a pulsating DC signal.
3. **Filtering:** The large **1000µF Capacitor (C1)** acts as a reservoir, smoothing out the pulses into a steady DC voltage with minimal ripple.
4. **Regulation:** * The **Zener Diode (D5)** is the heart of the project. It operates in "Reverse Bias" at its breakdown voltage $V_Z \approx 5.1V$.
    * Even if the input voltage fluctuates, the Zener clamps the output at 5.1V.
5. **Indication:** The **Green LED (D6)** lights up when the circuit is successfully providing the regulated output.

![Voltage Regulator with Zener Circuit](Voltage%20regulator%20with%20Zener.jpeg)

---

##  Technical Specifications

* **Input Voltage:** 220V AC, 50/60Hz.
* **Secondary Voltage:** ~12.4V AC.
* **Regulated Output:** ~5.08V - 5.1V DC.
* **Max Zener Current:** Limited by $R1$ to protect the diode from overheating.

---

## ⚠️ Safety Warning

> [!CAUTION]
> **High Voltage Hazard:** This project involves 220V AC mains electricity. Improper handling can lead to electric shock or fire.
> * Always use a fuse on the primary side of the transformer.
> * Ensure all connections are insulated.
> * **Do not touch** any part of the circuit while it is plugged in.

---

