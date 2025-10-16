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

full adder 

<img width="347" height="201" alt="image" src="https://github.com/user-attachments/assets/f3360d42-5c33-4962-a17e-84a8b01d7a0e" />

full subractor 

<img width="350" height="200" alt="image" src="https://github.com/user-attachments/assets/1637eb4f-b8be-404b-a91e-41f2e2d6e61c" />



**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.


**Program:**

```i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:R Tharun Rathish

RegisterNumber:25018411

Date:20/09/25
*/

**RTL Schematic**

full adder

<img width="350" height="178" alt="image" src="https://github.com/user-attachments/assets/48f243d9-d73e-4b1c-bb6b-67f4cd22bc41" />

full subractor

<img width="347" height="166" alt="image" src="https://github.com/user-attachments/assets/533c5e88-2fe3-419d-bd9d-41bd25d8b525" />







**Output Timing Waveform**

full adder

<img width="351" height="188" alt="image" src="https://github.com/user-attachments/assets/e4c7ff98-6761-4c42-95cf-343fd4a170ef" />

full subractor

<img width="351" height="191" alt="image" src="https://github.com/user-attachments/assets/e36485c4-6548-4ffc-aa8a-cda63d031d31" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



