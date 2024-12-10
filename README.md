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
Full Adder

![WhatsApp Image 2024-11-28 at 10 56 17_b5082baa](https://github.com/user-attachments/assets/4d067f86-95f5-42ba-b297-7b0ac29da290)

Full Subtractor

![WhatsApp Image 2024-11-28 at 10 55 54_dd14f54f](https://github.com/user-attachments/assets/00b5a05c-d04a-4a8f-b9e2-7f432ffade06)



**Program:**
```
Developed by:A.Ranen Joseph Solomon RegisterNumber:24006171
```
Full Adder
```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```
Full Subtractor 
```
module de42(a, b, bin, difference, borrow);
    input a, b, bin;
    output difference, borrow;

    xor(difference, (a ^ b), bin);
    or(borrow, (a & b), (bin & (a | b)));
endmodule
```



**RTL Schematic**
Full Adder 
![WhatsApp Image 2024-11-28 at 10 47 05_6124aca3](https://github.com/user-attachments/assets/56271b1a-314b-4fbe-8abf-b46f6a7d8169)

Full Subtractor
![WhatsApp Image 2024-11-28 at 10 46 48_e8129483](https://github.com/user-attachments/assets/6b6317bd-c0a7-4c72-8cac-ab1171771310)


**Output Timing Waveform**
Full Adder
![Screenshot 2024-11-28 102318](https://github.com/user-attachments/assets/d57f1ea2-7e03-4d6d-96a0-76de4d2adb99)

Full Subtractor 
![WhatsApp Image 2024-11-28 at 10 45 39_9042c4e1](https://github.com/user-attachments/assets/58d21a4e-7c6b-40c2-8b47-cce04047ed36)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



