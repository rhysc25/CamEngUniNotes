# Semiconductors

## Basic Properties
- A semiconductor is a material whose conductivity increases as temp increases, as electrons are freed from their valence shells.
- Holes flow in the opposite direction to electrons, the direction of hole flow = the direction of conventional current.
- Pure silicon is called intrinsic silicon, has 4 electrons in the valence shell, and is a very stable dielectric.
- N-type doping - adding $10^7$ppm of a pentavalent impurity.
- P-type doping - adding $10^7$ppm of a trivalent impurity.

## P-N Junction
- When a p-type region meets an n-type region, electrons fill the holes, creating an insulating depletion region. There is an electric field across it towards the holes, but it is not strong enough for electrons to cross the depletion region.
- There is a very small reverse saturation current $I_O$ however, as electrons can leak through.
- This small current can be varied with light intensity incident on the diode, allowing for photo diodes.

- When a reverse bias voltage is applied, electrons and holes pulled away from the depletion zone, increasing the size of the depletion zone.
- When a forward bias is applied, electrons and holes pushed into depletion region, causing it to disappear. Current only allowed in one direction, diode.
- The forward bias required to remove the depletion zone is about $0.7V$.
- When an electron falls into a hole in forward bias, energy is released, allowing for LEDs.

## Diodes
- The IV graph for a diode can be approximated as $I \propto V^2$.
- To find the voltage across a diode, we must draw the diode's IV graph and the load line for the circuit, then find their intersection.
- Diodes used in rectifier circuits, removing reverse voltage.

## Transistors
- If doping levels are controlled correctly it is possible to create a large current flow with a much smaller input.
- Field-effect transistors (FETs) are voltage controlled.
- Bipolar junction transistors (BJTs) are current controlled.

We are going to focus on n-channel enhancement/depletion MOSFETs, where the source and drain are made of n-type material. P-type functions the same way but with all the signs reversed.

![Transistors](Transistors.jpg)

![Enhancement Mode Characteristics](Enhancement_N-type.png)

![Depletion Mode Characteristics](Depletion_N-type.png)

- $V_{GS}$ is the voltage of the gate relative to the source. Current flows from drain to source when a the threshold voltage is applied to the gate.
- Ignore the Ohmic region, where $V_{DS} > V_{GS}$. In the saturation region, the output voltage roughly increases linearly with input voltage. Essentially a voltage controlled current source.

- A depletion MOSFET is when there is a pre-biased N-type channel, where the depletion region is created initially by repelling the electrons in the channel.

## FET Circuit Design
There are two stages to designing any FET circuit:
1. DC analysis/ biasing/ quiescent setup/ operating point. To determine the operating point of the transistor
2. AC analysis/ small signal model 

## Common Source Amplifier

![Common Source Amplifier](Common_Source_Amplifier.png)

- Input = $V_{GS}$. Output = $V_{DS}$
- As a general rule of thumb, set $V_{DS}$ to half of $V_{DD}$ to allow for maximum voltage swing. $R_G$ should be really large, typically $1$M$\Omega$ is good

- Gain = $\frac{\Delta Output}{\Delta Input}\approx \frac{\Delta V_{DS}}{\Delta V_{GS}}$. This is estimated from the graph and is highly inaccurate.
- An inverting amplifier is one with negative gain. To create a positive gain, add an even number in series.

## Self Biased Depletion MOSFET

![Self biased depletion MOSFET](Self_biased_depletion_MOSFET.png)

- $V_G=\frac{R_2}{R_2+R_1}V_{DD}$          $V_{GS}=V_G-V_S$
- $V_S=I_D R_S$ $I_D=\frac{V_{DD}-V_D}{R_D}$
- $R_S$ is the key to setting the operating point. The next stage is to see how the circuit operates with a small AC signal applied to the input.

## Small Signal Model
- For small signal, apply a small AC voltage to the existing DC voltage set up. Larger $V_{out}$ than $V_{in}$. $V_{out}$ cannot exceed $V_{DD}$, or else clipping occurs. It is essentially oscillating along the load line.

$$\Delta I_D=\frac{\partial I_D}{\partial V_{DS}}\cdot \Delta V_{DS} + \frac{\partial I_D}{\partial V_{GS}}\cdot \Delta V_{GS}$$
$$i_d=\frac{v_{ds}}{r_d}+g_m v_{gs}$$

