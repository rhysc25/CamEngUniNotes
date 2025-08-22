# Stress Analysis

0.1% proof stress is the stress at 0.001 strain. This is used if the stress strain graph is too steep to measure.

Constrained deformation: strain in either 1 or 2 axes is 0. Stress in any unconstrained axis is 0. Find the strain using the 3D Hooke's law equations, and from that find the effective Young's modulus, σ₁/ε₁

Thermal expansion coefficient, α = Strain/unit temperature change. Units: K⁻¹.  
ε_thermal = α ΔT  
Induced elastic stress, σ = E α ΔT  

## Constrained surface layers

Consider a thin film on a component of thickness >> film thickness, x, and examine a length l₀.  
On cooling, differential contraction of substrate.  
First, consider that the surface layer is not attached to the substrate:

![Differential Contraction](Differential%20Contraction.png)

Superpose tensile stress in the surface layer.  
Change in length: Δl = l₀α₁ΔT - l₀α₂ΔT  
Strain in surface layer: Δl/(l₀(1-α₁ΔT)) = ((α₁-α₂)ΔT)/((1-α₁ΔT))  

Since (α₁ΔT) << 1, strain = (α₁-α₂)ΔT  
If α₁ < α₂, compression.  
Stress in surface film ∝ (α₁-α₂).  
