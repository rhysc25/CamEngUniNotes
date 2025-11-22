**Line Integral**

In a line integral, the element is part of a specified line in 3-D space. The line element can be a scalar,  $\delta s$ measured along the curve, or a vector $\delta \textbf{r}$. The integrand can also be a scalar or a vector.
E.g.
$\int \rho(s)ds \qquad$ a scalar
$\int q \textbf{E}(s) ds \qquad$ a vector 
$\int \textbf{F}\cdot \textbf{r} \qquad$ a scalar
$\int \textbf{J}(\textbf{dr} \times \textbf{B}) \qquad$ a vector

Considering $\int_A^B \textbf{F}\cdot \textbf{r} \qquad$
$\textbf{F}=F_x\textbf{i}+F_y\textbf{j}+F_z\textbf{k}$
$\textbf{dr}=dx\textbf{i}+dy\textbf{j}+dz\textbf{k}$
So $W=\int_A^B F_xdx+F_ydy+F_zdz$

This is easiest when solved parametrically
If you can't find one variable which can express x,y,z, you just have two do three different integrals, using the relationships between the variables given to you by the equation of the line

**Conservative fields**
Conservative is the same as irrotational, being the result of $\textbf{V}$ being the divergence of a scalar potential. Traditionally, irrotational is used to describe fluid velocity and conservative is used to describe a force field $\textbf{F}$

Conservative means that $\int \textbf{V} \cdot d\textbf{r}$ between any two points A and B is independent of the path of integration.

It can be showed that If $\textbf{V}=\nabla \phi$ then $\textbf{V} \cdot d\textbf{r}=d\phi$
This means that $\int_A^B \textbf{V} \cdot d\textbf{r}=\int_A^Bd\phi=\phi_B-\phi_A$ which is path independent

For conservative fields, $\oint \textbf{F}\cdot d\textbf{r}=0$
For non-conservative fields, $\oint \textbf{F}\cdot d\textbf{r}=\Gamma$

**Surface Integrals**

These are the extension to 3D of the scalar double integral. A surface integral is the integration of a function over a specified surface. It can result in a scalar or a vector.

The most common form is to find the total flow rate passing through a surface S: $\int \int \textbf{V}\cdot d\textbf{A}$

The main difficulty is evaluating $d\textbf{A}$
If we consider $\textbf{r}$ as a position vector of a point on the surface:
$\textbf{r}(u,v)=x(u,v)\textbf{i}+y(u,v)\textbf{j}+z(u,v)\textbf{k}$
![[Pasted image 20251111140626.png]]
It is clear that $\delta \textbf{r}_v=\frac{\partial \textbf{r}}{\partial v}\delta v$ and $\delta \textbf{r}_u=\frac{\partial \textbf{r}}{\partial u}\delta u$
This makes the area given by the cross product:
$$d\textbf{A}=(\frac{\partial \textbf{r}}{\partial u}\times \frac{\partial \textbf{r}}{\partial v})\delta u \delta v$$
If $\textbf{V}$ is the velocity field, and $\rho$ is the density field, then $\int\int_S \rho \textbf{V}\cdot d\textbf{A}$ is the total mass flowrate crossing S. We are adding up all the dot products over the entire surface

$∯_S$ is the integration performed over a closed surface. 
$∯\textbf{V}\cdot d\textbf{A}=0$ is true for all solenoidal fields
If solenoidal, $\nabla \cdot \textbf{V}=0$, zero net efflux of $\textbf{V}$ from $\delta v$
Therefore no net efflux from finite volume (no sources or sinks)

If we consider a field tube, a tube made of streamlines, by definition there is not flux across the walls of the field tube. 
If the vector field is solenoidal, the total flux into the stream tube must be the same as flux leaving the field tube. 
For steady variable density flow, this would mean that $\nabla \cdot (\rho V)=0$

**Volume Integrals**

Can result in a scalar or vector. Example: $\iiint_{vol} \rho dv=$ the mass of a fluid with density $\rho$ occupying volume vol

**Gauss's Divergence Theorem**

The volume integral of $\nabla \cdot \textbf{V}$ over the volume vol is equal to the net flux of $\textbf{V}$ through the surface S enclosing vol
$$\iiint_{vol}(\nabla \cdot \textbf{V})dv=\iint_{s,closed} \textbf{V}\cdot d\textbf{A}$$
We can use Gauss' theorem to transform a surface integral over a closed surface, into a volume integral over the enclosed volume, and vice-versa.

From Gauss' theorem:
If $\textbf{V}$ is a solenoidal field, $\nabla \cdot \textbf{V}=0$ everywhere, then $\iint_{s,closed}\textbf{V}\cdot d\textbf{A}=0$: The net efflux of $\textbf{V}$from any finite volume is zero.    

Considering conservation of mass:
The rate of increase of mass in a control volume = - net efflux of mass from the control volume
$\frac{\partial}{\partial t}(\iiint_{vol}\rho dv)=\iiint_{vol}\frac{\partial \rho}{\partial t} dv=-\iint_{closed}\rho \textbf{v}\cdot d\textbf{A}$
Rewriting the right hand side with Gauss' theorem we get that:
$\iiint_{vol}(\frac{\partial \rho}{\partial t}+\nabla \cdot (\rho \textbf{V}))dv=0$
If we shrink the volume down to zero, just at a point, we get the differential expression:
$\frac{\partial \rho}{\partial t}+\nabla \cdot (\rho \textbf{V}) = 0$

Gauss's divergence theorem can be used to provide a coordinate-free definition of the divergence,
$$\nabla \cdot \textbf{V}=\lim_{\delta v \rightarrow 0} \frac{1}{\delta v}\iint_{closed}\textbf{V}\cdot d\textbf{A}$$
This is a compact definition of divergence which is valid for any coordinate system

**Stokes's Theorem**

The circulation of the vector field $\textbf{V}$ around the closed curve L is equal to the flux of $\nabla \times \textbf{V}$ passing through any surface S that spans the curve L.

If S is an open two-sided surface bounded by a closed non-intersecting curve L, and if the vector field $\textbf{V}$ has continuous derivatives, then:
$$\oint_L \textbf{V} \cdot d\textbf{r}=\iint_S(\nabla \times \textbf{V})\cdot d\textbf{A}$$
The direction of integration for the line integral must be chosen such that a right handed screw would advance in the positive direction of the $\delta \textbf{A}$ vector.

There are an infinite number of possible surfaces that would span the same closed curve, and the flux of $\nabla \times \textbf{V}$ through each of them must be the same. This implies that there are no sources or sinks of $\nabla \times \textbf{V}$. All curl fields are solenoidal.

Stokes's theorem converts a line integral to a surface integral.

The coordinate free definition of curl, using Stokes's theorem:
$(\nabla \times \textbf{V})\cdot \delta \textbf{A}=\oint_L \textbf{V} \cdot d\textbf{r}$

Summary:
If a vector field is conservative:
* $\oint_C \textbf{V} \cdot d\textbf{r}=0$ for any closed curve, C
* $\textbf{V}$ is also irrotational ($\nabla \times \textbf{V}=0$)
* A scalar potential exists
If a vector field is solenoidal:
* $\nabla \cdot \textbf{V}=0$
* $\iint_{closed S}\textbf{V}\cdot d\textbf{A}=0$
* A vector potential exists such that $\textbf{V}=\nabla\times \textbf{C}$