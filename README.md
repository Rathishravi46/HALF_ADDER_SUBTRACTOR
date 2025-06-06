NAME:RATHISH.R

REG NO :24901297

Date: 15.04.2025

# HALF_ADDER_SUBTRACTOR

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

**Half Adder**

![ha truthtable](https://github.com/user-attachments/assets/e645e07f-f76b-498c-96d3-34508f909ba4)

**Half Subtractor**

![hs_truthtable](https://github.com/user-attachments/assets/ce483827-8f26-4ab8-b45e-4901325db982)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
module halfaddsub(a,b,sum,cout,diff,borr);

input a,b;

output sum,cout,diff,borr;

xor g1(sum,a,b);

and g2(cout,a,b);

wire w1;

xor g3(diff,a,b);

not g4(w1,a);

and g5(borr,w1,b);

endmodule
```

**RTL Schematic**


<img width="736" alt="Screenshot 2024-11-22 123519" src="https://github.com/user-attachments/assets/ff5e017c-d02b-4758-8c19-807bf6ef499e">


**Output/TIMING Waveform**

<img width="960" alt="Screenshot 2024-11-22 123811" src="https://github.com/user-attachments/assets/bb91ec5e-295f-4165-b9e0-2161797354ff">


**Result:**

hence, the design of half adder and half subtractor circuit studied and its truth table is verified in Quartus using Verilog programming.
