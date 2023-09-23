# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
Write the detailed procedure here

## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: ALFRED AB
RegisterNumber:  212222110002
```
### HALF SUBTRACTOR
```
module exp04(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff = a^b;
assign borrow =((~a)&b);
endmodule
```
### FULL SUBTRACTOR
```
module exp04(a,b,bin,diff,borrow);
input a,b,bin;
output diff,borr;
assign diff= a^b^bin;
assign borrow = ((~a)&b)|(b&bin)|((~a)&bin);
endmodule
```
## Output:

## Truthtable
## HALF SUBTRACTOR:
![266774508-5a03b027-62a4-4d5c-9701-6fc26011a4f4](https://github.com/Alfredsec/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/120621608/0287cea4-b4ad-40b8-9cef-49a762cca477)
## FULL SUBTRACTOR:
![266774519-7cda216c-b83f-4f64-bbc3-28daaa47429c](https://github.com/Alfredsec/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/120621608/589c781f-e943-41eb-b2d1-3b698b81a18a)

##  RTL realization
## HALF SUBTRACTOR:
![half](https://github.com/Alfredsec/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/120621608/1f3540fd-a6ba-4026-99ec-df099de942ab)
## FULL SUBTRACTOR:
![full](https://github.com/Alfredsec/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/120621608/1d9d31f0-742e-4fd2-8ff4-6066452cbfc3)

## WAVEFORM:
## HALF SUBTRACTOR:
![half waveform](https://github.com/Alfredsec/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/120621608/24797857-477f-4e7b-a4f4-a481757803b7)
## FULL SUBTRACTOR:
![full waveform](https://github.com/Alfredsec/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/120621608/0cec785b-1806-4ce8-bf4c-032d77305fa2)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
