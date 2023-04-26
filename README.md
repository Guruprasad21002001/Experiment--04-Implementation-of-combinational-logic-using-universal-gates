Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates

AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

Logic Diagram
Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

Logic Diagram
Procedure
Program:
/* Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming. 
~~~
Developed by: Guruprasad.B 
RegisterNumber: 2122211230032
~~~
## Using NAND Operation:

~~~
module combine1(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule
~~~
## Using NOR Operation:
~~~
module combine2(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
assign F = ~S;
endmodule
~~~

## Output:
## NAND:
## RTL:

![op-1](https://user-images.githubusercontent.com/95342910/234519275-1bd03acb-0527-49eb-8272-a98d638c0d62.jpg)

## Truth Table:

![op-2](https://user-images.githubusercontent.com/95342910/234519308-28040d62-c799-4bd2-9609-386bc1d475eb.jpg)

## Timing Diagram:

![op-3](https://user-images.githubusercontent.com/95342910/234519360-1e2df646-272d-4623-8e72-5e9e6bce9ac7.jpg)

## NOR:
## RTL:

![op-4](https://user-images.githubusercontent.com/95342910/234519398-26f8e0f1-dcb4-4114-8aaa-33782fd401ba.jpg)

## Truth Table:

![op-5](https://user-images.githubusercontent.com/95342910/234519433-903f1efc-0159-46eb-8c3b-80838c26f3c8.jpg)

## Timing Diagram:

![op-6](https://user-images.githubusercontent.com/95342910/234519582-9c8fc5fe-efa4-4a78-9155-6312217af0fb.jpg)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.

