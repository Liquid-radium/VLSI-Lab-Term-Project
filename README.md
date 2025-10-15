#  4-Word × 4-Bit ROM Design (CMOS Implementation)

This project demonstrates the complete design and simulation flow of a **4-word × 4-bit Read-Only Memory (ROM)** circuit using **CMOS technology**, **SPICE simulation**, and **Magic VLSI layout**.

---

##  Overview

This repository contains a simple example of a ROM circuit built using CMOS transistors.  
It uses a **2-to-4 line decoder** to select one of four possible words, and each word outputs a 4-bit data value through pre-defined connections.

The design flow includes:
1. **Schematic/Netlist**: SPICE circuit description
2. **Simulation**: Using `ngspice` or `irsim` to verify logical operation
3. **Layout**: Using Magic VLSI to design and extract the circuit

---

##  Features

-  CMOS-based 4×4 ROM implementation
-  2-to-4 line decoder using logic transistors
-  Word-line and bit-line based addressing
-  SPICE-based transient simulation
-  Layout compatible with Magic VLSI
-  Extendable to larger ROM arrays

---

##  How It Works

###  1. Decoder
The **2-to-4 decoder** activates one of four word lines (`Y0h`–`Y3h`) based on the binary address inputs `A` and `B`.

###  2. ROM Cells
Each cell connects a **bitline (BL)** to either **VDD** or **GND** depending on whether the stored bit is `1` or `0`.

| Address | Wordline | Data (Bit3..Bit0) |
|----------|-----------|------------------|
| 00 | Y0h | 1011 |
| 01 | Y1h | 0010 |
| 10 | Y2h | 0100 |
| 11 | Y3h | 1000 |

### 🔍 3. Outputs
Each bitline is buffered by a CMOS pair to drive the final outputs `OUT0`–`OUT3`.

---

 Future Work

Extend to 4-word × 8-bit ROM

Integrate sense amplifiers for high-speed reads

Perform layout vs schematic (LVS) checks

 References

Magic VLSI Documentation – https://opencircuitdesign.com/magic/

NGSPICE User Manual – https://ngspice.sourceforge.io/docs.html

IRSIM Magic 

 Author

Shruti Ramesh Hegde
VLSI Design Project — CMOS ROM Cell Design and Simulation
