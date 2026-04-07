# Verilog Memory and ALU Design

## Overview

This project implements fundamental digital components using Verilog:

* 8-bit Arithmetic Logic Unit (ALU)
* 8-bit Single-Port RAM
* 8-bit Dual-Port RAM
* 8-bit ROM

Each module is designed, tested, and verified using simulation waveforms.

---

## What This Project Demonstrates

* Digital design using Verilog
* Memory design (RAM and ROM)
* Arithmetic and logic operations
* Simulation and waveform verification

---

## Modules

### ALU

The ALU performs arithmetic, logical, and shift operations.

Operations include:

* Addition and Subtraction
* AND, OR, XOR, NOT
* Logical Shift Left and Right

It also generates status flags:

* Carry
* Zero
* Sign
* Overflow

---

### RAM

#### Single-Port RAM

* One access port
* Supports either read or write at a time

#### Dual-Port RAM

* Two independent ports
* Allows simultaneous read/write operations

---

### ROM

* Read-only memory
* Stores predefined data
* Outputs data based on address

---

## Project Structure

```text id="k3d9gq"
verilog-memory-alu/
 ├── alu/
 │   ├── rtl/
 │   ├── tb/
 │   ├── sim/
 │   └── README.md
 │
 ├── ram/
 │   ├── rtl/
 │   ├── tb/
 │   ├── sim/
 │   └── README.md
 │
 ├── rom/
 │   ├── rtl/
 │   ├── tb/
 │   ├── sim/
 │   └── README.md
 │
 └── README.md
```

---

## Simulation

All modules are verified using:

* Testbenches written in Verilog
* Waveform analysis

Simulation tools used:

* EDA playground

---

## Waveforms

Each module contains its own waveform images inside its respective `sim/` folder.


---

## Key Concepts Covered

* Memory addressing
* Read/write operations
* Bitwise and arithmetic operations
* Flag generation in ALU
* Parallel memory access (dual-port RAM)

---

## Future Improvements

* Parameterized designs (configurable bit-width)
* Integration into a simple CPU


Your Name

