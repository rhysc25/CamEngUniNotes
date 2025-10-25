Transformations are governed by thermodynamics and kinematics.
Kinematic give transformations a time aspect. The key mechanism is diffusion, how particles move through a material

Each particle is oscillating, with an equally likely chance to move left or right. However if more particles are on the right, more will move left, causing a spreading out.

Each molecule undergoes random motion characterised by two parameters:
1) A length scale $\lambda$: in a gas this could represent the mean free path
2) A time scale $\tau$: in a gas this might represent the time between molecular collisions

Brownian motion: The resulting random trajectory of a diffusing particle due to thermal fluctuations. This leads to diffusion

For a random walk of polymer monomers, we found that $\sigma^2=na^2$
If we place a diffusing molecule at the origin and wait for a time t, it has made $t/\tau$ steps of size $\lambda$, so $\sigma^2=\frac{t}{\tau}\lambda^2$, so during a time t, the particles move an average of $\sqrt{\frac{\lambda^2 t}{\tau}}$
$\lambda^2/\tau$ is a diffusion constant, characterising the rate

By considering the concentrations $C(x)$ and $C(x+dx)$ in cubes of length $\lambda$, and netting the molecules jumping between the two gives $J_x=-\frac{\lambda^2}{6\tau}\frac{\partial C}{\partial x}$, where $J$ is the net flux of molecules in molecules per second per unit area
This is stated in Fick's first law: $J=-D\frac{dC}{dx}$

Finding two different equations for the number of diffusing atoms $dn_{cv}$ and combining gives this expression: $\frac{\partial C}{\partial t}=-\frac{\partial J}{\partial x}$ which, combining with Fick's first law gives Fick's second law:
$\frac{\partial C}{\partial t}=D\frac{\partial^2 C}{\partial x^2}$

Modelling statistically:
In a continuum model, we may model a set amount of material at a given location as a delta function of the concentration at $t=0$
The solution is a Normal distribution at mean 0 and variance $2Dt$
A particle would indeed diffuse with a displacement following a normal distribution, with its spread increasing as t increases

**Processes for Diffusion in Solids**

1) Bulk interstitial diffusion - small interstitial solute atoms move between the interstitial sires in a crystal lattice. Fast diffusion rate
2) Bulk vacancy diffusion - Substitutional solute atoms exchange with a vacancy in the crystal structure. Slow diffusion rate
3) Short-circuit diffusion along a grain boundary - Planar route along grain boundary where crystal packing is more open. Fast diffusion rate
4) Short-circuit diffusion along dislocation cores - Linear route where the atomic spacing around a dislocation core exceeds that in a perfect crystal. Fast diffusion rate

Considering the interstitial bulk diffusion, there is a very unfavourable location between the two interstitial sites, which acts as an energy barrier to the movement.

The average energy per atom: $E=3k_BT$
However according to statistical physics, the probability of an atom having an energy greater than q is: $p=\exp(-\frac{q}{k_BT})$

The rate $1/\tau$ at which the atom moves through the lattice will be $\propto p$
Therefore $J_x\propto \exp(-\frac{q}{k_BT})\frac{\partial C}{\partial x}$

**Arrhenius Law**
Processes which follow this type of exponential temperature dependence are known as thermally activated. A definition of a thermally activated process is given by the Arrhenius law:
Rate of process $\propto \exp(-\frac{Q}{RT})$
We can find out whether a process follows this law by plotting $\ln(rate)$ against $1/T$

The coefficient of diffusion in solids follows the Arrhenius law:
$D=D_0 \exp(-\frac{Q}{RT})$
