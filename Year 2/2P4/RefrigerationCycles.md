The second law tells us that moving heat from a cold source to a hot source would be impossible, as we would decrease entropy in a closed system. 
Therefore we must add the minimum work to make the entropy change zero. This is true for a reversible refrigerator

$COP_R=\frac{\dot{Q}_{cold}}{\dot{W}_x}$
$COP_{HP}=1+COP_{R}$

The best possible refrigeration cycle is the reversed Carnot cycle. This has a $COP_R=\frac{1}{\frac{T_{hot}}{T_{cold}}-1}$
Problems: Compression difficult in the two phase 
Turbine replaced with throttle valve

![[Pasted image 20251105200102.png]]

This can also be represented on a p-h diagram.
![[Pasted image 20251105200145.png]]

In the throttle valve, $\Delta h=0$. The enthalpy is constant, but the temperature can change as the proportions of fluid/gas changes
State 1 properties can be found from the data book. Point 2s can be found by linear interpolation to get $h_{2s}$, as we know $s_g, s_{2s}, s_{+20K}, h_g, h_{+20K}$, but not $h_{2s}$

From the data book, we can also find $h_4=h_3$

Refrigerants must be cheap, stable, inert and non-toxic. The pressure range corresponding to the operating temperature range should be small. The vapour pressure should be low to reduce condenser cost, but it should be higher than atmospheric pressure to prevent air leakage into the system. The latent heat of evaporation should be high in order to keep the mass flow rate low.

Refrigerators can also be designed which use only the gas phase. This is essentially the reverse Joule cycle.
![[Pasted image 20251105201734.png]]
This can be used to achieve very low temperatures for liquefaction of gases. it also has specialist uses such as aircraft cabin cooling.

Problem - Constant pressure lines don't flatten up any more. It has a much lower $COP_R$ than $COP_{R(Carnot)}$

**Properties of Mixtures**

Mass fraction (gravimetric analysis): $m_i/m$
Mole fraction (volumetric analysis): $n_i/n$

Dalton's Law:
The pressure of a mixture of gases separated into its constituents such that each occupies a volume equal to that of the mixture, and is at the same temperature as the mixture

So the total pressure is the sum of the partial pressures.
p,V sum with the mole fraction
$U,h,s,c_v,c_p,R$ sum with the mass fraction

$p_i=p\frac{n_i}{n}$
$u=\sum \frac{m_i}{m}u_i$

**Mixture of Dry air and Water vapour**
$p_a=p\frac{n_a}{n}$, $p_v=p\frac{n_v}{n}$
a denotes air, v denotes water vapour, w denotes liquid water

If there is a liquid layer in the bottom of the tank then the water will evaporate until the air becomes saturated and equilibrium is reached
The partial pressure of the water vapour will rise as more water evaporates

3 ways a mixture can become saturated:
1) Evaporation of liquid water raising the partial pressure
2) Raising the pressure of the mixture raises partial pressure
3) Lower the temperature of the mixture until we hit the Dew point on the saturation line

**Specific and Relative Humidity**

The specific humidity/ humidity ratio is $\omega=\frac{m_v}{m_a}=\frac{M_v}{M_a}\frac{p_v}{p_a}=0.622\frac{p_v}{p-p_v}$

The relative humidity is $\phi=\frac{n_v}{n_{v,sat}}=\frac{p_v}{p_{v,sat}}$
The ratio of how much water vapour is in the air to how much it could hold, or how much is necessary to saturate

$h_{v1}$ for a system is not very easy to calculate. We can try and read off the h-s diagram at the back of the data book. Or we can assume that the constant temperature lines in said diagram are relatively flat, so the value of h should be similar to that at saturation, so we just find $h_v$
