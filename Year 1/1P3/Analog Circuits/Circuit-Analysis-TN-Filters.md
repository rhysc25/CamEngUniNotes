# Analysis of Circuits - T+N and Filters

## Basics
- Potential difference points towards the side of the component with a more positive voltage
- Thevenin and Norton cannot be used to analyse the power dissipated in components, you must return to the original layout
- $V_{rms}=\frac{V}{\sqrt2}$
- $CIVIL$: For a capacitor: voltage follows current. For an inductor: current follows voltage
- $1/\omega C$ is the reactance of the capacitor, $\omega L$ is the reactance of an inductor
- The internal resistance of a voltage source is its open source voltage / short circuit current

## Kirchoff's Laws
- Kirchoff's voltage law: The sum of the voltages around a closed loop must be zero. 
- Kirchoff's current law: The sum of currents at a node must be zero.
- Bridge circuits: for the meter (G) to read zero, the bridging condition must be met: $Z_x=Z_3 \cdot \frac{Z_2}{Z_1}$

## First Order Low Pass Filter

![Low Pass Filter Circuit](Low-pass-filter-circuit.png)

- At DC, ($\omega$ = 0) ⇒ $Z_c = \infty$ ⇒ $V_{out}=V_{in}$
- At AC, as $\omega$ increases, $V_{out}$ approaches 0
- A high pass filter is identical but $V_{out}$ is across the resistor

## Filter Analysis
- Gain = $\frac{V_{out}}{V_{in}}$, which for the low pass filter = $\frac{1}{1+jRc\omega}$
- We want the gain as a ratio of complex numbers Eg. $\frac{A+jB}{D+jE}$
- For the $1/\sqrt{2}$ point/ $\frac{1}{2}$ power point/ 3 dB point/ 0.7 point then D = E. For this example it means that 1 = $RC\omega, \Rightarrow f =\frac{1}{2 \pi RC}$
- On decibel scale: $G=10log_{10}(P_2/P1)=20log_{10}(V_2/V_1)$ (Assumes $R_{in} = R_{out}$)
- Bode plot = Gain in dB against logarithmic scale of frequency
