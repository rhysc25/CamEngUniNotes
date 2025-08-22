# Microstructures and Properties

Property chart: Young's modulus vs Density. There is very little variability for metals, they have fixed properties.  
There is a general trend that the more dense a material, the more stiff it is.  
10¹⁰m is 1 Angstrom.

Grain boundary - where multiple grains meet - causes a defect. Freezing causes a bunch of defects. Heat treatment reduces the amount of defects.

Primary bonds behave as stiff elastic springs, with force-displacement response of the form:

![Bond stiffness](Bond%20stiffness.png)

Bond stiffness S = gradient of the force - displacement response at equilibrium spacing.

For a small displacement from equilibrium, u: Restoring force per atom = Su, and the strain is u/r₀  
Area per bond = r₀². Stress ≈ Su/r₀²  
E ≈ S/r₀, so Young's modulus is directly proportional to bond stiffness.

Alloys are a mixture of elements, forming solid solutions and compounds. Solid solutions contain a mixture of different bond stiffness's, so resultant is just the average of the two bond stiffness's. With compounds you can't do this.

In polymers, the weaker secondary bonds are overcome by thermal energy at a lower temperature: the glass transition temperature Tg. After this point, Young's modulus drops significantly. Above Tg:
- Amorphous thermoplastics melt to a viscous liquid
- In semi-crystalline thermoplastics, the amorphous regions melt but the crystalline regions survive to a higher temperature so rubbery
- In elastomers and thermosets, the cross links do not melt, so rubbery.

## Foams

Foams are porous solids. Any solid can be made into a foam by introducing air.  
Relative density = density of foam/density of solid used.

E_foam/E_solid = (ρ_foam/ρ_solid)²

On a log-log E vs ρ graph, this becomes a line of slope 2, which is a great predictor of the properties of unknown foams.

## Composites

Composite materials can improve the performance index of materials.  
There are three types of composite geometries: Particulate, fibre and laminate.  
Density: $\rho _c = V_f \rho_f + (1 - V_f)\rho_m$ where $V_f$ is the volume fraction of the fibre.

![Laminated composite](Laminated%20composite.png)

The longitudinal modulus (parallel to layers), as well as the transverse modulus (perpendicular to layers), are in the data book.  
These equations are upper and lower bounds for E - composite moduli must lie between or on these limits.

From Strength vs. Density and Young's Modulus vs. Strength graphs, we can see that metals have a lot of variability in strength, but very little variability in density or E.  
Elastic deformation displaces atoms by a fraction of their equilibrium spacing.  
Plastic deformation involves relative movement of material over very large multiples of the atomic spacing.

When a shear stress is applied to a material, as one layer shifts over the other, when set of bonds are broken, and another form. The atoms must overcome a periodic energy potential as they move over another atom in the layer below.  
τ₀ᴹᴬˣ = 2πU₀NA/b, where NA is the number of atoms per unit area.  
∂τ/∂γ = G, the shear modulus.  
τ₀ᵐᵃˣ = G/2π ≈ G/15  

Therefore, combining τ = σ/2 and G = E/(2(1+ν)), σel = strength = E/(10(1+ν)) = E/15  
This is an estimate of the ideal strength of a crystalline material.  
In reality, the failure stresses are 10-1000X smaller.  
This is due to dislocations, which control the strength of the material.

## Dislocations

Dislocations - planes of atoms that end in the lattice. These are line defects.  
The dislocations propagate to the edge of the material, causing slip steps.

![Dislocations](Dislocations.png)

Slip step produced by the passage of one dislocation is the Burgers vector b. It is essentially how far apart the atoms are along the line. b is smaller than r₀.  
The tangent vector t is a unit vector that points along the line of the dislocation.

For an edge dislocation: The shear stress and Burgers vector are both at right angles to the dislocation. The dislocation moves in the direction of the stress.  
For a screw dislocation: The shear stress and Burgers vector are both parallel to the dislocation. The dislocation moves at right angles to the stress.  
In reality, most dislocations are mixed, varying between pure edge and pure screw.

It is easier to forget about individual atoms moving, and easier to think of line defects "gliding" across slip planes under the action of imposed shear stress.  
Each dislocation causes a slip step of the order of magnitude of an atomic spacing, but their are so many, as there are shear stresses in every stress state, and there are very many dislocations.  
When a dislocation happens, volume is conserved, plastic deformation.

The intrinsic lattice resistance to dislocation motion τ₀ comes from additional bond stretching as the dislocation moves each Burgers vector step.

The line tension, the force which needs to be applied to the dislocation to move it across the lattice, also an energy per unit length: T ≈ Gb²/2  
The dislocation moves when the applied force from shear stress, f = τ₀b.  
Therefore, the intrinsic stress in order to move a dislocation, or the intrinsic lattice resistance: τ₀ = f/b = Gb/2l.

We want to hinder dislocation motion. When a gliding dislocation meets obstacles in its slip plane, it is pinned and forced to bow out between them.  
If the obstacle spacing = L, the force on the dislocation F = τbl

![Obstacle Spacing](Obstacle%20Spacing.png)

The force needed to overcome obstacles: F = cT, where T is the line tension. c = 2 for a strong obstacle.  
τ = cT/bl ≈ α(Gb/l), where α ≤ 1.  
G & b are fixed parameters, L & α can be manipulated by composition and processing.

![Obstacles](Obstacles.png)

Metals use several methods to pin dislocations:
- Work hardening to create more dislocations
- Solid solution hardening to add solute atoms
- Precipitation hardening to add particles of another solid

The total shear stress to move a dislocation is now: τy = τ₀ + τᵢ  
τᵢ could be τwh, τss or τppt

In a poly crystal, the dislocations move first in grains which are favourably oriented, then progressively throughout all the grains. The total shear stress to deform all crystals, k = 3τy/2. This is the shear yield stress, k. σy = 2k = 3τy.

### Work hardening

Gliding dislocations interact, creating jogs, which reduce the mobility of the other dislocations.  
The additional stress from dislocation pinning ∝ 1/L. The spacing L depends on the dislocation density: ρd, the total dislocation length per unit volume, units: m/m³. L = 1/√ρd  
Dislocation density rises with strain. Strength increases, but ductility decreases.

### Solid solution hardening

The solute atoms roughen the slip plane, providing more weak obstacles to dislocations, which bow out until the line tension pulls the dislocation past the solute atom.  
The yield stress contribution from solid solution, σy,ss ∝ Gb/l ∝ √C, where C is the solute concentration.  
The yield stress does not increase linearly with concentration of solid solution, but peaks at an optimal concentration.

### Precipitation hardening

Particles of compounds added within a lattice, providing strong obstacles. For an obstacle, τy = α(Gb/L) where α is between 0 and 1. As σy = 3τy, the stress contribution from work hardening = 3Gb/L.

Also, grain boundary hardening: Stress builds up in grain boundaries. (σy)gb ∝ 1/√d, where d is the grain size.  
Each process for deforming materials has a contribution to yield stress.

## Polymers

Considering polymers: The peak stress rises with crystallinity.  
Failure mechanism under Tg: Elastic-brittle.  
Above Tg there are three mechanisms:
- Cracking, where microcracks open and are held by stiff fibres
- Shear yielding, where shear bands form and are stabilised by the alignment of molecules
- Cold drawing, where necking occurs but the neck is stable, length increases until you are breaking primary bonds, where E increases drastically until failure.
