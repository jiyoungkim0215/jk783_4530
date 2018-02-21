# Laboratory 3 Pre Lab Questions
# Andrew Kang

 How many grams of NaHCO3 would be required to keep the ANC levels in a lake above 50 μeq/L for 3 hydraulic residence times given an influent pH of 3.0 and a lake volume of 4 L, if the current lake ANC is 0 μeq/L?


```python
from aide_design.play import*

import math
ANC_in = -0.001*(u.mole/u.L)    ##pH is 3.0 so ANC_in is -.001
ANC_out = 0.000050*(u.mole/u.L) ##Given
theta_t = 3                     ##Residence time is 3
V = 4 * u.L                     ## Given Volume
ANC_0 = (ANC_out - (ANC_in * (1-(math.e**theta_t))))*((math.e)**(theta_t))  ##Formula Given
NaHCO3_mass = 84 * (u.g/u.mole) ##Molecular weight of NaHCO3
NaHCO3_req = ANC_0 * V * NaHCO3_mass  ##Formula 1.26 from Lab
print (NaHCO3_req)
