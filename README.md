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
![Image 2](images/Height of the water in the tank.jpg)
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
![Image 4](images/Flow rate resistor tank accumulator.jpg)
