# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**
```
1.Open Quartus software and create a new project.
2.Write the Verilog code for the 4-bit ripple counter.
3.Compile the design and assign input/output pins.
4.Run simulation to check the counting output.
5.Program the FPGA board and observe the result.
```

**PROGRAM**
```
module EXP6(
    input clk,
    input rst,
    output reg [3:0] count
);

always @(posedge clk or posedge rst)
begin
    if (rst)
        count <= 4'b0000;
    else
        count <= count + 1'b1;
end

endmodule
```

**RTL LOGIC FOR 4 Bit Ripple Counter**

<img width="1916" height="1018" alt="{8EB8358C-8D92-4DB2-947E-BAAB79A096B4}" src="https://github.com/user-attachments/assets/9ff7f8f5-b27b-446c-b86a-ad43bf6df84d" />


**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

<img width="1920" height="1018" alt="{E12E6278-F867-4C6E-8170-8D7048BA3BAB}" src="https://github.com/user-attachments/assets/0a3122d5-aaf1-4534-9d66-60e52ffc1822" />


**RESULTS** :
Thus, the 4-BIT-RIPPLE-COUNTER successfully designed and verified using Quartus software.
