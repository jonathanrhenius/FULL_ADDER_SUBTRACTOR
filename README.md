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

**Procedure**

Full Adder: 1.Open Quartus II and create a new project. 2.Use schematic design entry to draw the full adder circuit. 3.The circuit consists of XOR, AND, and OR gates. 4.Compile the design, verify its functionality through simulation. 5.Implement the design on the target device and program it.

Full Subtractor: 1.Follow the same steps as for the full adder. 2.Draw the full subtractor circuit using schematic design. 3.The circuit includes XOR, AND, OR gates to perform subtraction. 4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: JONATHAN RHENIUS . S

RegisterNumber: 212224050016

~~~
//expt4a-full adder
module ex4a(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule
~~~
~~~
//exp-4b-full subtractor
module ex4b(df, bo, a, b, bin);
    output df;
    output bo;
    input a;
    input b;
    input bin;
	wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=(~a&b);
	 assign w3=(~w1&bin);
	 assign df=w1^bin;
	 assign bo=w2|w3;
endmodule
~~~

**RTL Schematic**

FULL ADDER

![434175859-92479cbd-8675-476c-ae60-134efc7395bd](https://github.com/user-attachments/assets/3e096cbf-988e-4855-bb5e-ea212152845f)

FULL SUBTRACTOR

![434176026-ec764f25-2b5b-4c7b-9b1d-a401ad0fb293](https://github.com/user-attachments/assets/2cb6a0e5-8210-4f81-8b3d-2eec24112e27)

**Output Timing Waveform**

FULL ADDER

![434176199-5b8b0061-0e05-4cdd-8716-335644d0d045](https://github.com/user-attachments/assets/5c0abbcb-aa72-43fc-abbf-8eb55d03c35b)

FULL SUBTRACTOR

![434176245-a7b99ed6-4ae7-412a-8339-e5ee3bb387b6](https://github.com/user-attachments/assets/354ff3f7-d5cd-4b11-a2a1-8a224c3893e0)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



