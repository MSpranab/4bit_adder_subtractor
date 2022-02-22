# 4bit_adder_subtractor
* Abstract
* Refrence Circuit Details
* Refrence Circuit Waveform
* Schematics and Symbols 
   * and gate
   * or gate
   * xor gate
   * Full adder
   * 4bit_adder_subractor
   * Simulation in Synopsys
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
* →The circuit shown in the reference diagram 
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
