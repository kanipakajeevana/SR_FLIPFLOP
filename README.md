# SR_FLIPFLOP
# AIM
To simulate and synthesis SR flipflop using vivado.
# APPARATUS REQUIRE
Vivado 2023.2 software.
# PROCEDURE
STEP:1 Start the vivado software, Select and Name the New project.

STEP:2 Select the device family, device, package and speed.

STEP:3 Select new source in the New Project and select Verilog Module as the Source type.

STEP:4 Type the File Name and module name and Click Next and then finish button. Type the code and save it.

STEP:5 Select the run simulation and then run Behavioral Simulation in the Source Window and click the check syntax.

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.

STEP:7 compare the output with truth table.


# Circuit Diagram
![image](https://github.com/kanipakajeevana/SR_FLIPFLOP/assets/170450203/e5f862eb-7a23-4434-ac10-76a4e06d9b5b)

# Truth Table
![image](https://github.com/kanipakajeevana/SR_FLIPFLOP/assets/170450203/d5bd12d4-75a9-4cba-a09d-41e7e65a1ffb)
# PROGRAM
module sr(clk,s,r,rst,q );
input s,r,clk,rst;
output reg q;
always@(posedge clk)
begin
if(rst==1)
q=1'b0;
else
begin
case({s,r})
2'b00: q=q;
2'b01:q=1'b0;
2'b10:q=1'b1;
2'b11:q=1'bx;
endcase
end
end
endmodule
# OUTPUT
![image](https://github.com/kanipakajeevana/SR_FLIPFLOP/assets/170450203/c48eddff-e331-4ec7-91f6-871be2f65c29)
# RESULT
Thus the verilog program for SR flipflop has been simulated and verified successfully.



