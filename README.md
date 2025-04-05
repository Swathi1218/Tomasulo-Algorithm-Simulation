# Tomasulo-Algorithm-Simulation
A Python simulator for Tomasulo’s algorithm with dynamic scheduling, register renaming, and out-of-order execution. Supports integer and floating-point operations, realistic latencies, and detailed cycle-by-cycle tracking of CPU state.

## Features

- ✅ Out-of-order execution
- ✅ Register renaming
- ✅ Load/store buffers
- ✅ Integer and floating-point operation support
- ✅ Configurable execution latencies
- ✅ Detailed cycle-by-cycle simulation output

## Instruction Support

- Integer: Add, Sub, Mul, Div
- Floating-point: Add, Sub, Mul, Div
- Logical: AND, OR, XOR
- Load/Store operations

## Architecture Overview

- 16 Integer Registers
- 16 Floating-Point Registers
- 2 Load Buffers, 2 Store Buffers
- Reservation Stations:
  - 2 Logical
  - 2 Integer Add
  - 2 Integer Mul
  - 4 FP Add
  - 4 FP Mul

## Execution Latencies

| Operation       | Latency (cycles) |
|----------------|------------------|
| Load/Store     | 1                |
| Logical        | 1                |
| Int Add        | 6                |
| Int Sub        | 10               |
| Int Mul        | 12               |
| Int Div        | 16               |
| FP Add         | 18               |
| FP Sub         | 24               |
| FP Mul         | 30               |
| FP Div         | 40               |

## Assumptions

- Subtraction is performed using addition units.
- Division is handled by multiplication units.
- Issue stage takes 0 cycles.
- No control hazards (e.g., no branches, jumps, or speculation).
- No branch prediction or speculative execution.
- Load/store instructions specify both register and memory address.
- Memory operations are assumed to be conflict-free and execute in-order.

## Improvements and Future Work

- Branch prediction and speculative execution
- Control hazard handling with support for conditional branches
- Support for program counters and jumps
- Input parsing for assembly-like instruction formats

## Usage

1. Clone the repo:
   ```bash
   git clone https://github.com/Swathi1218/tomasulo-simulator.git
   cd tomasulo-simulator
Run the simulation:

python tomasulo_simulator.py
View output in terminal or from the generated output file.
