# Thermodynamics - First Law

Thermodynamics is the study of heat, work and energy.

For a cyclic device, all work can be completely converted into heat.

But heat can only be converted into work and rejected heat. You cannot convert all heat into work, some must be thrown away, from the second law of thermodynamics.

Heat is a form of energy transfer.

1st law: A statement of the conservation of energy.

2nd law: Certain processes progress in only one direction. Defines reversibility and entropy.

Classical mechanics treats matter as a continuum.

We will consider closed systems - A fixed quantity of matter, around which a boundary can be drawn. Everything else is the surroundings.

The thermodynamic state is the overall definition of the system. This consists of thermodynamic properties, such as pressure, volume or temperature.

A property is a measurable characteristic of a system that has only one value for a given state.

Extensive properties are ones which change depend on how much system there is, such as volume.

Intensive properties are those which don't, such as temperature.

Extensive properties can be made into intrinsic by dividing by mass, these are specific properties, and are a subset of intensive properties. Eg. $v=V/m=1/\rho$.

2 independent intensive properties and the mass are sufficient to define the state, when the system is in equilibrium.

Thermodynamics can only furnish relationships connecting equilibrium states.

However, we can consider quasi-equilibrium/quasi-static processes by making small changes, and waiting for the system to stabilise.

The First Law for systems: $Q-W=\Delta E$.

Q is heat, and is positive going into the system. W is work and is positive going out of the system.

Work is done by a system on its surroundings if the sole effect of everything external to the system could have been the raising of a weight.

$W=\int \textbf{F}\cdot d\textbf{S}$

$pdV$ work: When the expansion or contraction of a gas is fully resisted, meaning that the properties of the gas are uniform throughout the process, so quasi-static. $W=\int \delta W=\int pdV$.

If there is unrestrained expansion, so the system boundary does not move for example, then there is no work done.

If there is a change in a property, we use an exact differential, eg. dx, dV, dp. If there are changes which are process dependant, we use inexact differentials, eg. $\delta W, \delta Q$.

Shaft work: $\int W_x=\tau d\theta$.

The rate of work, so shaft power: $\delta \dot{W}_x=\tau d\dot{\theta}\Rightarrow \dot{W}_x=\tau \dot{\theta}$.

Electrical work is always considered work, regardless of its use, eg. thermal dissipation in a resistor.

$W_e=\epsilon Q \Rightarrow \dot{W}_e=\epsilon I$.

Heat transfer, Q, energy transfer that is not work. There are 2 main mechanisms by which heat can cross a system boundary:

Conduction: Interactions between particles, passing on energy.

Radiation: EM waves radiated by matter due to changes in electronic configurations of the atoms.

There is also convection, which is just the carrying of energy from one place to another.

Changes in E consist of $\Delta KE, \Delta GPE,$ and $\Delta U$, where U is the internal energy of the system, comprised of random thermal energy of atoms, any potential energy due to force fields, and maybe magnetic, electrical and chemical energy.

They are all extensive properties, which can be converted to intensive by dividing by mass, turning them lower case.

If there is no change in GPE or KE, then $Q-W=\Delta U$.

$\delta q-\delta w=du$.

An adiabatic process is one in which there is no heat exchange, so $Q=0$.

This occurs if there are perfectly insulating walls, or if we consider an infinitely short duration.

For an adiabatic process: $-W=\Delta U$.

A cyclic process is one for which the system returns to its original state.

The net work output = the net heat input for a cyclic process.

We can only apply the laws of thermodynamics if we know how the properties relate to each other.

Pure substances are ones with the same thermodynamic properties everywhere.

n = number of kmols = $N/N_A$. 
$N_A$ = Avogadro's number = $6.022 \times 10^{26} kmol^{-1}$.

An ideal gas requires it to have very low density, so the particles are far enough apart not to exert any non contact forces on each other.

For an ideal gas: $pV=n\overline{R}T$.

Or, using $m=nM$ where M is the molar mass in kg kmol$^{-1}$ $pV=mRT$ where R is the specific gas constant.

In a constant pressure process, for which the only work is $pdV$ work, $Q=\Delta(U+pV)$.

Enthalpy: $H=U+pV$. $h=u+pv$.

This is a property of a system, as it is a function of only properties of the system.

For a constant volume process, $Q=\Delta U$. The constant volume specific heat capacity = $c_v=(\frac{\partial u}{\partial T})_v$, relating to changes in internal energy.

For a constant pressure process, $Q=\Delta H$. The constant pressure specific heat capacity = $c_p=(\frac{\partial h}{\partial T})_p$, relating to changes in enthalpy.

For ideal gases: $c_p=R+c_v$. The internal energy and enthalpy are both functions of temperature only.

It is a semi-perfect gas if $c_v$ and $c_p$ vary with temperature.

Semi-perfect gases need data book tables.

It is a perfect gas if they are both constants.

For a monatomic perfect gas: $\frac{c_p}{c_v}=1.67$

For a diatomic perfect gas: $\frac{c_p}{c_v}=1.40$

The ratio $\frac{c_p}{c_v}$ is given the symbol $\gamma$.

![Gas properties](gases.png)

Therefore to determine $\Delta H$ and $\Delta U$ for a semi perfect or perfect gas:

$\Delta U=mc_v\Delta T$ and $\Delta H=mc_p \Delta T$.

An Isobaric process is one with constant pressure.

If the only work is pdV work:

$W=p(V_2-V_1)=mR(T_2-T_1)$. $\Delta U=mc_v(T_2-T_1)$.

$Q=W+\Delta U=m(R+c_v)(T_2-T_1)=mc_p(T_2-T_1)$.

An Isochoric process is one with constant volume. In the absence of shaft work:

$W=0$. $Q=\Delta U=mc_v(T_2-T_1)$.

An Isothermal process is one with constant temperature. This does not mean adiabatic. Assuming only pdV work:

$W=\int pdV=\int \frac{mRT}{V}dV.$

$\Delta U=0$. $Q=W=mRT\ln(\frac{V_2}{V_1})$.

For a cyclic process, the overall $\Delta U$ is zero. The net heat transfer balances the net work produced.

An Isentropic process is a quasi-equilibrium and adiabatic process.

$\delta Q=dU+\delta W=0$. For a perfect gas: $\delta Q=mc_v dT+pdV=0$.

This gives: $c_v\frac{dT}{T}+R\frac{dV}{V}=0$.

This gives that: $Tv^{\gamma-1}=$ constant.

$pv^\gamma =$ constant.

$p/T^{\gamma/(\gamma-1)}=$ constant.

If a process is not quasi-equilibrium we can only relate the start and end state.

A Polytropic process is one for which the pressure and volume are related by:

$pV^n=k=$ constant.

We can see that if $n=\gamma$, this is an isentropic process.

If $n=1$, this is an isothermal process.

If $n=0$ is is isobaric, and if $n=\infty$ this is isochoric.

$W=\int pdV =\int \frac{k}{V^n}dV=[\frac{kV^{1-n}}{1-n}]^{V_2}_{V_1}=\frac{p_1V_1-p_2V_2}{n-1}$
