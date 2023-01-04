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
### Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: KANISHKAR M
RegisterNumber:22007816  

HALF ADDER

module exphalf(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule

FULL ADDER

module expfull(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```

### Output:
### RTL
The RTL Realization for Half Adder

![half adder logic diagram](https://user-images.githubusercontent.com/118886772/210480928-404e7637-c50a-4516-9f6f-ec8a85b5f2d1.png)

The RTL Realization for Full Adder

![full adder logic diagram](https://user-images.githubusercontent.com/118886772/210480984-1bc652fa-a627-43db-b04b-7f16d35efd16.png)

### TIMING DIAGRAM

Timing Diagram for Half Adder

![half adder time diagram](https://user-images.githubusercontent.com/118886772/210481003-ed38722e-2fbf-44f6-a0da-eef479ee7d59.jpg)

Timing Diagram for Full Adder

![full adder time diagram](https://user-images.githubusercontent.com/118886772/210481020-1499e6de-b600-4848-93c1-931c4c8669ec.jpg)

### TRUTH TABLE
Truth table for Half Adder

![half adder truth table](https://user-images.githubusercontent.com/118886772/210481042-28e7fd02-9300-4d9d-843b-38f7f390faa8.jpg)

Truth table for Full Adder

![full adder truth table](https://user-images.githubusercontent.com/118886772/210481049-33d658b6-d3fd-49c3-b924-7578afb31b3e.jpg)

### Result:
Thus the Half Adder and Full Adder Circuits was succesfully implemented.
