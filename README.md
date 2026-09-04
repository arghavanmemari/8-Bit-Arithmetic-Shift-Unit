# 8-Bit Arithmetic Shift Unit

## Digital Systems Course Project

An 8-bit Arithmetic Shift Unit designed and implemented using TTL logic integrated circuits.

This project presents the design, simulation, and hardware implementation of a multifunctional digital system capable of performing arithmetic and shifting operations on 8-bit binary data.

The system supports four different operations:

- 8-bit Addition
- 8-bit Subtraction
- Logical Right Shift
- Logical Left Shift

The complete system was designed using TTL ICs, simulated in Proteus Design Suite, and implemented practically on breadboards.

---

# Project Overview

The main objective of this project is to design an 8-bit processing unit capable of performing arithmetic and shift operations using fundamental digital logic components.

The designed system contains four main functional units:

- Operation Selection Unit
- Arithmetic Processing Unit
- Shift Register Unit
- Output Selection Unit

The circuit was first verified using Proteus simulation and then implemented using real hardware components.

---

# System Architecture

The system architecture consists of four main sections:

## Operation Selection Unit

The operation selection block determines the required function according to the control inputs.

A 2-bit control signal selects between the available operations.

## Arithmetic Processing Unit

The arithmetic section performs:

- Binary Addition
- Binary Subtraction

using:

- 74LS283 Binary Adders
- 74LS86 XOR Gates

## Shift Register Unit

The shift section performs:

- Logical Left Shift
- Logical Right Shift

using:

- 74LS194 Universal Shift Registers

## Output Selection Unit

The final output is selected using:

- 74LS157 Multiplexers

and displayed through LEDs.

---

# Operation Selection

The operation mode is selected using two control bits.

| Control Bits | Operation |
|---|---|
| 00 | Addition |
| 01 | Subtraction |
| 10 | Right Shift |
| 11 | Left Shift |

The selection logic is implemented using the 74LS139 decoder.

---

# Circuit Overview

Complete Proteus circuit schematic:

![Circuit Overview](images/circuit-overview.png)

---

# Hardware Implementation

The circuit was physically implemented using:

- TTL Integrated Circuits
- Breadboards
- LEDs
- Switches
- Clock input

Hardware implementation:

![Hardware Implementation](images/hardware-implementation.jpg)

---

# Components Used

| Component | Description |
|---|---|
| 74LS139 | 2-to-4 Decoder |
| 74LS283 | 4-bit Binary Full Adder |
| 74LS194 | Universal Shift Register |
| 74LS86 | XOR Gate |
| 74LS157 | Multiplexer |
| LEDs | Output Display |
| Push Button | Clock Signal |
| DPDT Switch | Operation Control |

---

# Decoder Unit

## 74LS139 Decoder

The decoder is responsible for generating control signals for different operation modes.

The decoder controls:

- Arithmetic mode selection
- Shift mode selection
- Output selection

---

# Arithmetic Unit

The arithmetic unit is designed using two 74LS283 4-bit binary adders connected together to create an 8-bit arithmetic processor.

The carry output of the first adder is connected to the carry input of the second adder.

---

# Addition Operation

During addition:

- XOR gates transfer operand B without modification.
- Carry input is set to zero.

The operation performed is:

A + B

---

# Subtraction Operation

Subtraction is implemented using two's complement arithmetic.

The circuit performs:

A - B = A + (~B) + 1

During subtraction:

- XOR gates invert operand B.
- Carry input is set to one.
- The adders perform subtraction.

---

# XOR Control Logic

The XOR gates control the second operand.

Addition:

B XOR 0 = B

Subtraction:

B XOR 1 = NOT(B)

---

# Shift Register Unit

The shifting section uses two 74LS194 universal shift registers.

The 74LS194 supports:

- Parallel Load
- Right Shift
- Left Shift
- Clock Controlled Operation

---

# Right Shift Operation

In right shift operation, the bits move toward the least significant bit.

Example:

ABCDEFGH → 0ABCDEFG

---

# Left Shift Operation

In left shift operation, the bits move toward the most significant bit.

Example:

ABCDEFGH → BCDEFGH0

---

# Output Multiplexer

The output stage uses 74LS157 multiplexers.

The multiplexer selects the final result between:

- Arithmetic output
- Shift register output

The final 8-bit output is displayed using LEDs.

---

# Proteus Simulation

The complete circuit was simulated using Proteus Design Suite.

The simulation verifies:

- Correct operation selection
- Arithmetic calculations
- Shift operations
- Output behavior

![Proteus Simulation](images/proteus.png)

---

# Practical Testing

After successful simulation, the circuit was implemented practically.

The hardware implementation successfully demonstrates:

- Addition
- Subtraction
- Right Shift
- Left Shift

---

# Demo Video

The demonstration video is available at:

demo/8-bit-arithmetic-shift-unit-demo.mp4

---

# Repository Structure

The repository contains:

| Folder | Description |
|---|---|
| demo | Demonstration video |
| documentation | Project report files |
| images | Circuit and hardware images |
| simulation | Proteus simulation project |

Main files:

| File | Description |
|---|---|
| arithmetic_shift_unit.pdsprj | Proteus simulation project |
| project-report-fa.pdf | Project report |
| 8-bit-arithmetic-shift-unit-demo.mp4 | Project demonstration |

---

# How to Run Simulation

1. Install Proteus Design Suite.

2. Open the Proteus project:

simulation/arithmetic_shift_unit.pdsprj

3. Run the simulation.

4. Select different operations using the control switches.

5. Observe the output LEDs.

---

# Results

| Function | Status |
|---|---|
| Addition | Successfully Tested |
| Subtraction | Successfully Tested |
| Right Shift | Successfully Tested |
| Left Shift | Successfully Tested |

---

# Conclusion

This project demonstrates the design and implementation of an 8-bit Arithmetic Shift Unit using TTL digital logic components.

The system combines:

- Decoder circuits
- Binary adders
- XOR gates
- Shift registers
- Multiplexers

to create a complete multifunctional digital processing unit.

This project provides practical experience in digital system design, simulation, and hardware implementation.

---

# Author

**Arghavan Memari**

Digital Systems Course Project
