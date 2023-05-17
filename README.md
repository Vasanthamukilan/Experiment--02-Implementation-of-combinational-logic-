# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher,Software – Quartus prime
## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
## Procedure
1. Create a project with required entities.
2. Create a module along with respective file name.
3. Run the respective programs for the given boolean equations.
4. Run the module and get the respective RTL outputs.
5. Create university program(VWF) for getting timing diagram.
6. Give the respective inputs for timing diagram and obtain the results.
## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Vasanthamukilan.M
RegisterNumber: 212222230167
*/
module Combinational(A,B,C,D,W,X,Y,Z,F1,F2);
input A,B,C,D,W,Y,X,Z;
output F1,F2;
wire A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1 = ((~A)&(~B)&(~C)&(~D));
assign A2 = (A&(~C)&(~D));
assign A3 = ((~B)&C&(~D));
assign A4 = ((~A)&B&C&D);
assign A5 = (B&(~C)&D);
assign B1 = (X&(~Y)&Z);
assign B2 = ((~X)&(~Y)&Z);
assign B3 = ((~W)&X&Y);
assign B4 = (W&(~X)&Y);
assign B5 = (W&X&Y);
assign F1 = (A1|A2|A3|A4|A5);
assign F2 = (B1|B2|B3|B4|B5);
endmodule
```
## Output:
## RTL realization
## F1
![1](https://github.com/Vasanthamukilan/Experiment--02-Implementation-of-combinational-logic-/assets/119559694/14c17251-e38b-4549-988d-7ec3ef5ae4b9)
## F2
![2](https://github.com/Vasanthamukilan/Experiment--02-Implementation-of-combinational-logic-/assets/119559694/89ac0b45-5736-4787-b3f8-55c9eb2b39ef)
## Timing Diagram:
![Screenshot 2023-05-17 142015](https://github.com/Vasanthamukilan/Experiment--02-Implementation-of-combinational-logic-/assets/119559694/53ff394f-f7bd-4880-978f-7d8a5a5f2db2)
## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
