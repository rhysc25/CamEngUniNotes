# Partial Differentiation

You can represent $f(x,y)$ using a contour map or a $3D$ surface.

$$\frac{\partial f}{\partial x}=\lim_{\delta x \rightarrow 0}\frac{f(x+\delta x,y)-f(x,y)}{\delta x}$$

Essentially taking a slice where k is fixed

Partial differentiation can be used to estimate small changes in values:
$\delta f \approx \frac{\delta f}{\delta x}\delta x+ \frac{\delta f}{\delta y}\delta y$, where the partial derivatives are evaluated from the starting values of $x$ and $y$.

If we want to find the gradient along a particular direction, we can take a directional derivative. The directional derivative of f in a direction of a unit vector $\textbf{u}$ is given by: $\nabla f\cdot \textbf{u}$.

$$\begin{bmatrix}
\frac{\partial f}{\partial x}\\
\frac{\partial f}{\partial y}
\end{bmatrix}
\cdot
\begin{bmatrix}
u_x\\
u_y
\end{bmatrix}$$

Grad $f$ is the direction of maximum change of $f$ and is perpendicular to the tangent at any point on a curve or surface. Therefore grad $f$ gives the normal to the surface at any point.

Chain rule: For f(u(x,y),v(x,y)...):

$$\frac{\partial f}{\partial x}=\frac{\partial f}{\partial u} \frac{\partial u}{\partial x}+\frac{\partial f}{\partial v}\frac{\partial v}{\partial x}+...$$
$$\frac{\partial f}{\partial y}=\frac{\partial f}{\partial u} \frac{\partial u}{\partial y}+\frac{\partial f}{\partial v}\frac{\partial v}{\partial y}+...$$
