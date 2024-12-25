# risc-v

This repo contains the design files of
## a soft processor implementing RISC-V RV32I with Verilog HDL
The components of the processor are implemented with individual Verilog HDL files. The top-level Verlog HDL file is rv32i_cpu.v. The processor is a 5-stage pipeline with fowarding and hazard detection units. For convenience of simulation in ModelSim/Questa, the design modules of register file and memory are merged into the top-level file. Register contents can be monitored with either their index number (genregs[0]-genregs[31]), or their names in RISC-V calling convention (ra, gp, a0-a7, etc).   
## a soft processor synthesizable in Intel Quartus Prime
## a Python-based assembler
## an custom FPGA evaluation board
## example RISC-V assembly programs to run on the soft processor
