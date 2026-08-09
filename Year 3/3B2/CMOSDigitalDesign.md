Inverter is the simplest gate of any logic family or technology

Resistor-transistor Logic (RTL) is where a transistor in series with a resistor determines the voltage output. It dissipates a large amount of power

Transistor-transistor Logic (TTL) - current flows constantly, even when the gate is not switching

A CMOS inverter consists of a PMOS transistor in series with an NMOS one, with an input connected to the gates of both. There is no static short circuit current, so low static power.

Sources of Noise in Digital Electronics -
* Coupling - if the current in one line changes rapidly, the resulting rapid change in the surrounding magnetic field may generate a voltage in adjacent lines

A noise margin is a measure of how much noise can be present in the logic inputs of a circuit without the circuit responding improperly.
In a graph of output vs input voltage, where the slope is -1 we define $V_{IL}$ and $V_{IH}$.
The low noise margin: $NM_L = V_{IL} - V_{OL}$
The high noise margin: $NM_H = V_{OH} - V_{IH}$
The logic swing: $V_{OH}-V_{OL}$

Regenerative Property:
The steep slope in the middle of the out/in graph means that a noisy input signal will be re-generated as a better output signal.

Propagation Delay:
Parasitic capacitance at inputs and outputs means a non-zero switch time
Propagation delay - the time difference between the 50% $V_{DD}$ points between the input and output
Rise/fall time ($t_f/t_r$) - the time difference between the 10% and 90% $V_{DD}$ points
Circuit performance is expressed in the clock cycle time dependent on the propagation delays

BJTs also have a measurable switching speed. They require a negative $I_B$ to remove all of the excess charge from the base

Three options to speed up switching: 
* TTL - use higher conductance paths to drive the base
* Emitter-Coupled Logic (ECL) - avoid saturation by controlling base emitter voltage
* Schottky-Transistor Logic - Use Schottky transistors with modified base-collector structure, preventing saturation

Power Dissipation -
Instantaneous power: $p(t)=v(t)i(t)=V_{supply}i(t)$
Peak power - for supply line sizing: $P_{\text{peak}}=V_{supply}i_{peak}=$ max$[p(t)]$
Average power - for cooling: $P_{ave}=\frac{1}{T}\int_0^Tp(t)dt=\frac{V_{supply}}{T}\int_0^T i_{supply}(t)dt$

It is decomposed into static and dynamic components
* Static - static conductive paths and leakage current
* Dynamic - during transients - prop to switching frequency

Compared to TTL and NMOS, CMOS is faster as transistors shrink, they have minimal power consumption (almost zero except during state switching), and they have excellent noise margin

MOSFETs -
Gate voltage at which the surface inverts from p to n type is the threshold voltage $V_T$
$V_T = V_{T0} + \gamma (\sqrt{V_{SB}+|2\phi_F|}-\sqrt{|2\phi_F|})$
where $\gamma$ is the body-effect coefficient and $\phi_F$ is the Fermi potential

I-V Equation -
Carrier velocity, $v = \mu_0 E = \mu_0 \frac{dV(y)}{dy}$
$I_{DS}=Qv=C_{ox}(V_{GS}-V(y)-V_T) \times \mu_0 \frac{dV(y)}{dy}\times W$

Linear region: $I_{DS}=\frac{W}{L}\frac{\mu_0 C_{ox}}{2}[2(V_{GS}-V_T)V_{DS}-V_{DS}^2]$
Saturation region: $I_{DS}=I_{DS}=\frac{W}{L}\frac{\mu_0 C_{ox}}{2}(V_{GS}-V_T)^2(1+\lambda V_{DS})$

$\lambda$ is an empirical parameter determining the channel length modulation
$\mu_0 C_{ox}$ is the transconductance parameter k

