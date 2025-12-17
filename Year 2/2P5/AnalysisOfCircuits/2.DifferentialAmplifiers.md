By choosing the appropriate model for an op-amp, we can analyse its function using only three basic parameters:
Input resistance, open-loop gain and output resistance

Almost all op-amps use the same basic circuit structure. The input circuit of an op-amp is a differential amplifier or 'long tailed pair'.
Uses an emitter or source coupled pair of transistors to amplify the difference between the voltages at the two separate inputs

Differential inputs are very useful when dealing with noisy environments

Differential amplifier:
![[DifferentialAmplifier.png]]
The circuit assumes DC biasing
They are n-type as the arrow's going towards the gate. That means current flows from drain to source.

The input signal is defined as the difference between the two inputs ($v_1$-$v_2$)

**Common mode input** 
When $v_1=v_2$
If both input rise together then the currents through $R_1$, $R_2$ and $R_3$ will increase
As the current increases, the voltage at the sources increase, so $V_{GS}$ decreases in a way which counters the increase from the inputs, so the gain will be small

**Differential mode input**

$v_1=-v_2$
Increasing $v_1$ increases the current through $R_3$ and $T_1$ and the voltage $v_2$ decreases, causing an equal fall in current through $R_4$ and $T_2$.
Therefore the current through and hence voltage across $R_3$ remains constant

Common Mode Rejection Ratio (CMRR) is a measure of performance of a differential amplifier and is defined as:

Gain for differential mode signals / gain for common mode signals

The higher the better the differential amplifier
We can use the symmetric nature of the circuit about $R_3$ to reduce the analysis to a single transistor

For common mode gain, we can split $R_3$ into two $2R_3s$ in parallel and consider each half, using the small signal model to get an expression for the gain
In the case of differential gain, as $R_3$ voltage is constant, that becomes a ground in our small signal model

CMRR $\approx \frac{1+2g_mR_3+2\frac{R_3}{r_d}+\frac{R_1}{r_d}}{1+\frac{R_3}{r_d}}\approx 2g_mR_3$
So CMRR increases with $R_3$. However, to maintain a reasonable dc bias current flow through $R_3$, the negative supply voltage increases with increasing $R_3$, soon reaching an absurd value

**The Zener Diode**
![[ZenerDiode.png]]
The Zener effect is a result of quantum tunnelling

We can replace $R_3$ with a transistor and $R_E$. There is a Zener diode connected to the base, as it has an essentially constant voltage drop over a range of currents, so together with a resistor act as a current source. The small-signal impedance looking into the collector of the transistor is very high, allowing for much larger gains.

As Zener diodes are very hard to get into ICs, a more elegant way of making a current source is via a circuit known as the current mirror.
![[CurrentMirrorCircuit.png]]

$I_{B1}$ and $I_{B2}$ can be ignored. If $T_3$ and $T_4$ are identical and $V_{BE1}$ = $V_{BE2}$ then the collector currents, $I_{C1}$ and $I_{C2}$ will be equal, mirroring each other. 
The current mirror can be used as a load for the long-tailed pair