# Logic Gates

Logic/ binary/ Boolean variables all refer to the same thing, variables with 2 values, 0 or 1.

A circle on the output of a gate always implies that it is an inverting output.

An exclusive OR gate, a XOR gate, only has an output of 1 where only 1 of the inputs is 1. $Y=A \oplus B$

A logic circuit is not linear. An ideal inverter, swaps from high to low output or vice versa at exactly $\frac{V_{max}}{2}$.

With non linear devices in electrical circuits, we have to find draw load lines and find their intersection.

We are going to be using enhancement mode N-channel MOSFETs, so it is off when $V_{GS}=0$.

The transistor starts conducting when $V_{GS}$ reaches a threshold voltage, $V_T$. The greater $V_{GS}$, the greater $I_{DS}$.

NMOS Inverter: 
![NMOS Inverter](NMOS%20Inverter.png)

From the diagram it is clear that $V_{in}=V_{GS}$ and $V_{out}=V_{DS}$. If we plot the load line, we can see that it does invert but very poorly, and only if we consider that $V_{out} > 9V$ to be logic 1 and $V_{out} < 2V$ to be logic 0.

For more complex gates, we must consider how $V_{out}$ varies as current flows in each transistor. This determines the boolean output given boolean inputs.

Real MOSFETs have stray capacitance that can be modelled by a capacitor in parallel across the FET.
This gives a temporal response, and a given time to reach the high logic state.

We can replace the resistor with a MOSFET with the gate connected to the drain, so $V_{GS}=V_{DS}$, to reduce the size of ICs.

Complementary MOS - CMOS. Reduces the power dissipation in FET circuits. PMOSFETs are essentially NMOSFETs with all the polarities reversed.
In the circuit symbol, the arrow is going outwards. It is usually drawn upside down, with the source connected to $V_{DD}$.
The current flows from source to drain.
Normally the gates of the PMOS and the NMOS are connected, so we again have to consider their states for low and high inputs.

CMOS inverters have no power consumption when at HIGH or LOW, only consuming power when switching states.
For a CMOS inverter:
![CMOS inverter](CMOS%20inverter.png)
