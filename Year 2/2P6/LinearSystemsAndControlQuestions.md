**Signals, Systems and Feedback**

Explain the principle of superposition.

What does causal and time-invariant mean for systems?

How do we linearise a non-linear system? Which systems can't be linearised?

Define a Laplace transform.

What do differentiation and integration correspond to in the s domain?

When do the initial and final value theorems apply?

**Impulse Responses and Step Responses**

How do we find the output to an LTI system in both the time and s domain?

Describe the sifting theorem.

Why can we put the limits of 0 and t onto the convolutional integral?

How can we transform positive feedback to negative feedback in our block diagrams?

Describe a quick way of finding the total transfer function for a negative feedback loop.

**Stability and Pole Location**

Explain the definition of asymptotic stability in term of the integral of the impulse response from 0 to infinity.

Why do we only need to consider the real part of the complex s when determining stability?

Therefore if each root contributes $R(Ae^{\sigma t}e^{j(\omega t + \phi)})$, what is that in sinusoidal terms, and what is the requirement on $\sigma$ for asymptotic stability?

What are $\sigma$ and $\omega$ equal to in mechanical systems?

What is the magnitude of the complex number equal to?

What is the angle from the imaginary axis equal to?

Why do complex pairs closer to the imaginary axis dominate the impulse response?

What defined marginal stability, considering the integral of the impulse response from 0 to infinity?

What happens to the impulse response as Imag(s) increases?

Why are the terms in the transient response of the same form as those of the impulse response?

**The Frequency Response**

What happens to a sinusoidal signal after being passed through an LTI system?

Explain the axes of both Bode plots and the Nyquist diagram.

If we have a transfer function: $G(s)=\frac{a_1(s)a_2(s)}{b_1(s)b_2(s)}$, how can we split  $\log|G(j\omega)|$ and $\angle G(j\omega)$ into components?

What three main values of $\omega$ do we have to consider when we want to draw the Bode plots of transfer functions?

Compare $(1+j\omega T)$ and $(1-j\omega T)$ in terms of their contributions to the gain plot and the phase plot.

When you hit a pole going from left to right on a Bode plot, what happens to the gain gradient, and what happens to the phase?

How do you find the centre of two points on a log scale?

**Feedback Control Systems**

Why do all inputs to a feedback system have the same expression in the denominator of their transfer functions?

What is the relationship between the sensitivity and the complementary sensitivity?

How do we easily find the final value of the step response using the transfer function?

How do we find the steady state error?

What is good about PD control?

How does integral control remove steady state error?

What is the requirement for stability when considering the Nyquist diagram of the return ratio?

How do we draw the Nyquist diagram, and what must we do if $G(j0)\rightarrow \infty$ to understand where we actually come from?

Explain what would happen sinusoidally if our return ratio was equal to -1.

How do we find the gain and phase margin both from the Nyquist diagram and the Bode plots of the return ratio?

Given a Nyquist diagram of $L(s)=kG(s)$, what point must we consider instead of -1?

The sensitivity needs to be less than 1 up to $\omega_1$. How do we find this point on our Nyquist diagram of the return ratio?

How do we find the point where the magnitude of the complementary sensitivity is 1?

How do we close all curves on the Nyquist diagram?

What is the formal Nyquist stability criterion in terms of clockwise and anticlockwise encirclements?

What are the three main things we want for our return ratio at different frequencies?

How does a phase lag compensator contribute to the Bode plots, what are the advantages and disadvantages?

How does a phase lead compensator contribute to the Bode plots, what are the advantages and disadvantages?