# 8-Bit Arithmetic and Shift Unit

An 8-bit digital arithmetic and shift unit designed as a university Digital Systems course project.

The circuit supports four operations: **addition, subtraction, right shift, and left shift**. The design was developed and simulated in **Proteus** and was also implemented as a physical circuit using digital logic ICs.

## Features

- 8-bit data processing
- Addition
- Subtraction using two's-complement logic
- Right shift
- Left shift
- 2-bit operation selection
- Proteus simulation
- Physical hardware implementation

## Operation Selection

The required operation is selected using two control bits.

| Control Input | Operation |
|---|---|
| `00` | Addition |
| `01` | Subtraction |
| `10` | Right Shift |
| `11` | Left Shift |

## Circuit Architecture

The arithmetic section is implemented using two cascaded 4-bit binary adders to create an 8-bit arithmetic path.

For subtraction, XOR gates are used to invert the required operand, while the carry input is used to implement two's-complement subtraction.

The shift section is implemented using two 4-bit shift registers connected together to provide 8-bit left and right shift operations.

A decoder generates the control signals required to select the desired operation, and multiplexers are used to route the appropriate result to the output.

## Main Components

- 74LS139 Decoder
- 74LS283 4-bit Binary Adders
- 74LS194 Shift Registers
- 74LS86 XOR Gates
- 74LS157 Multiplexers
- LEDs
- Push Button / Clock Input
- DPDT Switch

## Proteus Simulation

The complete circuit was designed and tested using Proteus Design Suite.

![Circuit Overview](images/circuit-overview.png)

The Proteus project file is available here:

[Open Proteus Simulation](simulation/arithmetic_shift_unit.pdsprj)

## Hardware Implementation

The circuit was also physically implemented using breadboards and digital logic ICs.

![Hardware Implementation](images/hardware-implementation.jpg)

## Documentation

A Persian project report containing the circuit description, operation-selection logic, component information, and implementation details is included in the repository.

[View Project Report](documentation/project-report-fa.pdf)

## Project Structure

```text
8-Bit-Arithmetic-Shift-Unit/
│
├── README.md
│
├── simulation/
│   └── arithmetic_shift_unit.pdsprj
│
├── documentation/
│   └── project-report-fa.pdf
│
└── images/
    ├── circuit-overview.png
    └── hardware-implementation.jpg
