Asymptotically stable - After a disturbance, returns to equilibrium
Marginally stable - After a disturbance, doesn't return, but doesn't diverge to infinity
Unstable - After a disturbance, diverges to infinity

An LTI system is asymptotically stable is its impulse response satisfies the condition:
$\int_0^{\infty}|g(t)|dt<\infty$
This means that the value of the impulse response must decay to zero

We determine the type of stability by the pole locations
If $R(s)<0$, the system is asymptotically stable
If $R(s)=0$, the system is marginally stable
If $R(s)>0$ or has repeated roots, the system is unstable

The auxiliary equation of the differential equation is the same as the denominator of the rational transfer function.
So you can find poles from the auxiliary equation or the transfer function.

We can break up any rational transfer function into partial fractions of the form:
![[Pasted image 20251021173135.png]]
Which will give an impulse response in the time domain in this form

If we consider individual terms in the form $e^{pt}$, how it contributes to $g(t)$ depends on whether $p$ is real or complex
If $p$ is complex we need to consider $R(\alpha e^{pt})$, as the imaginary part will cancel with is its conjugate, as complex roots always appear in conjugate pairs

Given that $\alpha$ could also be complex, and writing $p=\sigma + j\omega$:
$R(\alpha e^{pt})=R(Ae^{\sigma t}e^{j(\omega t + \phi)})=Ae^{\sigma t}\cos(\omega t + \phi)$
So each pair of complex poles contribute: $2Ae^{\sigma t}\cos(\omega t + \phi)$

Clearly, if $\sigma < 0$, this will converge, being asymptotically stable

This can be related to mechanical systems, with:
* $\sigma = -\omega_n \zeta$
* $\omega =\omega_d = \omega_n \sqrt{1-\zeta^2}$
Therefore the magnitude of the complex number is the natural frequency of the system $\omega_n$, and the angle from the imaginary axis is $\sin^{-1}(\zeta)$
Constant $\zeta$ contours give lines, constant $\omega_n$ contours give concentric circles, constant $\omega_n \zeta$ gives vertical lines. These can define specification regions for mechanical designs 

A complex pair with $R(s)$ closer to the imaginary axis will be a slower response, so will dominate the impulse response

An LTI system is only asymptotically stable if all poles lie in the LHP. This conclusion remains valid if they are repeated poles in the LHP

An LTI system is marginally stable if it is not asymptotically stable, but there nevertheless exists numbers $A,B<\infty$ such that:
$\int_0^T|g(t)|dt<A+BT$ for all T, so the integral is always bounded by a linear function

E.g. If $g(t)=\sum_{k=0}^{\infty}\delta(t-k)\quad \Rightarrow \quad \int_0^{T}|g(t)|dt\leq T+1$

A system is unstable if it is neither asymptotically stable nor marginally stable. Tends to infinity as time tends to infinity

The terms in the transient response are of the same form as those of the impulse response, so finding the poles still characterises the entire type of stability

As Imag(s) increases, the impulse response becomes more oscillatory
