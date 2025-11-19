# FULL_ADDER_SUBTRACTOR

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

**Procedure**

Write the detailed procedure here

**Program:**
```
fulladder

module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=(a^b^c);
assign carry=(a&b)|(b&c)|(c&a);
endmodule

fullsub

module fullsub(a,b,bin,dif,bout);
input a,b,bin;
output dif,bout;
assign dif=a^b^bin;
assign bout=(a&b)|(bin&(a^b));
endmodule
```
**RTL Schematic**
<img width="1920" height="1200" alt="fulladder" src="https://github.com/user-attachments/assets/8ca2c35f-daab-4beb-acc7-b3bff0f3f951" />

<img width="1920" height="1200" alt="fullsub" src="https://github.com/user-attachments/assets/a729dc61-3bfe-4351-9ac5-6263a7d7e15c" />


**Output Timing Waveform**

<img width="1920" height="1200" alt="fulladd" src="https://github.com/user-attachments/assets/65124899-bcd2-4e1c-8f8a-1a2834892159" />

<img width="1920" height="1200" alt="fullsu" src="https://github.com/user-attachments/assets/c0c3d0ed-53b9-4ff7-957c-757ace2cd7f8" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



