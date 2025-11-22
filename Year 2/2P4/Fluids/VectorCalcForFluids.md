There is the greatest pressure at stagnation points.
When the flow is steady, the pressure field is constant in time. However, when it is unsteady, we must consider the rate of change of the pressure field in time
$\frac{dp}{dt}=\frac{\partial p}{\partial t} + (\textbf{v} \cdot \nabla)p$
This relates that experienced by the particle to quantities held by the field

This is the material/substantive derivative:
$\frac{D}{Dt}=(\frac{\partial }{\partial t} + \textbf{v} \cdot \nabla)$

The description of fluids following its particles is a Lagrangian description, where as looking at fixed points in space is a Eulerian description.

It may seem strange, but we can also use to it find the acceleration at a given point.
Knowing that $-\nabla p = \rho \frac{D\textbf{v}}{Dt}$, essentially just Newton's second law, we can say:

$\rho(\frac{\partial \textbf{v}}{\partial t} + (\textbf{v} \cdot \nabla)\textbf{v})=-\nabla p$

If we include body forces with the $-\nabla p$ term, this has a direct correspondence with the SFME we found in 1A

When gravity acts on the fluid, we also need to include a $-\rho g \textbf{e}_z$ term.
$-\rho g \textbf{e}_z=\frac{\partial (\rho g z)}{\partial z}\textbf{e}_z$. This can be written as $-\nabla \rho g z$ as the other terms, x and y, are just zero
We can therefore write $-\nabla (p+\rho g z)$ and always consider the height when we evaluate pressure


If we manipulate this further $\rho(\frac{\partial \textbf{v}}{\partial t} + (\textbf{v} \cdot \nabla)\textbf{v})=-\nabla (p+\rho g z)$ we get to the Bernoulli equation. If we had streamlines in the x direction, this would be: $\frac{\partial}{\partial x}(p+\frac{1}{2}\rho V^2)=0$

If the vorticity is zero, Bernoulli can be applied across streamlines

Considering intrinsic (streamline) coordinates: $\nabla = \textbf{e}_s\frac{\partial}{\partial s}+\textbf{e}_n \frac{\partial}{\partial n}$
The Euler equations in stead flow give: $(\textbf{v} \cdot \nabla)\textbf{v}=-\frac{1}{\rho}\nabla p$
Expanding this out and relating coefficients gives:

$V\frac{\partial V}{\partial s}=-\frac{1}{\rho} \frac{\partial p}{\partial s}$, which is just Bernoulli's down a streamline
$\frac{V^2}{R}=\frac{1}{\rho}\frac{\partial p}{\partial n}$ This is the centripetal acceleration, across a streamline. It shows how normal pressure gradients cause the streamlines to bend

