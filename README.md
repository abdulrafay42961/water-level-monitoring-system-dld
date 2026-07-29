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
## 📂 Repository Files
* 📄 `OOP2main.cpp` — Main Application Execution & Control Loop
* 📄 `OOP2.cpp` — Class Member Function Implementations
* 📄 `OOP2.h` — Core Class Declarations & Header Specifications
* 📄 `OOP project Report.docx` — Complete Documentation, UML Diagrams & Testing Screenshots
* 📄 `OOP project diagram.drawio` — Editable UML Class Diagram Source
* 📁 `*.txt` — Dynamic File Stream Databases (Teams, Tournaments, Logs & Credentials)

---

## 🚀 How to Build & Run

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/abdulrafay42961/esports-tournament-management-cpp.git](https://github.com/abdulrafay42961/esports-tournament-management-cpp.git)
## ⚙️ Circuit Logic & Working Principle
Compile using G++:
g++ OOP2main.cpp OOP2.cpp -o esports_app
Run Application:
./esports_app
```text
💧 Water Level Sensors
       │
       ▼
🔄 Demux & Selection Line (Driven by D Flip-Flops)
       │
       ▼
⚙️ Combinational Logic & K-Maps (74HC11 AND Gates)
       │
       ├───────────────────────────────────────┐
       ▼                                       ▼
🔌 BC547 Transistor Switches             🛑 NOR Gate Auto Interlock
       │                                 (Shuts down system at max state)
 ┌─────┼─────┐
 ▼     ▼     ▼
🟢     🟡    🔴 + 🔔
Low   Mid    High + Buzzer

