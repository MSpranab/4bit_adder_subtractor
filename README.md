# 4bit_adder_subtractor
******************************************************************************************************************************************
* [Abstract](#Abstract)
* [Reference Circuit details](#Reference-Circuit-details)
* [Reference Circuit Diagram](#Reference-Circuit-Diagram)
* [Reference WaveForm](#Reference-WaveForm)
* [Synopsys Simulations](#Synopsys-Simulations)
* [Schematics and Symbols](#Schematics-and-Symbols):- 
   * and gate
   * Or gate
   * Xor gate
   * Full Adder
   * Main Circuit
* [Vdd and Vgs values for MOSFETS](#Vdd-and-Vgs-values-for-MOSFETS)
* [Transient settings](#Transient-settings)
* [Testbench](#Testbench)
* [Simulated Waveform](#Simulated-Waveform)
* [Netlist](#Netlist)
* [Conclusion](#Conclusion)
* [Acknowledgement](#Acknowledgement)
* [References](#References)

# Abstract
  The need to have hardware support for binary arithmetic is increasing in recent years because of the growth in the Binary data processing in 
  commercial, financial and internet based applications. In this paper you will go through A binary 4bit_Adder-Subtractor. 
  It is a combinational circuit which is capable of performing binary addition and subtraction in one circuitry. 
  The operation mode can be selected using control signal, control singal will also be taken as input to the 1st stage full adder.
  This circuitry is a combination of logic gates like and, or, xor gates.The major principle followed in this circutry is take from the ripple carry adder circuitry in which
  carry out of the previous stage full adder is given as input carry to the next full adder.This circuit majorly required the prerequisite knowledge on XOR gate, because 
  by which we are performing 2'complement on one set of input data to perform subtraction operation.

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
* The gates used in the diagram a,b are:-
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
# Schematics and Symbols
   *  and gate:-
   * ![and](https://user-images.githubusercontent.com/92252344/155165326-91be9a05-921f-4f69-8a8b-30b27b3ffc02.JPG)
   * ![and(s)](https://user-images.githubusercontent.com/92252344/155165925-82694b0f-0046-404e-9af5-cb55e4c9cd76.JPG)
   *  Or gate:-
   * ![or](https://user-images.githubusercontent.com/92252344/155166420-c51c24fa-9b06-4c6f-9256-2d38bf1d1396.JPG)
   * ![or(s)](https://user-images.githubusercontent.com/92252344/155166486-4a04b766-18cd-46b1-814e-2a53e5269eb5.JPG)
   *  Xor gate:-
   * ![xor](https://user-images.githubusercontent.com/92252344/155166920-def5e565-05b9-4ee8-b3a6-f670fea5d98a.JPG)
   * ![image](https://user-images.githubusercontent.com/92252344/155166958-824a68c0-3d43-4c34-83cf-b3e6c3e66fd5.png)
   *  Full Adder:-
   * ![full adder](https://user-images.githubusercontent.com/92252344/155167547-a7d93b3f-5dc7-417a-b8a0-9f3e8de3d51d.JPG)
   * ![full adder(s)](https://user-images.githubusercontent.com/92252344/155167828-b0f221e4-6253-40df-b566-850c3a0456ad.JPG)
   *  Main Circuit:-
   * ![4bas circuit](https://user-images.githubusercontent.com/92252344/155168248-537ec6be-ac00-43cd-8037-75ccad8679eb.JPG)

# Vdd and Vgs values for MOSFETS
* Vdd:-
* ![vdd input](https://user-images.githubusercontent.com/92252344/155169273-41e8f205-42d4-494c-834b-df47aeb14543.JPG)
* Vgs:-
* ![vgs input](https://user-images.githubusercontent.com/92252344/155169364-12376f62-67e4-4265-afb2-c6eeb8993032.JPG)

# Transient settings
* ![trans](https://user-images.githubusercontent.com/92252344/155170197-27dc80a8-ecfc-44c9-80bb-d5fd4abc28c8.JPG)

# Testbench
* ![test bench](https://user-images.githubusercontent.com/92252344/155170601-e748e993-b86d-44be-b7c3-c7d9c1b46d5a.JPG)

# Simulated Waveform
* ![sim](https://user-images.githubusercontent.com/92252344/155171019-bba8e113-f94b-4b56-9037-deca9445b165.jpg)

# Netlist
```
*  Generated for: PrimeSim
*  Design library name: add_sub
*  Design cell name: tb
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Tue Feb 22 16:09:10 2022

.global gnd! vdd!
********************************************************************************
* Library          : add_sub
* Cell             : or
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD

subckt or a b out vt_bulk_n_gnd! vt_bulk_p_vdd! 
xm8 net30 a net12 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1 
xm6 out net47 net12 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1 
xm3 net18 b net12 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1 
xm4 net47 net4 net18 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1 
xm5 net47 a net18 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1 
xm2 net18 net30 net12 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1 
xm0 net4 b net12 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1 
xm14 out net47 gnd! vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1 
xm13 net42 b gnd! vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1 
xm12 net47 net30 net42 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1 
xm11 net49 a gnd! vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1 
xm10 net47 net4 net49 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1 
xm9 net30 a gnd! vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1 
xm1 net4 b gnd! vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1 
v15 net12 gnd! dc=0.9 
.ends or
********************************************************************************

* Library          : add_sub
* Cell             : and
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD

subckt and a b out vt_bulk_n_gnd! vt_bulk_p_vdd!
xm2 out net18 net20 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm1 net18 b net20 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm0 net18 a net20 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm5 out net18 gnd! vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm4 net13 b gnd! vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm3 net18 a net13 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
v6 net20 gnd! dc=1.2
.ends and

********************************************************************************
* Library          : add_sub
* Cell             : xor
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD

subckt xor a b out vt_bulk_n_gnd! vt_bulk_p_vdd!
xm2 out net19 net26 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm1 net19 b net4 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm0 net4 a net26 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm5 out net19 gnd! vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm4 net19 a gnd! vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm3 net19 b gnd! vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
v8 net26 gnd! dc=0.9
.ends xor

********************************************************************************
* Library          : add_sub
* Cell             : adder
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD

subckt adder cin sum carry in1 in2 vt_bulk_n_gnd! vt_bulk_p_vdd!
xi2 net23 cin sum vt_bulk_n_gnd! vt_bulk_p_vdd! or
xi1 in1 in2 net23 vt_bulk_n_gnd! vt_bulk_p_vdd! or
xi4 in1 in2 net18 vt_bulk_n_gnd! vt_bulk_p_vdd! and
xi3 cin net23 net17 vt_bulk_n_gnd! vt_bulk_p_vdd! and
xi5 net17 net18 carry vt_bulk_n_gnd! vt_bulk_p_vdd! xor
.ends adder
********************************************************************************
* Library          : add_sub
* Cell             : adder_subtractor
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD

subckt adder_subtractor a0 a1 a2 a3 b0 b1 b2 b3 cout k s0 s1 s2 s3\
+ vt_bulk_n_gnd! vt_bulk_p_vdd!\
xi3 b0 k net13 vt_bulk_n_gnd! vt_bulk_p_vdd! or
xi2 b1 k net18 vt_bulk_n_gnd! vt_bulk_p_vdd! or
xi1 b2 k net23 vt_bulk_n_gnd! vt_bulk_p_vdd! or
xi0 b3 k net28 vt_bulk_n_gnd! vt_bulk_p_vdd! or
xi7 net30 s3 cout a3 net28 vt_bulk_n_gnd! vt_bulk_p_vdd! adder
xi6 net25 s2 net30 a2 net23 vt_bulk_n_gnd! vt_bulk_p_vdd! adder
xi5 net20 s1 net25 a1 net18 vt_bulk_n_gnd! vt_bulk_p_vdd! adder
xi4 k s0 net20 a0 net13 vt_bulk_n_gnd! vt_bulk_p_vdd! adder
.ends adder_subtractor
********************************************************************************

* Library          : add_sub
* Cell             : tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
 v36 a3 gnd! dc=0 pulse ( 0.9 0 0 0.1u 0.1u 2.5u 5u )
 v35 a2 gnd! dc=0 pulse ( 0.9 0 0 0.1u 0.1u 5u 10u )
 v34 b0 gnd! dc=0 pulse ( 0.9 0 0 0.1u 0.1u 2.5u 5u )
 v33 b1 gnd! dc=0 pulse ( 0.9 0 0 0.1u 0.1u 5u 10u )
 v32 b2 gnd! dc=0 pulse ( 0.9 0 0 0.1u 0.1u 2.5u 5u )
 v31 b3 gnd! dc=0 pulse ( 0.9 0 0 0.1u 0.1u 5u 10u )
 v37 k gnd! dc=0 pulse ( 0.9 0 0 0.1u 0.1u 20u 40u )
 v16 a1 gnd! dc=0 pulse ( 0.9 0 0 0.1u 0.1u 2.5u 5u )
 v8 a0 gnd! dc=0 pulse ( 0.9 0 0 0.1u 0.1u 5u 10u )
 c26 cout gnd! c=1p
 c21 so gnd! c=1p
 c23 s1 gnd! c=1p
 c24 s2 gnd! c=1p
 c25 s3 gnd! c=1p
 xi19 a0 a1 a2 a3 b0 b1 b2 b3 cout k so s1 s2 s3 gnd! vdd! adder_subtractor








.tran '0.001*(40u-0u)' '40u' start=0u name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1\
.probe tran v(a0) v(a1) v(a2) v(a3) v(b0) v(b1) v(b2) v(b3) v(cout) v(k) v(s1)
+ v(s2) v(s3) v(so)
.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end
```
******************************************************************************************************************************************

# Conclusion
* We can reduce the use of multiple hardware resources required to make 4-bit full adder separately and another 4-bit full subtractor.
* By just using the control signal we can which between two modes adder and subtractor.
* With this design we can make N-bit adder_subtractor.
******************************************************************************************************************************************
# Acknowledgement
* 1.Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd. - kunalpghosh@gmail.com
* 2.Chinmay panda, IIT Hyderabad
* 3.Sameer Durgoji, NIT Karnataka
******************************************************************************************************************************************
 # References
* https://www.geeksforgeeks.org/4-bit-binary-adder-subtractor/
* https://www.javatpoint.com/coa-binary-adder-subtractor







   




