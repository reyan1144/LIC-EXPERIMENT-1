# LIC-EXPERIMENT-1-
## AIM-
Using LTspice to examine a CS amplifier characterization like frequency response,bandwidth,phase difference,gain.Utilizing DC,transient,AC analysis using 180nm technology lib.-
## COMPONENTS REQUIRED-
NMOS and PMOS(180nm technology node),Resistor,voltage source,AC ground,Wires
## THEORY AND SIMULATION
A)DC ANALYSIS:When we talk about DC analysis for a MOSFET, the main goal is to figure out the stable operating point of the transistor. This is important because we want the MOSFET to work in its saturation region, which is where it can properly amplify signals.-
For the MOSFET to be in saturation, the voltage between the drain and source (VDS) needs to be greater than something called the overdrive voltage (VOV). The overdrive voltage is just the difference between the gate-source voltage (VGS) and the threshold voltage (VTH) of the MOSFET.  VOV = VGS - VTH.-
For simulating open LTspice click on configure analysis and in that select DC op pnt and then click ok.-
B)AC ANALYSIS:When we analyze a MOSFET for AC signals (small alternating signals), we treat it as a linear small-signal amplifier. This means we’re looking at how tiny changes in the input voltage (at the gate) affect the output current (at the drain). In this case, the drain current (iD) is directly proportional to the small changes in the gate voltage (vgs). ID=gm*vgs.The voltage gain (Av) of the amplifier is calculated using this formula:Av = -gm (RD || RL).-
For simulating open LTspice click on configure analysis then put the value which is shown in the fig below
![Image](https://github.com/user-attachments/assets/d095650b-5e16-4138-a121-2f1b8b738aa2)
and then right click on Vin and put the waves what you need and put amplitude value as 1.
C)TRANSIENT ANALYSIS:Transient analysis is all about understanding how the amplifier responds to time-varying signals, like sudden voltage changes or pulse inputs. Imagine you’re sending a quick "blip" of voltage into the amplifier—transient analysis helps us see how the circuit reacts to that blip over time.When the input signal changes suddenly (like a step or a pulse), the amplifier doesn’t respond instantly. Instead, its behavior is influenced by the charging and discharging of capacitors in the circuit.
For simulating open LTspice click on configure analysis then click on transient then just put the value of stop time as your wish.
## 1.1 CIRCUIT DIAGRAM
![Image](https://github.com/user-attachments/assets/780c8916-68cd-424c-aab2-06a45db15e21)-
## 1.2 PROCEDURE
1.Open LTspice and create a new schematic.-
2.Build the common source amplifier circuit as per the circuit diagram.-
3.Set component values-
4.Download the library file named tsmc018.txt from the provided source.-
5.Create a new folder on your computer.Save the downloaded library file (tsmc018.txt) into this folder.-
6.ADD a SPICE directive to import the library file.-
7.Set the MOSFET model name to CMOSN (as specified in the library file).-
8.Set the transistor parameters-
9.Run the simulation using the .op (operating point) analysis.-
10.After the simulation, check the current flowing through the resistor or the MOSFET-
## 1.3 CALCULATION
Given Power=100uW  
we have to find I  
WKT P=VI where V=1.8v  
hence,I=55.5uA  
Now,VDD=IDRD+VOUT,where VDD=1.8V,ID=55.5uA,RD=1kohm  
so,VOUT=1.745V  
Hence Qpoint=(1.745v,55.5uA)  
## 1.4 RESULTS
A)DC ANALYSIS:  
![Image](https://github.com/user-attachments/assets/744eee30-b993-44fd-b451-ac6143f0634c)
B)AC ANALYSIS:






