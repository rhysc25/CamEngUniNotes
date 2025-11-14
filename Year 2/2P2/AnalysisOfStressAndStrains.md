What if we wanted to cut through the structure and find stresses at an arbitrary angle?
We always find the initial easy state first, where everything is orthogonal with the walls.

From their we can take a smaller element and perform force balances, multiplying the stresses over the areas they are acting on

Nomenclature: $\tau_{xy}$ means its on face x and pointing towards face y

Performing this analysis for a generic case:
$\sigma_{aa}=(\sigma_{xx}\cos(\theta)+\tau_{xy}\sin(\theta))\cos(\theta)+(\sigma_{yy}\sin(\theta)+\tau_{xy}\cos(\theta))\sin(\theta)$
$\tau_{aa}=-\sigma_{xx}\sin(\theta)\cos(\theta)+\sigma_{yy}\sin(\theta)\cos(\theta)+\tau_{xy}(\cos^2(\theta)-\sin^2(\theta))$
These equations can be found in the data book

**Mohr's Circle of Stress in 2D**

For various angles $\theta$, plot a graph of normal stress on a face against shear stress
For Mohr's circle, shear stress is plotted positive when it is acting clockwise
![[Pasted image 20251112141725.png]]
Diametrically opposite points show the complementary shear stress
This circle repeats with a period of $180\degree$

With a bit of double angle manipulation, we get that:
![[Pasted image 20251112141906.png]]
We can clearly see the rotational matrix appearing and causing the circle nature


