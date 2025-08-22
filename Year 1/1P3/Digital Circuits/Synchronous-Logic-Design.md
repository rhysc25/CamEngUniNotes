There are 5 steps when designing synchronous logic circuits.

1) Firstly, draw a state diagram. There must be paths coming from each state equal to the number of possible input combinations
2) Then, allocate your bistables. If there are $2^n$ states, you need n bistables. Even if one state is not needed, you still need to formulate logic for it. Normally have it send the system back to state 0 for all inputs
3) Draw a state transition table. What do J and K need to be for each combination of inputs, at each given state
4) Draw a Karnaugh map for each input
5) Construct the full circuit. You may also need to produce a logic circuit for the outputs

## DAC conversion

To convert digital signals to analogue, we can implement a weighted resistor DAC. If the logic variable is $a_0$, then we can write the volts as $a_0 A$ where $A$ is the $V_DD$. 

We can calculate the total current to the op amp as the sum of all the currents through the decreasing resistances.

For increasing binary number inputs, the output voltage increases as a staircase, when the intended output it a linear increase.

The problems with the weighted resistor DAC are:
* Loads of resistor values, hard to implement as many would have to be different materials
* The resistor for the MSB would have to be incredibly accurate so as to not drown the effects of the lesser significant bits
* The way the different resistor values change with temperature would be different, so the output of the circuit would drift as it warms up

Instead, we can implement an R-2R Ladder DAC

![[Pasted image 20250508112329.png]]

$i_{n+1} = 2i_n$, due to the layout of the resistors. 

This gives $I$ as:$$I=\frac{A}{2^n R}\sum_0^{n-1}a_m 2^m$$
And $V=-IR'$, giving the output voltage

This is better as it only requires 2 resistor values, is much more accurate, much more stable and scalable

## ADC conversion

We can just use a 1-bit comparator, an op amp circuit with $V_{in} and $V_{ref}$
When the gain is very large:
* If: $V_{in} > V_{ref} \Rightarrow V_{out} = V_{-}$
* If: $V_{in} < V_{ref} \Rightarrow V_{out} = V_{+}$

However this leads to fluctuations in output when the AC voltage is near to the threshold $V_{ref}$

Therefore we introduce a Schmidt trigger, adding hysteresis to the comparator.
If $V_{in}$ is LOW initially then it must rise above $V_{upper}$ for a change in the output.
If $V_{in}$ is HIGH initially then it must drop below $V_{lower}$ for a change in the output.

Flash ADC
![[Pasted image 20250509133038.png]]


This is bad as it requires a huge amount of comparators

Instead, we can introduce a stair-step ramp to gradually rise and detect when the input becomes less than the ramp value. However this is much slower than the flash ADC

## Full adder circuit

![[Pasted image 20250509133259.png]]

Where $C_i$ is the carry in and $C_{i+1}$ is the carry out. This can be obtained by comparing inputs and outputs in a table

These can be chained together into a ripple carry adder circuit so that larger numbers can be summed, with the $C_{out}$ of one into the $C_{in}$ of another

If all the A inputs are inverted and $C_{0}$ is set to 1, this has the effect of calculating $-A+B$ instead, allowing for easy subtraction as well

