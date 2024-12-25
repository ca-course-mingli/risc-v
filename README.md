# risc-v

This repo contains the design files of
## a soft processor implementing RISC-V RV32I with Verilog HDL
The components of the processor are implemented with individual Verilog HDL files. The top-level Verlog HDL file is rv32i_cpu.v. The processor is a 5-stage pipeline with fowarding and hazard detection units. For convenience of simulation in ModelSim/Questa, the design modules of register file and memory are merged into the top-level file. Register contents can be monitored with either their index number (genregs[0]-genregs[31]), or their names in RISC-V calling convention (ra, gp, a0-a7, etc). Memory contents are relayed to the output of the WB stage and can be monitored with mirror_mem signal. Other important internal signals, such as pc, instruction and ALU result, are relayed similarly as debug_pc, debug_ins and debug_res. In a typical simulation in ModelSim/Questa, users monitor signals such as clk, rst, debug_pc, debug_ins, debug_res, and any interested register and memory units.

A testbench block is embedded in rv32i_cpu.v as well. The simulated clock is 50 Mhz (20ns period) and the first 40 ns is set for reset. Therefore, the first instruction's result should be visible between 130 ns and 150 ns after the simulation begins. Refer to online tutorials on how to compile and simulate in ModelSim/Questa.  
## a soft processor synthesizable in Intel Quartus Prime

## a Python-based assembler
## an custom FPGA evaluation board
## example RISC-V assembly programs to run on the soft processor
