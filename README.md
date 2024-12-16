# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![Screenshot 2024-12-16 191109](https://github.com/user-attachments/assets/f3acf43e-e043-42ca-a9b1-91e0b1119a3d)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![Screenshot 2024-12-16 190625](https://github.com/user-attachments/assets/f4cfbbec-e53d-4d48-8e39-c5021f19721e)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![Screenshot 2024-12-16 190611](https://github.com/user-attachments/assets/3d283e7a-9233-4703-b61a-d20ea0bbac83)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![Screenshot 2024-12-16 190601](https://github.com/user-attachments/assets/9ddf53a3-9e5e-47e2-8a1f-a61a124a91aa)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program. 

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram. 

5.For different input combinations generate the timing diagram.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by: Dinesh.V

RegisterNumber: 24010667

module jkflipflop(j,k,clk,q,qbar);

input j,k,clk;

output reg q,qbar;

initial 

begin

q=1'b0;

q=1'b1;

end 

always @(posedge clk)

begin 

q<=(j&~q)|(~k&q);

qbar<=~q;

end

endmodule


**RTL LOGIC FOR FLIPFLOPS**

![Screenshot 2024-12-16 191240](https://github.com/user-attachments/assets/6daf681a-b142-49d4-9c83-fc0aacf77e37)

**TIMING DIGRAMS FOR FLIP FLOPS**

**RESULTS**

Thus the truth table of JKFLIPFLOP in Quartus II using Verilog programming are studied, verified and executed successfully.
