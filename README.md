# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
~~~
Developed by:SRIDHAR C
RegisterNumber:212225040425
module de2(a, b, c, d, w, x, y, z, f1, f2);

input a, b, c, d;
input w, x, y, z;
output f1, f2;

// F1 implementation
assign f1 = (~a & ~b & ~c & ~d) |
            ( a & ~c & ~d )     |
            (~b &  c & ~d )     |
            (~a &  b &  c &  d )|
            ( b & ~c &  d );

// F2 implementation
assign f2 = ( x & ~y &  z ) |
            (~x & ~y &  z ) |
            (~w &  x &  y ) |
            ( w & ~x &  y ) |
            ( w &  x &  y );

endmodule
~~~
**Truth Table**
<img width="830" height="846" alt="truth_tables" src="https://github.com/user-attachments/assets/37c90ede-c108-4529-abd2-0b4c5706ee33" />


**Output:**
<img width="743" height="856" alt="image" src="https://github.com/user-attachments/assets/beaff711-c03a-46c6-b2d4-2a0bfb08b33e" />

**RTL realization**
<img width="1547" height="862" alt="image" src="https://github.com/user-attachments/assets/6844087c-8065-4f13-9260-50da82fdefb2" />

**Timing Diagram**
<img width="1918" height="1013" alt="image" src="https://github.com/user-attachments/assets/3e2b4e9c-ca78-4903-a49b-d00ba5b76f33" />

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

