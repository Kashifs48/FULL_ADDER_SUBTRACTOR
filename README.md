Name: SYED KASHIF S

Register Number: 24006084

EXP4: FULL ADDER AND SUBTRACTOR
Implementation-of-Full-Adder-and-Full-subtractor-circuit

AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

Full Adder and Full Subtractor

Full Adder

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin

Carry = AB + ACin + BCin

![image](https://github.com/user-attachments/assets/82548aa8-3582-4ecb-bcc1-3c8d9ee5590d)


Figure -1 FULL ADDER

Full Subtractor

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/user-attachments/assets/6b4c85d8-a181-43f5-a1b1-69d2ddb33245)


Diff = A ⊕ B ⊕ Bin

Borrow out = A'Bin + A'B + BBin

Truthtable

Full Adder

![image](https://github.com/user-attachments/assets/c5caad03-c92d-4128-b5b7-c88cacc13e82)


Full Subtractor
![image](https://github.com/user-attachments/assets/8154369a-2aed-4fcc-9836-d71c3e4e6901)



Procedure

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Full Adder

module fadd(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
wire w1,w2,w3;
assign sum=a^b^c;
assign w1=a&b;
assign w2=b&c;
assign w3=c&a;
assign carry=w1|w2|w3;
endmodule 
Full Subtractor

module fsub(a, b, bin, diff, borrow);
input a, b, bin;
output diff, borrow;
wire w1, w2, w3, w4;
xor g1(diff, a, b, bin);
not g2(w1, a);          
and g3(w2, w1, bin);    
and g4(w3, w1, b);     
and g5(w4, b, bin);     
or g6(borrow, w2, w3, w4); 
endmodule
RTL Schematic

Full Adder
![image](https://github.com/user-attachments/assets/d8a00fdf-dcec-4105-806d-3bfc7ce1b371)


Full Subtractor

![image](https://github.com/user-attachments/assets/1c8d74ba-7b72-4d7c-baf2-f8ef0c865f43)

Output Timing Waveform

Full Adder

![image](https://github.com/user-attachments/assets/39e8eb3e-5b17-4564-a8f7-00060ab4859c)


Full Subtractor

![Screenshot 2024-11-26 102204](https://github.com/user-attachments/assets/d23800ac-93c8-433a-ae85-efe09982eee7)


Result:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
