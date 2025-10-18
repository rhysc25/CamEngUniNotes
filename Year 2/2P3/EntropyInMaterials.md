**Revision:**

Microstructural basis of material properties:
* Stiffness: crystal structure, atomic bonding, inter-atomic forces
* Strength: dislocations, yield, plasticity
* Polymers: molecular structure, glass transition

U is the total kinetic and potential energy of all the microscopic constituents
$dU=\delta Q - \delta W$
If the work is due to pressure forces only, $\delta W = pdV$
Entropy is a thermodynamic property whose
variation from a state 1 to a state 2 is defined by:
$S_1-S_2=\int_1^2(\frac{dQ}{T})_{rev}$
Physically possible transformations are further defined:
$dS = \frac{\delta Q}{T}+\delta S_{irr}$ with $\delta S_{irr}\geq 0$
The entropy of an isolated system where $\delta Q=0$ must increase, and must be maximum at equilibrium

**New**

Particle diffusion makes a system evolve towards the most likely microscopic configurations

Macro-state: The set of properties such as temperature pressure and volume that together determine the thermodynamic state of the system
Micro-state: The state of the material at the smallest relevant length scale. E.g. a record of the positions, orientation, velocities and angular velocities of all the particles/molecules involved

One macrostate corresponds to many microstates

Entropy captures the uncertainty regarding the microstate, given the macrostate. The number $\Omega$ of microstates is a measure of uncertainty for a given macrostate

We can get an idea of how to quantify the number of microstates for a given macrostate:

Consider a system with set temperature but changing geometry. The distribution of velocities will be assumed to be constant, but the distribution of positions will change
We can discretise space to facilitate counting

Consider two systems, each containing $\Omega_1$ and $\Omega_2$ microstates, the total number is the product $\Omega_1 \cdot \Omega_2$

$$S=k_b \ln(\Omega)$$
Where $k_b$ is the Boltzmann Constant, $1.380649 \times 10^{-23}JK^{-1}$
We apply the natural log to the number of configurations, so that when we add volume, entropy increases via the multiplication of configuration numbers, not the addition, as we know that it should be an extensive property.

Assumes isolated system

From an information perspective, we can ask how many Yes-No questions we should ask, at a minimum, to know where the particle is. This number, expressed in bits, represents the information content of the answer. Only 4 questions are needed to determine the location in a 4 by 4 grid.

**Entropy of Mixing**

Consider two components A and B, with $n_a$ atoms of A and $n_b$ atoms of B, that mix.
The number of microstates, bases of spatial arrangements only, is of the order $\Omega = C_{n_a}^{n_a+n_b}$
Let $n = n_a+n_b$

The change of entropy is:
$\Delta S=k_b \ln(\frac{n!}{n_a!n_b!})$

This challenges our understanding as S should be an extensive property, so its value should be proportional to n.

If we use the Stirling approximation when n is large: $\ln(n!)\approx n\ln(n)-n$
We get that:
$\ln(\Omega)=n_a \ln(n)+n_b \ln(n)-n_a \ln(n_a)-n_b\ln(n_b)$
Using $x$ to represent mole fractions, where $x_i=n_i/n$:
$\Delta S=-nk_B (x_a\ln(x_a)+x_b\ln(x_b))$

Now we can see than the entropy of mixing is extensive in the limit of large systems (the thermodynamic limit), proportional to n and a function of the composition of the material. 

It is also necessarily positive, creating many more configurations the system can explore

Max entropy increase occurs when mixed in proportion, 50-50.

**Ideal Gases**

All gases at low density exhibit similar thermodynamic properties and obey the ideal gas law $PV = NRT$
The potential of interaction for molecules is largely irrelevant.

The internal energy U of an ideal gas only involves the kinetic energy of the molecules and is largely independent of the nature of the gas
$U=\sum \frac{1}{2}m_iv_v^2$ + rotational kinetic energy
$\Rightarrow U=U(T)$

For a reversible transformation of an ideal piston at constant temperature: $TdS=dU + pdV$
Because the gas is ideal, we know that a change in volume $dV$ alone would not change the internal energy, hence: $TdS=pdV$

In an ideal gas, because the particles do not interact with each other, the way to distribute the velocities is independent of the way to distribute positions.
$\Omega = \Omega_v \times \Omega_c$, the possible ways to distribute velocities and the possible ways to distribute positions repectively

$\Omega_v$ depends on T but not V as it deals with velocity distribution
$\Omega_c$ depends on V but not T as it deals with position distribution

$\Rightarrow S=k_B \ln(\Omega_v \cdot \Omega_c) = k_B (\ln(\Omega_v) + \ln(\Omega_c))$

$\Rightarrow \frac{\partial S}{\partial V}= k_B \frac{\partial(\ln(\Omega_c))}{\partial V} = k_B \frac{1}{\Omega_c}\frac{\partial \Omega_c}{\partial V}$

Any multiplicative factor for $\Omega_c$ will cancel out, so all we need is how $\Omega_c$ scales with V

As the number of ways to place each particle is assumed to be proportional to V, as we are ignoring the fact that particles limit the space available as the particle density is so low, we can say:
$\Omega_c = K V^n$

Combining all so far: $\frac{p}{T}= \frac{\partial S}{\partial V}=\frac{k_Bn}{V}$
$\Rightarrow pV=nk_BT \Rightarrow pV=NRT$

$N$ moles of gas, $N=n/N_A$
$R=N_A k_B$

This shows that the pressure of gas in the ideal limit is purely entropic (the statistic drive to spread out as much as possible, electrostatic/ energetic effects ignored), which is why all gases tend to behave the same at low density.
In other words, the Ideal Gas Law reflects the entropic nature of diluted gases









