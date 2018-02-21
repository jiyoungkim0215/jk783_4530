##Pre-Lab
1)	How many grams of NaHCO3 would be required to keep the ANC levels in a lake above 50 µeq/L for 3 hydraulic residence times given an influent pH of 3.0 and a lake volume of 4 L, if the current lake ANC is 0 µeq/L?

This problem is almost identical to the problem referenced in the lab section titled "Reactor Theory Applied to Lake Remediation" and solved in equations 1.21 through 1.26. The only difference is that we are calculating for when t = 3theta instead of just 1 hydraulic residence time.

```Python
from aide_design.play import *
import math
ANCout = 0.000050* (u.mole/u.L)
ANCin = -0.001 * (u.mole/u.L)
ttheta = 3
ANCo = (ANCout - (ANCin * (1 - (math.e)**(-ttheta))))*((math.e)**(ttheta))
V = 4 * u.L
mwNAHCO3 = 84 * (u.g/u.mole)
Quantity = ANCo * V * mwNAHCO3
print(Quantity)
