# AC Power - Transformers

$v=N\frac{d\phi}{dt}$

![Equivalent transformer circuit](Transformer%20equivalent%20circuit.png)

For an ideal transformer: Iron is a perfect conductor of flux. $\tilde{I}_2:\tilde{I}_1=N_1:N_2=$ Turns ratio.

The primary and secondary current are in phase, as are the primary and secondary voltage, but they aren't in phase with each other.

$\frac{\tilde{V}_1}{\tilde{V}_2}=\frac{\tilde{I}_2}{\tilde{I}_1}=\frac{N_1}{N_2}$

Load P and Q = Input P and Q. An ideal transformer does not consume any real or reactive power. $P_1=P_2, Q_1=Q_2$

A resistance on one side of the transformer has an equivalent resistance on the other side. $Z_s=(\frac{N_1}{N_2})^2 Z_p$

For a real transformer: The reluctance of the iron core is non-zero, so an inductor is added in parallel with the transformer. There are power losses in the iron core due to hysteresis (loss $\propto \phi^2 \propto E_1^2$), and eddy current loss (also $\propto \phi^2 \propto E_1^2$). These iron losses are represented by a resistor $R_0$ in parallel with the inductor.

The windings have a resistance, so the model is given series $R_1$ and $R_2$ on the primary and secondary winding respectively. Not all flux links the secondary coil, resulting in leakage flux, which induces additional voltage drop. So stray inductance inductors are put in series with $R_1$ and $R_2$.

![Real transformer](real%20transformer.png)

These components can be combined on one side using the turn ratio squared.

![Real transformer 2](real%20transformer%202.png)

As $R_0$ and $X_0$ are much much larger than $X_{t1}$ and $R_{t1}$, they can be ignored in this final circuit.

The transformer rating is the max input power before the copper losses or the iron losses are too high and the transformer overheats.

To determine $R_0$ and $X_0$, carry out an open circuit test. The turns ratio is slightly different, being $\frac{E_1}{E_2}=\frac{V_1}{V_2}$

![Open circuit test](Open%20circuit%20test.png)

As before, only the resistor consumes real power, and only the inductor consumes reactive power.

To determine $X_{t1}$ and $R_{t1}$, conduct a short-circuit test. $V_2=E_2=E_1=0$

![Short-circuit test](Short-circuit%20test.png)

A transformer reduces current to reduce losses in cables. It also isolates a circuit, making it safer in case of failure. It can also reduce voltages to measurable levels.

Low frequency transformers: laminated iron cores. High frequency transformers: ferrite.

Efficiency = $\eta=\frac{Power_{output}}{Power_{input}}=1-\frac{P_{losses}}{P_{in}}$. Specifically real power. You will have to add up all the real power consumption in the equivalent circuit.

Regulation measures the change in load voltage from the open-circuit value due to load current.

Regulation $=\frac{V_{2OC}-V_2}{V_{2OC}}\times 100\%$

Small regulation is better as you want your transformers output voltage to be as constant as possible.

We find the voltage across the load using a potential divider equation.
