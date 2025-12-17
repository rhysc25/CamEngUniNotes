**Differentiation**

If $\phi$ is a function of two independent variables, x and y, we write $\phi=\phi(x,y)$, which can be represents by a surface in 3-D space

Differentiation of a scalar function of more than one variable:
$\frac{\partial \phi}{\partial y}=\lim_{\delta y \rightarrow 0}(\frac{\phi(x,y+\delta y)-\phi(x,y)}{\delta y})$

The higher order partial derivatives are defined in a similar way

We can use the partial derivatives to evaluate the contribution to $\delta \phi$ from both $\delta x$ and $\delta y$:
$\delta \phi \approx \frac{\partial \phi}{\partial x}\delta x+\frac{\partial \phi}{\partial y}\delta y$
As the changes tend to 0: $d\phi = \frac{\partial \phi}{\partial x}dx+\frac{\partial \phi}{\partial y}dy$
Where $d\phi$ is called the total differential

If our field is also a function of time, then we would have a total differential of the form:
$\delta T=\frac{\partial T}{\partial x}\delta x+\frac{\partial T}{\partial y}\delta y+\frac{\partial T}{\partial t}\delta t$
Dividing through by $\delta t$:

$\frac{dT}{dt}=\frac{\partial T}{\partial x}\frac{\delta x}{\delta t}+\frac{\partial T}{\partial y}\frac{\delta y}{\delta t}+\frac{\partial T}{\partial t}$

$\frac{dT}{dt}$ is a total derivative. It is the rate of change of the temperature as 'seen' by the probe as it moves through the temperature field.
Note that the $\frac{\partial T}{\partial t}$ is a rate of change at a fixed point. 

If the temperature field is actually a property of a fluid and we are interested in the temperature of a fluid particle as it moves through this field, then $V_x$ and $V_y$ are now also vectors field in terms of x,y and t.
In this case, the total derivative is referred to as the substantive or material derivate, and is usually written as $\frac{DT}{Dt}$

**Chain rule with more than one variable:**

If $\phi = \phi(x,y)$, but we want $\frac{\partial \phi}{\partial u}$ and $\frac{\partial \phi}{\partial v}$ where $x=x(u,v)$ and $y=y(u,v)$

$\delta \phi = \frac{\partial \phi}{\partial x}\delta x+\frac{\partial \phi}{\partial y}\delta y$
And
$\delta x = \frac{\partial x}{\partial u}\delta u+\frac{\partial x}{\partial v}\delta v$
$\delta y = \frac{\partial y}{\partial u}\delta u+\frac{\partial y}{\partial v}\delta v$

Sub these in, and collect terms to give:
$\delta \phi = (\frac{\partial \phi}{\partial x}\frac{\partial x}{\partial u}+\frac{\partial \phi}{\partial y}\frac{\partial y}{\partial u})\delta u+(\frac{\partial \phi}{\partial x}\frac{\partial x}{\partial v}+\frac{\partial \phi}{\partial y}\frac{\partial y}{\partial v})\delta v$

Comparing this to: $\delta \phi = \frac{\partial \phi}{\partial u}\delta u+\frac{\partial \phi}{\partial v}\delta v$
We can see that $\frac{\partial \phi}{\partial u}=\frac{\partial \phi}{\partial x}\frac{\partial x}{\partial u}+\frac{\partial \phi}{\partial y}\frac{\partial y}{\partial u}$

Taylor series for functions of more than one variable:
![[TaylorSeriesOfMoreThanOneVariable.png]]

**Integration**

The integration of $\phi$ between a and b: 
$\int_a^b \phi (x) dx=\lim _{\delta x_i \rightarrow 0} \sum^N_1 \phi (i) \delta x_i$

If $\phi$ is a function of two independent variables, $\phi=\phi(x,y)$, we define the integration as:
$\int_A \phi (x) dA=\lim _{\delta A_i \rightarrow 0} \sum^N_1 \phi (i) \delta A_i$

A is an area on the x-y plane. The result of this integration is the volume enclosed by the surface $\phi = \phi (x,y)$, the area A on the x-y plane, and the vertical curtain connecting the two
![[Pasted image 20251009160227.png]]

Or we can use double integral notation:
$\int \int \phi dA=\int \int \phi dxdy=\int dx \int dy \phi (x,y)$

This of course scales to higher and higher number of independent variables
The limits of y are a function of x in this case.

Application of integration to find average values:

$m=\bar{\rho} V_{tot}$
$\Rightarrow \frac{\int \int \int \rho dxdydz}{\int \int \int dxdydz}$

**Change of variable and the Jacobian**

If $I=\int \phi dx$, we can change variables simply by considering $dx=\frac{dx}{du}du$, and substituting it in

For a function of two variables:
$I=\int \int \phi(x,y) dxdy$
$dydx$ means using vertical strips, $dxdy$ means using horizontal strips

If we want to switch variables to v and u, $x=x(u,v)$ and $y=y(u,v)$, we need to find the correct scale factor.

![[Pasted image 20251009161824.png]]

We need to find the area of a section contained between $v,v+\delta v, u,$ and $u+\delta u$. 
This area is given by $|\textbf{a}\times \textbf{b}|$

$\textbf{a}$ is given by moving $\delta u$ in the direction of constant $v$.
$\textbf{a}=\frac{\partial x}{\partial u}\delta u \textbf{i} + \frac{\partial y}{\partial u}\delta u \textbf{j}$
$\textbf{b}=\frac{\partial x}{\partial v}\delta v \textbf{i} + \frac{\partial y}{\partial v}\delta v \textbf{j}$

Finding the value of $|\textbf{a}\times \textbf{b}|$ gives $|\frac{\partial x}{\partial u}\frac{\partial y}{\partial v}-\frac{\partial x}{\partial v}\frac{\partial y}{\partial u}|$ $dudv$

$|\frac{\partial x}{\partial u}\frac{\partial y}{\partial v}-\frac{\partial x}{\partial v}\frac{\partial y}{\partial u}|$ is the Jacobian, sometimes written as $\frac{\partial(x,y)}{\partial (u,v)}$

When finding $\frac{\partial x}{\partial u}$ and the like, ensure that $x$ is purely a function of $u$ and $v$

$dxdy=\frac{\partial(x,y)}{\partial (u,v)} dudv$

The Jacobian, J, is just the ratio of elemental areas in one coordinate system (x,y) to another (u,v). It follows that the ratio of areas in (u,v) coordinates to the equivalent in (x,y) coordinates is given by the reciprocal of the Jacobian.

Sometimes it may be easier to evaluate $\frac{\partial(x,y)}{\partial (u,v)}$ than $\frac{\partial(u,v)}{\partial (x,y)}$ then invert it








