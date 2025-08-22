# Fluid Dynamics

A streamline - A line through the flow that is always parallel to the velocity vector.
No mass can cross a streamline as the normal velocity is 0.
A stagnation point is a point where the velocity of the streamline is 0. Every flow with a body present will have at least one stagnation point.

Beyond a separation point, the flow is unsteady. $v \approx 0$.

There are 3 types of unsteady flow: 
1. Small variations in steady flow
2. Actually unsteady flow, where at a given point, the trajectories change with time
3. Quasi-steady, where it is instantaneously steady, like water coming out of a bucket

Assumptions/considerations when working with fluids:
- Steady flow
- Inviscid
- Incompressible

If a fluid is sufficiently viscous, it will interact with the wall. The velocity of fluid will be 0 at the wall: the no-slip condition.

Reynolds number: $\frac{\rho VL}{\mu}$, where $V$ is the velocity far from the surface, L is the characteristic length, and $\mu$ is the viscosity.

As Re increases, the region by the wall effected by viscosity decreases.

We want to assume a fluid is incompressible, so its density is constant. If the error in assuming the density is constant is more than 1%, then we have to say that the fluid is compressible. This occurs when the difference in pressure or density is more than 5%.

For a control volume, whether the fluid is inviscid or incompressible is irrelevant. For everything else it is.

A system is a device that contains a fixed mass. But its volume can change.
Heat and work can cross system boundaries. Boundaries can move in systems.
The momentum of a system remains constant as long as no net force is applied to it.

For a fixed control volume: $\rho_{in} A_{in} v_{in}=\rho_{out} A_{out} v_{out} \Rightarrow \dot{m}_{in}=\dot{m}_{out}$.

Flow is drawn from left to right.
Mass flow is negative for flow into a control volume. The positive vector is facing outwards.

Volumetric flow rate: $Q=Av$

For non uniform flows: $\dot{m}=\int \rho v \cdot dA$

For mass flow in or out of a control volume, we only consider the normal component of the velocity to the area. $\dot{m} = \rho A v_n$

$F_{net}=\frac{d}{dt}(mv)=\dot{m}_{out}v_{out}-\dot{m}_{in}v_{in}$

Pick a sign convention and stick to it.

There are many ways in which a force can act on the fluid inside a control volume: 
- Internal forces such as gravity or magnetism
- Forces transmitted via the boundaries such as mechanical, pressure and viscous forces (shearing forces acting on the edge of the control volume)

As viscous forces are either taken into account by a velocity profile or are negligible, we can ignore them mostly.

Make sure pressure is gauge pressure, all forces have a way of acting on the fluid, and that all forces are resolved in a given direction.

This makes: $F_{net}=\sum F_x+p_{g,in}A_{in}-p_{g,out}A_{out}= \dot{m}_{out}v_{out}-\dot{m}_{in}v_{in}$

A positive $v_{out}$ requires a positive force. If there is no force to balance it, the pipe will rotate.

Warning: Pressure acts on the entire edge of the control surface, not just the bit that liquid flows through!

If velocity is not uniform, momentum flow rate = $\int (\rho v)vdA$
$$(\dot{m}v)_{in}=\int \rho v^2dA$$

The mass flow rate, $\dot{m}=\rho v_nA$, is always defined as normal to the control surface. It is treated as a scalar in the momentum flow rate vectors, $\dot{m}\textbf{v}$.

Pressure forces act normal to the surface, inwards.

For 2 dimensions, just resolve things into x and y components, with your coordinate system chosen to make the questions easiest. Remember to use projected area for pressures.

Careful! Fluid leaving by the top or bottom of the control volume have a contribution to the x momentum, so must be included when considering the momentum flows in the steady flow momentum equation.

## 5 steps to success:
1. Choose control volume and coordinate system to make it easiest for you
2. Evaluate pressure forces on all of the boundaries
3. Solve for unknowns using the conservation of mass equation
4. Calculate momentum flows in x and y directions for all inflows and outflows
5. Assemble the SFME, ensuring the signs of all forces are correct, eg. force has to be acting on the fluid

Along a streamline, if the velocity has changed, then there must be a resultant force acting.

The forces acting:
- Pressure
- Gravity
- Viscous forces (Can ignore in free stream, cannot ignore in separation or mixing)

![Pressure forces](Pressure_forces.png)

