# Experiment--03-Half-Subtractor-and-Full-subtractor
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
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: KULASEKARAPANDIAN K
RegisterNumber: 212222240052

module half_sub(x, y, d, b, x1);
input x,y;
output x1, d, b;
xor(d, x, y);
not(x1, x);
and(b, x1, y);
endmodule

module full_sub(x, y, z, d, b, x1, x2, x3, x4, x5);
input x,y,z;
output d, b, x1, x2, x3, x4 ,x5;
xor(x1, x, y);
xor(d, x1, z);
not(x2, x);
and(x3, x2, y);
and(x4, x3, z);
and(x5, y, z);
or(b, x3, x4, x5);
endmodule
*/
```

## Output:

## Truthtable
![image](https://user-images.githubusercontent.com/113496887/233282266-fadb3829-9785-4f30-abe9-ea7334ad9685.png)




##  RTL realization
![image](https://user-images.githubusercontent.com/113496887/233282370-49cb2c0b-6323-4a16-bea3-c91d7d33b0df.png)
![image](https://user-images.githubusercontent.com/113496887/233282422-1feb8334-9d3f-45fd-9e8a-154a98e42bfa.png)



## Timing diagram 
![image](https://user-images.githubusercontent.com/113496887/233282498-6a3968e7-b23d-4821-80b9-a56e5a94bc54.png)
![image](https://user-images.githubusercontent.com/113496887/233282567-dc722779-37af-4dc8-bbec-2cde98004c9a.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
