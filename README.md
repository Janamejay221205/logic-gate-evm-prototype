# Digital Logic Gate Electronic Voting Machine (EVM) Prototype

A hardware-level Electronic Voting Machine (EVM) prototype engineered entirely using discrete digital integrated circuits (ICs) and combinational/sequential logic blocks. Designed and simulated using **Proteus** and **ARES** for schematic capture and PCB layout design.

---

## ⚙️ Circuit Architecture & IC Breakdown

The system bypasses microcontrollers entirely, relying on pure hardware logic to handle debouncing, counting, comparison, and display drivers:

* **Control Unit (555 Timer):** Configured in monostable mode to generate uniform, clean clock pulses for every button press, filtering out mechanical switch bouncing.
* **Counter Stage (CD4510):** Utilizes CMOS Presettable Up/Down BCD Counters to independently increment vote tallies for competing candidates.
* **Decoder & Display Stage (CD4511):** BCD-to-7-Segment Latch/Decoder/Drivers translate binary state variables into human-readable numeric tallies on 7-segment LED displays.
* **Magnitude Comparator (74LS85):** Implements a 4-bit magnitude comparator circuit block to dynamically monitor vote counts and trigger logic states when predefined thresholds are met.

---

## ⚡ Key Engineering Features

* **Pure Hardware Implementation:** Operates without a software firmware layer, optimizing propagation delay and showcasing foundational digital systems design (DSD).
* **Hardware Debouncing:** Mitigates mechanical switch noise via RC time constants paired with timer gating, ensuring absolute count precision.
* **PCB Design Optimized:** Schematics translated into a clean PCB layout using ARES, incorporating optimized trace routing and single-row 6-pin DPDT configuration logic for mechanical input stability.

---

## 🛠️ How to View and Simulate

1. Download and install **Proteus Design Suite**.
2. Clone or download this repository to your machine.
3. Open the `.pdsprj` file inside Proteus to interact with the logic gates, press the candidate switches, and view the live 7-segment display increments in real-time.
