# Deflection

For a hanging cable: Find the reaction forces at the ends of the cable, and the tension in the bit of the cable that is horizontal. Then take moments at a generic point, $x$ across and $y$ up.

$e=\frac{T L}{A E}$

Total strain = Elastic + Thermal strain. $\epsilon_T=\frac{T}{AE}+\alpha \Delta \theta$

For displacement diagrams, find a point which doesn't move, or two points which don't move relative to each other. Draw to the known displacements in the given direction away from that point, then draw perpendicular guide lines. Where two guide lines meet is where that point ends up.

Virtual work: $$\sum_i \textbf{F}\mbox{*}\cdot \textbf{d} = \sum_j T\mbox{*} \cdot e$$ or
 $$\sum_i \textbf{F}\cdot \textbf{d}\mbox{*} = \sum_j T \cdot e\mbox{*}$$
depending on whether the force or the extension is virtual.

To find a displacement:
* With the real force acting on the structure, determine all the axial forces in the beams, and hence their extensions
* Remove all external forces, and add a virtual force of magnitude $1$ in the position and direction of the displacement you want to find
* Determine all the axial forces, $T\mbox{*}$
* Determine the sum of $T\mbox{*}e$
* This is equal to $\sum \textbf{F}\mbox{*}d$, but as $\sum \textbf{F}\mbox{*}=1$, it is equal to the displacement of that point (negative if in the opposite direction to the virtual force)

![Virtual Forces](Virtual%20Forces.png)

Determining axial forces from virtual displacements:
Create a virtual extension in the member you want to find the force in, then use similar triangles to determine the displacement of the points where forces act.

Structural optimisation:
To determine which beam needs to be made larger to reduce the displacement in a certain node, partially differentiate the expression for the displacement for virtual work, in terms of the volume of the beam, and compare which beam has the largest "gradient".
