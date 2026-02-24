**🚀 8-Point FFT – RTL to GDSII Physical Design Flow**
📌 Project Overview

This repository presents the complete RTL-to-GDSII implementation of an 8-point Fast Fourier Transform (FFT) using industry-standard EDA tools.

The project demonstrates the full ASIC Physical Design (PD) flow, starting from RTL design and simulation to synthesis, floorplanning, placement, routing, clock tree synthesis (CTS), and post-synthesis verification.

The FFT algorithm reduces the computational complexity of Discrete Fourier Transform (DFT) from O(N²) to O(N log N), making it highly efficient for signal processing applications.


├── fft_8pt.v           # RTL design of 8-point FFT
├── fft_8pt_Tb.v        # Testbench for FFT
├── FFT_PD.pdf          # Complete Physical Design Report
├── README.md

**🏗 Design Architecture**

The FFT RTL consists of the following key blocks:

✔ Butterfly Processing Unit

✔ Twiddle Factor Multiplication

✔ Bit-Reversal Logic

✔ Control FSM (stage & data flow management)

**🔎 RTL Constructs Used**

Fixed-point arithmetic operations (Adders, Multipliers)

FSM implemented using case and conditional constructs

Sequential and combinational logic using always_ff and always_comb


**Complete Physical Design Flow**
**1️⃣ RTL Simulation (Pre-Synthesis)**

Tools Used:

Synopsys VCS

Verdi

NCLaunch

Objective:
Functional verification of FFT RTL before synthesis to validate logic correctness and data flow integrity.

Waveform and schematic validation were performed to ensure correct stage-wise FFT computation.

**2️⃣ Synthesis**

Tool Used: Synopsys Design Compiler

Objective:

Convert RTL → Gate-Level Netlist

Apply timing constraints

Perform area and timing optimization

Critical path analysis

Key aspects:

Clock constraint definition

Timing-driven synthesis

Area optimization

Setup/hold analysis

**3️⃣ Floorplanning**

Tool Used: Cadence Innovus

Objective:

Define core area

Macro and I/O placement

Optimize routing resources

Improve core utilization

Initial layout structure is defined at this stage.

**4️⃣ Power Planning**

Tool Used: Innovus

Objective:

Create power rings

Insert power stripes

Ensure uniform power distribution

Minimize IR drop and electromigration

Robust power grid ensures reliable operation.

**5️⃣ Placement**

Tool Used: Innovus

Steps Performed:

Global Placement – Initial standard cell placement

Detailed Placement – Optimization and overlap removal

Legalization – DRC-compliant cell alignment

Commands Used:

place_opt

legalize

check_placement

Objective:

Minimize wire length

Optimize timing

Improve congestion

**6️⃣ Clock Tree Synthesis (CTS)**

Tool Used: Innovus

Objective:

Balanced clock distribution

Minimize clock skew

Optimize clock latency

Clock buffers and gating cells were inserted to maintain timing integrity.

Parameters adjusted:

Clock uncertainty

Clock latency

Skew optimization

**7️⃣ Routing**

Tool Used: Innovus

Objective:

Complete signal routing

Maintain signal integrity

Optimize congestion

Prepare design for timing closure

Special attention was given to:

Setup timing

Hold timing

Crosstalk

Routing congestion

**8️⃣ Post-Synthesis Simulation**

Tool Used: NCLaunch

Objective:

Gate-level simulation

Timing validation

Functional integrity verification

Ensures design correctness after synthesis and physical implementation.

**📊 Key Learning Outcomes**

✔ Complete RTL-to-GDSII ASIC flow
✔ Timing constraint handling
✔ Clock tree design and skew optimization
✔ Power grid planning
✔ Placement & routing optimization
✔ Gate-level simulation and verification
✔ Industry tool exposure (Synopsys & Cadence)



**Tools & Technologies Used**
| Stage           | Tool                     |
| --------------- | ------------------------ |
| RTL Design      | Verilog                  |
| Simulation      | VCS, Verdi, NCLaunch     |
| Synthesis       | Synopsys Design Compiler |
| Physical Design | Cadence Innovus          |
| Verification    | Gate-level simulation    |


**🎯 Applications**

Digital Signal Processing (DSP)

Wireless Communication Systems

Audio Processing

Image Processing

Embedded Systems

**📈 Future Improvements**

Parameterized N-point FFT

Pipelined architecture for higher throughput

Low-power optimization

Multi-clock domain support

DFT/Scan insertion

**👨‍💻 Author**

Aryan Kannaujiya
PhD Scholar – VLSI Design
Specialization: VLSI Design - Circuit
