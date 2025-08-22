$\text{r}(u,v)=x(u,v)\text{i}+y(u,v)\text{j}+z(u,v)\text{k}$
This is an object in 3D space with 2 independent variables, so maps a surface in 3D.

By setting u constant and varying v, we get a set of curves which are part of the surface.
$$\frac{\partial^2 f}{\partial x \partial y} = \frac{\partial^2 f}{\partial y \partial x}$$
To get the Taylor series for 2 variables, first do it with one variable, x. 
$f(x_1 + \delta x, y) \approx f(x_1,y) + \delta x \frac{\partial f}{\partial x}(x_1,y)$
Set this $g(y)$, then apply the Taylor series using y.
With some simplification it will give the result in the data book

For the normal at a point on a vector surface to go through the origin, $\frac{\partial r}{\partial u} \cdot r = 0$ and $\frac{\partial r}{\partial v} \cdot r = 0$

The Total Differential:
$$df = \frac{\partial f}{\partial x}dx + \frac{\partial f}{\partial y}dy$$
If we have a function $df = P(x,y)dx + Q(x,y)dy$:

If such a function $f(x,y)$ exists, then  $P(x,y)dx + Q(x,y)dy$ is a perfect differential. By comparing to the total differential expression, it is clear that to be a perfect differential:

$\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$

An example from thermodynamics would be the equation $du = Tds - pdv$

The general Chain Rule:
$$\frac{\partial f}{\partial u} = \frac{\partial f}{\partial x}\frac{\partial x}{\partial u} + \frac{\partial f}{\partial y}\frac{\partial y}{\partial u} + \frac{\partial f}{\partial z}\frac{\partial z}{\partial u}$$
To implicitly differentiate something:
$$\frac{d y}{d x} = -(\frac{\partial f}{\partial y})^{-1} \frac{\partial f}{\partial x}$$
The gradient operator, $\nabla$, acts on a scalar function and returns a vector whose dimension is equal to the number of independent variables of the function
$$\nabla f = \begin{bmatrix}
\frac{\partial f}{\partial x}\\
\frac{\partial f}{\partial y}\\
\end{bmatrix}$$
Directional derivative: $b\cdot \nabla f$
Where $b$ is a unit vector in the direction you want to differentiate along

$\nabla f$ always points in the direction of greatest change for the function
The direction of a contour must be perpendicular to $\nabla f$
When we have a function of 3 variables, if we hold $f(x,y,z) =$ constant, we can draw level surfaces

$\nabla f$ is always normal to the level surface

$z^2=4(x^2+y^2)$ is a cone of revolution

In order to simply the 2 variable Taylor expansion we can define a new matrix, the Hessian
$$S = 
\begin{bmatrix}
\frac{\partial^2 f}{\partial x^2} & \frac{\partial^2 f}{\partial x \partial y} \\
\frac{\partial^2 f}{\partial y \partial x} & \frac{\partial^2 f}{\partial y^2}
\end{bmatrix}$$
$\nabla f =0$ for a maximum or minimum, so $\frac{\partial f}{\partial x}=\frac{\partial f}{\partial y}=0$
If the eigenvalues of the Hessian are both less than zero, maximum
If the eigenvalues of the Hessian are both more than zero, minimum
If one is positive and one is negative, it must be a saddle

A saddle point looks like a minimum in one direction, but looks like a maximum in another

The determinant of the Hessian defines $\Delta$, which is used to classify stationary points on a 3D surface

