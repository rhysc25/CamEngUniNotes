The entropy of a system is an extensive thermodynamic property
$$S_2 - S_1 = \int_1^2 (\frac{dQ}{T})_{REV}$$
The integration must be carried out over a reversible path
Only changes of entropy are defined, and only for a reversible process

The change of entropy is independent of the reversible path. It doesn't matter how we get there

For an infinitesimal process, $dQ_{REV} = T dS$
The area under the T-S curve is Q

For a cyclic and reversible process, $\oint dQ = \oint dW$ and $dW = pdV$
So $\oint TdS = \oint pdV$. The area enclosed by the cyclic and reversible T-S plot is the same as the area enclosed by the P-V plot, both equal to the work done.

Now imagine one of the parts of the cycle is irreversible. An irreversible process cannot be full resisted to technically cannot exist on the pV plot, the properties are not defined when not in equilibrium.

$dS = \frac{dQ}{T}+dS_{IRREV}$
$dS_{IRREV} \ge 0$ always, and is essentially the entropy increase due to irreversibility

The only way to reduce the entropy of a closed system is to extract heat

The value of $\Delta S$ can be used even if the process is irreversible, as it is the same for all paths

From the first law, we can form these equations:
$TdS=dU+pdV$
$H = U+pV \Rightarrow dH = dU + pdV + Vdp \Rightarrow$
$TdS = dH - Vdp$

As they are functions of properties only, they apply to all processes, reversible and irreversible

For a perfect gas, we can rearrange to give results like:
$\Delta s = c_v \ln{T_2/T_1} + R\ln{v_2/v_1}$
and so on, given in the data book

## Drawing T-s diagrams

For constant pressure, $dp = 0$ so $Tds = dh$
$dh = c_p dT$, therefore:
$$\frac{\partial T}{\partial s}|_p=\frac{T}{c_p}$$
The slope of a constant pressure line on a T-s diagram is proportional to temperature
This corresponds to an exponential curve on the T-s diagram. 

With a bit of rearranging, it can be shown that:
$$\frac{\partial T}{\partial s}|_v=\frac{T}{c_v}$$
As $c_v$ is smaller, the lines of constant volume are steeper

From the equation $dS = \frac{dQ}{T}+dS_{IRREV}$, it is clear than if we know any two of the conditions adiabatic, reversible and isentropic to be true, then we know the third must also be true
If a system is closed then $dQ=0$, so entropy can only increase

Irreversible entropy increases can be due to things such as the expansion not being fully resisted or pressure drops.
We can calculate the work for an equivalent reversible system, to find the lost work due to irreversibility
The lost work is always $w_{rev}-w=T_a \Delta s_{irrev}$, where $T_a$ is the ambient temperature

If you are analysing an irreversible process, try and split it into two reversible processes. The entropy change for any path is the same.



