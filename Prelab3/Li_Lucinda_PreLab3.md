```python
from aide_design.play import*
```
## Laboratory 3 Pre Lab Questions
### Lucinda Li

1)	How many grams of NaHCO3 would be required to keep the ANC levels in a
lake above 50 µeq/L for 3 hydraulic residence times given an influent pH of 3.0
and a lake volume of 4 L, if the current lake ANC is 0 µeq/L?

```python
import math
# ANCout = ANC in lake outflow at any time t (for a completely mixed lake the effluent ANC is the same as the ANC in the lake)
# ANCin = ANC of acid rain input
# V = volume of reactor
# Q = acid rain input flow rate.
# restime = residence time
ANCin=-0.001 #eq/L
ANCout=0.00005 #eq/L
restime=3
ANC0=(ANCout-ANCin*(1-math.exp(-restime)))*math.exp(restime) #eq/L
print(ANC0)
MWNaHCO3=84 #g/mole
ConcNaHCO3=ANC0 #mole/L
Vol=4 #L
MassNaHCO3=ConcNaHCO3*MWNaHCO3*Vol #g
print(MassNaHCO3)
```
