# 8to3_encoder
ENCODER 8TO3 DATAFLOW Modelling
AIM:

To implement Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

SOFTWARE REQUIRED: Quartus prime

THEORY

Encoder 8 To 3

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

<img width="325" height="250" alt="image" src="https://github.com/user-attachments/assets/db8c679c-91ec-4229-84cd-641a5e8ef293" />

Figure 01 Block Diagram of Encoder 8 * 3

Truth Table

<img width="425" height="322" alt="image" src="https://github.com/user-attachments/assets/e20f4b08-88f0-4676-be62-dc4f69add89e" />

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

Logical circuit of the above expressions is given below:

<img width="602" height="351" alt="image" src="https://github.com/user-attachments/assets/51662317-26f7-447b-8f4a-392bdef61c9a" />

Figure 02 Encoder 8 * 3

#Procedure

Identify the 8 input lines (D0–D7) and 3 output lines (A2, A1, A0).

Assume only one input is active at a time.

Write the truth table mapping each active input to its binary output code.

Derive Boolean expressions for each output using logic minimization.

Implement the circuit using logic gates and verify correct encoding by simulation.

#PROGRAM
```
module Encoder(
    input  wire [7:0] in,   
    output reg  [2:0] out   
);
    always @(*) begin
        case (in)
            8'b0000_0001: out = 3'b000;
            8'b0000_0010: out = 3'b001;
            8'b0000_0100: out = 3'b010;
            8'b0000_1000: out = 3'b011;
            8'b0001_0000: out = 3'b100;
            8'b0010_0000: out = 3'b101;
            8'b0100_0000: out = 3'b110;
            8'b1000_0000: out = 3'b111;
            default:      out = 3'bxxx;
        endcase
    end
endmodule
```

Developed by: VANATHI T

RegisterNumber: 25013590

RTL LOGIC FOR Encoder 8 To 3 in Dataflow Modelling

<img width="1920" height="1020" alt="Screenshot 2025-12-15 212156" src="https://github.com/user-attachments/assets/5351ee58-2e32-45fb-aaba-743955e172c9" />


TIMING DIGRAMS FOR Encoder 8 To 3 in Dataflow Modelling

RESULT:
 Implemented Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

