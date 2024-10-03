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
module Boolean_min(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);

and(s,x,y);
and(t,w,y);
and(u,ydash,z);
or(f2,s,t,u);
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


![Screenshot 2024-10-03 105515](https://github.com/user-attachments/assets/5ae85c72-e719-4096-9cca-3ba94fa53340)




**Output:**

![Screenshot 2024-10-03 105144](https://github.com/user-attachments/assets/20125deb-4132-472e-b471-c6be66c318b9)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

