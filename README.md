# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware 
PCs, Cyclone II , USB flasher
## Software 
Quartus prime
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

STEP 1: Use module project name(input,output) to start the Verilog programmming.

STEP 2: Assign inputs and outputs using the word input and output respectively.

STEP 3: Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

STEP 4: Use each output to represnt onre for differnce and the other for borrow.

STEP 5: End the verilog program using keyword endmodule.

## Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: SUJITHRA B K N

RegisterNumber:  212222230153

### Half Subtractor:

```
module exp4(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff = (a^b);
assign borr = ((~a)&b);
endmodule
```

### Full Subtractor:

```
module fullsubtractor(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=(a^b^bin);
assign borr=(~a&(b)|(b&bin)|((~a)&bin));
endmodule
```

## Output:

## Truthtable

### Half Subtractor:

![Screenshot 2023-09-09 093959](https://github.com/sujithrabkn/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119477857/4019897b-f35b-432a-91c2-fcc00129cc33)


### Full Subtractor:

![Screenshot 2023-09-09 094315](https://github.com/sujithrabkn/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119477857/e4dfc8b4-d27d-4ac3-807c-745b46d51346)

##  RTL realization

### Half Subtractor:

![Screenshot 2023-09-09 090243](https://github.com/sujithrabkn/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119477857/e044ab92-b89c-4899-8603-e54c264da946)

### Full Subtractor:

![Screenshot 2023-09-09 092010](https://github.com/sujithrabkn/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119477857/6bc51f4e-77cc-4c1e-9416-0fb1f098cca1)


## Timing diagram 

### Half Subtractor:

![Screenshot 2023-09-09 091054](https://github.com/sujithrabkn/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119477857/3967461a-b0b7-4ae4-8435-e8f63afb672b)


### Full Subtractor:

![Screenshot 2023-09-09 092541](https://github.com/sujithrabkn/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119477857/b0a4a510-5d54-43cc-94ea-fe8748967a79)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
