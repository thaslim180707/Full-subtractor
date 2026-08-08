# Full Subtractor using Verilog HDL

## Overview

A Full Subtractor is a combinational logic circuit that subtracts two binary bits along with a borrow input.

Inputs:
- A (Minuend)
- B (Subtrahend)
- Bin (Borrow Input)

Outputs:
- Difference (Diff)
- Borrow Out (Bout)

## Truth Table

| A | B | Bin | Diff | Bout |
|---|---|-----|------|------|
|0|0|0|0|0|
|0|0|1|1|1|
|0|1|0|1|1|
|0|1|1|0|1|
|1|0|0|1|0|
|1|0|1|0|0|
|1|1|0|0|0|
|1|1|1|1|1|

## Boolean Equations

Difference = A ⊕ B ⊕ Bin

Borrow Out = (~A & B) | (~A & Bin) | (B & Bin)

## Files

- full_subtractor.v → Verilog module
- full_subtractor_tb.v → Testbench
- simulation_result.png → Simulation waveform

## Software Used

- Verilog HDL
- Icarus Verilog
- ModelSim / Vivado Simulator
- GTKWave (optional)

## How to Run

Compile:

iverilog -o full_subtractor full_subtractor.v full_subtractor_tb.v

Run:

vvp full_subtractor

Generate waveform:

gtkwave full_subtractor.vcd

## Expected Output

A B Bin | Diff Bout

0 0 0 | 0 0
0 0 1 | 1 1
0 1 0 | 1 1
0 1 1 | 0 1
1 0 0 | 1 0
1 0 1 | 0 0
1 1 0 | 0 0
1 1 1 | 1 1

## Author

Your Name

