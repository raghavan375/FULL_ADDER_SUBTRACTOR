Implementation-of-Full-Adder-and-Full-subtractor-circuit

*AIM:*

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

*Equipments Required:*

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

*Full Adder and Full Subtractor*

*Full Adder*

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

*Figure -1 FULL ADDER*

*Full Subtractor*

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

*Truthtable*

FULL ADDER:


![Full adder EXP 4 (3)](https://github.com/user-attachments/assets/a8fa1a11-bf57-449d-8e36-ddcef46bd61d)


FULL SUBTRACTOR:


![Full subtractor EXP 4 (3)](https://github.com/user-attachments/assets/6f6e3352-31be-4fc8-97b3-76c39a9e097a)




*Procedure*



1) Type the program in Quartus software
2) Compile and run the program
3) Generate the RTL schematic and save the logic diagram
4) Create nodes for inputs and outputs to generate the timing diagram
5) For different inputs combinations generate the timing diagram



*Program:*



FULL ADDER:

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

FULL SUBTRACTOR:

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule





Developed by:AAKIL AHAMED S 
Register Number:212224040002



*RTL Schematic*


FULL ADDER:



![Full adder EXP 4](https://github.com/user-attachments/assets/8a225dc4-7221-4fc3-bd03-79b4960c92b1)


FULL SUBTRACTOR:


![Full subtractor EXP 4](https://github.com/user-attachments/assets/51de4b6f-3e00-433d-a337-18a4f70280c2)


*Output Timing Waveform*


FULL ADDER:


![Full adder EXP 4 (2)](https://github.com/user-attachments/assets/9c077610-ba39-4925-8eab-14c9558e99b1)



FULL SUBTRACTOR:


![Full subtractor EXP 4 (2)](https://github.com/user-attachments/assets/acf81ac8-1c93-44e4-8585-617a49e9a414)


*Result:*

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
