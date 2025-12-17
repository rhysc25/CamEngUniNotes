Our equations must be independent of any scale of measurement.

First list your relevant variables and their dimensions, then remove a dimension one by one, dividing through by as many of any variable as is necessary

We can then form relationships between the model and full sized versions of our experiments, as the non dimensional expressions must always be the same.

**The $\pi$ Theorem**
If we have N variables and K fundamental dimensions involved, then we have N - K truly independent dimensionless groups.

**Non-Dimensionalising an Equation**
We just need to pull out the dimensional quantities from each parameters.
E.g. $x_1=x^*L_1$ where $x^*$ is dimensionless
Do this for every variable in your equation then group them together

**Order of Magnitude Analysis**
If we pull all the dimensional quantities out to the rough order of magnitude, then we can compare the importance of certain expressions in an equation.
For example, the Reynold's number $\frac{\rho v_1L_1}{\mu}$ is a measure of the importance of viscous forces against advection in the Navier Stokes equations

For most dimensional analysis problems involving fluids and drag we can pretty much always write down the Reynold's number as 1 of our dimensionless quantities. From there, we consider which independent variables we haven't used yet, and try and form dimensionless quantities for them. Usually something like Froude's number or Mach number.

Sometimes we are told we can break down the resulting function further.
For example if we had $C_D=f(Re,Fr)$, we may be told that we can write this as:
$C_{D,Total}=C_{D,form+friction}(Re)+C_{D,wave}(Fr)$
In this case we can sum or subtract them

