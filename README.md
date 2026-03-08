# 🚦 Traffic Light Controller using Verilog

## 📌 Project Overview

This project implements a **Traffic Light Controller** using **Verilog HDL** and simulates it using **ModelSim**.
The design is based on a **Finite State Machine (FSM)** that controls three traffic lights: **Red, Yellow, and Green**.

The controller cycles through the following sequence:

RED → GREEN → YELLOW → RED

This project demonstrates the fundamentals of:

* Sequential logic design
* Finite State Machines (FSM)
* Verilog HDL coding
* Digital simulation using ModelSim

---

# 🛠 Tools Used

* **Verilog HDL** – Hardware Description Language used to design the controller
* **ModelSim** – Used for simulation and waveform analysis
* **GTKWave (optional)** – For waveform visualization

---

# 📂 Project Structure

```
Traffic-Light-Controller/
│
├── traffic_light.v        # Main Verilog design module
├── tb_traffic_light.v     # Testbench for simulation
├── waveform.png           # Simulation waveform output
└── README.md              # Project documentation
```

---

# ⚙️ Traffic Light States

The controller operates using **three states**.

| State  | Light ON        | Description        |
| ------ | --------------- | ------------------ |
| RED    | Red light ON    | Vehicles must stop |
| GREEN  | Green light ON  | Vehicles can move  |
| YELLOW | Yellow light ON | Prepare to stop    |

State transitions follow this order:

```
RED → GREEN → YELLOW → RED
```

---

# 🧠 Design Description

The controller uses:

* **Clock signal** to control timing
* **Reset signal** to initialize the system
* **State register** to store the current traffic light state
* **Timer counter** to control how long each light stays active

### State Encoding

```
RED    = 2'b00
GREEN  = 2'b01
YELLOW = 2'b10
```

---

# ▶️ Simulation Steps (ModelSim)

Compile the files:

```
vlog traffic_light.v
vlog tb_traffic_light.v
```

Start simulation:

```
vsim tb_traffic_light
```

Add waveform signals:

```
add wave *
```

Run simulation:

```
run -all
```

---

# 📊 Expected Waveform Behavior

The waveform should show the following sequence:

```
RED = 1   GREEN = 0   YELLOW = 0
RED = 0   GREEN = 1   YELLOW = 0
RED = 0   GREEN = 0   YELLOW = 1
RED = 1   GREEN = 0   YELLOW = 0
```

Only **one light should be ON at any time**.

---

# 🎯 Learning Outcomes

By completing this project, you will understand:

* Verilog module design
* FSM implementation
* Clock-based sequential circuits
* Writing testbenches
* Waveform analysis in ModelSim

---

# 🚀 Possible Improvements

Future enhancements can include:

* Two-road traffic signal controller
* Pedestrian crossing signal
* Emergency vehicle priority
* FPGA implementation using LEDs

---

# 👨‍💻 Author

Verilog Traffic Light Controller Project
Created for learning **Digital Design and VLSI concepts**.

---

⭐ If you found this project useful, consider giving the repository a **star**!
