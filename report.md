# Part3

## First Section 

1. Powers:
   - > **Dynamic Power**: the power comsumed while the inputs are active. While active switching of transistors occurs, meaning the switch of a gate (0 to 1, 1 to 0), the capacitor is charging and discharging. The required energy for the procedure causes the dissipation of the dynamic power. It depends on the capacitance of the transistors, the frequency of switching and the activity level. 
   - > **Leakage** : the power consumed while the circuit is inactive is the static power. At this state, leakage of the transistors occurs. Leak-
age current depends on the width of the transistors and the local state of the devices. There are two types of leakage, the subthreshold and the gate leakage. Subthreshold leakage is related to the source an drain while the gate leakage is related to current leaking through the gate.

By looking at the different defenitions above we can assume that when we run different programs on a procesor only the dynamic power will be affected and not the leakage. This can be explained by the dependencies the two powers have. More specifically, the leakage depends only on the width of the transistor and the state of the circuit, which are not affected by the program, whereas the dynamic power depends on the frequency of switching, which is determined by the program.

Apparently, the duration of the execution does not affect either of the powers above, considering that neither of them have a time dependency.

2. - We have a system with a certain battery capacitance and using two processors with different power consumtions (first 5W and second 50W).
   The battery life is directly connected to the CPU clock speed. Specifically, higher clock speed results to shorted battery life. Furthermore, a relation between the clock speed and the power consumption also exists. The higher the power consumption is the higher the clock speed. 
   - So in our case, since the second processor consumes more power, it can't provide longer duration to the battery.
   - McPAT only provides information regarding the dynamic and static power of the processor. For this reason we cannot make assumptions regarding the battery life. An auxiliary information from McPAT would be something related to the CPU clock speed.

3. The results provided by McPAT for the processors Xeon and ARM A9 (in this case with print_level 3) are copied in the files Xeon_results.txt and ARM_results.txt respectively.  
By reviewing these results we deduce that the Xeon processor cannot be more energy efficient than the ARM A9 since both the dynamic and the static(leakage) power dissipation of Xeon is larger than ARM's processor, as shown below:  

**Xeon results**:
```python
  Peak Power = 134.938 W
  Total Leakage = 36.8319 W
  Peak Dynamic = 98.1063 W
  Subthreshold Leakage = 35.1632 W
  Subthreshold Leakage with power gating = 16.3977 W
  Gate Leakage = 1.66871 W
  Runtime Dynamic = 72.9199 W
```
**ARM A9 results**:
```python
  Peak Power = 1.74189 W
  Total Leakage = 0.108687 W
  Peak Dynamic = 1.6332 W
  Subthreshold Leakage = 0.0523094 W
  Gate Leakage = 0.0563774 W
  Runtime Dynamic = 2.96053 W
```
Also, since the clock speed of Xeon is 50 times higher than ARM A9, as mentioned and explained in the previous section the battery life of Xeon is lower than ARM A9 and consequently Xeon is less energy efficient.

## Second Section

## Referencies
- [Dynamic-static power](https://www.edaboard.com/threads/what-is-static-power-dissipation-and-dynamic-power-dissipation.67491/)
- [Dynamic power and leakage](https://acg.cis.upenn.edu/milom/cis501-Fall10/lectures/12_power.pdf)
- [Clock and battery life relation](https://www.quora.com/Does-CPU-clock-rate-effect-battery-life)
- [Power and clock speed realtion](https://en.wikipedia.org/wiki/List_of_CPU_power_dissipation_figures)
- [Processor power dissipation](https://en.wikipedia.org/wiki/Processor_power_dissipation)
