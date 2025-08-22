# Analysis of Circuits - Resonance and Amplifiers

## Resonance
- From the gain of the circuit, the resonant term will be the real part of the denominator, of the form $1-\omega^2 LC$, meaning that the resonant frequency occurs when $f=\frac{1}{2\pi \sqrt{CL}}$
- Quality factor, $Q$, is reduced when imperfections or resistors are present. A $Q$ above 10 is good, below 1 is very bad.
- $|v_2|=Q|v_1|$, so Q is the amplification at resonance

- If the two values of frequency where the peak voltage is reduced by a factor of $\sqrt{2}$ are $f_1$ and $f_2$, then the band with, $\delta \omega = f_2-f_1$.
- Or $\delta \omega = \frac{\omega_0}{Q}$
- At resonance, we can change a resistor in parallel with a capacitor/inductor into one in series, and vice versa. The Q factor is the same for both
- $Q_T$ can only be found once all the resistors are combined

## Amplifier Circuit

![Amplifier Circuit](amplifier2.png)

- $R_{in}$: Input impedance. $R_{out}$: Output impedance. $R_L$: Load resistor. $A$: Gain.
- This model applies to circuits with linear gain. Can calculate the total gain using potential dividers.
- If $R_L >> R_{out}$ and $R_{in} >> R_S$ then Gain $\approx$ $A$.
- We can also have current amplifiers, current to voltage amplifiers (trans-impedance), or voltage to current amplifiers (trans-conductance)
- The overall power gain: 
  $$\frac{P_{out}}{P_{in}}=\frac{V_{out}^2}{V_{in}^2}\frac{R_{in}}{R_L}$$
- $G_P=10\log_{10}(\frac{P_2}{P_1})$
- Maximum power theory: The maximum output power occurs when $R_L=R_{out}$. Match the load to the output impedance.
- The added power comes from an external bipolar DC power supply to the amplifier. This limits the signal, as $V_{out}$ cannot go above V+ or below V-, causing the top of the sinusoid to be clipped off.

## Calculating Parameters
- $A_V=\frac{V_{out}}{V_{in}}$
- $R_{in}=\frac{v_{in}}{i_{in}}$
- $R_{out}=\frac{V_x}{i_x}$

## Band-Pass Filter
When a high-pass and low-pass filter are paired together, they create a band-pass filter

![Band Pass Filter](band_pass_filter.png)
