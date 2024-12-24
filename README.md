# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

/* write all the steps invloved */

**PROGRAM**
```
/* 
  Program for flipflops and verify its truth table in quartus using Verilog programming.
  Developed by:JAHAN J
  RegisterNumber:24004359
*/
```
```
module d_flipflop (
    input clk,    // Clock signal
    input reset,  // Active-high reset signal
    input d,      // Data input
    output reg q  // Output
);
    always @(posedge clk or posedge reset) begin
        if (reset) 
            q <= 1'b0; // Reset the output to 0
        else 
            q <= d;    // Capture the value of d on clock edge
    end
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**



![Screenshot 2024-12-24 215319](https://github.com/user-attachments/assets/762cfe3b-7511-424a-ac12-181f2cc27bb7)



**TIMING DIGRAMS FOR FLIP FLOPS**


![Screenshot 2024-12-24 215319](https://github.com/user-attachments/assets/bd963d6b-569b-4785-81fb-e09525b040b2)



**RESULTS**:
The observation of the stimulation results and confrim the successful execution of the program.
