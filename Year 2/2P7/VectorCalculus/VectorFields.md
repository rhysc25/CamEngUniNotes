Both the scalar and vector product are distributive:
$\textbf{a}\times(\textbf{b}+\textbf{c})=\textbf{a}\times\textbf{b}+\textbf{a}\times \textbf{c}$

A vector field is just made up of scalar fields. But it would be inconvenient to keep track of them all at the same time

Field lines - tangential to the vector field $\textbf{V}$ at all times. 
It shows direction, but not magnitude.

How to form them: Create a tangential $\delta s$. Move to the end of it and repeat. As $\delta s \rightarrow 0$, the line becomes exactly tangential to $\textbf{V}$ so forms a field line

If $\textbf{V}$ is a vector field with components, $V_x, V_y, V_z$, then the equation of a field line projected onto the (x,y) place must satisfy the condition that the slope of the field line is parallel to the velocity direction in the (x,y) plane,
$\frac{dy}{dx}=\frac{V_y}{V_x}$. Similarly: $\frac{dz}{dy}=\frac{V_z}{V_y}$ and $\frac{dx}{dz}=\frac{V_x}{V_z}$

$d\textbf{r}$, a small change in a position vector must be parallel to $\textbf{V}$
So $d\textbf{r}=k\textbf{V}$ and $\textbf{V}\times d\textbf{r}=0$
You must draw the field lines, and don't forget to draw arrow heads to indicate direction

$\frac{d \textbf{V}}{ds}=\lim_{\delta s \rightarrow 0}(\frac{\textbf{V}(s+\delta s)-\textbf{V}(s)}{\delta s})$

The velocity must be tangential to a curve, but the acceleration is unlikely to be, unless it has zero curvature.

The differentiation formulas for vector functions are all in the data book and can be proven by breaking each vector function down into its cartesian scalar components.
$\frac{d}{ds}(\textbf{A}\cdot\textbf{B})=\textbf{A}\cdot\frac{d\textbf{B}}{ds}+\textbf{B}\cdot \frac{d\textbf{A}}{ds}$

**Partial Derivatives**

$\frac{\partial \textbf{V}}{\partial x}=\lim_{\delta x \rightarrow 0}(\frac{\textbf{V}(x+\delta x,y,z)-\textbf{V}(x,y,z)}{\delta x})$
This is a vector representing, in magnitude and direction, the rate of change of $\textbf{V}$ with x when y and z are both kept constant. We can evaluate $\frac{\partial \textbf{V}}{\partial x}$ from the components of $\textbf{V}$

$\frac{\partial \textbf{V}}{\partial x}=\frac{\partial V_x}{\partial x}\textbf{i}+\frac{\partial V_y}{\partial y}\textbf{j}+\frac{\partial V_z}{\partial z}\textbf{k}$

The rules for partial derivatives are similar to those for ordinary derivatives, e.g. $\frac{\partial}{\partial s}(\textbf{A}\cdot\textbf{B})=\textbf{A}\cdot\frac{\partial \textbf{B}}{\partial s}+\textbf{B}\cdot \frac{\partial \textbf{A}}{\partial s}$

**The Gradient of a Scalar Field**

The vector operator del, $\nabla$, acts on a scalar field and gives a vector field.
$\nabla = \textbf{i}\frac{\partial}{\partial x} + \textbf{j}\frac{\partial}{\partial y} + \textbf{k}\frac{\partial}{\partial z}$ 
Grad $\phi$: $\nabla \phi = \textbf{i}\frac{\partial \phi}{\partial x} + \textbf{j}\frac{\partial \phi}{\partial y} + \textbf{k}\frac{\partial \phi}{\partial z}$

Identities: $\nabla (f+g)=\nabla f+\nabla g$
$\nabla (fg)=f\nabla g+ g\nabla f$
Prove by expanding into cartesian components

We can rewrite the total derivative of $\phi$ as $\delta \phi = \nabla \phi \cdot \delta \textbf{r}$, which holds for any coordinate system
If we rewrite $\delta \textbf{r}$ as $\delta s \hat{\textbf{n}}$, divide through by $\delta s$ then as $\delta s$ tends to 0, we get that:
$$\frac{d\phi}{ds}=\nabla \phi \cdot \hat{\textbf{n}}$$
This is a directional derivative. We can see it is max when $\hat{\textbf{n}}$ is parallel to $\nabla \phi$

$\nabla \phi$ points in the direction of greatest increase of $\phi$

If we have a scalar field we can always make a vector field where $\textbf{V}_0=\nabla \phi$. Here $\phi$ is called the scalar potential.
However if we have a vector field, we can't always find a scalar potential for it.

The operation has many applications:
* Heat conduction: $\textbf{q}=-\lambda \nabla T$. We can assume that $\lambda$ is constant so $-\lambda T$ is the scalar potential
* Diffusion: $\textbf{m}=-D\nabla c$ where D is diffusion constant, m is diffusive mass flux and c is concentration
* Current flow: $\textbf{j}=-\sigma \nabla V$ where j is the current density

We can now more easily express the substantive derivative earlier by using the del operator:
$\frac{dT}{dt}=\textbf{V}\cdot \nabla T + \frac{\partial T}{\partial t}=(\textbf{V}\cdot \nabla )T + \frac{\partial T}{\partial t}$ 

$(\textbf{V}\cdot \nabla )$ is a scalar operator, and can act on either a scalar or a vector

