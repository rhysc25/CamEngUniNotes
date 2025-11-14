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

**Combustion Processes**

First we will set up the chemical equations, then use the 1st law to solve combustion problems

We always assume that air is $21\%$ oxygen and $79\%$ nitrogen
First find the required moles of oxygen to react, then, add $\frac{79}{21}N_2$
We keep this in the molar equation just so that finding the mass ratios is easier, however it does not actually take part in the combustion

For the reactants, we can calculate an air fuel ratio AFR = $\frac{\dot{m}_a}{\dot{m}_f}$
**Lambda and Equivalence Ratio**
Lambda is commonly used to express the stoichiometry
$\lambda=\frac{AFR}{AFR_{stoichiometric}}$

This is just a measure of how much excess oxygen we have.
* $\lambda>1$ the combustion is lean
* $\lambda=1$ the combustion is stoichiometric
* $\lambda<1$ the combustion is rich (rich in fuel)

Equivalence ratio is also used, $\phi=\frac{1}{\lambda}$

Once we have found the stoichiometric number of moles of $O_2$ in the equation, we can just multiply that number by lambda in the equation to accurately represent what we have.
If $\lambda<1$, the hydrogen combusts first, becoming water. Then the rest is split between $CO_2$ and $CO$

**First Law Applied to Combustion**

A wet reaction is one where the water turns to steam, so has an effect in the reaction equation. This would be when the temperature is greater that $100\degree$
A dry reaction is the opposite, where the water leaves as liquid

To work out the calorific value of a combustion reaction, we use a calorimeter, which records the necessary $\dot{Q}_0$ (heat removed) to bring the temperature back to the initial temperature

The calorific value of different combustion reactions can be found in the CUED data book

How can we determine the temperature of a gas after combustion?
Split the combustion into three idealised processes:
1) Heat removed so reactants brought from initial state (R1) to $25\degree$ (R0)
2) Heat removed so that combustion occurs at constant $25\degree$ (0R to 0P)
3) Heat added so combustion products raised to final T (P0 to P2)

![[Pasted image 20251112143748.png]]

From the first law:
$\dot{Q}-\dot{W}_x=0=\dot{m}(h_{P2}-h_{R1})=\dot{m}[(h_{P2}-h_{P0})+(h_{P0}-h_{R0})+(h_{R0}-h_{R1})]$
$0= \dot{m}(h_{P2}-h_{P0})+\dot{Q}_0+\dot{m}(h_{R0}-h_{R1})$

We can represent this process on an enthalpy - temperature diagram:
![[Pasted image 20251112144148.png]]
$\dot{m}h$ for inlet and outlet must be the same as $\dot{Q}-\dot{W}_x=0$

For low temperatures: Use $\dot{m}_i c_{pi}(T_{R0}-T_{R1})$ for each component in the mixture
For high temperatures, we use tabulated data, as the gases are semi perfect.

There is a table of molar enthalpies ($\bar{h}$) in the CUED data book. $\dot{m}h=n\bar{h}$
It is best to do these kind of questions in spreadsheets

