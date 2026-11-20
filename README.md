ECE 128 Lab 10 – ROM, Multiplier, and RAM System with Control Unit

Project Description

This project implements a complete system that reads two numbers from a ROM, multiplies them with a combinational multiplier, and writes the result into a RAM. A control unit, designed as a finite state machine, sequences the reading, multiplying, and writing stages and generates the addresses and enable signals for the other blocks. The design reuses the ROM, RAM, and combinational multiplier from earlier labs and connects them in a top module. The control unit moves through its states in order: waiting for the start signal, reading the first operand, reading the second operand, multiplying, writing the product to the RAM, and finishing. The top module is verified with a testbench and programmed on the Basys 3 board.

Simulation

1. Open the project in Vivado.
2. Add the ROM, RAM, combinational multiplier, control unit, and top module as design sources.
3. Add the text file containing the ROM data to the project, and make sure the file path used in the Verilog code points to it.
4. Add the top module testbench as a simulation source.
5. Set the testbench as the simulation top module.
6. Run Behavioral Simulation.
7. Verify from the waveform that the control unit moves through its states in order after start is applied, that the two operands are read from the ROM, that the multiplier output shows the correct product, and that the RAM stores the product at the result address when write enable is active.

FPGA Implementation

1. Select the Basys 3 as the target FPGA board.
2. Select the top module as the top module for implementation.
3. Add the Basys 3 constraints file and assign the clock, reset, and start signals to the board clock and buttons or switches, and the result to the LEDs or seven-segment display.
4. Run Synthesis.
5. Run Implementation.
6. Generate the Bitstream.
7. Connect and power the Basys 3.
8. Open Hardware Manager and program the FPGA with the generated bitstream.
9. Start the operation and verify that the displayed product matches the expected result for the operands stored in the ROM.
