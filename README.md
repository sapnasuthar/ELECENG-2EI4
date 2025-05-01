# ELECENG-2EI4
This repository collects my four design projects from McMaster University’s ELECENG 2EI4 course.Students learn transistor‑level design, simulation, and measurement techniques by building:

Project 1: DC Power Supplies
Project 2: Voltage‑Controlled MOSFET Switches
Project 3: Single‑Transistor Amplifiers
Project 4: CMOS Logic Gates

## Project 1: DC Power Supply
Objective: Convert a 120 V rms AC (simulated via AD3) to a regulated 3 V ± 0.1 V DC output delivering 10 mA.

### Components & Tools:
Hardware: Digilent AD3 function generator, full‑wave rectifier diodes, 25 µF RC filter (2×10 µF + 5×1 µF), 2×150 Ω series load
Simulation: LTSpice
Measurement: AD3 oscilloscope

### Approach:
1. Design calculations: turns ratio (22:1), diode drop, capacitor sizing for <0.2 V ripple
2. Simulation: transient analysis in LTSpice to predict performance
3. Hardware build: assemble on breadboard and adjust component values (e.g., 100 µF filter, 330 Ω resistor)
4. Measurement: scope screenshots to verify 2.9–3.1 V output

## Project 2: Voltage‑Controlled MOSFET Switches
Objective: Design two switches that behave as ideal on‑off elements; quantify real non‑idealities.

### Components & Tools:
Hardware: CD4007B MOSFET array, 470 kΩ resistors for pull‑downs
Simulation: LTSpice
Measurement: Digilent AD2 logic analyzer and voltage measurements

### Approach:
1. Research: define ideal switch properties (Ron, Ioff, bidirectionality)
2. Test plan: measure on‑state drop, off‑state leakage, voltage range
3. Build: create Switch 1 and Switch 2 circuits on breadboard
4. Verify: compare LTSpice waveforms with real measurements

## Project 3: Single‑Transistor Amplifier
Objective: Amplify a ±0.5 V source (100 Ω internal impedance) to drive a 100 Ω load with < 10 % attenuation.

### Components & Tools:
Hardware: 2N3904 BJT, biasing resistors, coupling capacitors
Simulation: LTSpice (transient and AC sweep)
Measurement: Digilent AD2 oscilloscope

### Approach:
1. Topology selection: common‑collector for unity gain and input impedance matching
2. Calculations: bias currents, small‑signal gain, input/output resistance
3. Simulation: determine gain, bandwidth, and linearity in LTSpice
4. Hardware: assemble on breadboard and record waveforms

## Project 4: CMOS XOR Gate
Objective: Implement a 2‑input CMOS XOR gate using MOSFETs; measure functionality and timing metrics.

### Components & Tools:
Hardware: CD4007B (6 NMOS + 6 PMOS), Digilent AD2 logic analyzer
Simulation: LTSpice
Measurement: AD2 logic and oscilloscope

### Approach:
1. Logic derivation: Y = A ⊕ B; apply De Morgan for PUN/PDN structure
2. Sizing: PMOS width 2.5× NMOS to match propagation delays
3. Build & test: verify truth table, static VH/VL, and measure τPLH/τPHL
