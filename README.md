# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
### Hardware – PCs, Cyclone II , USB flasher
### Software – Quartus prime


## Theory
+ A combinational logic circuit implement logical functions where its outputs depend only on its current combination of input values. On the other hand sequential circuits, unlike combinational logic, have state or memory.
+ Some logic operations may require more than one logic gate. Different combinations of gates are designed for different operations. The behaviour of the combined logic gates can be determined by constructing a truth table of the combined gates.

## Logic Diagram
![logic diagram](https://user-images.githubusercontent.com/130548870/234523906-0663ec62-983e-4177-b638-d092239a7c02.png)



## Procedure
1. Create a project with required entities.
2. Create a module along with respective file name.
3. Run the respective programs for the given boolean equations.
4. Run the module and get the respective RTL outputs.
5. Create university program(VWF) for getting timing diagram.
6. Give the respective inputs for timing diagram and obtain the results
## Program:
```verilog
Program For F1

module combilogic(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire G1,G2,G3,G4,G5;
assign G1=((~A)&(~B)&(~C)&(~D));
assign G2=((A)&(~C)&(~D));
assign G3=((~B)&(C)&(~D));
assign G4=((~A)&(B)&(C)&(D));
assign G5=((B)&(~C)&(D));
assign F1=G1|G2|G3|G4|G5;
endmodule
```
```verilog
Program For F2

module combilogic(W,X,Y,Z,F);
input W,X,Y,Z;
output F;
wire G6,G7,G8,G9,G10;
assign G6=((X)&(~Y)&(Z));
assign G7=((~X)&(~Y)&(Z));
assign G8=((~W)&(X)&(Y));
assign G9=((W)&(~X)&(Y)); 
assign G10=((W)&(X)&(Y));
assign F=G6|G7|G8|G9|G10;
endmodule
```


```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by:AKASH R 
RegisterNumber:212222050005  
```


## Output:
### output for F1
## RTL
![rtl](https://user-images.githubusercontent.com/130548870/234524817-642aba98-e83f-4b77-be06-9bc327c390ed.png)

## Timing Diagram
![td](https://user-images.githubusercontent.com/130548870/234524832-e4e01651-1e34-410b-8c82-d83c44059686.png)

### output for F2
## RTL
![rtl-2](https://user-images.githubusercontent.com/130548870/234524856-cb4e681d-d5a1-44e9-b1b7-6d70ab9531f8.png)

## Timing Diagram
![td-2](https://user-images.githubusercontent.com/130548870/234524888-c969cf97-9016-44f2-9849-8e1b3db59264.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
