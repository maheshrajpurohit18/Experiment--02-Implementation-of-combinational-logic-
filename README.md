# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. ###Using NAND gates NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

###Using OR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms. F2=xy’z+x’y’z+w’xy+wx’y+wxy

### Procedure
## Step 1:

Create a project with required entities.

## Step 2:

Create a module along with respective file name.

## Step 3:

Run the respective programs for the given equations.

## Step 4:

Run the module and get the respective RTL outputs.

## Step 5:

Create university program(VWF) for getting timing diagram.

## Step 6:

Give the respective inputs for timing diagram and obtain the results.
## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Mahesh Raj Purohit.J
RegisterNumber: 212222240058 
*/

```
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
module EXP2a (a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1 = (~b&~d)|(~a&b&d)|(a&b&~c); 
endmodule

for F2=xy’z+x’y’z+w’xy+wx’y+wxy

module EXP2b (w,x,y,z,f2); 
input w,x,y,z; 
output f2;
assign f2 = (x&y)|(w&y)|(~y&z);
endmodule */
```
## RTL realization
## F1
![image](https://user-images.githubusercontent.com/119475943/233779704-2b0fbd70-e26f-4bc8-975c-66e843343575.png)
## F2
![image](https://user-images.githubusercontent.com/119475943/233779710-12c90d88-5a09-4893-b7ed-89fbff78b1b4.png)
## Output:
## Timing Diagram
## F1
![image](https://user-images.githubusercontent.com/119475943/233779663-0dab23b6-b7ce-4991-8577-4e474f732b40.png)

## F2
![image](https://user-images.githubusercontent.com/119475943/233779676-e5e92010-a115-4c80-bc84-1f2fa4c80862.png)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
