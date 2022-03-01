
# Source Follower



## Table of Contents

* Abstract
* Reference Circuit Details
* Reference Circuit Diagram
* Reference Circuit Waveform
* Simulation in Synopsys
   * Schematic
   * Parameters set for Voltage Source for Input
   * Transient Settings
   * Netlist
   * Waveform
* Conclusion
* References





## Abstract

The source follower also known as 
the Common drain amplifier has a very wide 
variety of applications in analog electronics 
which include buffers and level shifters. It has a 
unity voltage gain and provides a low output 
impedance. This design is implemented on a 
Synopsys tool to check the output waveform of 
the CMOS source follower in 28nm technology.
## Reference Circuit Details

A buffer circuit is used to prevent circuit 
dysfunctionalities as it can drive a low 
impedance load with very little loss of signal 
strength and minimum possible noise. The 
source follower provides a high voltage gain 
with high load impedance. This buffer is 
commonly used in many high speed integrated 
circuits attached to the amplifiers.
The gain of a common drain amplifier is given 
by-
- Av=gmRS/ ( gmRS+1)
This is achieved by the small signal
analysis of the source follower.
And the output impedance is
given by-
- Zout=RS||1/gm
## Reference Circuit Diagram




![](https://user-images.githubusercontent.com/46897100/156207733-6fae6b6b-c9de-439f-84af-bfe37cce1d5a.jpeg)


## Reference Circuit Waveform ( with sine wave input)
![](https://user-images.githubusercontent.com/46897100/156208033-871065ce-7145-4770-b0ad-f96f977c18bc.jpeg)
## Simulations in Synopsys
## Schematic

![](https://user-images.githubusercontent.com/46897100/156208576-42b0cd8c-a848-415b-b0bd-4d52dad2db2c.png)
## Parameters set for Voltage Source for Input 

![](https://user-images.githubusercontent.com/46897100/156208977-610b7c0e-6744-4df2-8c8c-6e395f0236e7.png)

## Transient Settings

![](https://user-images.githubusercontent.com/46897100/156209105-8673030d-0333-43db-8f41-31633bbee45a.png)
## Netlist

*Generated for: PrimeSim

*Design library name: cp_lib1

*Design cell name: cp_sourcefollower

*Design view name: schematic

.lib 'saed32nm.lib' TT


*Custom Compiler Version S-2021.09

*Sat Feb 26 17:04:50 2022

.global gnd!
********************************************************************************
*Library          : cp_lib1

*Cell             : cp_sourcefollower

*View             : schematic

*View Search List : hspice hspiceD schematic spice veriloga

*View Stop List   : hspice hspiceD

********************************************************************************
xm0 net23 net3 net40 gnd! n105 w=0.1u l=0.03u nf=1 m=1

r4 net10 gnd! r=1k

r3 net40 gnd! r=2k

r2 net6 gnd! r=12k

r1 net23 net6 r=82k

c7 net3 net42 c=16m

c6 net40 net10 c=10m

v18 net23 gnd! dc=20

vs net42 gnd! dc=0 pulse ( 0 1 0 0.5 0.5 2n 4n )


## Waveform( with pulse wave input )

![](https://user-images.githubusercontent.com/46897100/156209786-2c101d6a-56a8-4fcb-9e38-e86650dca41e.png))
## Conclusion

Hence, the common drain apmlifier or source follower is implemented using the 32nm technology node of Synopsys. The result with output following the input recieved.
## References

1. Design of Analog CMOS integrated circuits, Behzad
Razavi

2. Design and Analysis of Super Source Follower, Asst.
Prof Guru Prasad, MIT Manipal

3. Analysis and Design of CMOS Source Followers and
Super Source Follower Mr. D. K. Shedge1 Mr. D. A.
Itole, Mr. M. P. Gajare, and Dr. P. W. Wani