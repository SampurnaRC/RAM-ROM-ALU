# 8-bit RAM Design

## What is RAM?

Random Access Memory (RAM) is used to store data temporarily in digital systems.
It allows both read and write operations using an address.

---

## How is RAM used?

RAM is used to:

* Store intermediate data
* Allow fast access during computation
* Support read and write operations in real time

---

## Types of RAM Implemented

This project includes:

* Single-Port RAM
* Dual-Port RAM

---

# Single-Port RAM

## Description

Single-Port RAM has one access port.

This means:

* Only one operation can occur at a time
* Either read or write

---

## Operation

| we | Action                 |
| -- | ---------------------- |
| 1  | Write data into memory |
| 0  | Read data from memory  |

---

## Code Explanation

### Memory Declaration

```verilog
reg [7:0] mem [0:255];
```

* 256 locations
* Each stores 8 bits

---

### Write Operation

```verilog
if (we)
    mem[addr] <= data_in;
```

* When `we = 1`, data is written to memory

---

### Read Operation

```verilog
data_out <= mem[addr];
```

* Outputs data stored at given address

---

# Dual-Port RAM

## Description

Dual-Port RAM has two independent ports.

This allows:

* Simultaneous read and write
* Parallel memory access

---

## Operation

* Port 1 and Port 2 can operate independently
* Both can read or write at the same time

---

## Code Explanation

### Memory Declaration

```verilog
reg [7:0] mem [0:255];
```

---

### Port 1

```verilog
if (we1)
    mem[addr1] <= data_in1;

data_out1 <= mem[addr1];
```

---

### Port 2

```verilog
if (we2)
    mem[addr2] <= data_in2;

data_out2 <= mem[addr2];
```

---

## Key Difference

| Feature     | Single-Port RAM | Dual-Port RAM |
| ----------- | --------------- | ------------- |
| Ports       | 1               | 2             |
| Operations  | One at a time   | Simultaneous  |
| Complexity  | Simple          | More complex  |
| Performance | Lower           | Higher        |

---

## Simulation

Both designs are tested using Verilog testbenches to verify:

* Read operation
* Write operation
* Correct data storage
* Timing behavior

---

## Waveforms

### Single-Port RAM

![Single Port RAM](sim/single_port_ram_waveform.png)

### Dual-Port RAM

![Dual Port RAM](sim/dual_port_ram_waveform.png)

---

## Project Structure

```text
ram/
 ├── rtl/
 │   ├── single_port_ram.v
 │   └── dual_port_ram.v
 ├── tb/
 │   └── ram_tb.v
 ├── sim/
 │   ├── single_port_ram_waveform.png
 │   └── dual_port_ram_waveform.png
 └── README.md
```

---
