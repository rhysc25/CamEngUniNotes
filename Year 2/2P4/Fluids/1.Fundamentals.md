Mean free distance $\lambda$ is the distance a molecule can move before collision
As there are way too many molecules to consider, we will smear them, considering the average velocity and molecular mass and molecules per $m^3$ of a region

The momentum change on collision $\propto mv_i$
The number of collisions per unit area per unit time $\propto n_v v_i$
So the presser, the force per unit area $\propto mn_vv_i^2$
Pressure = $mn_v \times \frac{constant}{m}\times \frac{1}{2}\overline{mv_i^2}=\rho R T$
This is the equation of state

The continuum assumption treats fluids as continuous media. This is only true if the mean free path is small compared to the characteristic length scale
The Knudsen number, $K_n=\frac{\lambda}{L}$ must be $<<$ 1

Viscosity is how a fluid resists deformation.
A solid brick can support shear in static equilibrium because its molecules are held in place by rigid bonds
A viscous fluid cannot support shear in static equilibrium
If we have an inviscid fluid, there is no shear stress at the interface, there is just perfect slip

If we have two layers of fluid, we can say that one is moving with velocity $v_x$ and the other is moving with velocity $v_x+\frac{\partial v_x}{\partial y}\delta y$
This means that the shear stress, $\tau=\mu\frac{\partial v_x}{\partial y}$, where $\mu$ is the viscosity
The viscosity is a function of temperature $f(T)$.
In a gas, viscosity increases with temperature
In a liquid, viscosity decreases with temperature
There are also shear thickening and thinning materials whose shear stress changes depending on the force you apply
![[Pasted image 20251114121610.png]]

In IB fluids we will consider all liquids to have constant viscosity and density

When using curvilinear coordinate systems, be wary that spherical and cylindrical unit vectors change as $\theta$ changes, so they too need to be differentiated

**Vector Calculus in Fluids**

Mass flux, the flow of mass per unit area per unit time, $\frac{\dot{m}}{A}=\rho v$

The law of conservation of mass in differential form:
$\frac{\partial \rho}{\partial t}=-\nabla \cdot (\rho \textbf{v})$
We will be assuming that density is constant, so this simplifies to:
$\nabla \cdot \textbf{v}=0$

The divergence is the net flux OUT of a region.

If we superimpose a constant velocity onto a source:
Close the the source: Behaves normally
Away from the source: Behaves like a normal constant velocity flow
We must merge them at their intersection

Vorticity: $\omega= \nabla \times \textbf{v}$
Curved streamlines do not imply vorticity. The particles can be moving in a circle, but not actually rotating themselves.
Straight streamlines do not imply a lack of vorticity.

When vorticity is zero, Bernoulli's equation can also be applied across streamlines.

**Advection**
This is the changes due to motion through a field.
Say we are walking over hills, so a scalar field in h.

$\frac{dh}{dt}=\frac{dh}{ds}\cdot\frac{ds}{dt}=\nabla h \cos(\theta) \textbf{v}=\textbf{v}\cdot \nabla h$

Looking at $(\textbf{v}\cdot \nabla) h$, we can see that $(\textbf{v}\cdot \nabla)$ is the advection operator, which gives the variation of a scalar field following $\textbf{v}$
It can also be applied to a vector
Scalars can only change in magnitude, so their directional derivative is a number.  
Vectors can change in magnitude _and_ direction, so their directional derivative must itself be a vector.

It is not the same as the divergence of $\textbf{v}$, resulting instead in $(v_x\frac{\partial}{\partial x}+v_y\frac{\partial}{\partial y}+v_z\frac{\partial}{\partial z})$
