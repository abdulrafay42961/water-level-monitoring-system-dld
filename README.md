# Automated Water Level Monitoring System (DLD Project)

A digital logic control system designed to monitor tank water levels using multi-stage visual indicators (LEDs) and trigger an overflow audio alarm (buzzer) under a low-voltage (3.5V) operating constraint.

## 📌 Features & Highlights
* **Multi-Stage Detection:** Low, Medium, and High water level sensing.
* **Cumulative Visual Indication:** Sequential LED tracking (Green → Yellow → Red).
* **Automated Safety Interlock:** 3-input AND gate logic triggers the buzzer only when all sensors are active (overflow condition).
* **Low-Voltage Optimization:** BC547 NPN transistors used as switching drivers to efficiently operate loads at 3.5V.

## 🛠️ Components & Tools Used
* **Simulation Tools:** Tinkercad Circuits, Logisim
* **ICs & Semiconductors:** 74HC74 (Dual D Flip-Flops), 74HC11 (Triple 3-Input AND Gate), BC547 NPN Transistors
* **Output Actuators:** LEDs (Green, Yellow, Red), Piezo Buzzer

## 📐 Circuit Architecture & Logic
- **Optimization:** Truth tables minimized using Karnaugh Maps (K-Maps).
- **Sequential Logic:** D Flip-Flops manage state progression across clock pulses.

---
*For detailed circuit schematics, truth tables, and implementation steps, please refer to the uploaded PDF report.*
