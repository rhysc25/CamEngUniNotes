**Thin-walled Sections**

Through-thickness stresses are zero everywhere
The stress state is uniform through the section

Stiffeners prevent local buckling and can carry concentrated loads

From 1A: $\sigma_l = \frac{pr}{2t}$ and $\sigma_h = \frac{pr}{t}$

Bellow joints allow expansion of the pipeline:
 $\sigma_l = 0$ at bellows joint

Circumferential stiffeners must reduce the average hoop stress as the area is now greater than $2lt$
![[Stiffeners.png]]
But depends on the section we take, we get different values, so hoop stress must vary. Therefore we still use the estimate that $\sigma_h = \frac{pr}{t}$

Longitudinal stiffeners will carry the same load as the skin, and hence the longitudinal stress will be reduced. This will not very with the cut taken
![[University/Images/LongitudinalStiffeners.png]]

Considering non-circular cylinders with a vertical axis of symmetry under axial forces, bending moments and shear forces:
Only vertical deflection
Neutral axis at the centroidal level
$\sigma_l = P/A$. $\sigma_l = \frac{My}{I}$. $I_{xx}=\int y^2 dA$

Complementary Shear Stress:
A state of simple shear requires equal shear stress on all four faces of an arbitrary small block. This can be shown by taking moments about any point on the face.
We can see how the shear forces must be acting in the piece by taking more cuts and balancing forces:
![[Pasted image 20251030194111.png]]

$q = \frac{S\bar{y}A_{S}}{I}$
The shear stress can be found be dividing the shear force by the area of the longitudinal cut
The maximum shear stress will be found with the minimum area, so the cut should be perpendicular to the wall

**Effect of Stiffeners**
Stiffeners will increase A and I, reducing stress due to axial loads and reducing the stress due to bending
As it increases both A and I, it will negligible effect on the shear stresses due to shear-loading

To avoid the full complications of calculating exact section properties including stiffeners, the
stiffeners are often ‘smeared’ out by making the thin walls a little thicker.

**Strain in 3-D**

$\epsilon_{xx}$ is the extension between two x-faces

Shear stresses will cause shear strains, causing the material to deform with an angle $\gamma$ from its original position

We are using the assumptions that the model is linear-elastic (stress-strain curve is a straight line, and no permanent deformation), homogeneous (doesn't vary with position), isotropic (doesn't vary with direction) and time-independent (no creep)

Superposed extension: $\epsilon_{xx}=\frac{1}{E}(\sigma_{xx}-\nu \sigma_{yy}-\nu \sigma_{zz})+\alpha\Delta T$

**Shear Strain**
$\gamma_{xy}=\frac{1}{G}\tau_{xy}$, where $G=E/2(1+\nu)$

In an isotropic material, a shear stress will cause no normal strain in any direction. Shear stresses only cause shear strain in its own plane
Normal stresses only cause normal strain

$\frac{\Delta C}{C}=\epsilon_h$. As $C$ and $r$ are linearly related, $\epsilon_h=\frac{\Delta r}{r}$
This has nothing to do with through wall strain

$\Delta V=\frac{\partial V}{\partial l}\Delta l+\frac{\partial V}{\partial r}\Delta r$
This will normally be some linear sum of longitudinal and hoop strains

If restrained by a wall, the strain in the longitudinal direction must be zero.

