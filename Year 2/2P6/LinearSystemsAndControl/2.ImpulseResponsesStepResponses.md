
Given the input to an LTI (Linear, Time Invariant and causal) system, the output can be determined:
* In the time domain: as the convolution of the impulse response and the input
* In the Laplace domain: as the multiplication of the transfer function and the Laplace transform of the input

The transfer function is the Laplace transform of the impulse response
If $u$ is the input, $G$ is the transfer function and $y$ is the output, then:
$\bar{y}(s)=G(s)\bar{u}(s)$
and:
$y(t)=\int_0^t u(t)g(t-\tau)d\tau$

**Impulse Function**
The impulse function is the limit of a square or triangular pulse with area of 1.
As width $\rightarrow 0$, the function becomes $\delta (t-T)$

The unit impulse is defined as any "function"/ distribution $\delta(t)$ which has the property:
$\int_{-\infty}^{\infty}f(t)\delta(t-T)dt=f(T)$
This is the sifting theorem.

Using the sifting theorem, the Laplace transform of the delta function = 1.

Convolution integral: The response to the input $u(t)$ is given by:
$y(t)=\int_{-\infty}^{\infty}u(\tau)g(t-\tau)d\tau$
Using the fact that $u(\tau)=0$ for $\tau<0$, we can equivalently say:
$y(t)=\int_{-\infty}^{\infty}u(t-\tau)g(\tau)d\tau$
Also due to this reason, and because of causality, we can write it as: 
$y(t)=\int_{0}^{t}u(\tau)g(t-\tau)d\tau$

**The Transfer Function**

As an alternative to convolution, the response of a linear system to arbitrary inputs can be determined using Laplace transforms.

If we Laplace transform an ODE, we get a result such as:
$\bar{y}(s)=\frac{as+b}{s^2+\alpha s+\beta} \bar{u}(s)$.
$\frac{as+b}{s^2+\alpha s+\beta}$ is the transfer function here

A Laplace transform turns a convolution into a multiplication:
$L\{\int_0^t f(\tau)g(t-\tau)d\tau\}=L\{f(t)\}L\{g(t)\}$
It follows that for all LTI systems:
![[Pasted image 20251010134142.png]]

The transfer function is usually most easily calculated directly from the system's differential equations, using Laplace transforms.

If a system has more than one input, the transfer function from a particular input to a particular output is defined as the Laplace transform of that output when an impulse is applied to the given input, all other inputs are zero and all initial conditions are zero.
$\bar{y}(s)=G(s)\bar{u}(s)$ + other terms independent of $u$.

Once in this form: $\bar{y}(s)=G(s)\bar{u}(s)$, we can set $u(s)$ as anything such as the impulse or step function, to get the impulse and step response easily.

**Proof: Step response is integral of impulse response**
$y(t)=\int_{0^-}^{t}g(\tau)H(t-\tau)d\tau=\int_{0^-}^{t}g(\tau)d\tau$
Therefore, the step response is the integral of the impulse response

Mathematically there is no distinction between a transform of a signal and its transfer function. However they are for different things. One for signals, and one for systems respectively. Signals and systems are obviously different.

**Interconnections of LTI systems**

![[Pasted image 20251011121933.png]]

In this case, $\bar{v}(s)=F(s)\bar{x}(s)+G(s)\bar{y}(s)$, and $\bar{z}(s)=H(s)\bar{v}(s)$
So, combing these, we can say that:

$\bar{z}(s)=H(s)F(s)\bar{x}(s)+H(s)G(s)\bar{y}(s)$
Where $H(s)F(s)$ is the transfer function from $\bar{x}(s)$ to $\bar{z}(s)$

These can become simultaneous equations

Recognising that blocks represent multiplications, we can now simplify block diagrams very easily
![[Pasted image 20251011123633.png]]
And so on

The additive feedback can be negative by flipping the sign and introducing a gain/ transfer function of -1.

The right combination was found through simultaneous equations, an example of which is here:
![[Pasted image 20251011123718.png]]

A spring damper system, an RC network, and a water heater all end up having the same transfer function

Water heater:
![[Pasted image 20251011124158.png]]

Assume perfect mixing so all water in the tank is at the same temperature $\theta_0$

$\dot{Q}=Mc\dot{\theta}_0+\dot{m}c(\theta_0-\theta_i)$
The input energy is heating both the water present and the incoming water
This gives that:
$\bar{\theta}_0=\frac{1}{\dot{m}c}\frac{1}{Ts+1}\bar{q}(s)+\frac{1}{Ts+1}\bar{\theta}_i(s)$, where $T=\frac{M}{\dot{m}}$

A transfer function of $\frac{1}{Ts+1}$ is common to all 3


