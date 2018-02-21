```python
from aide_design.play import*
import math as math
```
## Leah Balkin

Find grams of NaHCO3 required to keep ANC levels in a lake above 50u.eg/l
```python
volume = 4*u.l
molecular_weight = 84*u.mg/u.mmol
#actual units for ANC are u.eq/u.l
currentANC = 0*1/u.l
out_ANC = .000050*1/u.l
influent_pH = 3.0
ANC_in = -.001*1/u.l
ANC_knot = (out_ANC-ANC_in*(1-math.exp(-3)))*math.exp(3)
grams_needed = (ANC_knot*molecular_weight*volume)
print(grams_needed)
```
