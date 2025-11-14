If we have a controller K and a plant G, we could try making an arbitrary transfer function by setting $K=F/G$. However this would never work in practice as the knowledge of the transfer function of G is only approximate, and also the effect of disturbances would never allow it to be accurate.
Therefore we need feedback

![[Pasted image 20251107112045.png]]

We know have that $\bar{y}=\frac{GK}{1+HGK}\bar{r}+\frac{1}{1+HGK}\bar{d}_0+\frac{G}{1+HGK}\bar{d}_i$
The term $1+HGK$ appears as the denominator of all the closed-loop transfer functions. Therefore it determines the poles and hence the stability of the system

We call $L(s)=HGK$, where L is the return ratio of the loop or the loop transfer function.
The closed loop characteristic equation is $1+L(s)=0$

If a feedback system has input $r(t)$ and disturbance $d_0(t)$ then we can say that:
$\bar{y}(s)=T(s)\bar{r}(s)+S(s)\bar{d}_0(s)$
Where T(s) is the complementary sensitivity and S(s) is the sensitivity
$S(s)+T(s)=1$ always

**The Final Value Theorem**

Let $y(t)$ be the step response of the system.
As dividing my s in the Laplace domain is equivalent to integrating: $\bar{y}=\frac{G(s)}{s}$

From this we can see that the final value of the step response = transfer function evaluated at $s=0$. This final value is the steady state gain or DC gain
$\lim_{s\rightarrow 0}=G(0)$

The steady state response of the system to a step input that is equal to U is a constant G(0)U
The steady state response to a sinusoidal input is $|G(j\omega)|\cos(\omega t + \arg G(j\omega))$
We can see these are equivalent is $\omega =0$

We can see that the error signal a feedback system is given by $\bar{e}=\frac{1}{1+L(s)}\bar{r}$
If $r(t)=H(t)$ then, using the final value theorem, the steady state error is $\frac{1}{1+L(0)}$

**Control Policies**
**Proportional Control**
$K(s)=k_p$. This increased $L(0)$ so reduces steady state error. However it also means more aggressive control so damping is reduced, and there is a possibility for loss of closed-loop stability
$\omega_n=\sqrt{1+k_p} \qquad \zeta=\frac{1}{\sqrt{1+k_p}}$
As $k_p$ increases, more oscillatory output
Steady state error: $\frac{1}{1+k_p}$

To increase damping - use derivate action or velocity feedback
To remove steady state errors - use integral action

**Proportional + Derivative (PD) Control**
$K(s)=k_p+k_ds$
Increased damping, but greater sensitivity to noise
$\omega_n=\sqrt{1+k_p} \qquad \zeta=\frac{2+k_d}{2\sqrt{1+k_p}}$

**Proportional + Integral (PI) Control**
Steady state error is $\frac{1}{1+G(0)K(0)}$
Therefore to remove steady steady state error, we need $K(0)=\infty$
Therefore $K(s)=k_p+\frac{k_i}{s}$
The integral of the error signal will only ever remain stable if the error signal converges to zero. The only equilibrium possible is one where $\lim_{t\rightarrow \infty} e(t) =0$
Provided the closed loop system is asymptotically stable

**Proportional + Integral + Derivative (PID) Control**
Combines the advantages of both derivative and integral action
$1+G(s)(k_p+\frac{k_i}{s}+k_ds)$
There are many empirical rules for tuning PID controllers (Ziegler-Nichols for example)


