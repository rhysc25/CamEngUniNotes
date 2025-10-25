**Phases**
A phase is defined by two criteria: The atomic arrangement, and the chemical species present.

Two materials or regions of a material are considered different phases if they differ in either atomic arrangement or chemical species.

Phases of a pure material: solid, liquid, gas.
A solid can also undergo a change in phase due to a transformation from one crystal arrangement to another (FCC, BCC, HCP)

The phases present in an alloy depend on the temperature, pressure and composition of the alloy

**Free Energy**
The driving force behind phase transformation and phase equilibrium.

Consider a material made of components that could transform:
$dU=\delta Q=\delta W=TdS-T\delta S_{irrev}-\delta W$

The work $\delta W$ can be split into a contribution from pressure forces, and other work that we may collect/give away, $\delta W'$
$\Rightarrow dU=TdS-T\delta S_{irrev}-pdV-\delta W'$
We can estimate the maximum useful work that could be collected as:

$\delta W'=-dU+TdS-T\delta S_{irrev}-pdV\leq -dU+TdS-pdV$

**Gibbs Free Energy**
Considering the situation where pressure and temperature are constant, we introduce:

$G=U+pV-TS=H-TS$

If, as said earlier, $dp, dT=0$, then
$dG=dU+pdV-TdS$

We therefore get that: $\delta W'\leq -dG$
The useful work available for a transformation is at best equal to the decrease of G, where G is the Gibbs Free Energy

**Thermodynamic Potentials**
Here we are not interested in collecting useful work. $\delta W'=0$
Therefore:
* During the evolution of a material under isobaric and isothermal condition, the variation of Gibbs Free Energy must be negative: $dG\leq 0$
* G must always decrease
* At the equilibrium, the Gibbs Free Energy is minimum

The Gibbs Free Energy is an extensive quantity that depends on pressure, temperature, as well as the composition, state and microstructure of the material.
Considering a system that is not necessarily at equilibrium, one can introduce internal variables that characterise its state and eventual transformation towards equilibrium: $G(P,T,\phi)$

The variable $\phi$ represents any quantity affected by the evolution towards equilibrium. E.g. proportion of solid or liquid or composition of the different phases

Because the system evolves towards a state that minimises G for a given P and T, the Gibbs Free Energy is called a thermodynamic potential.
The variable $\phi$ is not controlled by us. For a given P and T, the state observed at equilibrium is the state $\phi_{eq}(P,T)$ such that:
$\frac{\partial G}{\partial \phi}(P,T,\phi_{eq})=0$
This allows us to establish a condition for equilibrium and use this result to predict or control the equilibrium state $\phi_{eq}$. It will be useful later on.

![[Pasted image 20251013203551.png]]

At equilibrium, the Gibbs Free Energy is a function of P and T only

Because atoms attract each other, the internal energy is lower when particles are closer to each other for a given temperature.
$U_s(T)<U_l(T)<U_g(T)$
$V_s(T)\approx V_l(T)<V_g(T)$
Entropy is a measure of disorder, so we know that:
$S_g(T)>S_t(T)>S_s(T)$

As a result, the G of a gas starts higher but decreases faster with temperature.
![[Pasted image 20251013205029.png]]
The lowest G is the phase that will be transformed to

If we consider a solid and a liquid together, the total G is the weighted sum of their Gs, considering the mole fraction: $G=\phi_s G_s + \phi_l G_l$.
$\phi_s$ evolves towards a minimum of free energy
This gives $dG=(G_s-G_l)d\phi_s\leq 0$

If $T>T_M$, the melting point, then $G_s>G_l$, and $d\phi_s<0$. G is therefore minimum for $\phi_s=0$, so all liquid

If we consider mixing two miscible components: The G of the unmixed state is just the weighted average of the two Gs. This gives a straight line on a G-x diagram, linking $G_a$ and $G_b$.
After mixing: $G_m=G_u+\Delta U_m +p\Delta V - T\Delta S_m$
$\Delta U_m$ is the variation of internal energy due to mixing, $\Delta S_m$ is the entropy of mixing

This is almost always less than the weighted sum, so mixing tends to occur
For non-miscible materials:
![[Pasted image 20251018115037.png]]
Two minima are formed, causing a phase separation, some ending up in either well.

We can draw similar G-x graphs for energy given temperature from the phase diagram.
![[Pasted image 20251018115236.png]]
For example, the bottom right graph shows why phase separation occurs, having the separation of two minima on the G curves

**Nucleation**

The interface between two phases, say solid and liquid, is a much higher energy state. This means there is such thing as a surface energy, $\gamma$. As we increase the nucleated region, the surface energy increases

Therefore there are two energies summing when the radius of a solid nucleating region is increasing. The bulk free energy and the interfacial energy.

$G(r)=\frac{4}{3}\pi r^3 \Delta G_v+4\pi r^2 \gamma$

$\Delta G_v$ is negative, it is the driving energy, the Gibbs free energy of solidification per unit volume

![[Pasted image 20251020195254.png]]
These energies combine, meaning there is actually an energetic barrier at $r^*$
By statistical distribution, regions of atoms will have enough energy to overcome it initially

If we compute $\frac{dG}{dr}(r^*)=0\Rightarrow r^*=\frac{2\gamma}{\Delta G_v}$
The larger the $r^*$ the more difficult it will be to nucleate the solid

By consider $\Delta G(T_m)$ we can get to the result that $\Delta G(T)$, the change in gibbs free energy in order to solidify, is given by $\Delta H \cdot (\frac{T_m - T}{T_m})$
Also, $r^*=\frac{2\gamma}{\Delta H_v}\frac{T_m}{T_m-T}$, both proportional to the amount of undercooling

This is a flawed model, as we see that as T tends to $T_m$, $r^*$ tends to infinity, which we don't observe in reality
This is also assuming homogeneous nucleation, that is the spherical crystal suspended in the liquid nucleates

In reality, most often we get heterogeneous nucleation, where the solid nucleates off of defects/dirt/grit floating in the liquid, which actually looks like this:

![[Pasted image 20251020200139.png]]

We can write the Gibbs free energy of the system as:
$G = V_S(r)\Delta G_v + A_{SL}(r)\gamma_{SL} + A_{CS}(r)(\gamma_{CS} - \gamma_{CL})$
Where $A_{SL}$ is the area of the solid liquid interface, and $(\gamma_{CS} - \gamma_{CL})$ is the change in surface energy as the solid - catalyst interface increases

Balancing forces, we must have that: $\gamma_{CL}=\gamma_{CS}+\gamma_{SL}\cos(\theta)$

If we carry through with the algebra, we get the same answer for $r^*$. The difference here is that for the same $r^*$ we have far fewer atoms required to lump together

**Osmosis**

Solvent flows through a semi permeable membrane until the distribution of solute is even, maximising entropy and minimising Gibbs free energy

We find that $\pi = RTc$, where $\pi$ is the osmotic pressure and c is the solute concentration expressed in moles per $m^3$
We find this by considering the equilibrium point where $\frac{\partial G}{\partial n_1} = 0$, where $n_1$ is the number of water molecules on one side of the membrane

This is used in plant cells, where intaking more water makes the cell more rigid
This also causes a depletion force between particles in suspension, squeezing them together. This tends to clump and aggregate larger particles, meaning filtering is easier
