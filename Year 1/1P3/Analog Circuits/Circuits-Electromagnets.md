# Circuits - Electromagnets

## Electrostatics
- Fixed charges - assume charges have stopped moving
- For insulators: uniform distribution of charge
- For conductors: charge uniformly distributed on the surface of the volume
- Superposition - When multiple charges are present, the electric field is given by the vector summation of the fields arising from each individual charge:

$$\textbf{E} = \sum_{i=1}^N \frac{Q_i}{4 \pi \epsilon_0 r_i^2} \, \hat{\textbf{r}}_i$$

- Electric flux density, $\textbf{D}$, is conserved when passing through one dielectric to another
- Gauss' Law: use a sphere for a sphere or point charge, use a cylinder for a wire, use a plane for a capacitor
- No charge conserved inside a Faraday Cage ⇒ flux=0 ⇒ $\textbf{D}$=0 ⇒ $\textbf{E}$=0
- Electric flux density $\textbf{D}$ = the charge on the plates of a parallel plate capacitor

## Capacitors
For a capacitor with two different dielectrics between the plates:

$$V=\textbf{E}_1 (t_1 + \frac{t_2}{\epsilon_r})=\frac{\alpha}{\epsilon_0}(t_1 + \frac{t_2}{\epsilon_r})$$

## Current
- Current density when the conductor has uniform, orthogonal cross sectional area: $J=I/S$. If not:
- $\Delta I = \textbf{J} \cdot \Delta \textbf{S}$ or $I=\int_s \textbf{J} \cdot d\textbf{S}$
- If we consider a conducting volume with charge moving at velocity $\textbf{u}$: $\textbf{J}=\rho_v \textbf{u}$

## Magnetism
Using Biot-Savart law:
- The magnetic flux density around a straight wire: $B = \frac{\mu I}{2 \pi R}$ 
- Force: $\textbf{F}=\textbf{B} I L$, allowing you to calculate force exerted on parallel wires
- Magnetic flux density in a solenoid = $B = \mu_0 N I$, where N is turns per unit length

## Inductors
- An inductor will pass a DC current but block an AC current, a choke
- $L=\frac{\mu_0 \mu_r N^2 A}{L}$
