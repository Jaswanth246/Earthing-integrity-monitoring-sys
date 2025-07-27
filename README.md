# ⚡ Earthing Integrity Monitoring System for Street Lights

A real-time embedded system to monitor the **safety and integrity of streetlight earthing systems** in public areas such as parking lots and railway stations. Designed around an **Arduino UNO**, this system detects **leakage currents**, verifies **earth continuity**, and measures **earth resistance**, generating alerts through a **buzzer** and **GSM module**. It's scalable, cost-effective, and built for real-world reliability.

---

## ✅ Features

- ⚙️ Leakage current detection using CT sensor (1000:1)
- 🔌 Earth continuity testing via voltage injection and reference resistor
- 🧮 Earth resistance calculation using Ohm's Law
- 🔔 Real-time alerts with a piezo buzzer
- 📲 Fault notifications via SMS using GSM (SIM800L)
- 🔄 Adaptive software rectification and gain calibration
- 🛡️ Safe, non-invasive retrofit for existing installations
- 📡 Future-ready for Power Line Communication (PLC)
- 🌐 Scalable to networked monitoring via central server

---

## 🔩 Hardware Components

| Component         | Description                                  |
|------------------|----------------------------------------------|
| Arduino UNO       | Central controller and data processor        |
| CT Sensor         | Current Transformer (1000:1 turns ratio)     |
| Burden Resistor   | 1kΩ or 4.7kΩ depending on current range       |
| Capacitor         | 10μF smoothing capacitor                     |
| Diode             | For signal rectification (optional)          |
| Op-Amp            | Signal amplification from CT sensor          |
| Low Pass Filter   | Removes high-frequency noise                 |
| MOSFET            | Controls voltage injection circuit           |
| GSM Module        | SIM800L or compatible for SMS alerts         |
| Relay (Optional)  | For switching/isolation                      |
| Buzzer            | 5V piezo buzzer for on-site alerting         |

---

## 🧠 Methodology

1. **Leakage Current Detection**:
   - CT Sensor detects current imbalance.
   - Output passed through burden resistor → voltage.
   - Op-Amp amplifies low voltage signal.
   - Low-pass filter removes noise.
   - Arduino digitizes signal and calculates leakage current.
   - Software-based rectification + gain calibration for accuracy.

2. **Earth Continuity Test**:
   - 9V voltage injected via MOSFET into earth path.
   - Current measured via 1kΩ reference resistor.
   - Voltage drop analyzed to verify path continuity.
   - Fault triggers alert if expected current is not detected.

3. **Earth Resistance Measurement**:
   - Uses Ohm's Law on voltage/current from test circuit.
   - Compares measured resistance against threshold limits.

4. **Communication**:
   - Fault detected → alert via buzzer + SMS via GSM.
   - Designed for optional future upgrade to PLC.

---

## 📐 System Diagram (Conceptual)

*(Add your schematic image here using GitHub's markdown image syntax)*  
`![System Diagram](images/system-diagram.png)`

---

## 🛠️ Future Improvements

- Powerline Communication (PLC) integration
- Remote OTA firmware update capability
- Web dashboard for centralized monitoring
- Environmental data analysis (temp/humidity effects)
- Predictive fault analysis using ML

---

## 📝 Claims Overview

1. Leakage current detection via CT with amplification and filtering.
2. Software rectification and adaptive gain for accurate readings.
3. Voltage injection method for earth continuity check.
4. Resistance calculation using voltage drop across known resistor.
5. Integrated monitoring and fault alerting system.
6. GSM as primary communication, future PLC support.
7. Retrofitting for existing streetlights.
8. Environmental correlation for adaptive sensitivity.
9. Predictive diagnostics with sensor fusion.
10. Scalable node-based network with centralized control.

---

## 📚 Description

This project offers a **complete embedded solution** for **public safety** in outdoor electrical systems. It combines sensor-based measurement, microcontroller processing, and wireless communication into a compact, efficient, and reliable product. Designed with **non-invasive retrofitting**, this solution ensures **early detection** of electrical faults and **proactive maintenance**, reducing both risks and costs in urban infrastructure.

---
