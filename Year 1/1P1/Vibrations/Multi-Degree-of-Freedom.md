If we have 2 masses, we get 2 simultaneous equations

These can be rearranged into 1 matrix equation, always in the form $[m]\ddot{\textbf{y}}+[k]\textbf{y}=\textbf{f}$

It is in this form, no matter the degrees of freedom

We can solve any equation of this form by assuming harmonic motion, where 
$$y = \begin{bmatrix}
Y_1 e^{i\omega t}\\
Y_2 e^{i\omega t}\\
\end{bmatrix}$$
This will give two solutions for $Y_1/Y_2$, so equate them to find the two natural frequencies, $\omega_1$ and $\omega_2$
Then plug these back in, to give the mode shapes, $Y_1/Y_2$

For a symmetric mass problem with 2 masses and 3 springs, the modes $Y_1/Y_2$ come out to 1 and -1, with the masses moving together, or in opposite direction

Any nodal point in a spring can be modelled by a fixed wall, and any spring that isn't extending can be removed to simplify the model

The equation of motion has the form $[m]\ddot{y}+[k]y=0$
Putting $y=Ye^{i\omega t}$ as vectors of course, gives:
$$(-\omega^2[m]+[k])Y=0$$
The determinant must be equal to zero, giving the eigenvalues as $\omega_i^2$
As well as this, the eigenvectors give the mode shapes. These eigenvectors have arbitrary size, all you are considering is the ratio of $Y_1$ to $Y_2$

The eigenvectors are independent/ orthogonal so any motion of the system can be expressed as a linear combination of the eigenvectors

If $\omega_j=0$ then the eigenvector corresponds to a rigid body mode. If the system is given a displacement in the eigenvector it will not vibrate

## Undamped Free Vibration

The total complementary function can be written as a combination of vibration in the normal modes
$\textbf{y}=Y^{(1)}(A_1 \cos(\omega_1 t)+B_1 \sin(\omega_1 t))+Y^{(2)}(A_1 \cos(\omega_2 t)+B_1 \sin(\omega_2 t))$

Use the initial conditions to determine the four constants

## Harmonic Excitation

If we have forces acting on the system:  $[m]\ddot{\textbf{y}}+[k]\textbf{y}=\textbf{f}$
So $(-\omega^2[m]+[k])Y=DY=F$
Therefore, $Y=D^{-1}F$

Solving this gives the frequency response functions

The determinant of the dynamic stiffness matrix will always appear in the form $$constant \times (1-\omega^2/\omega_1^2)(1-\omega^2/\omega_2^1)$$So we can find the mode frequencies from the determinant 

The dynamic vibration absorber or tuned mass damper, is a mass which can be added to the system

![[Pasted image 20250521115005.png]]

This turns the frequency response of the system into this form: $\frac{Y}{F/k}=\frac{(1-\omega^2/\omega_a^2)}{(1-\omega^2/\omega_1^2)(1-\omega^2/\omega_2^2)}$

As we can see, when $\omega \approx \omega_a$ then the response goes to zero, neutralising the vibration, as the effective stiffness goes to infinity
We can tune $\omega_a$ to be close to $\omega_n$ for the system, reducing the rise of resonance in a specific frequency range

In practice, the presence of damping means a wider bandwidth of operation, but at the expense of worse performance at $\omega_n$

