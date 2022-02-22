# 4bit_adder_subtractor
* Abstract
* Refrence Circuit Details
* Refrence Circuit Diagrams
* Refrence Circuit Waveform
* Simulation in Synopsys
* Schematics and Symbols:- 
   * and gate
   * or gate
   * xor gate
   * Full adder
   * 4bit_adder_subractor
* Parameters set for source and inputs(vdd and vpulse values)
* Transient settings
* Netlist
* Waveforms
* Conclusion
* Acknowledgement
* References

# Abstract
  The need to have hardware support for binary arithmetic is increasing in recent years because of the growth in the Binary data processing in 
  commercial, financial and internet based applications. In this paper you will go through A binary 4bit_Adder-Subtractor. 
  It is a combinational circuit which is capable of performing binary addition and subtraction in one circuitry. The operation mode can be selected using control signal.
  This circuit majorly required the prerequisite knowledge on XOR gate.

# Reference Circuit details
* The circuit shown in the reference diagram 
(a) has 
total of 9 input ports, In which a0 to a3 and b0
to b3 are the binary inputs, K is the control 
signal input which decides the mode of 
operation. Cin, c0 to c2 are the internal wires. 
S0 to s3 are the output ports with gives the 
addition or subtraction value depending on the
selected mode and cout is also a output port 
which may give carry in case of addition and 
borrow in case of difference .
As it is 4 bit adder-subtractor we are using 
four xor gates and 4 one bit full adders.
The diagram (b) show the internal circuitry of 
the one bit full adder which is having 3 input 
ports(a,b,cin) and 2(cout,sum) output ports.
* The gate used in the diagram a,b are:-
1. xor 3.or
2. and
* boolean equations for full adder:-
* SUM=A⊕B⊕C
* CARRY=A.B + A.Cin + B.Cin
* boolean equations for full subtractor:-
* DIFFERENCE =A⊕B C⊕
* BORROW =A’.B + A’.Cin + B.Cin

# Reference Circuit Diagram
* Main Circuit:-
* ![dig51](https://user-images.githubusercontent.com/92252344/155161891-ec27472e-3103-4866-9f40-855cd4e984a6.png)
* Full adder:-
* ![3-57](https://user-images.githubusercontent.com/92252344/155162159-e3b3f67b-9a37-4654-bcee-ae0821c2e6ad.png)

# Reference WaveForm
![Capture](https://user-images.githubusercontent.com/92252344/155162644-a334d721-879e-47e5-9706-f61f42dbb66d.JPG)

# Synopsys Simulations
* 1.Schematics and Symbols
   * and:-
   * ![and](https://user-images.githubusercontent.com/92252344/155165326-91be9a05-921f-4f69-8a8b-30b27b3ffc02.JPG)
   * ![and(s)](https://user-images.githubusercontent.com/92252344/155165925-82694b0f-0046-404e-9af5-cb55e4c9cd76.JPG)
   * Or:-
   * ![or](https://user-images.githubusercontent.com/92252344/155166420-c51c24fa-9b06-4c6f-9256-2d38bf1d1396.JPG)
   * ![or(s)](https://user-images.githubusercontent.com/92252344/155166486-4a04b766-18cd-46b1-814e-2a53e5269eb5.JPG)
   * Xor:-
   * ![xor](https://user-images.githubusercontent.com/92252344/155166920-def5e565-05b9-4ee8-b3a6-f670fea5d98a.JPG)
   * ![image](https://user-images.githubusercontent.com/92252344/155166958-824a68c0-3d43-4c34-83cf-b3e6c3e66fd5.png)
   * Full Adder:-
   * ![full adder](https://user-images.githubusercontent.com/92252344/155167547-a7d93b3f-5dc7-417a-b8a0-9f3e8de3d51d.JPG)
   * ![full adder(s)](https://user-images.githubusercontent.com/92252344/155167828-b0f221e4-6253-40df-b566-850c3a0456ad.JPG)








   




