Input signal -> plant -> output signal
From this output signal, we have a feedback controller than changes the input slightly

The oldest feedback system:
![[OldestFeedbackSystem.png]]

Equivalent block diagram:
![[OldestFeedbackBlockDiagram.png]]
Every signal must be a measurable quantity

The float chamber is described by: $x(t)=\frac{1}{A}\int_0^t q(\tau)d\tau$
or $\dot{x}(t)=\frac{1}{A}q(t)$

**Block Diagrams**

Sometimes in the blocks we have amplifiers or attenuators. Many are dynamic processes however, described by ODEs. We shall later describe these by transfer functions

If we describe something like an opamp circuit with a block, we have to be aware that we are implicitly assuming that any current it draws has negligible effect on the preceding block and the following block draws insignificant current from it (close to ideal).

Blocks represent systems, whose inputs and outputs are signals.

If we consider this LC circuit:
![[LCCircuitForBlocks.png]]
This gives the differential equation: $LC\ddot{y}+\frac{L}{R}\dot{y}+y=x$, so that's what goes into the block.

For the control engineer, some blocks are given (fixed) e.g. steam engine dynamics (the plant) while other blocks need to be designed e.g. geometry of fly-ball mechanism (the controller)

A system is linear if superposition holds: $f(u_1)+f(u_2)=f(u_1+u_2)$
This can be written in terms of blocks:
![[Superposition.png]]

We shall also assume that all systems are:
* Causal - output at time T depends only on the input up to time t, where $t \leq T$
* Time-invariant - The response of a particular system doesn't depend on when the input was applied.

If a system can be described by linear differential equations with constant coefficients, then it is necessarily linear.
This is because: $\frac{d}{dt}(u_1(t)+u_2(t))=\frac{du_1}{dt}+\frac{du_2}{dt}$, which is just a superposition of solutions. 
If there are $x^2$ or $\sin(x)$ terms then this doesn't work

**Linearisation**
All real systems are non linear, but we can linearise them for small perturbations from equilibrium, e.g. with small angle approximations.

Suppose a system is described by $\dot{x}=f(x,u)$ where $f$ is a smooth function. Assume equilibrium at $x_0,u_0$, so $f(x_0,u_0)=0$

$x$ is normally the state vector describing the systems configuration, and $u$ is the control input or control vector, and $\dot{x}$ is the rate of change of state

Use a Taylor series expansion:
$\dot{x}_0+\dot{\delta x}=f(x_0+\delta x, u_0+\delta u)=f(x_0,u_0)+\frac{\partial f}{\partial x}\delta x+\frac{\partial f}{\partial y}\delta u+$ higher order terms
Excluding what is zero and neglecting higher order terms, we have a linear ODE:
$$\dot{\delta x}=A\delta x+B\delta u$$
Linearity is desirable, if our system is near equilibrium. In Hi-Fi audio systems non-linearities are called distortion.
If a system is binary then linearity is of no use to us.

**Laplace Transforms**

Definition:
$L{y(t)}=Ly=\bar{y}(s)=\int_{0^-}^{\infty}y(t)e^{-st}dt$
$y(t)=L^{-1}\bar{y}(s)$

The operation of taking a Laplace transform is linear.

If $y(0)=\dot{y}(0)=\ddot{y}(0)=...=0$, then:
$Ly=\bar{y}$, $L\dot{y}=s\bar{y}$, $...$
Differentiation in the time domain corresponds to multiplication by s in the s domain.

Similarly, using the fact that $\bar{y}_n=L\frac{t^n}{n!}$:
Integration in the time domain corresponds to division by s in the s domain.

**Poles and Zeros**
Suppose $G(s)$ is a rational function of s, by which we mean:
$G(s)=\frac{n(s)}{d(s)}$ where both are polynomials in s.

The roots of $n(s)$ are called the zeros of $G(s)$
The roots of $d(s)$ are called the poles of $G(s)$
![[PolesAndZeros.png]]

**Shift in s Theorem**
If $Ly(t)=\bar{y}(s)$ then $Le^{at}y(t)=\bar{y}(s-a)$

**Initial and Final Value Theorems**
Used to quantify the behaviour of a signal as time tends to infinity, from its Laplace transform. This theorem cannot be used for signals that do not tend to a constant value as $t\rightarrow \infty$

If the limits exist:
* $\lim_{t\rightarrow \infty}y(t)=\lim_{s\rightarrow 0}s\bar{y}(s)$
* $\lim_{t\rightarrow 0^+}y(t)=\lim_{s\rightarrow \infty}s\bar{y}(s)$

In the data book!

This is very hard to prove, but can be shown for rational functions of s quite easily, if we put them in the form $\bar{y}(s)=\frac{b_0}{s}+\sum^n_1\frac{b_i}{s+a_i}$

