# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Truth Table**

Serial In Serial Out

![image](https://github.com/user-attachments/assets/dc6e604e-9fe9-463a-a8a1-43db4033b15f)


**Procedure**

1.Type the program in Quartus software

2.Compile and run the program

3.Generate the RTL schematic and save the logic diagram

4.Create nodes for inputs and outputs to generate the timing diagram

5.For different input combinations generate the timing diagram.

/* write all the steps invloved */

**PROGRAM**
```
module exp10(clk,sin,q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0]<=sin;
q[1]<=q[0];
q[2]<=q[1];
q[3]<=q[2];
end
endmodule
```

/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by: Thirunavukkarasu meenakshisundaram

RegisterNumber:24006365

*/

**RTL LOGIC FOR SISO Shift Register**

![image](https://github.com/user-attachments/assets/6b4aa33c-416b-4e5e-a8c8-1db9ec9e620a)


**TIMING DIGRAMS FOR SISO Shift Register**

![Screenshot 2024-12-08 132433](https://github.com/user-attachments/assets/8beaf225-588a-4acb-a431-0d73e82e0429)


**RESULTS**

Thus shift register implemented successfully and outputs are verified
