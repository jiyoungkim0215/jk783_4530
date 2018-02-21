##CEE 4530
###Prelab 3
####Elle Blake
1)	How many grams of NaHCO3 would be required to keep the ANC levels in a lake
above 50 µeq/L for 3 hydraulic residence times given an influent pH of 3.0 and a
lake volume of 4 L, if the current lake ANC is 0 µeq/L?

The definition of total acid neutralizing capacity is given by the following:
$ANC = \left [HCO_{3}^{-} \right ]+2\left [ CO_{3}^{-2} \right ]+\left [ OH^{-} \right ]-\left [ H^{+} \right ]$
However, due to the assumption that carbon is conserved, we can cancel out the first two terms. Additionally,
we are given a solution with a pH of 3, which further simplifies the above equation to:
$ANC \simeq  -\left [ H^{+} \right ]$
this results in an $ANC_{in}$ of -0.001 eq/L

Using the equation:
$ANC_{0} = -\left [ ANC_{out} - ANC_{in}\cdot \left ( 1-e ^{\frac{-t}{\Theta }} \right )\right ]\cdot e^{\frac{-t}{\Theta }}$
We plug in the above value we determine for $ANC_{in}$ and $\frac{-t}{\Theta }$ = 3 given the three hydraulic residence times. Further,
we were given that $ANC_{out}$ = 50 $\frac{\mu \ eq}{L}$.

$ANC_{0} = \left [ 0.000050- 0.001\cdot  \left ( 1-e ^{-3} \right )\right ]\cdot e^{3} = 20.09\frac{\mu \ eq}{L}$

The quantity of sodium bicarbonate needed is found by:

$\left [ NaHCO_{3} \right ]_{0} = ANC_{0}$

$\frac{20.09 mmoleNaHCO_{3}}{Liter}\times \frac{84mgNaHCO_{3}}{mmoleNaHCO_{3}}\times 4 Liters = 6,750mg NaHCO_{3}$
