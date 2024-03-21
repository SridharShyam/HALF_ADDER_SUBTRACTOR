Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

HALFADDER:

![image](https://github.com/SridharShyam/HALF_ADDER_SUBTRACTOR/assets/144871368/9c17c044-c00e-4e5c-a155-bd1ed2562911)

HALFSUBTRACTOR:

![image](https://github.com/SridharShyam/HALF_ADDER_SUBTRACTOR/assets/144871368/700fa719-8bf8-4fa0-a869-8ea25f497272)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.*/
```
Developed by: SHYAM S
RegisterNumber: 212223240156

HALFADDER:

module halfadder(a,b,sum,carry);
input a,b;
output sum,carry; 
assign sum=a^b;
assign carry=a & b;
endmodule

HALFSUBTRACTOR:

module halfsubtractor(a,b,D,Bo);
input a,b;
output D,Bo;
assign D=a ^ b;
assign Bo=~a & b;
endmodule
```


**RTL Schematic**

HALFADDER:

![Screenshot 2024-03-19 084016](https://github.com/SridharShyam/HALF_ADDER_SUBTRACTOR/assets/144871368/0983be68-f3b9-465b-ab47-efa4e2cd95a0)

HALFSUBTRACTOR:

![Screenshot 2024-03-21 083636](https://github.com/SridharShyam/HALF_ADDER_SUBTRACTOR/assets/144871368/07edfbb6-9585-4cd5-93d0-1b4618c557b9)

**Output/TIMING Waveform**

HALFADDER:

![Screenshot (82)](https://github.com/SridharShyam/HALF_ADDER_SUBTRACTOR/assets/144871368/fd98871d-61de-4903-8549-c07a8e534325)

HALFSUBTRACTOR:

![Screenshot (90)](https://github.com/SridharShyam/HALF_ADDER_SUBTRACTOR/assets/144871368/70e6fff9-8ab0-482d-b2c0-09fd5ba56f73)

**Result:**

Thus, the Half-Adder-and-Half Subtractor-circuit is implemented successfully.
