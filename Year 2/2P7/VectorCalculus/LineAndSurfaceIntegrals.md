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