Considering pressure forces on a streamline: $F_{net,x}=-\Delta p_x \delta y \delta z$. $\Delta p_x=\frac{\partial p}{\partial x} \delta x$.
$\Rightarrow F_{net,x}=-\frac{\partial p}{\partial x} \times Vol$

If we consider the intrinsic coordinates for a streamline:
- In the s direction: Position = S; Velocity = $\frac{\partial s}{\partial t}=v$; Acceleration = $\ddot{s}=\frac{\partial v}{\partial t}$
- In the n direction: Position = R, where R is the instantaneous radius of curvature; Velocity = 0 (from the definition of a streamline); Acceleration = $\frac{\dot{s}^2}{R}=\frac{v^2}{R}$

Warning: In mechanics, the n direction in intrinsic coordinates is positive inwards. In fluid mechanics, it is positive outwards.

In order to apply Bernoulli's equation, the flow must be steady, it must have negligible friction forces, it must have constant density, and we are considering movement along a streamline.

To derive: $m\textbf{a}_s=\rho \times Vol \times \frac{\partial v}{\partial t}=\rho \times Vol \times v \frac{\partial v}{\partial s}=\rho \times Vol \times \frac{1}{2} \frac{\partial v^2}{\partial s}$

Considering s component of weight: $w_s=mg\cos(\alpha)=\rho \times Vol \times \frac{\partial z}{\partial s}$.

Combine all in the form $F_{net,s}=m\textbf{a}_s$, giving:

$$p+\rho gz+\frac{1}{2}\rho v^2=constant$$

A Pitot tube is a tube with a right angle in it. When the spout is pointed towards the incoming stream, the pressure increases. The Pitot pressure is the pressure in the spout when aligned with the flow. The velocity in the spout is zero, as the fluid has settled.

$p_{pitot}-p=\frac{1}{2}\rho v^2$, where $p$ is the pressure by the spout that is faced at right angles to the flow.

Mostly we use the Pitot-Static tube, which measures the two pressures at once.

We use the idea of a pressure and velocity far, far away to use in Bernoulli's equation. It is an undisturbed free stream. The opening which is at right angles to the flow can be approximated as $v_{\infty}$.

$p_1=p_2+\frac{1}{2}\rho v^2_{\infty} \Rightarrow v_{\infty}=\sqrt{\frac{2}{\rho}(p_1-p_2)}$

Use continuity and Bernoulli's equation to determine values, then sub them into the steady flow momentum equation.

Where we have separation regions, the velocity is essentially constant, so there is no pressure gradient across it, so the pressure is constant throughout.

We will now consider the equation of motion normal to the streamline: $F_{net,n}=ma_n, a_n=-\frac{v^2}{R}\Rightarrow F_{net,n}=-m\frac{v^2}{R}$.

Once again, $F_{net,n}=-\Delta p\delta x \delta y$. Subbing this in gives $\frac{\partial p}{\partial n}=\rho \frac{v^2}{R}$

This is a very important equation, and shows that if a fluid is curving inwards, then the pressure inside the turn is less than outside. As you move outwards from the centre of a hurricane, pressure increases, and hence velocity decreases.

It also explains the Coanda effect, the fact that streamlines follow walls. Walls are essentially streamlines, they have the same definition. As a streamline curves around an object, the pressure on the inside of the turn is greater than that on the outside, so it has a resultant force which keeps it on the wall. This same effect explains lift.

For parallel flow, the instantaneous radius is infinite, so the pressure gradient is $0$. Straight streamlines can have $\frac{\partial p}{\partial n}=0$ but $\frac{\partial p}{\partial s}$ has a value, only for straight and parallel streamlines are both zero.

Separations require viscosity, so if there is no viscosity, streamlines stick entirely onto objects.

The Magnus effect: when a cylinder rotates in a free stream flow, it curves the streamlines in such a way as to provide lift.

The pressure coefficient, $C_p=1-(\frac{v}{v_{\infty}})^2=\frac{p-p_{\infty}}{\frac{1}{2}\rho v_{\infty}^2}=\frac{p-p_\infty}{p_0-p_\infty}$

This is constant for any geometrically similar scenario.

For straight and parallel flow, there is no pressure gradient from velocity.

Bernoulli doesn't apply to a hydraulic jump as there is a lot of mixing.

Bernoulli's equation is the energy stored per unit volume. Therefore the change in Bernoulli's constant multiplied by the rate of flow of volume is the rate of energy lost.
