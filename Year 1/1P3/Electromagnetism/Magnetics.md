# Electromagnetics - Magnetics

If $\textbf{B}$ is not perpendicular to the area, we must take the component of $\textbf{B}$ perpendicular. $\phi = \sum\textbf{B}\cdot \textbf{dS}$

For a current carrying wire, use the right hand rule for the direction of $\textbf{B}$.

Biot-Savart law: A short element of wire of length $\textbf{dl}$ carrying a current I produces a magnetic flux density $\textbf{dB}$ at position described by a vector $\textbf{r}$. $\textbf{dB}=\frac{\mu_0 I \textbf{dl}\times \textbf{r}}{4 \pi r^3}$.

We can integrate over many tiny segments to give: $B=\frac{\mu_0I}{2\pi r}$

Circulation of B = B X Path length of a 360° closed loop

Ampere's law: The circulation of \textbf{B} around any closed path C is $\mu_0I$.

This is $\mu_0IN$ for a winding, where N is the number of turns around the mean path that B takes.

When calculating the circulation of \textbf{B}, we consider only the component of \textbf{B} that is parallel to the closed path.

Using a small angle approximation, we can say that $Bdl\cos(\alpha)=Brd\theta$. Then we can integrate from 0 to $\theta = 2\pi$

Faraday's law: The emf is proportional to the rate of change of magnetic flux linking the circuit. Remember that the emf generated is in opposition to the change in flux (Lenz's law). $v=\frac{d\phi'}{dt}$.

Self inductance, $L=\frac{\phi'}{I}$. Combining: $V=L\frac{dI}{dt}$

4 steps to success for finding the self inductance of a system:
Specify a current I on a conductor. Using Ampere's law, find a general expression for the magnetic flux density produced by said current. Calculate the total flux, $\phi=BA$, by integrating B over radii r, considering strips $dr$ and an appropriate expression for thickness. Find self-inductance, $L=\frac{\phi'}{I}$.

When two electrical circuits are close to each other, a current $I_1$ in one may cause magnetic flux $\phi_2$ to link the other. $\phi_2=MI_1$, where $M$ is the mutual inductance between the circuits.

When currents are established in an electrical circuit, there is an increase in B and $\phi$. An increase in $\phi$ means an opposite emf is induced. The voltage source must do work against the induced emf. Electrical energy is stored in the flux.

The flux linking a circuit is the sum of its own flux from self inductance, plus the flux generated from the mutual inductance.
$\phi_1=L_1I_1+MI_2$

Total power of two interacting circuits: $\frac{dW}{dt}=P=I_1V_1+I_2V_2=I_1(\frac{d}{dt}(L_1I_1+MI_2))+I_2(\frac{d}{dt}(L_2I_2+MI_1))$

This becomes: $W=\frac{1}{2}L_1I_1^2+\frac{1}{2}L_2I_2^2+MI_1I_2$

$F=I_1I_2\frac{\delta M}{\delta x}$

When an AC current in a wire is changing at a very high frequency, strong opposing emfs are induced in the centre of the wire, causing opposing eddy currents. The resultant effect is that the current will tend to flow near the surface of the wire. This is called the skin effect. The skin depth, $\delta$, increases as frequency increases.

$\delta=\frac{1}{\sqrt{\pi\mu_0\sigma f}}=\frac{\sqrt{\rho}}{\sqrt{\pi\mu_0 f}}$

$R\approx \rho \frac{l}{2\pi r \delta}$

If we want to increase the magnetic flux density, B, generated, we cannot just increase current as that causes resistive heating in the wires, and we cannot just increase the turns, as this will increase resistance.

Fill the coil with a magnetic material. The coil generated a magnetic flux density $B_I$, and this in turn aligns the atomic magnets in the magnetic material. This creates atomic current loops, $I_m$, which generate an extra mag flux density $B_m$.

Therefore, the total $B=B_I=B_m$

Ampere's law: $Bl=\mu_0NI+\mu_oI_m=\mu_0NI+\mu_o\chi_mNI$, as we expect $I_m$ to be proportional to $NI$.

$1+\chi_m=\mu_r \Rightarrow Bl=\mu_0\mu_rNI$

We now define the magnetic field intensity, \textbf{H}. Units: $Am^{-1}$

$\textbf{B}=\mu_0\mu_r\textbf{H}$

$\sum \textbf{H}dl=NI$. $NI$ is often called the magnetomotive force, of mmf.

Mag flux density lines always form closed loops, there must be a north and south pole.

If flux travels from a magnetic material into another material without significant divergence, then the flux will be conserved.

$\phi_1=\phi_2 \Rightarrow B_1A_1=B_2A_2 \Rightarrow B_2=\frac{B_1A_1}{A_2}$.

This is true even if we leave an air gap, ignoring fringing magnetic fields.

We can assume that a high $\mu_r$ material channels flux density, effectively containing it. If at a T junction, they divide.

The first step to every question is to apply Ampere's law.

If air gap, sum contributions to Ampere's law. $H_ml_m+H_gl_g=NI$

$B=\mu_0\mu_rH$ is only valid if the material is linear.

![Non-linear magnetic materials](Non-linear%20magnetic%20materials.png)

The initial region is approximately linear, then it plateaus as there are no more domains to align.

This is only for the initial magnetisation of the material, as domains don't easily unalign.

![Hysteresis](Hysteresis.png)

The hysteresis shows that there is an energetic loss, as it takes energy to line up domains. When $I=0$, there is remnant flux $B_r$. When $B=0$, the measured $H$ is called coercivity.

Saturates again at negative current.

As $B$ varies non-linearly, we need to get an expression for $B$ in terms of $H$, and plot this line like a load line on the graph and find their intersection.

Permanent magnets: Produce a magnetic flux even after any magnetising currents have been removed, the maximum flux corresponding to the point $r$ on the hysteresis curve.

Permanent magnetic materials are expensive, so used in conjunction with soft iron usually.

![Permanently Magnetic Materials](Permanently%20Magnetic%20Materials.png)

As there are no electrical currents, $NI=0$

$H_ml_m+H_il_i+H_gl_g=0$. Assume that the iron and air gap behave linearly. Assume that there is no flux leakage.

This permanent magnet operates in the demagnetisation section, the second quadrant.

Work must be done to create a magnetic field. As $I$ gradually increases, then their is a positive change in $\phi$, so an opposing emf. This energy is stored in the coil and the core.

The total change in energy per unit volume. $\frac{\delta W}{AL}=H\delta B$

$\frac{W}{AL}\int_0^B HdB=$ the area under the H-B curve, which is the area between the $y$ axis and the curve for a B-H curve.

As we can see, the area under the curve when demagnetising is less than the area under the curve when magnetising, so the energy released is less than that input. The area inside the B-H loop = loss.

If we consider the force required to just crack a linear magnetic material, remove the pole piece or keeper:

$\frac{W}{A\delta x}=\frac{B_g^2}{2\mu_0}$. As there are two air gaps we double this.

$\frac{F}{A}=\frac{B_m^2}{\mu_0}$. This can be very large. We assume that at the instant we are removing the pole piece, the flux remains constant, so no induced emf to consider.

For a non-linear material, we just need to find the operating point, then complete the analysis as before. It is likely to be very close to the y-intercept of the hysteresis loop.

In practice, flux leakage would reduce the force per unit area need to remove the pole piece.
