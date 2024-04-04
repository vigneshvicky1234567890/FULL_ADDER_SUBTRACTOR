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
![319496358-d7541d03-9e3c-4e4b-9e83-6e2ff3e40d0d](https://github.com/vigneshvicky1234567890/FULL_ADDER_SUBTRACTOR/assets/166011899/81ec3a72-ffc8-455f-9ced-44f3c3631fbd)
![319496392-a48155ec-6f4a-4d35-8f62-ba7970c9ae92](https://github.com/vigneshvicky1234567890/FULL_ADDER_SUBTRACTOR/assets/166011899/071a8a9a-3936-439e-95e4-d0164eba7e7d)


**Procedure**
Full Adder:

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.

Full Subtractor:

1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR, AND, OR gates to perform subtraction.

4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: VIGNESH.J
RegisterNumber:212222053005
*/
```
module fulladdsub(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry= a&b | a&c | b&c;
wire a0;
not (a0,a);
assign BO= b&c | a0&c | a0&b;
assign DIFF=a^b^c;
endmodule
```

**RTL Schematic**
![319496611-d483fb23-6310-4d37-aeef-084e10e521db](https://github.com/vigneshvicky1234567890/FULL_ADDER_SUBTRACTOR/assets/166011899/67cc7d1b-e4a1-4cdf-95df-f18cef8d4bc8)

**Output Timing Waveform**
![319497400-733b8a90-21c2-4f99-8ad0-1dfa5dfae965](https://github.com/vigneshvicky1234567890/FULL_ADDER_SUBTRACTOR/assets/166011899/8f90f1e6-ee6b-4334-a73d-59723af6a1ab)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



