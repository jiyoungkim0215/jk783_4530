Sophia He

Pre-Lab: Acid Precipitation and Remediation of Acid Lakes

######How many grams of NaHCO3 would be required to keep the ANC levels in a lake above 50 µeq/L for 3 Mhydraulic residence times given an influent pH of 3.0 and a lake volume of 4 L, if the current lake ANC is 0 µeq/L?

```Python
from aide_design.play import*
import math

math.e

math.e

# using moles because python doesnt recognize eq

ANCin = -0.001*u.mol/u.L
ANCout = 0.000050*u.mol/u.L
ttheta = 3

e = math.e

print(e)



ANCo = (ANCout-(ANCin)*(1-(e**(-ttheta))))*e**ttheta

print (ANCo)

#to calculate the quantity of sodium bicarbonate

NaHCO3o = ANCo  #moles of sodium bicarbonate required per liter of lake

molecular_weight_NaHCO3 = 84*u.g/u.mol

V = 4*u.L

NaHCO3_required = NaHCO3o*molecular_weight_NaHCO3*V

print(NaHCO3_required)

```
