# Weibull Statistics

The strength at which brittle materials fail depends on the presence of flaws.

The strength depends on the weakest link theory, the strength of the material is the strength of the weakest section.

We must ensure an acceptably low risk of failure.

$P_f=$ failure probability. Survival probability, $P_s=1-P_f$.

The equations determining the probability of survival are provided in the data book.

m is a measure of the variability of failure stress. A low m means a wider spread

![Weibull Distribution](Weibull.png)

$P_s(V)= P_s(V_0)^n=P_s(V_0)^{V/V_0}$

One average, a larger sample is more likely to contain one of the larger flaws and therefore fail at a lower stress.

For the same failure probability, failure stress is larger for smaller volumes.

If a component is subject to varying stress, we only perform the integral over the section in tension, as the compression section has much greater strength.

If we consider a beam in bending, we can use $\sigma=\frac{My}{I}$ to determine $\frac{\sigma}{\sigma_b}$ where $\sigma_b$ is the maximum tensile stress in the beam.

Then perform the 2D Weibull integral across part of the beam under tensile stress.

Ceramic rod in bending is stronger than in tension.

Uniform tension is a difficult test to apply to brittle materials, due to high stress concentrations and cracks caused at the grips. Instead, bend tests are preferred.
