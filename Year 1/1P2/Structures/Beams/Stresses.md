# Stresses

Because strain is uniform, we can assume stress to be uniform along a beam.

Plane sections in a beam remain plane when subjected to bending.

In all bent beams there will be a neutral axis, a bent line on which there is no strain, so no extension.

Sections rotate, they don't shear, when bending is applied.

For a beam subjected to pure bending, the strain in a fibre is proportional to the curvature and to the distance from the neutral axis.
$$\epsilon = \frac{y}{R}=\kappa y$$

$\sigma = E \kappa y$

First moment of area = $\int y dA = \int bydy$

Second moment of area = $\int y^2 dA = \int by^2dy$

The second moment of area of a rectangular cross section $=\frac{bd^3}{12}$

$M=EI\kappa$

$\sigma = \frac{M}{I}y$

First moment of area = $\int y dA = 0$ defines the centroid of the object, essentially the centre of mass of the lamina.

To find the centroid: $\bar{Y}=\frac{1}{A}\int Yda$

When find the second moment of area, $I$, integrate above and below the centroid, to $y_{max}$ and $y_{min}$. The major axis refers to $I_{xx}$

Parallel axis theorem: $I_{about given axis}=I_{about parallel axis through centroid} + Ad^2$

This is what we will be using mostly.

Any object with the same distribution of mass with respect to an axis, eg. a hollow rectangle vs. an I-beam, will have an identical $I_{xx}$

We know that $\sigma = \frac{M}{I}y$. We now define the elastic section modulus, $Z= \frac{I}{|y_{max}|}$

Combining bending moment and axial force:
$\sigma =\frac{T}{A}+\frac{My}{I}$

This can be found nicely by superposing the tension stress graph with the moment stress graph.

Bending stresses in composite beams:

$\sigma_s=E_s\kappa y$, $\sigma_w=E_w\kappa y$, where $E_S/E_W\approx25$. Because of this, there is a jump in the stress diagram, as the material shifts.

![Stresses in composite beams](Stresses%20in%20composite%20beams.png)

To find the corresponding bending moment, $M=\int \sigma ydA$, which will have to be completed in two parts.

Alternatively, we can transform the section of the beam: For example if it was wood and steel, we could imagine the wood as an equivalent piece of steel, 25 times thinner. We would have to calculate the second moment of area about the neutral axis again.

The bending stiffness of the transformed sections are equal to the bending stiffness of the original composite section. Under a bending moment, the calculated curvatures and strains will be correct.

However, the stresses from bending, calculated by $\frac{My}{I_s}$, in the thin steel will be $\approx$ 25 times too high, as they appear to act on 25 times less area.

Considering reinforced concrete: Concrete needs to be reinforced with steel as concrete is terrible in tension.

The modular ratio: $m = \frac{E_s}{E_c}$

![Reinforced concrete](Reinforced%20concrete.png)

The concrete in tension is ignored as it can take essentially zero stress. The steel is transformed to concrete using the modular ratio.

We find the neutral axis by finding the centre of mass, then find the second moment of area using the parallel axis theorem.

Strain ratio = $|\frac{\epsilon_s}{\epsilon_c}|=\frac{1-\alpha}{\alpha}$. $|\frac{\sigma_s}{\sigma_c}|=\frac{E_s}{E_c}|\frac{\epsilon_s}{\epsilon_c}|$

Dividing shear force by the area will give you the average shear stress. However, shear stresses on the face are not uniform.

Principle of Complementary Shear: If $\tau$ acts on a plane, at a point in a stressed body, then $\tau$ acts also on the orthogonal plane.

The shear force per unit length, $q=\frac{S}{I}\int ydA$

$\int y dA=A_c\bar{y} \Rightarrow q=\frac{S}{I}A_c\bar{y}$, where $A_c$ is the area of the cut section, and $\bar{y}$ is the mean y coordinate from the neutral axis of the cut section, together forming the first moment of area of the cut section.

The actual shear stress, $\tau = \frac{q}{b}=\frac{SA_c\bar{y}}{Ib}$

This comes out to be a parabola, with 0 shear stress at the edges, and mix shear stress in the centre of the beam.

If we cut in two places then we have to remember that the length of the cut is $2t$.

For an I-beam, essentially all of the shear force acts in the web, and it is roughly constant, so we can say:

For an I-beam: $\tau \approx \frac{S}{A_{web}}$

There is zero shear stress at a free surface.

The largest shear stress is in the middle of an I-beam.
