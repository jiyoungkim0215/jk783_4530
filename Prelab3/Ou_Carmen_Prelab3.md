```python
from aide_design.play import*
from math import*
```
## Laboratory 3 Pre Lab Questions
### Carmen Ou

1. How many grams of NaHCO<sub>3</sub> would be required to keep the ANC levels in a lake above 50 µeq/L for 3 hydraulic residence times given an influent pH of 3.0 and a lake volume of 4 L, if the current lake ANC is 0 µeq/L?

```python
ANCout=50*10**(-6)*u.mol/u.L
pH=3.0
ANCin=-10**(-pH)*u.mol/u.L
ANC0=((ANCout-ANCin*(1-exp(-3)))*exp(3)).to(u.mol/u.L)
mass=(ANC0*(84.007*u.g/u.mol)*(4*u.L)).to(u.g)
print(mass)
```

6.751 g
