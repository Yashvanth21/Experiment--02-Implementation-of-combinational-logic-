### NAME:Yashvanth K
### Register number:23011613
## Experiment 02 Implementation of combinational logic
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
 
## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 
 Software – Quartus prime


## Theory
A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.

## Procedure
1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).
2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors:*
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6.Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output waveform

## Program:
```
module verilog(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire x1,x2,x3,x4,x5;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign F1=x1|x2|x3|x4|x5;
endmodule
```
## RTL realization
![experiment 2 RTL](https://github.com/Ashwathm12/Experiment--02-Implementation-of-combinational-logic-/assets/138849225/06169d68-8453-462b-a91a-708669471b8b)
## Truth table
![experiment 2 table](https://github.com/Ashwathm12/Experiment--02-Implementation-of-combinational-logic-/assets/138849225/b980ee4e-9c0c-46c8-bfab-1395ca58560c)

## Timing Diagram
![experiment 2 waveform](https://github.com/Ashwathm12/Experiment--02-Implementation-of-combinational-logic-/assets/138849225/a9853019-0754-44bf-a1b2-78a1173eea36)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
