$V=$ bulk velocity = $\frac{\text{flow rate}}{\text{cross-sectional area}}=\frac{Q}{A}=\frac{\int v dA}{A}$

Using this, we get that the shear force at the wall of a pipe $\tau_w=-\frac{R}{2}\frac{dp}{dx}$

As the wall shear stress is dependent on $\rho,V,D,\mu$ we can say that there are 2 dimensionless variables
$c_f=\frac{\tau_w}{\frac{1}{2}\rho V^2}=f(\frac{\rho V D}{\mu})=f(Re)$

The development of the velocity profile when a uniform profile enters a pipe
![[Pasted image 20251203142816.png]]

Doing the entire analysis, we find that $c_f=\frac{16}{Re}$, a slope of -1 in the log plot

When we defined $c_f$, we did so by forming a dimensionless group for the wall shear stress, For that, we used the dynamic pressure, but we might as well have used the order-of-magnitude value of the viscous stress $\frac{\mu V}{D}$. This would have been a more convenient choice at lower Reynolds number, when viscous terms dominate. Nevertheless, we are interested in what happens at large $Re$.

**Turbulence, Mixing and Friction**
As the Reynolds number increases by increasing V, the flow is not viscous enough to dissipate all the energy put into it merely by viscous friction, and breaks it down into smaller and smaller eddies, down to sizes where viscosity can eventually act. We say it has become turbulent.
![[Pasted image 20251203143557.png]]

Eddies provide a much more efficient exchange of momentum, as they move molecules at a larger scale. We can use this model:
$\mu_T=\mu+$ eddy viscosity, where the eddy viscosity is usually much larger than $\mu$
This causes a lot of dissipation at the wall

![[Pasted image 20251203143824.png]]

For any smooth, straight, pipe:
![[Pasted image 20251203143905.png]]

**Roughness**
As we increase Re, the eddies get smaller, so will interact more with the small surface roughness of the pipe, hence increasing friction.
We need a dimensionless constant for the bump scale, so we use $k/D$ where k is bump scale and D is pipe diameter

This leads to a graph like this:
![[Pasted image 20251203144101.png]]

We can see it reaches a point where the shear friction coefficient is no longer dependent on Reynolds number, as the eddies are so small that we have essentially flow through obstacles

