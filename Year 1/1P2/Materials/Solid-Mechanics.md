# Solid Mechanics

Volume is not conserved in elastic deformation. A Poisson's ratio (ν) of 0.5 is the max. (Volume conserved).

From Poisson's ratio: Hooke's law in 3D for an isotropic material (elastic response is identical in all directions):

ε₁ = (1/E)(σ₁ - ν σ₂ - ν σ₃)  
ε₂ = (1/E)(-ν σ₁ + σ₂ - ν σ₃)  
ε₃ = (1/E)(-ν σ₁ - ν σ₂ + σ₃)  

The volumetric strain is called the dilation, Δ = Change in volume/original volume  
Final volume = (1+ε₁) × (1+ε₂) × (1+ε₃) ≈ 1 + ε₁ + ε₂ + ε₃ ⇒ dilation = ε₁ + ε₂ + ε₃  

A state of hydrostatic stress is when all three normal stress are equal and negative.  
The bulk modulus, K = Hydrostatic stress / volumetric strain = E/(3(1-2ν))  

Normal stress is stress perpendicular to the plane.  
Shear stress, τ, is stress parallel to the plane.  
You can always resolve to find a plane with shear force in it. The area has changed so you have to recalculate the shear stress.  

## Shear strain

Shear stress, τ, distorts the shape of the volume element, rather than changing its axial dimensions. Shear strain will be an angle, but very small so can be approximated. γ = w/l₀  

Shear modulus, G = shear stress/shear strain = τ/γ  
G = E/(2(1+ν))  

Pure normal strain is equivalent to pure shear strain, γ at 45°  
Given any 2 of E, ν, K or G, you can find the rest.  

After the elastic limit, the material gets harder - work hardening  
During the elastic regime volume is not conserved, however during the plastic regime volume is conserved. A₀l₀ = Al  

The instantaneous true stress is F/A. For convenience, we use nominal stress F/A₀. Equivalent nominal strain: x/l₀  

The elastic stored energy is the area under the linear region of the stress-strain graph. Max = σ²ᵧ/(2E)  
The dissipated energy due to plastic deformation is given by the area under the plastic regime section.  

If the material is unsuitable to tensile testing, compression tests can be carried out. Tensile tests can only be carried out as far as necking. After that, compression tests must be used.  
For a brittle material: Compressive strength >> tensile strength, as cracks are not allowed to propagate.  

Non destructive test: The Vicker's hardness test. A diamond pyramid is pressed into the surface under constant load.  
Hardness, H = load / projected area of indent. H ≈ 3 σᵧ  

Nominal stress, σₙ = F/A₀. During plastic deformation A₀l₀ = Al. Therefore σₜ = σₙ(A₀/A) = σₙ(l/l₀ = 1+$\epsilon$ₙ)  
True stress > nominal stress (for tension)  

True strain, εₜ = ln(l/l₀) = ln(1+εₙ)  
True strain < nominal strain (for compression)  
Nominal strain ≈ true strain for εₙ << 1  

True stress-strain curves for tension and compression are identical.  
The advantage of true strains is that they can be added, separate strains can be summed. This is not true for nominal strain.
