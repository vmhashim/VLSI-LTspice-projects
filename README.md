# CMOS Inverter

A CMOS (Complementary Metal-Oxide-Semiconductor) inverter is a fundamental building block in digital electronics, particularly in VLSI (Very Large Scale Integration) design.

## Overview

### Composition
A CMOS inverter consists of two transistors:
- **PMOS (p-type MOS) transistor**
- **NMOS (n-type MOS) transistor**

These are connected in a complementary fashion.

### Operation
- **Input Low (0)**: 
  - The NMOS transistor is off, and the PMOS transistor is on.
  - This connects the output to the supply voltage (Vdd), making the output high (logic 1).
  
- **Input High (1)**: 
  - The NMOS transistor is on, and the PMOS transistor is off.
  - This connects the output to ground, making the output low (logic 0).

### Advantages
- **High Noise Margins**: Due to the complementary operation, CMOS inverters have good noise margins.
- **Low Power Consumption**: CMOS technology consumes power only during the switching transitions, not in the steady state.

## Characteristics
- **Voltage Transfer Curve (VTC)**: 
  - Shows the relationship between the input and output voltages of the inverter.
  - Crucial for analyzing the inverter's performance.
  
- **Propagation Delay**: 
  - The time it takes for the output to change after the input changes.
  
- **Power Dissipation**: 
  - CMOS inverters have low static power dissipation but consume power during switching due to dynamic power.

## Applications
- Used in digital circuits for logic gates, memory cells, and various digital components.
- Foundational for building more complex circuits like flip-flops, multiplexers, and processors.
## Truth Table 
| Input | Output |
|-------|--------|
|   0   |    1   |
|   1   |    0   |
## LTspice code
```
VDD VDD 0 DC 5 
VSS GND 0 DC 0 
Vin A 0 PULSE 0 5 0 1n 1n 10n 20n 
.tran 0 50n 
.include
.END
```
**For dc response 
```
VDD VDD 0 DC 5
VSS GND 0 DC 0
Vin A 0 PULSE 0 5 0 1n 1n 10n 20n
.dc Vin 0 5 1m
.include
.END
```
### Cmos schematic

<img src ="assts/Cmos sch.png">

### Cmos layout

<img src ="assts/cmos layout.png">

### Cmos waveform

<img src="assts/Cmos trans .png">

### Cmos dc response

<img src="assts/dc response .png">














