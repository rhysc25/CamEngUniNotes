# Unit Vectors

- Consider where forces act, for example friction for a bike acts between the tyres and the ground, and acts forwards, to propel the cyclist
- An inertial frame refers to a frame that is not accelerating, where Newton's laws can be applied
- See data book for velocities and accelerations in different coordinate systems
- For spherical and polar systems **e** points towards the particle
- To differentiate unit vectors:

$$\frac{d \textbf{e}_r}{d t}=\frac{d \theta}{d t} \textbf{e}_{\theta}$$

$$\frac{d \textbf{e}_{\theta}}{d t}=-\frac{d \theta}{d t} \textbf{e}_{r}$$

$$\frac{d \textbf{e}_r}{d t}=\dot{\theta} \textbf{e}_{\theta}=\dot{\theta} \textbf{k} \times \textbf{e}_r =\boldsymbol{\omega} \times \textbf{e}_r$$

In general: 
$$\frac{d \textbf{e}}{d t}=\boldsymbol{\omega} \times \textbf{e}$$

## Numerical differentiation

- Single-sided estimate: 
$$\dot{x}(k\Delta t)=\dot{x}_k\approx \frac{x_k-x_{k-1}}{\Delta t}$$

- Central difference: 
$$\dot{x}_k\approx \frac{x_{k+1}-x_{k-1}}{2 \Delta t}$$

## D'Alembert Forces
Including the $m\ddot{r}$ term as a force on your free body diagram. This always acts opposite to the designated positive direction.

## Numerical Methods
- Euler's method is a truncated Taylor series: 
$$x_n \approx x_{n-1} + v_{n-1} \Delta t$$
$$v_n \approx v_{n-1} + a_{n-1} \Delta t$$

- The Euler-Cromer or semi-implicit method builds upon this: 
$$x_n \approx x_{n-1} + v_{n} \Delta t$$

- Both methods are first order methods as the error is proportional to the size of the time step.
- To check numerical solutions:
  - Check the answer agrees at times where the situation can be analytically checked
  - Check that it converges as the time step decreases
  - Check that energy is conserved

## Energy Relationships
$$\int_A^B \textbf{F}\cdot d\textbf{r} = -(V_B - V_A) = +(T_B-T_A)$$
$$T+V= \text{constant}$$

For a torsional spring:
- Torque, $T=K\theta$
- Potential energy, $V=\frac{1}{2}K\theta^2$

## Equilibrium and Collisions
- An object is in stable equilibrium when $V''>0$
- The internal forces have no effect on linear momentum, only external forces can
- For an elastic collision: $u_A+v_A=u_B+v_B$
- Coefficient of restitution, $e=-\frac{v_2-v_1}{u_2-u_1}$

## Mass Flow Systems
The force on a body due to ejecting or gaining mass $=\dot{m} \textbf{v}_{P/B}$, where $\dot{m}$ is the rate of increase of mass and $\textbf{v}_{P/B}$ is the velocity of the mass relative to the body

## Moments and Angular Momentum
- The moment of a force, $\textbf{q}_o=\textbf{r} \times \textbf{F}$, using the right hand rule for $\textbf{a}\times\textbf{b}$
- The moment of a force about an axis, $Q_o=\textbf{q}_0\cdot\textbf{n}=(\textbf{r} \times \textbf{F})\cdot\textbf{n}$
- This is the same as the shortest distance from the axis to the particle multiplied by the component of the force that is perpendicular to both the axis and the short-distance line

- The angular moment of a particle around a point can also be thought of as the moment of momentum: 
$$\textbf{h}_0=\textbf{r}\times\textbf{p}=\textbf{r}\times(m\textbf{v})$$
- The angular momentum about an axis, $H_0=\textbf{h}_0\cdot \textbf{n}=(\textbf{r}\times m\textbf{v})\cdot \textbf{n}$

- The rate of change of the moment of momentum about an axis, which can be found via the product rule, is equal to the moment of force about that axis: 
$$\frac{dH_0}{dt}=(\textbf{r} \times \textbf{F})\cdot \textbf{n}=\textbf{q}_0 \cdot \textbf{n}$$

Therefore, for angular momentum about an axis to be conserved, the resultant force on a body must act through that axis.
