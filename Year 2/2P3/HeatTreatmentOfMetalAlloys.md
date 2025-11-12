Manufacturing processes are used to manipulate the microstructure of a material.
Process variables (inputs): material type, composition, thermal history and deformation history.
Microstructure: Phases present, spatial distribution, grain size/shape, dislocation density.
Material properties: stiffness, yield strength and fracture toughness

**Heat Treatment of Aluminium Alloys**
Al is very light and not very stiff. 
The most important hardening mechanism for Al is precipitate hardening - the pinning of dislocations by strong, second phase particles

Yield is caused by the glide of dislocations, so yield stress is inversely proportional to the obstacle spacing.

Requirements for heat treatable alloys:
* At high temps: single phase solid-solution
* At low temps: two-phase region
* Must cross solvus line (the solubility line), driving precipitation of the second phase

**Slow Cooling**
![[Pasted image 20251106133816.png]]
Precipitates form in the Al, with large nucleation on grain boundaries due to the ease of diffusion
The volume drives G down, but the surface area and surface tension drive G up. 
The spreading out is bad for $\sigma_y$, which is inversely proportional to the obstacle spacing

As we've already seen, the rate of transformation depends on the amount of undercooling, with an optimal value.
It is convenient in materials processing to invert the rate axis and show instead the time taken for a certain fraction to transform. This is a C-curve
The plot of fraction transformed for a given temperature and time is known as a Time Temperature Transformation (TTT) diagram
![[Pasted image 20251106134848.png]]
These apply to isothermal transformations only. In reality we have continuous cooling, so we need an analogous continuous cooling transformation (CCT) diagram, where the C-curves show the fraction transformed for a fixed cooling rate

![[Pasted image 20251106135023.png]]
The critical cooling rate (CCR) is the slowest cooling rate where precipitation doesn't happen. There is insufficient time or temperature for nucleation of precipitates.

This is what quenching is, where we cool so quickly that the alloy ends up in a metastable state, as a supersaturated solid solution. This is not an equilibrium state.

This results in a material with effective solid solution hardening. However, this is not optimal.

**Age Hardening**
3 steps: Dissolve alloying element, to achieve single phase solid solution. Cool faster than CCR, forming a SSSS. Reheat, allowing time for precipitation to occur from the metastable SSSS. 
This is heavily controlled, so we can allow the perfect amount of precipitate to form.

2 types:
Artificial ageing, as described above, or natural ageing where we leave at room temperature for several days

With increasing ageing time, the precipitates coarsen, so average size and spacing increases.
2 ways for a dislocation to overcome an obstacle: Shearing (cuts through the obstacle) (as radius increases, strength increases), Bypassing (breaking and reforming on the other side)

These two methods trade off as the the precipitate size increases and the spacing increases, leading to an optimal peak age.
![[Pasted image 20251106135936.png]]
As we can see, naturally aged alloys never evolve to their largest size, but it is cheaper.

Higher ageing temperature means:
More rapid coarsening, but a lower equilibrium fraction of precipitates, so the peak moves down and to the left

A first look at the TTT diagram would suggest there would be no precipitation during ageing, but we actually get metastable precipitates forming at these low temperatures. There is another set of C-curves governing the precipitation of these metastable phases.
![[Pasted image 20251106140828.png]]
Some alloys are non-heat-treatable as they form no metastable precipitates at low temperatures.

Metastable precipitates have a different crystal structure to equilibrium $CuAl_2$. The precipitate is coherent, matching that of the Al closely. This reduces the interface energy penalty to nucleation. These are relatively weak obstacles, and not the lower Gibbs free energy.

Overall, it becomes energetically favourable for the precipitates to transform through a whole sequence of metastable phases, eventually reaching equilibrium $CuAl_2$, with a progressive loss of coherency at the interface.
![[Pasted image 20251106141228.png]]

**Heat Treatment of Steel**

Lost cost. High Young's modulus (stiff), High strength and toughness. However: high density.
Very amenable to variation through changing alloying and/or heat treatment
Alloying and heat treatment can 7x the yield strength, uses in cutting tools

![[Pasted image 20251110140249.png]]
We are interested in the behaviour of steels around the Eutectoid point.
Hypo-eutectoid steel is like mild steel, low carbon steel. Start in a single phase region and cool into a two phase region

Making steel alloys requires a three phase transformation.
FCC Austenite $\gamma \rightarrow$ BCC Ferrite $\alpha$ + $Fe_3C$

Unlike slow cooled Al, slow cooled steel is very useful. Slow cooled steels are referred to as normalised. Slow cooled steels: Allow enough time to reach equilibrium phases.
![[Pasted image 20251110140930.png]]
Firstly ferrite nucleates at austenite grain boundaries and rejects carbon into the surrounding austenite. The carbon atoms want to minimise diffusion distance, leading to pearlite. Then the austenite passes through the eutectoid point so transforms into pearlite containing $\alpha$ + cementite $Fe_3C$

