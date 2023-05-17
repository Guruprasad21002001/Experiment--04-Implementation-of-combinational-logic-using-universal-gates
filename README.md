# Experiment--02-Implementation-of-combinational-logic...

Implementation of combinational logic gates
 
## AIM:

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher.

Software – Quartus prime.

## Theory:
 
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

## Using NAND gates:

NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram:

![out1](https://user-images.githubusercontent.com/93427534/234936628-83a6ce0f-99e9-487f-825f-f1d5b826b8d1.png)

## Using NOR gates:

NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram:

![out2](https://user-images.githubusercontent.com/93427534/234947763-464e19ba-ba01-4d69-a228-c93e441b138c.png)

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


## Truth Table of NAND gate:

![screenshot 2](https://github.com/Guruprasad21002001/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/95342910/a3047f1c-3c56-41f8-9875-7ca1ca2c3125)


## Truth Table of NOR gate:

![screenshot 3](https://github.com/Guruprasad21002001/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/95342910/f0d9551b-9da7-48eb-94c7-6f406e7ab689)


## Timing Diagram:

![Screenshot 4](https://github.com/Guruprasad21002001/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/95342910/1e3d5126-9c6b-4ca7-8442-375d19899962)



## Result:

Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.

