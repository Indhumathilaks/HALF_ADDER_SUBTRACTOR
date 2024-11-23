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

![Screenshot 2024-11-23 184703](https://github.com/user-attachments/assets/c1af0531-4a62-4819-bbc5-f7d2ed36d804)



**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: L INDHUMATHI 24900500

 **Half_adder**

 ```
 module halfadd_top(a,b,sum,carry);
 input a,b;
 output sum,carry; 
assign sum = a^b;
 assign carry = a & b;
 endmodule
```

 **Half_subtractor**

 ```
 module halfsub_top(a,b,D,Bo);
 input a,b;
 output D,Bo; 
 assign D = a ^ b;
 assign Bo = ~a & b;
 endmodule
```

**RTL Schematic**

**HALF ADDER**

![Screenshot 2024-11-23 191544](https://github.com/user-attachments/assets/50ff829c-7114-4e52-bc04-5c47fae24ecb)


**HALF SUBTRACTOR**

![Screenshot 2024-11-23 192155](https://github.com/user-attachments/assets/5e9c7ffc-9fca-4022-aefb-e667ecca31fc)



**Output/TIMING Waveform**

**HALF ADDER**

![Screenshot 2024-11-23 194025](https://github.com/user-attachments/assets/26c80179-3459-4df8-8da5-260bd94814f8)



**HALF SUBTRACTOR**

![Screenshot 2024-11-23 182720](https://github.com/user-attachments/assets/43a532d5-26c8-4608-97ce-b15884f8934c)


**Result:**

Thus the half adder and half subtractor circuit are implemented using and their operations are verified using Verilog programming.