The properties of normalised hypo-eutectoid steels are determined by the carbon content:
The carbon content affects the proportion of ferrite and pearlite. The lever rule just above the eutectoid temperature gives the proportion of austenite which transforms into pearlite.

The higher the pearlite fraction, the harder and stronger the substance.

**TTT Diagrams for Hypo-Eutectoid Steels**
![[Pasted image 20251110142851.png]]
* If we quench to temperatures just above the temperature asymptotic to the carbide line (A1 temperature) and stop and wait, we will get ferrite + austenite
* If we quench to temperatures above the node of the C-Curve but below the A1 temperature we will get ferrite forming first, then transformation switch to pearlite at the carbide line - Final microstructure - ferrite plus pearlite
* If we quench to temperatures below the nose of the C-curve: diffusion is more limited (diffusion rate decreases as temperature decreases here). Not enough diffusion to allow pearlite to form. Therefore just forms bainite, which is ferrite + iron carbide, in a fine scale dispersion. Needles of iron carbide exist within the ferrite lattice.

Once we're at a set temperature and past the carbide line, the more right we go will not change the percentage of ferrite.

If we instead quench all the way down to room temperature, we undergo a phase transformation. to a metastable phase. Austenite $\gamma$ $\rightarrow$ martensite $\alpha'$
Diffusion-less phase transformation. Mechanical rearrangement of structure.
All the iron wants to be BCC instead so the lattice shears.
![[Pasted image 20251110144100.png]]
Shear transformation in order to make deformed BCC lattice closer to equilibrium structure which is regular BCC.
Shearing a material is equivalent to stretching it in one direction and compressing it in another.

A needle of this sheared structure will nucleate on a grain boundary or other irregularity and propagate across the lattice effectively at the speed of sound. Essentially instant.
![[Pasted image 20251110144359.png]]
Depends on temperature but not time. Therefore horizontal lines on TTT diagrams.
The fraction transformed into martensite depends on temperature, with zero at martensite start and 1 at martensite finish. This happens because at a given temperature, the transformation of a percentage of the austenite into martensite can reduce the free energy sufficiently to stop further transformation. The undercooling (and hence $\Delta G$) must be increased further to induce further transformation.

Shape memory alloys exploit this, as it will return to it's original shape after we reheat back to austenite.

**Effect of Carbon Content on the Steel TTT Diagram**

As the carbon content increases: 
1) The proportion of ferrite to pearlite decreases. This continues until the eutectoid composition, where all the austenite turns straight into pearlite. 
2) The C-curves move to longer times: A greater amount of carbon means diffusion takes longer.
3) The start and finish temperatures for the martensite phase transformations drop, as it's more difficult to carry out shearing when there's more carbon in the lattice. For high enough concentration, the martensite finish temp is below room temp. 


Bainite has the ideal microstructure for effective precipitation hardening: a fine scale dispersion of hard precipitates.
Martensite has an enormously high yield stress. Enormous solid solution hardening concentration. Heavily supersaturated with carbon. This is further enhanced by the distortion of the lattice, as many interstitial holes contain C atoms that are too large to fit. The higher the C content, the greater the distortion of the lattice, and the higher the hardness. 

Martensite is also incredibly brittle (negligible fracture toughness). Cannot resist cracks. 

**Tempering**
Therefore it needs to be tempered. This is where we reheat it to a temperature of the order of 500 degrees C (still in the 2 phase region) to encourage diffusion. Fracture toughness increases significantly. Yield strength halfs. 

This encourages diffusive phase transformation. Distorted martensite lattice reverts to equilibrium ferrite lattice. Carbon diffuses out of lattice, forming cementite, but in a very fine-scale way. As with the aluminium, we can tune this process with ageing.

As the tempering time increases, the $Fe_3C$ precipitates coarsen, giving a steady fall in strength. They will want to decrease their surface area to volume ratio.
![[Pasted image 20251110194700.png]]

**Hardenability**
How easily a steel forms martensite on cooling. Measures of hardenability:
* TTT diagram: Look at the time it takes for diffusive phase transformation to begin (e.g. ferrite pearlite C-curves). Higher hardenability = longer transformation times.
For a CCT diagram: Higher hardenability = slower CCR
* Critical component size / critical bar diameter. The largest bar diameter that will give 100% martensite at its centre after quenching. Higher hardenability - largest diameter.
Heat flow analysis is used to relate cooling rate and component geometry.

When do we want hardenability - 
If we want to quench large components
If we don't want to quench for very long as our component is delicate. Don't want to form heat stresses and cracks.
When do we want a low hardenability -
When you don't want to form martensite. Welding. Forming martensite is undesirable as it is brittle. High hardenability = poor weldability.


