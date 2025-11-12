If we have a torsion, T,  applied to the end of a thin walled cylinder we will have shear stresses acting in the opposite direction.
The torque from an element of torque is:
$\delta T=\tau \delta A r = \tau r d\theta t r$
Integrating this, we get that $\tau = \frac{T}{2\pi r^2 t}$

The shear flow is a useful concept for thin walled structures, and it is the shear force per unit wall length of the structure. $q=\tau \times t$
As $\tau = \tau'$ then $q=q'$. The shear flow around the cross section must be equal to the shear flow along the length

If we consider two phases of an element and balance forces: $\tau_2(t_2l)=\tau_1(t_1l)$
Therefore, $q$ is constant. Shear flow due to applied torque is constant around a thin walled section

If we apply the same integrating analysis, and using the fact that q is constant, we can derive that for a general thin-walled cross section, 
$T=2qA_e \qquad$ where $A_e$ is the enclosed area
Therefore $\tau = \frac{T}{2A_et}$. To find the maximum shear stress, cut at the thinnest section

This only applies to closed sections, as q will equal 0 at the cut, so q must equal 0 everywhere

Stiffeners will not affect $A_e$, and hence the shear flow $q$ will be unaffected

**Torsional Rigidity**
We want to find the stiffness relationship between applied torque and resultant twist of a section. 
Considering a cylinder: 
![[Pasted image 20251111134802.png]]
For equilibrium, as before, $\tau=T/(2\pi r^2 t)$
For compatibility, $\theta r=\gamma l$
For material law, $\tau=G\gamma$.
We want the twist per unit length: $\phi=\theta / l$
Combining all gives $T/\phi=G2\pi r^3 t$ and the shear stress $\tau=Gr\phi$

We define $T/\phi$ as the torsional rigidity/ torsional stiffness

For a general section, we can find the torsional rigidity by using virtual work.
Equate the external work, $W=T\theta$, to the internal work
Considering a small element:
![[Pasted image 20251111135348.png]]
It is clear that only one shear stress is doing any work, so we can say that:
$\delta w_i=\tau bc \times \gamma a$
Considering this for a strip of the section as the volume $\delta V$
$\delta w_i=\tau \gamma l t \delta s \Rightarrow w_i=ql\oint \gamma(s) ds$

Now we equate this to $\theta T$, giving $\phi=\frac{\oint \gamma (s) ds}{2A_e}$
Again combining equilibrium, material law and torsional stiffness we get that:
$$\frac{T}{\phi}=\frac{G4A_E^2}{\oint \frac{ds}{t(s)}}$$
Torsional stiffness is often denoted as GJ where J is the torsion constant.
$T=(GJ)\phi$, very similar to $M=EI\kappa$
We can see that to maximise relative stiffness we need to maximise enclosed area, which makes a circular section optimal.


