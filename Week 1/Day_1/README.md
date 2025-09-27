Day 1: Introduction to Verilog RTL Design \& Synthesis - My Learning Chronicle

1. Understanding Simulation Fundamentals
   Today I began by establishing the fundamental concepts of digital design verification. I learned that:

A simulator serves as a software tool that enables me to validate my digital circuits by applying test inputs and observing corresponding outputs, providing crucial verification before physical implementation.

The design represents my actual Verilog code that defines the logical functionality I intend to create.

A testbench functions as a simulation environment that systematically applies various input combinations to my design and verifies the correctness of the outputs.

This understanding formed the foundation for my subsequent practical work.

2. Initial Setup with Icarus Verilog
   I proceeded to configure my simulation environment using the open-source tool Icarus Verilog (iverilog). The simulation workflow I implemented follows this sequence:

Providing both the design and testbench as inputs to iverilog

Generating a .vcd file containing waveform data

Visualizing the results using GTKWave

This setup provided me with a complete verification pipeline for my digital designs.

3. Practical Lab: 2-to-1 Multiplexer Simulation
   Implementation Steps
   I began by cloning the workshop repository to access the necessary files:


git clone https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git
cd sky130RTLDesignAndSynthesisWorkshop/verilog\_files
After installing the required tools (iverilog and gtkwave), I compiled and simulated the multiplexer design:


iverilog good\_mux.v tb\_good\_mux.v
./a.out
gtkwave tb\_good\_mux.vcd
The waveform visualization in GTKWave confirmed the correct functionality of my multiplexer design, showing the proper selection between inputs i0 and i1 based on the sel signal.

4. Verilog Code Examination
   I analyzed the multiplexer implementation in good\_mux.v:

verilog
module good\_mux (input i0, input i1, input sel, output reg y);
always @ (\*)
begin
if(sel)
y <= i1;
else
y <= i0;
end
endmodule
This examination revealed how the design uses:

Input signals i0 and i1 as data inputs

Select signal sel to determine the output path

Registered output y that updates based on the select signal condition

Combinational logic triggered by any input change using the always @ (\*) construct

5. Introduction to Logic Synthesis with Yosys
   I explored Yosys as a synthesis tool that transforms my Register Transfer Level (RTL) descriptions into gate-level netlists. My investigation revealed that Yosys provides:

Synthesis capabilities for converting HDL to logic circuits

Optimization features to improve speed or reduce area

Technology mapping to match logic elements with physical library cells

Verification tools to ensure design correctness

Extensible architecture supporting custom design flows

Understanding Gate Library Variants
I discovered that standard cell libraries contain multiple versions of basic gates with different characteristics to address various design constraints:

Performance optimization through faster gates for critical paths

Power efficiency using low-energy consumption gates

Area reduction with compact gate implementations

Drive strength variations to handle different load requirements

Signal integrity considerations for noise-sensitive applications

This variety enables synthesis tools to select the most appropriate gate implementations based on specific design requirements.

6. Synthesis Laboratory Exercise
   I conducted my first synthesis operation using Yosys with the following procedure:

Synthesis Flow Implementation
Initialized Yosys environment


yosys
Loaded the technology library


read\_liberty -lib /address/to/your/sky130/file/sky130\_fd\_sc\_hd\_\_tt\_025C\_1v80.lib
Read my Verilog design file


read\_verilog /home/vsduser/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog\_files/good\_mux.v
Performed synthesis targeting the good\_mux module


synth -top good\_mux
Executed technology mapping


abc -liberty /address/to/your/sky130/file/sky130\_fd\_sc\_hd\_\_tt\_025C\_1v80.lib
Generated and examined the gate-level schematic


show
The resulting schematic visualization demonstrated how my behavioral Verilog code was successfully transformed into an optimized gate-level implementation using standard cells from the library.

7. Day 1 Summary
   Today's session provided me with comprehensive hands-on experience in:

Establishing the relationship between designs, testbenches, and simulators

Implementing functional verification using Icarus Verilog and GTKWave

Analyzing Verilog code for a fundamental multiplexer circuit

Understanding the role and capabilities of the Yosys synthesis tool

Performing my first complete RTL-to-gates synthesis flow

This foundation prepares me for more advanced digital design concepts in the upcoming sessions.

