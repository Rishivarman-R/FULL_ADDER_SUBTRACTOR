 FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
Full adder<br>
![WhatsApp Image 2024-11-12 at 10 24 46_dccfa330](https://github.com/user-attachments/assets/cc1fffd1-4898-48ce-a1bc-d95d290ac0b4)
Full sbtracter<br>
![WhatsApp Image 2024-11-12 at 10 22 49_d0fce231](https://github.com/user-attachments/assets/42577de2-3190-4059-81ef-09e4d7943b08)

**Procedure**
1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

Write the detailed procedure here

**Program:**
```
module exp4 a(df, bo, a, b, bin);
 output df;
 output bo;
 input a;
 input b; 
 input bin;
 wire w1,w2,w3;
 assign w1=a^b;
 assign w2=(~a&b);
 assign w3=(~w1&bin);
 assign df=w1^bin;
 assign bo-w2/w3;
 endmodule
module exp4a (df, bo, a, b, bin);
 output df;
 output bo;
 input a;
 input b;
 input bin;
 wire w1,w2, w3;
 assign w1=a^b;
 assign w2=(~a&b); 
 assign w3=(~w1&bin);
 assign df=w1^bin;
 assign bo=w2|w3;
 endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/24900419

**RTL Schematic**

Full adder<br>
![WhatsApp Image 2024-11-12 at 10 03 25_fe518936](https://github.com/user-attachments/assets/0c67dfbc-ce03-41dd-917e-e802f122aa69)

Full sbtracter<br>

![WhatsApp Image 2024-11-12 at 10 05 43_d1fe7f23](https://github.com/user-attachments/assets/c637d884-caf0-499c-89e3-a391eb05b433)

**Output Timing Waveform**
Full adder<br>
![Screenshot (19)](https://github.com/user-attachments/assets/a299f5fd-90d9-4b80-82ff-91d5a507ed35)
Full sbtracter<br>
![Screenshot (24)](https://github.com/user-attachments/assets/ca015316-dcf1-4f01-a8ff-e51401190fc2)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



