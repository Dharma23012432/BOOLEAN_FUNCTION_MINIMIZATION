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
```
module Boolean_min(A,B,C,D,W,X,Y,Z,F1,F2);
input A,B,C,D,W,X,Y,Z;
wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
output F1,F2;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign x6=(X)&(~Y)&(Z);
assign x7=(~X)&(~Y)&(Z);
assign x8=(~W)&(X)&(Y);
assign x9=(W)&(~X)&(Y);
assign x10=(W)&(X)&(Y);
assign F1=x1|x2|x3|x4|x5;
assign F2=x6|x7|x8|x9|x10;
endmodule
```
```
Developed by: DHARMALINGAM S

RegisterNumber:212223040037

*/
```
## Logic symbol & Truthtable:

![image](https://github.com/23004205/BOOLEAN_FUNCTION_MINIMIZATION/assets/138971114/a9ccb75e-db7b-490e-8b69-10f820e6bff4)


![image](https://github.com/23004205/BOOLEAN_FUNCTION_MINIMIZATION/assets/138971114/6835b6c0-9fe5-4f55-8288-53b7d0c42104)



**RTL realization**


![image](https://github.com/23004205/BOOLEAN_FUNCTION_MINIMIZATION/assets/138971114/5ffd7097-c99c-4ef3-a82d-0108e72a8b9e)



**Output:**


![image](https://github.com/23004205/BOOLEAN_FUNCTION_MINIMIZATION/assets/138971114/3294f442-723b-4550-ab9c-49ed60325deb)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

