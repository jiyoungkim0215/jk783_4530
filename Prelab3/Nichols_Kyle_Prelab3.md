## Laboratory 3 PreLab Questions
### Kyle Nichols

```python
from aide_design.play import*
```

1. How many grams of NaHCO3 would be required to keep the ANC levels in a lake above 50 µeq/L for 3 hydraulic residence times given an influent pH of 3.0 and a lake volume of 4 L, if the current lake ANC is 0 µeq/L?

$ANC = [HCO_{3}^{-}] + 2[CO_{3}^{-2}] + [OH^{-}] - [H^{+}]$
$ANC_{0} = [ANC_{out} - ANC_{in} * (1 - e^{-(t/\theta )}] * e^{t/\theta }$

Since $t=3\theta$

$ANC_{0} = [ANC_{out} - ANC_{in} * (1 - e^{-3})] * e^{3}$

Since NaHCO3 dissolves to Na and HCO3-:

$ANC_{0} = [HCO_{3}^{-}]$

Molecular weight of 84 g/mol

```python
ANCin =  -10**(-3)/(u.l)
ANCout = .00005/(u.l)
ANCo = (ANCout-(ANCin*(1-2.71828**(-3))))*(2.71828**(3))
HCO3 = ANCo * 84*(u.g)*4*(u.l)
print(HCO3)
```
6.75 grams of NaHCO3 are required.
