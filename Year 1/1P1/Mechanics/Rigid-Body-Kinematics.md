# Rigid Body Kinematics

$$\textbf{V}=\boldsymbol{\omega}\times \textbf{r}$$
represents the velocity of a particle in a rotating system.

## Relative Motion
$$\textbf{r}_B=\textbf{r}_A + \textbf{r}_{B/A}$$
$$\textbf{v}_B=\textbf{v}_A + \textbf{v}_{B/A}$$
$$\textbf{a}_B=\textbf{a}_A + \textbf{a}_{B/A}$$

When the reference frame is rotating, define a rotating unit vector $\textbf{e}$, where:
$$\dot{\textbf{e}}=\boldsymbol{\omega} \times \textbf{e}$$

Example for orthogonal unit vectors:
$$\dot{\textbf{e}}_2=\boldsymbol{\omega} \times \textbf{e}_2=-\omega\textbf{e}_1$$

## Rigid Bodies
A rigid body is an object with continuously distributed mass that cannot deform. If two particles, $A$ and $B$ on the body have velocities $\textbf{V}_A$ and $\textbf{V}_B$, the components of said velocities acting in the direction $AB$ must be equal.

Any motion of $A$ relative to $B$ must be due to rotation alone.

From data book:
$$\textbf{V}_B=\textbf{V}_A+\dot{r}\textbf{e}+r(\boldsymbol{\omega}\times \textbf{e})$$

Or for a rigid body:
$$\textbf{V}_B=\textbf{V}_A+r(\boldsymbol{\omega}\times \textbf{e})$$

## Instantaneous Centre
An instantaneous centre for a $2D$ lamina is a point somewhere in the plane of the lamina that has zero velocity, instantaneously at rest. It is perpendicular from all the velocities in the body.

The velocity of a particle = the angular velocity $\times$ the distance to the instantaneous centre:
$$\textbf{V}_A=\omega \rho_A$$

The instantaneous centre changes constantly, and can be infinitely far away if the body is purely translating.

## Centre of Mass
The position vector of the centre of mass of an object:
$$\textbf{r}_G=\frac{1}{M}\int\textbf{r}dm$$

If the object has no symmetry, this leads to a double integral in $(x\textbf{i}+y\textbf{j})$

$\textbf{F}=m\textbf{a}$ refers to the centre of mass of a large object.

## Rotational Dynamics
Torque = rotational inertia $\times$ angular acceleration

$$\begin{bmatrix}
q_x\\
q_y\\
q_z
\end{bmatrix} =
\begin{bmatrix}
I_{xx} & I_{xy} & I_{xz}\\
I_{yx} & I_{yy} & I_{yz}\\
I_{zx} & I_{zy} & I_{zz}
\end{bmatrix}
\begin{bmatrix}
\dot{\omega}_x\\
\dot{\omega}_y\\
\dot{\omega}_z
\end{bmatrix}$$

If the rotational inertial matrix is diagonal, the applied torque causes rotation in just one direction.

## Moment of Inertia
Moment of inertia:
$$J_o=\int r^2 dm$$

$$Q=J\dot{\omega}$$

Common moments of inertia:
- Circular disk: $\frac{MR^2}{2}$
- Rod rotating about one end: $\frac{ML^2}{3}$

## Mass Moment of Inertia
Around $x$ axis:
$$I_{xx}=\int r_x^2 dm = \int (y^2+z^2)dm$$
and similar for the other axes.

For a lamina only:
$$I_{xx}=\int r_x^2 dm = \int y^2dm$$
and similar for $I_{yy}$

$$I_{zz}=\int r_z^2 dm = \int (x^2+y^2)dm$$

### Perpendicular Axis Theorem (for laminae only):
$$I_{zz}=I_{xx}+I_{yy}$$

### Parallel Axis Theorem (applies to any body):
The moment of inertia about an axis passing through O is equal to the moment of inertia about a parallel axis passing through the centre of mass, plus the mass of the object multiplied by the distance between the axes squared.

$$I_O=I_G+Mx_G^2$$

Note:
- The perpendicular axis theorem only applies to laminae
- The parallel axis theorem applies to any body
- The moment of inertia is minimum at the centre of mass, and increases as you stray from it

For a composite body: The total moment of inertia about an axis is the sum of the moment of inertias about that axis.

For a planar, rigid body, translating and rotating:
$$\textbf{q}=I_G \dot{\boldsymbol{\omega}}$$

## Rolling Bodies
The no slip condition, when using D'Alembert forces:
$$\textbf{a}_x=-\dot{\boldsymbol{\omega}}R$$

Also:
$$v=\Omega R$$

Draw the D'Alembert forces, gathered from the polar accelerations in the data book, and the D'Alembert torque, $I_G \dot{\boldsymbol{\omega}}$. Take moments then resolve to determine $\dot{\theta}$ and $\ddot{\theta}$

## Angular Momentum and Energy

$$\textbf{q}_G=\frac{d \textbf{h}_G}{dt}$$

$$\textbf{h}_G = I_G \boldsymbol{\omega}$$

$$\int_{t_A}^{t_B} \textbf{q}_G dt=\textbf{h}_{G_B}-\textbf{h}_{G_A}$$

Can be used to find the time for a change in angular momentum to occur, or the total angle rotated using:
$$\ddot{\theta}=\dot{\theta} \frac{d\dot{\theta}}{d \theta}$$

Total kinetic energy:
$$T=\frac{1}{2}m\textbf{v}_G^2+\frac{1}{2}I_G\omega^2$$
