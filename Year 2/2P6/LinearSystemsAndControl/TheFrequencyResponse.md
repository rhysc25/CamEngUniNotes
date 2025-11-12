For an asymptotically stable system:
When we input a sinusoidal signal into an LTI system, the output (after transience has decayed) is a similar sinusoid but with:
1) Magnitude scaled by $|G(j\omega)|$
2) Phase shift by arg $G(j\omega)$

This can be proven by setting the input of a system of differential equations to $u=e^{j\omega t}$ and its output to $y(t)=Ye^{j\omega t}$
Solving for $Y$ gives it to be the same as the transfer function $G(s)$ but with $s$ set to $j\omega$

**Plotting the Frequency Response**
Number of common ways to represent $G(j\omega)$:
* The Bode Plot: Two separate diagrams, one of $|G(j\omega)|$ vs $\omega$, and one of $\angle G(j\omega)$ vs $\omega$. This is good as it is relatively easy to sketch an accurate diagram, and it gives us insight into how gain changes with $\omega$
* The Nyquist Diagram: One single parametric plot, of the real part against the imaginary part of $G(j\omega)$ as $\omega$ varies. Provides a rigorous way to determine the stability of a feedback system.
* The Nichols Diagram (Not assessed): $|G(j\omega)|$ vs $\angle G(j\omega)$ as $\omega$ varies

To determine the frequency response experimentally, we measure input and output steady state sinusoids. You can clearly see the gain and phase shift. With $G(j\omega)$ we can find $G(s)$, which characterises our entire system

**Sketching Bode Diagrams**
Any polynomial can be broken down into quadratic, linear, and constant terms.
Considering a broken down transfer function: $G(s)=\frac{a_1(s)a_2(s)}{b_1(s)b_2(s)}$

Clearly: $\log|G(j\omega)|=\log|a_1(j\omega)|+\log|a_2(j\omega)|-\log|b_1(j\omega)|-\log|b_2(j\omega)|$
and: $\angle G(j\omega)=\angle a_1(j\omega)+\angle a_2(j\omega)-\angle b_1(j\omega)-\angle b_2(j\omega)$

The Bode plot of a complex system is then obtained by adding the gains and phases of the individual terms.
ALWAYS rewrite the transfer function in terms of the standardised terms, so they are all $1+...$

**Plotting Powers of s: $(sT)^k$**
The simplest term in a transfer function is a power of s, written in the form $a(s)=(sT)^k$
$\log|a(j\omega)|=k\log(\omega T)$. This is normally written in terms of dB, so $20\log|a(j\omega)|=20k\log(\omega T)$, so these are straight lines through the origin with slope 20k
$\angle G(j\omega)=90k$, so horizontal lines on the phase plot

**Plotting First Order Terms: (1+sT)**
$|G(j\omega)|=\sqrt{1+\omega^2T^2}$
$\angle G(j\omega)= \arctan(\omega T)$

To draw this, we must consider three regions:
$\omega \rightarrow 0$: Gain = 0, phase = 0
$\omega \rightarrow \infty$: Gain = $20\log\omega-20\log(1/T)$, a straight line with slope 20dB/decade and x axis intercept at $\omega=1/T$
$\omega=1/T$: Gain = $20\log(\sqrt(2))$ = 3dB. Phase = $45\degree$
![[Pasted image 20251031161739.png]]

**Second Order Terms: $(1+2\zeta s T + s^2T^2)$**

$\omega\rightarrow 0$: Gain = 0. Phase = 0
$\omega \rightarrow \infty$: Gain = $40\log(1/T)-40\log\omega$. Phase = -180
$\omega=1/T$: Gain = $20\log (\frac{1}{2\zeta})$. Phase = -90

![[Pasted image 20251031162204.png]]
As $\zeta$ tends to 0, the phase plot tends to asymptotic

Interesting points:
Comparing $(1+j\omega T)$ and $(1-j\omega T)$
$\angle (1-j\omega T)=-\angle (1+j\omega T)$ but the gain is the same. Therefore the contribution to the gain plot is the same, but the contribution to the phase plot is negative now. This is as though it appeared in the denominator instead