- Drain resistance = $r_d$. $\frac{1}{r_d}=\frac{\partial I_D}{\partial V_{DS}}$ which is the gradient of the characteristic graph of the FET with $V_{GS}$ constant.
- Mutual conductance = $g_m=\frac{\partial I_D}{\partial V_{GS}}$ which is the rate of change in a straight vertical line on the FET's characteristic graph.

The small signal model of a FET:

![Small Signal Model](SSM.png)

- Take $V_{DD}$ and any other DC sources to be connections to ground. Example conversion:

![Source Follower](Source_Follower.png)

![SSM Equivalent](SSM_equivalent.png)

- In this case, $v_1=v_{gs}+v_s$. This effects how we calculate gain and output resistance.
- Determining the gain becomes much simpler if we use the assumption that $r_d$ is very large, so can be ignored.
- To determine output resistance: Apply a test voltage $v_x$ and a test current $i_x$, with the input shorted, then find $\frac{v_x}{i_x}$.

- A FET circuit with a gain of 1 is called a buffer circuit.
- In order to stop $R_S$ from reducing the gain, add a capacitor in parallel with it. This has no effect in DC, but at high AC frequency removes the effect of $R_s$.
- However this also causes a frequency cut off for the circuit, where it has reduced gain.

- In order to cascade FET circuits, connect them together, output to input. However the DC biasing will mean they have different DC voltages, so a coupling/decoupling capacitor is inserted between the two. $f=\frac{1}{2\pi C(R_{out1}+R_{in2})}$, where $R_{out1}$ and $R_{in2}$ are the equivalent input and output resistors for the FET amplifying circuits.
- However, each capacitor means a 3dB cut off point, reducing the gain significantly.

- There is also parasitic capacitance within the FET, eg. $C_{gd}$, which can provide an alternate path from the gate to the drain at high frequencies. $C_M=(1-A)C$. The more gain in a single stage, the more miller capacitance.

## Op-Amps
- An OpAmp simplifies the entire DC biasing and iterating process so much easier. Are essentially an entire self-biasing FET circuit within a chip.
- OpAmps are powered by an external bipolar power supply, which sets the max voltage swing at the output before clipping occurs.

- An OpAmp has a (+) and a (-) input, and is designed so that the potential difference across the two inputs is always zero. This is because it has essentially infinite open-loop gain.
- An OpAmp has infinite input resistance, so there is no current at either input.
- An OpAmp also has zero output resistance.

- An OpAmp can be used to make good filters. Bandpass filter:

![OpAmp bandpass filter](OpAmp_bandpass_filter.png)

- $Z_1$ is a high pass filter, $Z_2$ is a low pass filter.
- $\frac{v_{out}}{v_{in}}=-\frac{Z_2}{Z_1}=-\frac{R_2}{R_1}(1+\frac{1}{j\omega C21 R_2})(\frac{1}{1+\frac{1}{j\omega C_1 R_1}})$
- Midband gain = $\frac{-R_1}{R_2}$. The lower 3dB point is when $\omega_1C_1R_1=1$ and so on.

- Transimpedance amplifier: If the imput is a current and the output a voltage, then the gain is essentially an impedance. These can be used with a photo-diode, which is essentially a light controlled current source, to give high voltages.
- But don't make R/Gain too high as Miller effect (essentially a capacitor from input to output).

## Comparator Circuit

![Comparator](Comparator.png)

- $V_{ref}=\frac{R_2V}{R_1+R_2}$.
- If $V_{in}>V_{ref}$ then $V_{out}=+V$. If $V_{in}<V_{ref}$ then $V_{out}=-V$.
- If $V_{in}\approx V_{ref}$, then there is a lot of noise, so add hysteresis.

## Gyrator Circuit

![Gyrator](Gyrator.png)

- $V_e=\frac{1}{2}V_s$ by potential divider. $i=\frac{V_e-V_s}{R_1} \Rightarrow V_e= -R_1 i$.
- Essentially negative Ohm's law. If $R_1$ is an inductor, it will be essentially turned into a capacitor in terms of response. And a capacitor will become and inductor.
