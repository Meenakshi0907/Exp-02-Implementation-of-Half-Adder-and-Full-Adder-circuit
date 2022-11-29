# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
## AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

## Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

## Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

## Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
## Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Meenakshi M
RegisterNumber: 212221230057
*/
```
### Half Adder:
```
module halfadder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
### Full Adder:
```
module fulladder(a,b,c,carry,sum);
input a,b,c;
output sum,carry;
assign sum=((a ^ b) ^ c);
assign carry=((a & b)|(b & c)|(c & a));
endmodule
```
## Logic symbol & Truthtable
### Half Adder:
![image](https://user-images.githubusercontent.com/94165108/195993629-17b2144d-c16e-4fd1-ab1a-5d52eea05300.png)
![image](https://user-images.githubusercontent.com/94165108/195993641-77cc8f75-d36a-48df-80ef-4312c0d0f5b6.png)
![image](https://user-images.githubusercontent.com/94165108/195993645-10c80f4e-ba86-40fb-8a18-aafed07af653.png)

### Full Adder:
![image](https://user-images.githubusercontent.com/94165108/195993665-5dda7b9e-cacc-4e08-9b7e-a2e9775818db.png)
![image](https://user-images.githubusercontent.com/94165108/195993676-671eb6bd-9476-4a1b-b358-6e20e5959370.png)
![image](https://user-images.githubusercontent.com/94165108/195993685-352e3032-d444-43c3-9c20-ee0be1802b8d.png)
![image](https://user-images.githubusercontent.com/94165108/195993695-12ce8ef7-b7d8-4ead-9429-20d7b3220701.png)

## Output:
## RTL:
### Half Adder:
![ha2](./ha2.png)
### Full Adder:
![fa 2](https://user-images.githubusercontent.com/94165108/195993714-37e9010b-20b9-4cf2-93ba-54e2ea5d7a4d.png)

## TIMING DIAGRAM
### Half Adder:
![ha1](./ha1.png)
### Full Adder:
![fa 1](https://user-images.githubusercontent.com/94165108/195993730-0a42b21d-07e8-4a4c-a8ec-ed8ae1797c75.png)

## Result:
Designing of a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming is sucessfully done
