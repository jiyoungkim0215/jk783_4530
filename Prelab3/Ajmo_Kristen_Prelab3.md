#Pre-Lab Questions
##Lab 3: Acid Precipitation and Remediation of Acid Lakes
###Kristen Ajmo

```python
from aide_design.play import *  
import math as math 
ANC_OUT= 50*1/u.L
HYDRAULIC_RESIDENCE_TIME=  3 #t/theta   #Where multiplied by 1, this is a micro equivalent
PH_IN= 3
ANC_IN= 0*1/u.L
V_LAKE=4*u.L
ANC_0=(math.exp(HYDRAULIC_RESIDENCE_TIME))*(ANC_OUT-ANC_IN(1-math.exp(-HYDRAULIC_RESIDENCE_TIME)))
print(ANC_0)

NAHCO3_0= ANC_0  ##moles/L
NAHCO3_0_MASS= NAHCO3_0*(84*u.mg/u.mmol)*V_LAKE
print(NAHCO3_0_MASS)
#Where multiplied by 1, this is a micro equivalent
```
