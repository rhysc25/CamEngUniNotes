If we have two layers of fluid flowing, if a particle moves between layers, there will be an exchange of momentum, i.e. a shear force

$\tau = \mu \frac{d v_x}{dy}$

If we have one wall moving and not the other, once particles hit the wall they will gain momentum. On average, molecules leave the wall with the wall's velocity.
Momentum diffuses to the other wall, leading to a linear velocity profile.

**Viscous Flow Between Parallel Plates**
The streamlines are straight and parallel with the plates. Therefore $v_x$ is a function of y only and $v_y=0$

This means that the material derivative of $\textbf{v}$, the acceleration of a fluid particle, is zero.
This means that we can do force balance on regions of fluid.
Finding the net force along x and y, we get two equations:

$\frac{\partial p}{\partial y}=\frac{\partial \tau}{\partial x}$
$\frac{\partial \tau}{\partial y}=\frac{\partial y}{\partial x}$

From $\tau = \mu \frac{d v_x}{dy}$ we can say that $\frac{\partial \tau}{\partial x}=0$ so $\frac{\partial p}{\partial y}=0$
This means that pressure is a function of x only

$\frac{\partial \tau}{\partial y}=\frac{\partial y}{\partial x}$ is our defining equation. Subbing in the definition of $\tau$:
$\mu \frac{d^2v_x}{dy^2}=\frac{dp}{dx}=$ constant

Two main flow types through parallel plates:
* Couette flow - The flow is driven by one plate moving relative to the other. This causes a linear function of $v_x$ in y, with $v_x=V$ at one plate and $v_x$ at the other
* Poiseuille flow - Stationary plates, the flow is driven by a pressure gradient - This gives  a parabola as the velocity profile

Say we have viscous flow down a slope, we would need to include the $\rho g h$ in our expression for pressure

**Combining Couette and Poiseuille Flow**
Depending on the sign of $\frac{dp}{dx}$, we either have the constructive superposition of the two, or the destructive
![[Pasted image 20251126141151.png]]

The Navier Stokes equations include viscous friction:
$\mu \nabla^2 \textbf{v}-\nabla p = \rho \frac{\partial \textbf{v}}{\partial t}+\rho \textbf{v}\cdot \nabla \textbf{v}$


