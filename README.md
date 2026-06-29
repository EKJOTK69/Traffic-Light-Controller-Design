# Traffic-Light-Controller-Design

A Finite State Machine (FSM) based Smart Traffic Light Controller designed in Verilog HDL and implemented using Xilinx Vivado. The controller manages traffic at a T-intersection by changing traffic lights according to predefined states.

---

## 📌 Project Objective

The objective of this project is to design and simulate a Traffic Light Controller for a T-intersection using Verilog HDL. The controller follows a sequence of states to safely manage traffic flow on all roads.

---

## 🛠️ Tools Used

- Verilog HDL
- Xilinx Vivado
- FPGA
- FSM (Finite State Machine)

---

## ✨ Features

- FSM-based traffic control
- Six operating states
- Automatic state transitions
- Separate control for four traffic signals
- Simulation and synthesis performed in Vivado
- FPGA compatible design

---

## 🚦 Traffic Signals

The controller manages the following roads:

- **M1** – Main Road 1
- **M2** – Main Road 2
- **MT** – Turn Lane
- **S** – Side Road

Each signal uses 3-bit encoding:

| Code | Light |
|------|-------|
| 100 | 🔴 Red |
| 010 | 🟡 Yellow |
| 001 | 🟢 Green |

---

## 🔄 State Sequence

```
S1 → S2 → S3 → S4 → S5 → S6 → S1
```

The controller continuously cycles through these six states to regulate traffic efficiently.

---

## 📂 Project Structure

```
Traffic-Light-Controller/
│
├── Traffic_Light_Controller.v
├── Traffic_Light_Controller_TB.v
├── STATE_TABLE.md
├── images/
│   ├── State_Diagram.png
│   ├── RTL_Schematic.png
│   ├── Simulation_Waveform.png
│   └── Schematic.png
└── README.md
```

---

## 📸 Results

The project includes:

- FSM State Diagram
- State Table
- RTL Schematic
- Simulation Waveform
- Synthesis Reports
- Implementation Reports

---

## 📚 References

- NPTEL Digital Design Lectures
- Xilinx Vivado Documentation
- Verilog FSM Design Resources

---

## 👨‍💻 Author

**Ekjot Singh Kundal**

B.Tech Electrical Engineering  
Indian Institute of Technology (IIT) Ropar


