# Part3

## First Section 

1. Powers:
   - > **Dynamic Power**: the power comsumed while the inputs are active. While active switching of transistors occurs, meaning the switch of a gate (0 to 1, 1 to 0), the capacitor is charging and discharging. The required energy for the procedure causes the dissipation of the dynamic power. It depends on the capacitance of the transistors, the frequency of switching and the activity level. 
   - > **Leakage** : the power consumed while the circuit is inactive is the static power. At this state, leakage of the transistors occurs. Leak-
age current depends on the width of the transistors and the local state of the devices. There are two types of leakage, the subthreshold and the gate leakage. Subthreshold leakage is related to the source an drain while the gate leakage is related to current leaking through the gate.

By looking at the different defenitions above we can assume that when we run different programs on a procesor only the dynamic power will be affected and not the leakage. This can be explained by the dependencies the two powers have. More specifically, the leakage depends only on the width of the transistor and the state of the circuit, which are not affected by the program, whereas the dynamic power depends on the frequency of switching, which is determined by the program.

Apparently, the duration of the execution does not affect either of the powers above, considering that neither of them have a time dependency.

2. 


## Second Section
