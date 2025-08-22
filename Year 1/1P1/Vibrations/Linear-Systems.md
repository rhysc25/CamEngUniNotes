# Linear Systems

$$\ddot{y}=\frac{dv}{dt}=v\frac{dv}{dy}$$

## Mechanical Components

### For Translational Motion
Components that store, dissipate and transmit energy respectively:

- **Mass**: $F=m\ddot{y}$
- **Damper/Dashpot**: $F=\lambda \dot{y}$ (No energy stored, just dissipated. Power $=Fv=\lambda \dot{y}^2$)
- **Spring**: $F=ky$

### For Rotational Motion
- **Inertia**: $T=J\ddot{\theta}$
- **Torsional Damper**: $T=\lambda \dot{\theta}$
- **Torsional Spring**: $T=k\theta$

There are analogous elements for electrical systems, if we consider $F\equiv e$, where $e$ is the electromotive force, and the degree of freedom is charge, where $y \equiv Q$.

## Analysis of Mechanical Systems

When considering mechanical systems, we have to consider:
- Compatibility of displacements (e.g., extension of spring = distance travelled by mass)
- Equilibrium of forces (using D'Alembert)

The spring and dashpot are both massless, so have no $ma$ component.

Many systems have the same form of differential equation: $T\dot{y}+y=x$

## Response Curves and Inputs

On exponential curves, add an initial tangent with its x intercept, to scale the x axis.

There are 4 main inputs:
1. Step
2. Impulse
3. Ramp
4. Harmonic

### Step Response
To determine the step response, solve $T\dot{y}+y=x_0$ where $x_0$ is the scaled step function.

### Impulse Response
For a linear system, if the response to $x(t)$ is $y(t)$, then the response to $\dot{x}(t)$ is $\dot{y}(t)$.

Therefore, the derivative of the step response is the impulse response.

### Ramp Response
The ramp response is where the input function is $\alpha t$.

The ramp response is the integral of the step response.

### Sinusoidal Input
For a sinusoidal input, you can either:
- Use a sinusoidal particular integral (not recommended)
- Or use the form: $x=\Re(Xe^{i\omega t})$ and $y=\Re(Ye^{i\omega t})$, where both X and Y are complex numbers

X has angle $\phi_x$ and Y has angle $\phi_y$.

x, y, $\dot{y}$ etc. can be plotted on a phasor diagram - essentially an Argand diagram with arrows showing magnitude and direction.

## Second Order Systems

Considering a basic second order system with mass which stores kinetic energy:

$$m\ddot{y}+\lambda \dot{y}+ky=F$$

If you multiply everything by $\dot{y}$, it is essentially a power balance equation.

Defining the natural frequency $\omega_n=\sqrt{\frac{k}{m}}$ and the damping ratio $\zeta =\frac{\lambda}{2\sqrt{\frac{k}{m}}}$, we obtain:

$$\frac{\ddot{y}}{\omega_n^2}+\frac{2\zeta}{\omega_n}\dot{y}+y=\frac{F}{k}=x$$

Solving this, we get:
$$\alpha = -\zeta \omega_n \pm \omega_n \sqrt{\zeta^2-1}$$

### Damping Types

- If $\zeta > 1$, $\alpha_{1,2}=$ real. This is **over damping**.
- If $\zeta = 1$, $\alpha_{1,2}=$ repeated real. $\alpha_1=\alpha_2=-\omega_n$ This is **critical damping**, the fastest route to equilibrium position.
- If $\zeta < 1$, $\alpha_{1,2}=$ complex. This is **lightly damped**. $\alpha = -\zeta \omega_n \pm i \omega_n \sqrt{1-\zeta^2}$

We define $\omega_d=\omega_n\sqrt{1-\zeta^2}$, the damped natural frequency.

The complementary function can be written as:
$$y_{CF}=De^{-\zeta \omega_n t}\cos(\omega_dt-\psi)$$

### Step Function Response

For a step function:
$$y=y_{PI}+y_{CF}=x_0+y_{CF}$$

$$y=x_0[1-\frac{e^{-\zeta \omega_n t}\cos(\omega_dt-\psi)}{\cos(\psi)}] \approx x_0[1-e^{-\zeta \omega_n t}\cos(\omega_nt)]$$ (In data book)

The dynamic amplification factor is at most 2. Mass overshoots equilibrium position.

### Impulse Response

To find the impulse response, we differentiate the step response, giving:
$$g(t)=\frac{\beta\omega_n}{\sqrt{1-\zeta^2}}e^{-\zeta \omega_n t}\sin(\omega_d t)$$ when worked through.

## Logarithmic Decrement

$$D=\ln(\frac{y_1}{y_2})$$

At peaks:
$$\frac{y_1}{y_2}=\frac{e^{-\zeta \omega_n T}}{e^{-\zeta \omega_n (t+T)}}=e^{\zeta \omega_n T}$$

Therefore:
$$D=\frac{2 \pi \zeta}{\sqrt{1-\zeta^2}} \approx 2\pi \zeta$$ for small $\zeta$.

For multiple decrements:
$$D_N=\ln(\frac{y_1}{y_{1+N}})=2\pi N\zeta$$ for N cycles.

## Applications

### Simple Pendulum
Where all mass is concentrated in the bob. If we resolve tangentially with D'Alembert we get:
$$mL\ddot{\theta}+mg\sin(\theta)=0$$

$$\omega_n=\sqrt{\frac{g}{L}}$$

### Trifilar Pendulum
A trifilar pendulum exhibits torsional oscillations. The natural frequency is derived by considering energy.

We get that:
$$\omega_n=\frac{r}{k}\sqrt{\frac{g}{L}}$$

If a gravity force acts initially on our system, or any static force for that matter, then the input f becomes $f + mg$, however this can be countered by replacing y with $y - mg/k$. This measures y from the static equilibrium position $mg/k$

Case (a) is when the base is stationary.
The damped natural frequency is the frequency at which the system vibrates when unforced.

The damped resonance frequency is the frequency at which the response amplitude peaks, found by differentiating the response $Y/X$.

The Q-factor is $|\frac{Y}{X}|_{MAX}$

At low values of $\omega$, $\omega << \omega_n$, there are low inertia forces.
At high values of $\omega$, $\omega >> \omega_n$, there are high inertia forces, and the response $\propto \frac{1}{\omega^2}$

The transient response (complementary function) has to decay before the response is purely sinusoidal (particular integral)

For case (b) where we consider relative motion to the base, the input is given as the negative of the acceleration of the base.

If we have excitation by an out of balance rotor, find an expression for the force at a given time using inertia forces.

If we plot $|\frac{Y}{X}|$ against $\omega$ we get a bell shape. If we consider the points $\omega_1$ and $\omega_2$ where $|\frac{Y}{X}| = \frac{1}{\sqrt{2}} |\frac{Y}{X}|_{MAX}$, the bandwidth $\Delta \omega= \omega_2 - \omega_1$

$\frac{\Delta \omega}{\omega_n}=2\zeta$

The transmissibility, $T(\omega) = Y / X$

For maximum vibration isolation we want the lowest damping, but this is very risky if the frequency approaches the resonance frequency

The vibrating system imparts a force on the ground. This force is minimised when the transmissibility is minimised

Seismic transducers and geophones are both case B devices, measuring displacement and velocity respectively
The accelerometer is a case A device, as we can consider $|\frac{Z}{A/\omega_n^2}|$


 

