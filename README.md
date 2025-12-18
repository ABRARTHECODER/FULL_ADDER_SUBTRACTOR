# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
FULL ADDER
<img width="539" height="480" alt="TRUTH TABLE FULLL ADDED" src="https://github.com/user-attachments/assets/9a4db3cf-09a5-491b-9a2d-358f35d0c28f" />
FULL SUBTRACTOR
<img width="558" height="495" alt="FULL SUBTRACTOR" src="https://github.com/user-attachments/assets/91bd611d-2977-4712-a366-35fdd3627c19" />



**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**

```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: MOHAMED ABRAR M
RegisterNumber:25009852

     i)FULL ADDER
  
  module fa(a,b,cin,sum,carry);
  input a,b,cin;
  output sum,carry;
  assign sum=( (a ^ b)^cin);
  assign carry= ( (a & b)| ( cin &(a ^ b )));
  endmodule
  
  ii)FULL SUBTRACTOR
  
  module fs(a,b,bin,difference,borrow);
  input a,b,bin;
  output difference,borrow;
  assign difference= ( (a ^ b)^bin);
  assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
  endmodule
*/
```

**RTL Schematic**
<img width="1886" height="1026" alt="RTL SCHEME" src="https://github.com/user-attachments/assets/38fe7ca1-a2be-4440-be99-718b78af9964" />
<img width="1866" height="948" alt="RTL 2" src="https://github.com/user-attachments/assets/5ec77c02-1ad8-4934-9305-edbe189a8496" />

**Output Timing Waveform**
<img width="801" height="259" alt="WAVE 1" src="https://github.com/user-attachments/assets/f2f9bf68-33e5-41dc-9885-40ca093a5c26" />
<img width="807" height="177" alt="WAVE2" src="https://github.com/user-attachments/assets/bd2bf4a6-6632-49b3-8135-7e6470329c66" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



