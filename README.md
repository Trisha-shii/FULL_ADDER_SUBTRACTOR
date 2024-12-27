# FULL_ADDER_SUBTRACTOR #

Implementation-of-Full-Adder-and-Full-subtractor-circuit.

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor:**

**Full Adder:**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor:**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Truthtable:**

![image](https://github.com/user-attachments/assets/a6a8b5ed-cf99-49e0-baaa-28ab66f23f07)


![image](https://github.com/user-attachments/assets/76e40b6e-523f-4c29-beb5-7e72b80ee65e)


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. /*

Developed By:  Trisha Priyadarshni Parida

Register No:  212224230293

```
i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^c);
assign carry= ( (a & b)| ( cin &(a ^ b ));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));
endmodule
```

**RTL:**

<img width="709" alt="EXP 4 DE FA RTL" src="https://github.com/user-attachments/assets/36737466-76d2-4785-bb1a-f5bdad18ad2d" />

<img width="649" alt="EXP 4 DE FS RTL" src="https://github.com/user-attachments/assets/4df5543a-6c84-43a9-a21f-48901901e278" />


**Timing Waveform:**

<img width="958" alt="EXP 4 DE FA WF" src="https://github.com/user-attachments/assets/0ebdf140-7439-4d6c-8180-740bc3e0556d" />

<img width="957" alt="EXP 4 DE FS WF" src="https://github.com/user-attachments/assets/16544a2b-ffcf-4500-b531-88619c41d47c" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



