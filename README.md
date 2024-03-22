# Hydraulic-System-Control
In this project, we model a hydraulic system and design a controller to stabalize the system. 
<br>
<br>
__System Description and Modeling__:
<br>
<br>
The system is a single input-single output system. The input is the volumetric flow rate of the hot water going into the system and the output is the temperature of the water in the tank. 
The hot water temperature, cold water flow rate, and temperature are fixed. 
The tank's initial temperature is between cold and hot water. 
Tank and accumulator temperatures are equal and unaffected by accumulator water due to its negligible volume. The specific heat of tank water is constant and matches hot and cold water inputs.
<br>
<br>
![Image 1](images/system.jpg)
<br>
<br>
H1 = Height of the water in the tank
<br>
H2 = Height of the water in the accumulator
<br>
P1 = Pressure in the tank
<br>
P2 = Pressure in the accumulator
<br>
A1 = Cross sectional area of the tank
<br>
A2 = Cross sectional area of the accumulator
<br>
R1 = Fluid resistor between the tank and the accumulator
<br>
R2 = Fluid resistor between the accumulator and the outside
<br>
k = Spring constant of the spring in the accumulator
<br>
u = Input volumetric flow rate of the hot water
<br>
uc = Input volumetric flow rate of the cold water
<br>
Q1 = Volumetric flow rate across the first fluid resistor
<br>
Q2 = Volumetric flow rate across the second fluid resistor
<br>
Th = Temperature of the input hot water
<br>
Tc = Temperature of the input cold water
<br>
T = Temperature of the water in the tank
<br>
<br>
__Differential Equations__:
<br>
Height of the water in the tank:
<br>
![Image 2](images/Height_Water.jpg)
<br>
 Pressure and the height in the tank:
 <br>
  ρ is the density of the water and g is the acceleration due to gravity
 <br>
 ![Image 3](images/Pressur_Height.jpg)
<br>
<br>
 Flow rate across the first fluid resistor and the
pressures in the tank and accumulator:
<br>
![Image 4](images/Flow_resistor_tank_accumulator.jpg)
<br>
<br>
The height of the
water in the accumulator and the pressure in the accumulator:
<br>
![Image 5](images/Height_pressure_accumulator.jpg)
<br>
The pressure in the accumulator and the flow rate across the second fluid resistor:
<br>
![Image 6](images/Flowrate.jpg)
<br>
<br>
Using the mentioned equations, we can get:
<br>
![Image 7](images/EQ1_Diff.jpg)
<br>
![Image 8](images/EQ2_Differ.jpg)
<br>
![Image 9](images/EQ3_Diff.jpg)
<br>
<br>
__State Space__:
<br>
<br>
we set T, P1, P2 as the state variables:
<br>
x1: T,   x2:P1,   x3:P2,  y: output
<br>
![Image 10](images/state_space.jpg)
<br>
Since we have a single input single output system with 1 equilibrium point, we use the equation below to finde the transfer function from the state matrices:
<br>
![Image 11](images/transfer_func.jpg)
<br>
Now we plot the RootLocus and Bode diagram of the system:
<br>
<br>
Gain Margin: $\infty$,  Phase Margin:96.1,  Band Width:0.013 Hz
<br>
<br>
__Controller__:
<br>
<br>
We design a lead lag controller:

<br>
Then we compare the system before and after the conteoller:
<br>
<br>
As we can see, the rise and settling time decreased and the system became faster.
<br>
We plot the Root locus and the bode diagram of the conterolled system:
<br>
<br>
Gain Margin: $\infty$,  Phase Margin:135.14,  Band Width:0.173 Hz
<br>
<br>
__Distrurbance__:
<br>
<br>
input: step function with 0.02 amplitude.
<br>
System without disturbance:
<br>
We add a white guassian noise :
<br>
<br>
__Non linear Model__:
<br>
Now we use the original non-linear model of the system to check the performance of the controller:
<br>
