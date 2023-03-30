# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:

### Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: D.Vinitha Naidu
RegisterNumber: 212222230175

### Half Adder :
```
module halfadder(a,b,s,c);
input a,b;
output s,c;
xor (s,a,b);
and (c,a,b);
endmodule
```
### Full Adder:
``` 
module fulladder(a,b,ci,s,co);
input a,b,ci;
output s,co;
wire d,e,f;
xor (d,a,b);
xor (s,d,ci);
and (f,a,b);
or (co,e,f);
endmodule

```
### Output:
### RTL 

### Half Adder :
![Screenshot_20230330_085312](https://user-images.githubusercontent.com/121166004/228885839-7a5aae55-6bac-4ca7-89bd-00884f171204.png)

### Full Adder:
![Screenshot_20230330_085324](https://user-images.githubusercontent.com/121166004/228885966-1665409b-db75-419f-8a12-b3441049ad5f.png)

### TIMING DIAGRAM:

### Half Adder :
![Screenshot_20230330_085339](https://user-images.githubusercontent.com/121166004/228886282-76195889-2b5c-48f6-863c-e3eba0032072.png)

### Full Adder:
![Screenshot_20230330_085353](https://user-images.githubusercontent.com/121166004/228886739-427a2ad3-7773-4f30-9fd3-471748b82aa9.png)

### TRUTH TABLE :

### Half Adder :
![Screenshot_20230330_085411](https://user-images.githubusercontent.com/121166004/228887106-010390f0-a281-4249-85e4-fe6bfc4a2c46.png)

### Full Adder:
![Screenshot_20230330_085420](https://user-images.githubusercontent.com/121166004/228887223-af9f7d84-251d-44d4-a2a1-f6db9d52b2e5.png)

### Result:
Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.
