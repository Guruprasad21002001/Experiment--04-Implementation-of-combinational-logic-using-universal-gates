# Experiment--02-Implementation-of-combinational-logic...
 
## AIM:

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher.

Software – Quartus prime.

## Procedure:

1) Create a project with required entities.
2) Create a module along with respective file name.
3) Run the respective programs for the given boolean equations.
4) Run the module and get the respective RTL outputs.
5) Create university program(VWF) for getting timing diagram.
6) Give the respective inputs for timing diagram and obtain the results.

## Program:

```c
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Guru Prasad.B
RegisterNumber: 212221230032

module combination(a,b,c,d,w,x,y,z,fl,f2);
input a,b,c,d,w,x,y,z;
output fl,f2;
wire g1=((~a)&(~b)&(~c)&(~d)); 
wire g2=((a)&(~c)&(~d));
wire g3=((~b)&(c)&(~d));
wire g4=((~a)&(b)&(c)&(d)); 
wire g5=((b)&(~c)&(d));
assign fl=g1|g2|g3|g4|g5; 
wire g6=((x)&(~y)&(z));
wire g7=((~x)&(~y)&(z));
wire g8=((~w)&(x)&(y)); 
wire g9=((w)&(~x)&(y));
wire g10=((w)&(x)&(y)); 
assign f2=g6|g7|g8|g9|g10;
endmodule

```

## Output:

## RTL realization of NAND and NOR gates:

![Screenshot 2023-05-17 135815](https://github.com/Guruprasad21002001/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/95342910/5df2e29c-367e-4508-884b-65db4d1fbc96)


## Timing Diagram:

![Screenshot 4](https://github.com/Guruprasad21002001/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/95342910/1e3d5126-9c6b-4ca7-8442-375d19899962)



## Result:

Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.

