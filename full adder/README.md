# Verilog Full Adder

## Overview
A Full Adder is a combinational logic circuit that adds three binary inputs:

- A
- B
- Cin (Carry Input)

It produces:

- Sum
- Cout (Carry Output)

## Truth Table

| A | B | Cin | Sum | Cout |
|---|---|-----|-----|------|
|0|0|0|0|0|
|0|0|1|1|0|
|0|1|0|1|0|
|0|1|1|0|1|
|1|0|0|1|0|
|1|0|1|0|1|
|1|1|0|0|1|
|1|1|1|1|1|

## Logic Equations

Sum = A ^ B ^ Cin

Cout = (A & B) | (B & Cin) | (A & Cin)

## Files

- full_adder.v → Verilog design
- full_adder_tb.v → Testbench
- simulation_output.png → Simulation waveform

## Simulation

Compile

```bash
iverilog full_adder.v full_adder_tb.v -o fulladder
```

Run

```bash
vvp fulladder
```

Generate Waveform

```bash
gtkwave fulladder.vcd
```

## Output

The simulation verifies all possible combinations of A, B, and Cin.