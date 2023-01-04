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

Connect the supply (+5V) to the circuit.

Switch ON the main switch.

If the output is 1, then the led glows.

Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: P.Sri Varshan
RegisterNumber:  22008051

HALF ADDE

module exphalf(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule



module expfull(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule

```

### Output:
### RTL
RTL Realization for Half Adder

![exphalf rtl](https://user-images.githubusercontent.com/114944059/210393281-7b7e5515-04b6-4b63-a754-2f58ea2bd669.jpg)

RTL Realization for Full Adder

![expfull rtl](https://user-images.githubusercontent.com/114944059/210394541-f756ef71-0c80-46f2-8ba3-c489bcb2e1e3.jpg)

### TIMING DIAGRAM
Timing Diagram for Half Adder

![time diag half](https://user-images.githubusercontent.com/114944059/210393555-13c253f9-79d6-49f1-baff-df6cc5ea736a.png)

Timing Diagram for Full Adder

![time diag full](https://user-images.githubusercontent.com/114944059/210394253-4ccd65cc-ad36-43ed-859f-90bebaf72d83.png)


### TRUTH TABLE 

The Truth Table for Half Adder

![exphalftruth](https://user-images.githubusercontent.com/114944059/210388206-9f3ac8b1-ee4b-459e-aa07-c706c57db395.jpg)

The Truth Table for Full Adder

![expfulltruth](https://user-images.githubusercontent.com/114944059/210388708-c847152b-0d07-4f0a-8aa2-df6f205a27d1.jpg)



### Result:
Thus the Half Adder and Full Adder circuit was succesfully implemented.
