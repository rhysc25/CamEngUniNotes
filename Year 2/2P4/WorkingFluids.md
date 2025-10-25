Every thermodynamic device relies on a working substance, usually a fluid whose function is to provide a medium for the transfer of heat and work

The air-standard cycles such as the Joule cycle using an ideal gas like air do not approach Carnot as Q not at constant T.
Air follows a constant pressure line in the Joule cycle so not constant T.
However other working fluids can be used which behave more like this so closer to the ideal

Revision:
Properties at a particular state have one value
A state is the condition of a system as described by its properties
A pure substance has a homogeneous and invariable composition
Phases are solid, liquid, vapour

Each working fluid in this course will be considered to be:
A pure substance
One, two or more different phases
As long as we stay far from the liquefaction temperature of oxygen and nitrogen we can assume air is a pure substance

State principal: In the absence of external effects, the state of a pure substance is fixed by the values of 2 independent properties

As p=f(T,v), we should be able to experimentally determine p-v-T surfaces, graphs of 3 variables
Only for an ideal gas can this be written as an equation of state. Normally we have to experimentally determine the function

* Saturation state: A state at which phase change starts and ends
* Vapour dome: The region composed of the two-phase liquid-vapour states (where the fluid can be both at the same time). The saturated liquid and vapour lines are the lines bordering the vapour dome
* Critical point: The point where the saturated liquid and vapour lines meet. Only gas exists at temperatures higher. The critical temperature of a pure substance is the maximum temperature at which liquid and vapour phases can coexist. Any higher temp and they become indistinguishable as they molecules are so far apart. The isotherm running through this point is the critical isotherm
* If a substance at normal temperatures and pressures lies above its own critical isotherm it is called a gas, otherwise it is a vapour
The triple line is the line along which three phases can exist together

The temperature at which a phase change takes place for a given pressure is called the saturation temperature
The solid-vapour and liquid-vapour regions are separated by the triple point line. They are also separated from the single-phase regions by the saturation lines. 
In the liquid-vapour region, there is some liquid and some vapour, the proportion changing with changing temp/pressure

The difference between the temperature of a superheated vapour (at a temp higher than its boiling point) and the saturation temperature at the same pressure is called the degree of superheat.

![[Pasted image 20251023153300.png]]
You can see the difference between water and other substances here, with only water expanding upon freezing, causing the ledge

**Phase Changes**

Liquid -> vapour: vaporisation
Solid -> liquid: melting
Solid -> vapour: sublimation

During a phase change both phases can coexist
Accompanied by absorption or release of energy resulting from breaking or reformation of intermolecular bonds

**During phase change p and T are not independent properties**

Heat transferred in a phase change: latent heat. This is a function of p or T

A p-T diagram is known as a phase diagram. Al three phases are separated by lines. These lines are saturation lines
The vapourisation line ends at the critical point as no distinction can be made between vapour or liquid. You just have supercritical fluid, which has properties of both a liquid and a gas
![[PhaseDiagram.png]]
The triple point extends as a line on the p-v-T surface, which we call the triple point line

Ideal gas assumptions:
* Molecules are rigid, no momentum or time lost during collisions (satisfied by all gases, or else pressure would drop over time)
* Volume occupied by molecules negligible compared to total volume (satisfied at low pressures, sufficiently far apart)
* Forces between adjacent molecules are negligible (satisfied at high pressures and/or low temps)

$\lim_{p\rightarrow 0}\frac{p\overline{v}}{T}=\overline{R}$ for all gases and all temperatures
Where $\overline{R}$ is the universal gas constant, $\approx 8.312kJ/kmol\cdot K$

The compressibility factor, Z, or a gas is $Z=\frac{p\overline{v}}{\overline{R}T}=\frac{pv}{RT}$
As pressure tends to zero, the gas acts ideal, p and v act inversely and Z tends to 1
As the pressure is raised, the interactions become significant and Z diverges from 1

Reduced pressure, $P_R$ = pressure / critical pressure
Reduced temperature, $T_R$ = temperature / critical temperature
![[GeneralisedCompressibilityChart.png]]

Another equation for describing the behaviour of a real gas is van der Waals equation of state: $(p+\frac{a}{v^2})(v-b)=RT$, where a and b are constants. 

This equation allows for the attractive force between molecules with the $a/v^2$ term, and the volume occupied by them, $b$

A substance in the two-phase liquid-vapour region consists of both liquid and vapour coexisting in equilibrium
x is called the dryness fraction of the mixture
Each 1kg of mixture contains x kg of vapour and (1-x)kg of liquid

Volume of the mixture: $V=m_fv_f+m_gv_g$
Specific volume of the mixture: $v=\frac{V}{m}=v_f+x(v_g-v_f)=v_f+xv_{fg}$

Thus the dryness factor provides a measure of how far the phase change has proceeded

The main tables of note in the CUED data book are those for water and steam
The data book is incredibly useful, learn where everything is
Page 17-18 tells you the properties on the saturation lines at different temperatures

If we need to interpolate, use the linear interpolation formula:
$y=y_1+(\frac{y_2-y_1}{x_2-x_1})(x-x_1)$
This may need to be done three times if interpolating the value on both axes

Diagram types:
T-s diagram: Most commonly used for cycles, good for comparing to Carnot. Can run an almost optimal Carnot cycle in the 2 phase region, taking advantage of how pressure and temperature behave when phase changing
h-s diagram: Easiest graph to solve cycle problems on, much quicker than using tables. This contains lines of constant x, allowing you to read them off the graph, without having to calculate them
p-h diagram: Used for refrigerant calculations, not as easy to use. It is really good in the vapour region, but bad in the 2 phase region as no entropy lines

If a material passes down through the critical point as temperature decreases, the material will not know which state it should be in, so density fluctuates at the speed of light, turning the material black before making its mind up








