# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

             Half Adder
![Screenshot 2025-04-02 214418](https://github.com/user-attachments/assets/35bb1973-7783-4fcc-8e1c-5cc739fa7fff)

             Half Subtractor
![Screenshot 2025-04-02 214431](https://github.com/user-attachments/assets/d8255034-a236-4284-b401-d061d29be5c4)



**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/**Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: RegisterNumber:**/R.SUBITHRA

       Half Adder
```module ha(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum=(a^b);
assign carry=(a&b);
endmodule
```
     Half Subtractor
```module hs(a, b, dif, bor);
input a,b;
output dif,bor;
assign abar=~a;
assign dif=a^b;
assign bor=abar&b;
endmodule
```
  

**RTL Schematic**
  Half Adder
  ![Screenshot 2025-04-02 205321](https://github.com/user-attachments/assets/a42b6724-cbb9-415e-8d3d-4124b18e3f7d)
  
  Half Subtractor
  ![Screenshot 2025-04-02 212455](https://github.com/user-attachments/assets/5f31d2d9-d46f-4f88-8bc2-d70dc47f418a)


**Output/TIMING Waveform**
Half adder
![Screenshot 2025-04-02 210355](https://github.com/user-attachments/assets/6344126f-a258-4353-9226-3a88d0fa9d2a)

Half subtractor
![Screenshot 2025-04-02 213501](https://github.com/user-attachments/assets/fa258566-e5d9-478a-9b06-d71490f6c4b5)



**Result:**
The Half adder and Half subtractor are designed and their truth table is verified

