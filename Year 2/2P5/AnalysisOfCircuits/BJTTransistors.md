**Bipolar Transistor**

The first solid-state semiconductor transistor
The p-n junction is formed by bringing together p-type and n-type silicon

In the region of the junction, holes and electrons recombine to leave a the depletion region with no free carriers. Causes a potential barrier

Forward bias is p-side positive, and narrows the depletion width

Under reverse bias, p-side negative, majority carriers repelled from the junction. A flow of minority carriers, generated thermally, results in a small leakage current

Construction of the bipolar transistor:
![[BipolarTransistorConstruction.png]]

Two diodes back to back (npn). 
The arrow on the circuit diagram show the direction of conventional current. Collector to emitter for npn, opposite for pnp.

A small change in base voltage, and hence base current, causes a large change in collector current.

The collector current is almost equal to the emitter current: $I_C=\alpha I_E$
$\alpha$ is the 'common base current gain'

By Kirchoff's law: $I_E=I_C+I_B \Rightarrow I_C=\frac{\alpha}{1-\alpha}I_B=\beta I_B=h_{FE}I_B$
$\beta=h_{FE}=\frac{I_C}{I_B}$, where $h_{FE}$ is the current gain, between 20 and 500

Input characteristic:
![[TransistorCharacteristic.png]]
The base-emitter junction begins to conduct at $V_{BE}\approx 0.7V$
![[OutputCharacteristic.png]]

Region 1 - Linear region. $I_C$ depends mainly on $I_B$. Small rise in $I_C$ with $V_{CE}$
Region 2 - Nonlinear region. $I_C$ depends strongly on $V_{CE}$

The performance limits of the bipolar transistor:
* Maximum $I_C$
* Maximum power
* Maximum $V_{CE}$
* Linear limit

First find operating point. We choose $V_{CE}$, $I_C$ and $I_B$ accordingly for linear region
Output voltage = Gain $\times$ input voltage

The input characteristic allows us to calculate $V_{BE}$
Plot load line on the output characteristic
We can then graphically estimate the current gain $(\frac{\Delta I_C}{\Delta I_B})$ and the voltage gain $(\frac{\Delta V_{CE}}{\Delta V_{BE}})$

To select a good operating point:
Stay within safe limits, choose highest allowable $V_{CC}$, try to set $V_{CE}$ as close to $V_{CC}/2$ as possible, and draw the load line to have the max length in the linear region

For the AC aspect, the output varies little around the operating point

**Considering current**
$\partial I_C=i_c=\frac{\partial I_C}{\partial I_B} \partial I_B + \frac{\partial I_C}{\partial V_{CE}} \partial V_{CE}$

$\frac{\partial I_C}{\partial I_B}$ is the current gain at constant $V_{CE}=h_{fe}$
$\frac{\partial I_C}{\partial V_{CE}}$ is the output admittance (1/impedance) at constant $I_B=h_{oe}$

$i_c=h_{fe}i_b+h_{oe}v_{ce}$, which suggests a model with a current generator and a conductance
![[BJTRepresentation.png]]

**Considering Voltage**

The input characteristic is similar to that of a diode. Using similar logic as before we can say that:

$v_{be}=h_{ie}i_b+h_{re}v_{ce}$
Which suggests a model involving a resistance and a voltage generator

**Combining the Two Models**

![[OverallSmallSignalCircuit.png]]

Where: 
* $h_{ie}$: input resistance ~ $k\Omega$
* $h_{re}$: reverse voltage transfer ratio ~ 0
* $h_{fe}$: forward current gain (50 - 600)
* $h_{oe}$: output conductance $(1/h_{oe})$ ~ 50 - 200 $k\Omega$
For a pnp everything is reverse polarity

The reverse voltage transfer ratio $h_{re}$ is almost invariably ignored

Solve just as you would for a FET, drawing the small signal model, grounding $V_{CC}$

To find output resistance, short circuit the input then find total resistance
Make sure to check whether $h_{fe}i_b$ is 0 or not

**BJT Circuits**

Connecting $R_1$ to the collector rather than $V_{CC}$ improves the stability of the biasing, giving a degree of self-compensation

Including a resistance in the emitter circuit enables a stable
operating point to be achieved, albeit at the expense of circuit complexity
Remember the bypass capacitor, blocking in DC and shorting in AC, as a resistor at the emitter reduces gain significantly

Using a Thevenin equivalent allows you to replace $R_1$ and $R_2$ with $V_T$ and $R_T$
![[ThevEquivalent.png]]

We can do mesh analysis around the first loop (with $V_T$ in it), providing us with an equation for:
$I_C=\frac{h_{FE}(V_T-V_{BE})}{R_T+R_4(1+h_{FE})}$

**Emitter Follower**
If we want a buffer, we need a high input impedance and a low output impedance. For that we use an emitter follower:
![[EmitterFollower.png]]
$R_1$ provides base current which sets the operating point. The stability of the operating point is reasonable because of the presence of $R_2$.





