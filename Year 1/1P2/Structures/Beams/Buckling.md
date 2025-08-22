# Buckling

We must analyse the equilibrium in the deformed shape, or else there will never be deformation.

Considering equilibrium of a buckled beam: $Pv(x)=M(x)$. Considering material law: $M(x)=EI\Delta \kappa (x)$. Considering geometry: $\kappa (x) =-\frac{d^2 v}{dx^2}$.

Combining gives the governing differential equation: $\frac{EI}{P}\frac{d^2v}{dx^2}+v=0$.

The lowest critical value of P for a pin-jointed column, $P_E=\frac{\pi^2EI}{L^2}$. Or if we consider $n\pi$ as the solution:

$P=\frac{n^2\pi^2EI}{L^2}$, giving the different modes of buckling.

$v=A\sin(\frac{\pi x}{L})$

$[EI-\frac{PL^2}{\pi^2}]v=0$. $[EI-\frac{PL^2}{\pi^2}]$ is the effective stiffness. Buckling occurs when the effective stiffness decreases to zero.

Next we consider a column with both ends fixed. The governing differential equation is given by:

$\frac{EI}{P}\frac{d^2v}{dx^2}+v=\frac{M_0}{P}$, where $M_0$ is the moment at each end, which will be the same.

If instead we consider the effective length of the buckled beam, the distance between the points of inflection, we essentially get an example of pin joint buckling, but with half the length.

We sub this into $P=\frac{\pi^2EI}{L_e^2}$, where $L_e$ is the effective length.

The ideal, optimistic value of effective length is $0.5L$, however realistically we will use $0.7L$.

The critical stress: $\sigma_E=\frac{\pi^2E}{L^2}\frac{I}{A}$.

Radius of gyration, $r=\sqrt{\frac{I}{A}}$.

Therefore $\sigma_E=\frac{\pi^2E}{(L/r)^2}$, inversely proportional to the slenderness squared.

If there was initial curvature in the column, for example $v_0=\delta_0\sin(\frac{\pi x}{L})$

This means that $\Delta \kappa =\kappa - \kappa_0 = -(\frac{d^2v}{dx^2}-\frac{d^2}{dx^2}(\delta_0\sin(\frac{\pi x}{L})))$, so $\delta \kappa = -\frac{d^2(v-v_0)}{dx^2}$ and the governing differential equation has the form:

$\frac{EI}{P}\frac{d^2v}{dx^2}+v=-(\frac{P_E}{P})\delta_0 \sin(\frac{\pi x}{L})$

Solve this.

This will give that $v=\frac{\delta_0}{1-(\frac{P}{P_E})}\sin(\frac{\pi x}{L})$

The central deflection is given by $\frac{\delta_0}{1-(\frac{P}{P_E})}$, where $\delta_0$ is the initial deflection.

Perry's law considers a buckling column, and says that the column can be said to have failed if any part has exceeded its yield stress.

This will first occur in the midpoint, the most deflected part.

To find the stress, we must add the compressive stress and the stress from the moment
$\sigma_{max}=\frac{P}{A}+\frac{P\delta y_{max}}{Ar^2}$

$$\sigma_{max}=\sigma_y=\sigma_{crit}(1+\frac{\delta y_{max}}{r^2})$$

Where $\sigma_{crit}$ is the stress in the centroid, the average stress, and r is the radius of gyration.

A bit of rearrangement gives that: $(\sigma_y-\sigma_{cr})(\sigma_E-\sigma_{cr})=\frac{\delta_0 y_{max}}{r^2}\sigma_{cr}\sigma_E$
