# Fluid Statics

A fluid cannot sustain shear stress when at rest.

Pressure forces act normal to a surface.
Pressure acts uniformly in all directions.
The gradient of pressure through a uniform fluid is constant.

All points at the same depth have the same pressure.

A manometer is used to measure pressure. $p_m-p_a=(\rho_l-\rho_a)gh$

Gauge pressure is the pressure relative to atmospheric pressure.

![Barometer](Barometer.png)

A barometer, filled with mercury, with a small vacuum at the top. Depending on the outside pressure, the liquid level will rise or fall, measured using a ruler. Be careful as the point you're measuring from will also change height.

$$p_a=\rho_{Hg}gh$$

Archimedes Principle: Upthrust = The weight of fluid displaced

The horizontal force on a submerged surface is always: $F = \rho g w {\frac{(h_1+h_2)^2-{h_1}^2}{2}}$

This is always true as all that matters for pressure is the projected area.

The total force on the surface is the integral of all the tiny forces from pressure.
$$F=\rho g \sin(\theta)\int_{plane}b(s) \cdot s \cdot ds $$
Where s is the distance down the plane, $\sin(\theta)$ is the angle from the horizontal of the plane, and $b(s)$ is the function of the width of the plane, usually constant.

To find the point at which this force applies, sum all the tiny moments due to pressure along the face.
$$F \cdot s_{CoP}=\rho g b\int_{plane} (s\cdot \sin(\theta)+Y')s \cdot ds $$
Where $s_{CoP}$ is the centre of pressure and Y' is the starting depth.

In most cases, $S_{CoP}$ is $\frac{2}{3}l$ down the plane.