$\nabla$ in non-Cartesian coordinate systems:
Something like $\delta f=\nabla f \cdot \delta \textbf{r}$ is true for any coordinate system
However the definition of $\delta \textbf{r}$ changes across coordinate systems, so $\nabla$ must change too

In cylindrical: $\delta \textbf{r}=\delta r e_r + r\delta \theta e_{\theta} + \delta z e_z$
The $r\delta \theta$ appears as we are considering movement along an arc swept out by theta
Therefore $\nabla f$ must change too, having a $\frac{1}{r}\frac{\partial f}{\partial \theta}$ in the $e_{\theta}$ term. These changes can be seen in the maths data book.

**Divergence of a Vector Field**

The divergence of $\textbf{V}$, div $\textbf{V}$.
This acts on a vector and gives a scalar.

$\nabla \cdot \textbf{V}=\frac{\partial V_x}{\partial x}+\frac{\partial V_y}{\partial y}+\frac{\partial V_z}{\partial z}$

There are several identities for divergence, all given in the data book. They can all be proven by breaking down into cartesian components

To consider the conservation of mass in fluid dynamics, we first consider an element of volume $\delta v$ in a varying scalar field of density $\rho$
![[Pasted image 20251023155657.png]]
The mass flow rate out of the control volume on face 2:
$\rho_2 v_{x2}\delta y \delta z \approx (p_0v_{x1}+\frac{\delta x}{2}\frac{\partial (\rho v_x)}{\partial x})\delta y \delta z$
Summing this with the mass flow rate into the control volume on face 1, we get:
$\rho_2v_{x2}-\rho_1v_{x1}\delta y\delta z\approx \frac{\partial (\rho v_x)}{\partial x} \delta x \delta y\delta z$

Summing these over all faces, the rate of mass efflux (flux exiting) =
$\nabla \cdot (\rho \textbf{V})\delta v$
As the volume is fixed we can also say that the rate of decrease of mass is given by: $-\frac{\partial \rho}{\partial t}\delta v$
Therefore, $\frac{\partial \rho}{\partial t}+\nabla \cdot (\rho \textbf{V})=0$
If $\rho$ is a constant, we must have that $\nabla \cdot \textbf{V}=0$

In general, the net rate of efflux of any vector field $\textbf{A}$ of volume $\delta v=(\nabla \cdot \textbf{A})\delta v$

If $\nabla \cdot \textbf{V}=0$ everywhere, then the vector field is called solenoidal, so it has no sources or sinks. This is true for incompressible steady flow.
If $\nabla \cdot \textbf{V}>0$ there is net flux out, so a source

When we switch coordinate systems, say to cylindrical, we compute the dot product between vectors in cylindrical coordinates. We must be careful, as actually expanding out the dot product will create another term, due to the fact that $\frac{\partial \textbf{e}_r}{\partial \theta}=\textbf{e}_{\theta}$
This extra term is included in the data book expression

When a vector field is governed by a scalar potential, and is also solenoidal, it follows that: $\nabla \cdot (\nabla \phi)=0$
We can write this as $\nabla^2\phi$ where $\nabla^2$ is the Laplacian, given by $\frac{\partial^2}{\partial x^2}+\frac{\partial^2}{\partial y^2}+\frac{\partial^2}{\partial z^2}$

**Curl of a Vector Field**

Curl $\textbf{V}$: $\nabla \times \textbf{V}$
This acts on a vector field and gives a vector field
Twice the local angular velocity of a fluid particle

$\nabla \times \textbf{V}=\textbf{i}(\frac{\partial V_z}{\partial y}-\frac{\partial V_y}{\partial z})+\textbf{j}(\frac{\partial Vx}{\partial z}-\frac{\partial V_z}{\partial x})+\textbf{k}(\frac{\partial V_y}{\partial x}-\frac{\partial V_x}{\partial y})$
This can be found from the determinant method of finding the vector product

The direction of $\nabla \times \textbf{V}$ can be at any angle to $\textbf{V}$

For all 2D vector fields, the curl field is normal to the plane of the original field. It represents how much the field is rotating.

Identities can be found in the data book, once again proven by breaking into cartesian components. Most importantly:
$\nabla \cdot (\nabla \times \textbf{A})=0$. This shows that the divergence of the curl field is 0. Therefore all curl fields are solenoidal
$\nabla \times (\nabla \phi)=0$. This shows that the curl of any vector field formed from a scalar potential = 0

$(\textbf{B}\cdot \nabla)$ is a scalar operator, which acts on a vector and gives a vector with 9 terms

The curl in different coordinate systems is given in the data book

The angular velocity of a line element depends on theta. This is because it deforms as well as rotates. Because of this, we need to find the instantaneous mean angular velocity by integrating over theta and dividing by $2\pi$

The curl vector points in the direction of the axis of rotation of the fluid particle. In fluid mechanics, it is called vorticity.
The local magnitude of the curl of the velocity field is equal to twice the instantaneous mean angular velocity of a fluid particle at that point. 

Since all curl fields are solenoidal, then there can be no sources or sinks of vorticity within the fluid flow field

A vector field which has $\nabla \times \textbf{V}=0$ everywhere is called an irrotational field

If $\textbf{V}=\nabla \phi$, then $\nabla \times \textbf{V}=0$ and $\textbf{V}$ is irrotational
Conversely, if $\textbf{V}$ is irrotational, we can find a scalar potential $\phi$ such that $\textbf{V}=\nabla \phi$ 
This is the test to see if a scalar potential exists






