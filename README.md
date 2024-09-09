# Experiment 1

# Aim
To write and simulate 4:1 Mux using verilog HDL in Gate level, Data flow, Behavioural, Structural Modeling styples with testbench.

# Program
module mux(i,s,y);
input[3:0]i;
input[1:0]s;
output reg y;
always@(i,s)
begin
case(s)
2'b00:y=i[0];
2'b01:y=i[1];
2'b10:y=i[2];
2'b11:y=i[3];
default:y=4'b0;
endcase
end
endmodule

# Test Bench
module mux_tb;
reg[3:0]i;
reg[1:0]s;
wire y;
mux dut(i,s,y);
initial
begin
i=4'b1100;
s=2'b00;
#100
s=2'b01;
#100
s=2'b10;
#100
s=2'b11;
end 
endmodule

# Circuit Diagram
![Screenshot 2024-09-09 080858](https://github.com/user-attachments/assets/24f1523d-4d34-4548-86d1-ec7580ff83df)

# Output
![Screenshot 2024-09-09 080945](https://github.com/user-attachments/assets/0ed1353f-589e-4612-9c55-6270784f8d50)

# Result
Thus, 4:1 Mux is implemented using verilog HDL with testbench.
