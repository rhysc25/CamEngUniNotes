# Thermodynamics - Second Law

An irreversible process is one in which both the system and the surroundings cannot return to their original conditions. The system can return to its original conditions but only with the addition of work.

For example, work may have been extracted from the environment, and an equal amount of heat may have been transferred to the environment.

Some examples of irreversible processes:
- Any process involving friction
- Heat transfer across a finite temperature difference
- Unrestricted expansion of a gas
- Anything involving mixing

A reversible process is one in which the system and its surroundings can be returned to their initial state.

This is true for heat transfer over infinitesimally small temperature differences.

Reversible processes must be quasi-equilibrium and they must take place slowly.

Some examples of reversible processes:
- The stretching of a spring within elastic limit
- Fully resisted expansion of a gas
- Slow discharge of a battery
- The slow melting of ice where the temp diff between phases is infinitesimally small

Kelvin-Planck statement of the second law:

It is impossible to construct a cyclic device whose sole effect is to produce positive work whilst receiving heat from a single thermal reservoir.

A thermal reservoir is a body which can act as a source or a sink of heat.

We cannot convert all heat into work, but we can convert all work into heat.

Clausius statement of the second law:

It is impossible to construct a cyclic device whose sole effect is the transfer of heat from a cooler to a hotter body.

Heat cannot spontaneously pass from a colder body to a hotter.

We now adopt a new convention, where Q is positive in the direction of the arrows in a figure.

For a heat engine (A cyclic device for converting heat into work):

![Heat engine](Heat_engine.png)

$W=Q_1-Q_2$

Thermal efficiency $=\eta =\frac{W}{Q_1}=1-\frac{Q_2}{Q_1}=$ Useful work/heat input.

Carnot states that to achieve maximum efficiency, all processes within a cycle must be reversible. As well as this, all input heat should be at the same temperature as the hot reservoir, and all output heat should be the same temperature of the cold reservoir.

![Carnot cycle](Carnot_cycle.png)

First we apply the hot reservoir at $\approx T_1$. This is isothermal expansion. Then we adiabatically expand it until it is at $T_2$. Then we apply the cold reservoir at $T_2$. Then we compress it until it returns to $T_1$.

All processes must be slow and fully resisted and quasi equilibrium, with infinitesimally small temperature differences, hence reversible.

Carnot Efficiency: $\eta =1-\frac{T_2}{T_1}$

This is the maximum thermal efficiency of any cyclic heat engine operating between $T_1$ and $T_2$, which occurs when the process is reversible.

All reversible heat engines operating between the same thermal reservoirs are equally efficient.

We prove this by assuming there is a reversible heat engine and an irreversible heat engine, which produces more work than the reversible one, despite them being connected between the same heat sources.

We then reverse the one engine, and use part of the output work from the irreversible engine to power it. Then, consider the new system, we are taking heat from a cold source and converting it all into work. This clearly violates the second law, so cannot be true.

For all cyclic heat engines the efficiency is also $1-\frac{Q_2}{Q_1}$. Therefore:

$\frac{T_2}{T_1}=\frac{Q_2}{Q_1}$ or $\frac{Q_1}{T_1}=\frac{Q_2}{T_2}$.

All efficiencies are going to be lower than the theoretical max as they may not be reversible, or not all the heat transfer takes place at $T_1$ and $T_2$.

To analyse refrigerators and heat pumps, we consider the coefficient of performance.

For a fridge: $COP_R=$ heat from cold space/work input = $\frac{Q_2}{W}=\frac{Q_2}{Q_1-Q_2}$

For a heat pump: $COP_P=$ heat to hot space/work input = $\frac{Q_1}{W}=\frac{Q_1}{Q_1-Q_2}=1+COP_R$

The maximum COP can be found using the fact that $\frac{Q_1}{T_1}=\frac{Q_2}{T_2}$ for a reversible cycle.

The zeroth law: If systems B and C are separately in thermal equilibrium with system A, then they would be in thermal equilibrium with each other if brought into thermal contact.

This is vital to define temperature.

Empirical temperature scale: Using length of mercury in a column or the electrical resistance of a platinum wire for example

The ideal gas temperature scale: Connect a manometer to a gas at constant volume. The temperature is proportional to the pressure.

Using this we can extrapolate, and determine there must be an absolute zero, at -273.15 degrees.

Also, $\frac{Q_1}{Q_2}$ must be a function of some property in a heat engine and as it is dimensionless, the property must also be in that ratio. $\frac{Q_1}{Q_2}=\frac{T_1}{T_2}=\frac{\theta_1}{\theta_2}$

The fixed point used is the triple point of water.

Practically, we also use thermocouples and thermistors.

Efficiency, $\eta = 1 - \frac{Q_2}{Q_1}$ 
Maximum Carnot efficiency, $\eta_{REV} = 1 - \frac{T_2}{T_1}$

Therefore, $\frac{Q_1}{T_1} - \frac{Q_2}{T_2} \leq 0$
Or, using the formal thermodynamic signs of Q, $\sum \frac{Q_i}{T_i} \leq 0$
This is the Clausius inequality.

Generalised, this gives $\oint \frac{dQ}{T} \leq 0$
If its less than 0, the process is irreversible. If it is zero, the process is reversible. if its greater than zero, the process is impossible and violates the second law.

When tackling questions it's best to combine many systems into one to make your analysis easier.