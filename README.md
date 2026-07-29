# 🌊 Automated Water Level & Overflow Monitoring System

An end-to-end Digital Logic Design (DLD) project featuring sequential water level tracking, multi-stage visual LED indicators, and automated overflow audio alarm protection. Simulated and verified on **Logisim** and **Tinkercad Circuits** under a low-voltage (3.5V) operating constraint.

---

## 📌 Project Overview
This system dynamically monitors tank water levels across sequential states (Low → Medium → High) and triggers a safety alarm upon reaching full capacity.

* **Sequential State Control:** Driven by clock-synchronized D Flip-Flops.
* **Demux-Based Input Selection:** Automated input routing using counter logic.
* **Auto Power Cutoff / Interlock:** Feedback loop using a NOR Gate to automatically freeze/shut down the system state when maximum output capacity is reached.
* **Multi-Stage Output Drivers:** BC547 NPN Transistors operating as switches to safely drive output LEDs and buzzer loads at low operating voltage (3.5V).

---

## 🖼️ Circuit Simulations & Architecture

### Tinkercad Breadboard Implementation
![Tinkercad Circuit Diagram](./Water%20Level%20Monitoring%20System%20Tinkercad.jpg)

### Key Circuit Highlights (Logisim Schematics)
* **Counter Selection Line:** D Flip-Flop counter logic paired with XOR gates to drive a 1-to-4 Demultiplexer for automatic input state cycling.
* **Combinational Logic:** Integrated 74HC11 (3-input AND gates) to verify simultaneous activation of all level sensors prior to activating the overflow warning.
* **Global Reset & Enabler:** Manual push-button reset line integrated across all output D Flip-Flops.

---

## 🛠️ Hardware & Components Breakdown

| Component Category | Component Name / IC | Quantity / Description |
| :--- | :--- | :--- |
| **Logic ICs** | **74HC74** Dual D Flip-Flops | State storage & sequential switching |
| **Logic ICs** | **74HC11** Triple 3-Input AND Gate | High-level overflow alarm detection |
| **Semiconductors** | **BC547** NPN Transistors | Transistor switching drivers for output loads |
| **Outputs** | LEDs (Green, Yellow, Red) | Multi-stage visual water level indicators |
| **Outputs** | Piezo Buzzer | High-frequency audio overflow alert |
| **Inputs & Controls** | Push Button & Clock Generator | Global circuit reset & clock pulse drive |

---

## ⚙️ Circuit Logic & Working Principle
