To analyse trade offs between material properties, we need a performance index.

The procedure for creating a performance index:
1) Identify objective, the thing to be maximised or minimised
2) Identify functional constraints, e.g. specified stiffness
3) Identify geometric constraints, which dimensions are fixed and which can vary
4) Eliminate free variables, and identify performance index of properties

E.g. if $E/\rho$ is constant, then $\log(E) = \log(\rho) + \log(C)$
Which is a line of slope one on an E vs $\rho$ property chart

Then when you've listed potential materials above this line, you can apply secondary restraints like toughness, corrosion or cost

An upper limit on A is a lower limit on stress

The maximum elastic energy stored per unit volume in tension is $\sigma_f^2 /2E$, so the performance index for space-efficient springs is $\sigma_f^2 /E$

Section shape is used to improve the efficiency of components and structures loaded in bending
The stiffness, $S \propto I$
Mass, $m/L \propto A$

Shaping a section improves efficiency by either increasing the stiffness at a constant mass (1), or more commonly reducing mass at a constant stiffness (2).

Case (1): Constant area:
Define shape factor for stiffness in bending: $\Phi_e =$ I for shaped section / I for reference shape

A simple reference shape could be a square

Case (2): Minimum mass for a given stiffness:
$S = W/\delta = \frac{C_1 EI}{L^3}$
$\frac{(W/\delta)L^3}{C_1}=\frac{E\Phi_e A^2}{12}$ for a square reference area
If we rearrange for area then multiple by $\rho L$, we have a performance index of:
$$\frac{\sqrt{E\Phi_e}}{\rho}$$
The maximum shape factor depends on the physical limits on section thickness due to:
* The capabilities of manufacturing processes
* Buckling failure of thin-walled sections

Shape factor for bending strength:
$\Phi_f = Z_e$ for shaped section / $Z_e$ for reference shape
Where $Z_e$ is the elastic modulus

When shape can be varied, metals perform better, then composites, then wood (due to knots and grains)

If we want to select a material with multiple constraints, we must first find expressions for the free variable in terms of each constraint
Then, evaluate each to find which is the limiting case, then proceed as normal with that case
For example if the radius of a beam is our free variable and the radius to exceed the deflection limit is larger than the radius to cause failure of the beam, then the limiting scenario is deflection

