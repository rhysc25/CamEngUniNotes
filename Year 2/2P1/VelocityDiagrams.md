$M\bar{y}=\int ydm$
Perpendicular axis theorem: $I_{zz}=I_{xx}+I_{yy}$ for a lamina
Parallel axis theorem: $I_{xx}'=I_{xx}+Mr^2$. If you're instead going from a random point to G, then you'd subtract $Mr^2$.

Radius of Gyration, k, is defined such that $I_{xx}=Mk_x^2$. The value of k is the distance at which all the mass of the body can be concentrated to give the same moment of inertia. It is the radius of a hoop with the same moment of inertia.

$\textbf{r}=r\textbf{e}_r$
$\dot{\textbf{r}}=\dot{r}\textbf{e}_r+(r\dot{\theta})\textbf{e}_{\theta}$

Total kinetic energy: $T=\frac{1}{2}mv^2+\frac{1}{2}I\omega^2$
Always do about G, it will work every single time

A conservative force moving through a distance stores PE/V, recoverable

D'Alembert Inertia Force = -ma acting at G
D'Alembert Inertia Couple = -$I\dot{\omega}$
Main method to solving mechanics questions: Draw all forces and torques and d'Alembert forces. Take moments and resolve to find $\ddot{x}$ and $\dot{\omega}$

Angular momentum $\textbf{h} = I\omega \textbf{k}$
The impulse is the change of linear momentum: $\textbf{I}_P=\Delta \textbf{P}$
Moment about G of the impulse: $\textbf{r} \times \textbf{I}_P = \Delta \textbf{h}$
Finite forces can be ignored when compared with impulsive forces. If there is a point P through which all impulsive forces pass then angular momentum conserves about P

To solve these types of impulse equations: 
1) First consider the conservation of angular momentum/ moment of momentum, considering the point which the impulse acts through. However always use the velocity through G and the angular velocity about it
2) Then consider conservation of energy - or use coefficient of restitution if given
3) Combine and solve

$\dot{\textbf{e}}=\omega \times \textbf{e} = \dot{\theta} \textbf{e}^*$

In polar coordinates:
$\ddot{\textbf{r}} = (\ddot{r}-r\dot{\theta}^2)\textbf{e}_r+(2\dot{r}\dot{\theta}+r\ddot{\theta})\textbf{e}_{\theta}$
Radial, centripetal components. Coriolis and circumferential components.
Coriolis acceleration is logical if you consider moving outwards on a rotating turntable. Your sideways velocity will increase, so there must be sideways acceleration

Use these as D'Alembert forces when the reference frame is rotating

**Velocity Diagrams**

Four bar mechanisms: Crank rocker, Slider crank, Quick return

The instantaneous centre is the point at which all velocities are perpendicular from. $v=\rho \omega$.
Once the velocities have been determined then a velocity diagram can be drawn
You can then connect velocity vectors into triangles

Use triangles in the velocity diagram to find unknown magnitudes. The velocity direction is always perpendicular to the line linking the point and the instantaneous centre of rotation

**Virtual Power**

Consider a system moving/rotating slowly without friction. Net work done is zero as no energy transferred. 

Therefore the sum of all the forces acting on the system times their infinitesimal distance travelled and all the torques acting on the system times the infinitesimal angle rotation = 0.

During a time interval $\delta$t:
$\sum F_i \cdot \delta x_i + \sum T_i \delta \theta_i = 0$

Dividing by $\delta t$:
$\sum \textbf{F}_i \cdot \textbf{v}_i + \sum T_i \omega_i = 0$

Use the method of instantaneous centres/ velocity diagrams to find the velocities/ angular velocities at each point
1. Reaction forces at fixed pivots do no work as do not move
2. Friction at sliders can be considered as an external force - use the relative sliding velocity
3. Friction at pivots can be considered as an external torque - use the relative angular velocity
4. Friction always acts to oppose the motion
5. Use consistent sign convention
6. Be aware of the dot product in $\textbf{F}_i \cdot \textbf{v}_i$ and be sure to evaluate the displacement in the direction of the force

**Acceleration Image**

This is very similar to the velocity image. Any rigid body in the form of a polygon ABC will have a similar polygon abc in the acceleration diagram.
Unlike the velocity image, the acceleration image abc is rotated from ABC through some angle that is not necessarily 90$\%$

**Inertia Forces in Mechanisms**

As a mechanism moves the various links and sliders are accelerating. 
The d'Alembert Inertia forces and couples can be applied as if they were external forces and couples.
We can use virtual power to determine, for example, the driving torque needed to resist the inertia forces of the accelerating mechanism

For a vector $\textbf{r}$ which is rotating at an angular velocity $\omega$:
$\dot{\textbf{r}}=\frac{d\textbf{r}}{dt}+\omega \times \textbf{r}$

$\dot{\textbf{e}}=\omega \times \textbf{e}$

The acceleration of B relative to A is
$\ddot{\textbf{r}} = (\ddot{r}-r\dot{\theta}^2)\textbf{e}+(2\dot{r}\dot{\theta}+r\ddot{\theta})\textbf{e}*$
But if AB is a rigid link then: $\ddot{\textbf{r}} = r\ddot{\theta}\textbf{e}*$, dramatically simplifying the construction of an acceleration diagram

An element of beam $dx$ with mass per unit length $m'$ is accelerating with acceleration $a$ then the d'Alembert inertia force is -$m'adx$. 
This can be considered as a distributed load $\omega(x)$ on a beam, and the usual methods of statics can be used to find bending moments and shear forces

**Gyroscopic Mechanics**

The full 3D differentiation of rotating unit vectors can be found in the data book

For motion of a particle we know that F=ma and p=mv, so $\textbf{F}=\dot{\textbf{p}}$
If the speed of the particle is constant but it is moving on a circular path then $\textbf{p}$ is rotating at an angular velocity, so $\dot{\textbf{p}}=\omega \times \textbf{p}$
This leads to $F = m\omega^2 r$

Now consider the analogous case for angular momentum: $\textbf{Q}=\dot{\textbf{h}}$
If a rotor is spinning with constant angular velocity $\omega \textbf{e}$ where $\textbf{e}$ is aligned with the axis of spin then $\textbf{h}=J\omega \textbf{e}$.
If the axis of the rotor is turning at a rate $\Omega \textbf{k}$ about an axis at right angles to $\textbf{e}$ then:
$\dot{\textbf{h}}=\Omega \textbf{k} \times \textbf{h} \qquad = \qquad J\omega\Omega\textbf{k} \times \textbf{e}$ 

This gives the formula for the gyroscopic couple:
$Q=J\omega \Omega$
The rate of turning $\Omega$ is called *gyroscopic precession*

