Materials which are soft (low yield stress) and/or compliant (low stiffness) at room temperature are called soft matter

Latex needs to be cured to become rubber. The curing process is called vulcanisation. Add a few % of sulphur to the polymers and heat

The stiffness of metals, ionic crystals or covalent solids is determined by the atomic potential of interaction. Electrostatic interactions are responsible for attractive forces between atoms or molecules. Steric (contact) interactions cause short range repulsion. The balance between the two determines the atomic distances and the rigidity of bonds.

Foams are easy to deform because deformations are accommodated by bending the cell walls, with greatly reduced distortion at the atomic scale

The Young's modulus of polymers can be varied easily without changing density

**Polymers**

Amorphous:
Below $T_g$, the thermal energy is too weak to allow the chains to slide past each other
Above $T_g$, polymers are viscoelastic. In this regime, the chain is flexible and fluctuates due to thermal agitation. On short time scales, polymer chains are entangled and can store deformation, leading to a transient elastic response.

Elastomers:
Elastomers are crosslinked networks of polymer chains.
Remain solid above $T_g$, but is a network of "liquid" polymer chains
The properties are explained by microscopic entropy

Consider a floppy amorphous polymer chain made of n monomers of length a, and contour (total) length L=na:
![[PolymerChain.png]]

Constant temp T. $\delta W = -fdr \Rightarrow$ $TdS=dU-fdr$

We need to estimate $dU$ and $TdS$ for a given change $dr$
As U depends on temperature and bond stretching only, if we assume $r << L$, then U does not depend on r
$\Rightarrow f=-T\frac{\partial S}{\partial r}$
To further this, we need to know $\frac{\partial S}{\partial r}$, where $S=k_b\ln(\Omega_c)$
So we need to know how the number of different configuration of the chain depends on r. This is an example of random walk

For a 1D example, we can say that each monomer is either pointed + or -. The total configurations is:
$\Omega_c=C^n_{n+}=\frac{n!}{n_+!n_-!}$

The result holds for larger dimensions

Substituting for expressions of n, r and a only, then using Stirling's approximation we get that $f=\frac{k_B T}{na^2}r$
So the entropic spring constant is $\frac{k_B T}{na^2}$
Therefore stiffness increases as temperature increases

In the absence of any force this says the mean end-to-end distance would be zero, but we know it's not. 
We need to find the root mean squared end-to-end distance, or the radius of gyration
From $\Omega_c\propto \exp(-\frac{r^2}{2na^2}​)$, which is a Gaussian distribution:
The standard deviation of the normally distributed end-to-end positions, $\sigma^2=na^2$
The radius of gyration is the standard deviation of the distribution in this simple model: $r_g=\sqrt{<r^2>} \approx \sqrt{n} a$

![[PolymerEntropy.png]]

The larger the end-to-end distance, the lower the number of available microscopic configurations.

**Polymer Structure Between Cross-links**

When cross linking takes place, polymers are just behaving like single flexible polymers in the absence of tension
The typical distance between two points in the chain separated by n monomers is $\sqrt{n} a$
Hence, the number $n_c$ of monomers between cross links is given by:
$r_c=\sqrt{n_c} a \Rightarrow n_c=\frac{r_c^2}{a^2}$
Where $r_c$ is the distance between crosslinks

The effective spring constant of each polymer segment between cross links is therefore $k=\frac{k_B T}{r_c^2}$

To find the density of the chain segments, i.e. how many segments per unit volume:
$N_c=$ number of monomers in $r_c^3$ / number of monomers
$N_c=\frac{r_c^3 / v_m}{n_c}=\frac{a^2r_c}{v_m}$, where $v_m$ is the volume of a monomer

Considering a cube of volume $r_c^3$. The force F if the cube is stretched by a distance $\delta x$ is: $F=N_ck\delta x$

This gives the Young's modulus, $E=\frac{F}{\delta x r_c}= \frac{k_BTa^2}{v_mr_c^2}=\frac{k_B T}{v_m n_c}$

Reminder: $v_m$ is the volume of a monomer and $n_c$ is the number of monomers between cross links

So stiffness increases with temperature. This is visible experimentally, but often limited due to the proximity to the glass transition temperature of the polymers which cause a great decrease in stiffness. Also longer chains between linkages also reduces the modulus.




