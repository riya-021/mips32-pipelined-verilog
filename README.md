MIPS32 Processor with Pipelining
Project Overview
This project implements a MIPS32 processor in a pipelined fashion using the Verilog hardware description language. The processor supports a variety of operations, including arithmetic, selection, branching, memory operations, and halting. The project also includes three test cases to validate the functionality and performance of the processor.

Key Features:
Pipeline Architecture: Implements instruction pipelining for improved performance.

Supported Instructions:

Arithmetic Operations:
ADD: Addition
SUBTRACT: Subtraction
MULTIPLY: Multiplication
Immediate Operations:
ADD IMMEDIATE
SUBTRACT IMMEDIATE
SELECT IMMEDIATE
Memory Operations:
LOAD: Load data from memory
STORE: Store data to memory
Branching:
BRANCH
Control:
HALT
Test Cases: Includes three comprehensive test cases to demonstrate and verify the processor’s functionality.

Getting Started
Prerequisites
To run this project, you will need:

A Verilog simulator (e.g., ModelSim, Xilinx Vivado, or Icarus Verilog)
A waveform viewer for analyzing the pipeline stages (e.g., GTKWave)
Running the Simulation
Clone the repository:
git clone <repository_url>
cd project
Open the desired test case file from the testbench/ directory.
Compile the Verilog files and the testbench using your simulator:
vlog src/*.v testbench/test_case_1.v
vsim -c -do "run -all"
View the simulation results in the waveform viewer.
Analyzing Test Cases
Test Case 1: Verifies basic arithmetic operations (ADD, SUBTRACT, MULTIPLY).
Test Case 2: Tests immediate operations (ADD IMMEDIATE, SUBTRACT IMMEDIATE, SELECT IMMEDIATE).
Test Case 3: Focuses on branching, memory operations (LOAD, STORE), and halting instructions (BRANCH, HALT).
How It Works
Pipelining Stages
The processor implements a 5-stage pipeline:

Instruction Fetch (IF): Fetches the instruction from memory.
Instruction Decode (ID): Decodes the instruction and reads registers.
Execute (EX): Performs arithmetic/logic operations or calculates branch targets.
Memory Access (MEM): Accesses data memory if required.
Write Back (WB): Writes results back to the register file.
Control Signals
The control unit generates appropriate signals for each stage, ensuring proper operation and handling hazards when required.

Testing and Verification
The processor has been tested against three test cases, covering:
Functional correctness of supported instructions.
Handling of immediate values.
Proper branching, memory operations, and halting behavior.
Waveforms generated during simulations provide a visual verification of pipeline execution.
