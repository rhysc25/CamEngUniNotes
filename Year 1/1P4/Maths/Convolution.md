# Convolution

Linear systems satisfy the principle of superposition: $\alpha f_1(t)+\beta f_2(t)=\alpha y_1(t)+\beta y_2(t)$

A system is time-invariant if delaying an input results in the same output, just delayed by the same amount. If $f(t)\rightarrow y(t)$ then $f(t-\tau) \rightarrow y(t-\tau)$ for any $\tau$.

Linear time-invariant systems have the special property that a sine wave at the input has an output of a sine wave, with the same frequency.

The step function: 
$$H(t) =
\begin{cases}
   0 & t<0\\    
   1 & t>0    
\end{cases}$$

If you input the step function, you get the step response, $r(t)$ as the output.
Linear combinations of the step function can be input.

The Dirac Delta function/ Impulse function: An infinitely tall and infinitely thin peak centred at 0, with area 1.
$\delta(t)=0$ except at $t=0$

$$\int_a^b \delta(t)dt = 1$$ 

provided $a < 0$ and $b > 0$

If we input the delta function, we get the impulse response, $g(t)$ as the output.

The derivative of a step function is a delta function, so the integral of a delta function is a step function.
Similarly, the derivative of a step response is an impulse response, so the integral of an impulse response is a step response.

Sifting theorem: As $\int_a^b \delta(t)dt = 1$ provided $a < 0$ and $b > 0$, then we can say for any function $f(t)$:
$\int_a^b \delta(t-c)f(t)dt = f(c)\int_a^b \delta(t-c)dt=f(c)$, provided $a < c$ and $b > c$

If we have a linear differential equation: $a\frac{dy}{dt}+by=f(t)$, then $f(t)$ is the input and $y(t)$ is the output.
If we replace $f(t)$ with $\delta(t)$ then $y(t)$ is the impulse response. However it is usually easier to set $f(t)$ to the step function, so that $y(t)$ is the step response, then differentiate the impulse response.

Considering boundary conditions: We know for a first order differential equation that $y(t)$ must equal 0 at $t=0$, or else there would be a jump, so $\frac{dy}{dt}=\infty$, the equation cannot be satisfied. With the same logic, for a second order differential equation, both $\dot{y}(t)$ and $y(t)$ must equal 0 at $y=0$.

Suppose out input is composed of lots of delta functions: $f(t)=\sum p_n \delta(t-q_n)$, then the corresponding output will be $y(t)=\sum p_ng(t-q_n)$

Any function can be equivalent to a combination of shifted delta functions, scaled to the height of the function at that value of t.

If we consider a mock delta function, which is a box function of width $\Delta \tau$ and height $\frac{1}{\Delta \tau}$.
$f(t)=\sum d(t-\tau_i)f(\tau_i)\Delta \tau_i$. As $\Delta \tau \rightarrow 0$:
$f(t)=\sum \delta(t-\tau_i)f(\tau_i)\Delta \tau_i$. Therefore the response of the system is $y(t)=\sum g(t-\tau_i)f(\tau_i)\Delta \tau_i$

Convolution integral:
$$\int_0^t g(t-\tau)f(\tau)d \tau$$

The integration variable is $\tau$, t is time as relates to the output of the system. The output is of course 0 for negative t.

If we are fed an input that is a piecewise function, we need to evaluate the convolution integral for each piece of the function separately.

4 steps to success:
Find general solution to equation for input = 1 (the step function). Set boundary conditions, $y(0)=\dot{y}(0)=0$, to get the step response. Differentiate to get the impulse response. Use convolution integral with the impulse response to find the output for any desired input.

If we apply the substitution $t=t-\tau$ to the convolution integral, we get $\int_0^t g(u)f(t-u)d u$. Both $u$ and $\tau$ are dummy integration variables, so are equivalent. Therefore, it does not matter which way round you get the arguments to the functions, provided both functions are 0 for $t<0$. This can make calculation easier in certain scenarios.

Temporal functions are causal. This means that there can be no output before the input that causes it, essentially affecting the output to the right.
Spatial systems are not causal, as an input can affect the output on either side.

For a shift-invariant function, meaning that the position has no effect on the output, only its position, we just need to rewrite the convolution integral as an integral from $-\infty$ to $+\infty$:
$\int_{-\infty}^{\infty} g(x-a)f(a)d a$

This is easier, as we don't have to split the integral for each case, we can just calculate them all at once.

If the spatial function is not shift-invariant, for example a distributed load on a wire, where the deformation changes based on where a point load is applied, how close it is the boundaries.
The total deformation from the distributed load is the sum of all the deformations from the individual point loads.

We now have to consider a two-variable functions $g(x,a)$, the displacement at position $x$ for a point load at $a$.

For the wire example: $y(x)=\int_{0}^{L} g(x,a)F(a)d a=\int_{0}^{L} g(x,a)Kd a$
