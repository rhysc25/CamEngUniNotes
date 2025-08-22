A system has a fixed mass, a control volume has a fixed volume but not necessarily mass
Mass crosses the control surface, the surface of the control volume
The properties are not usually uniform in a CV

A flow is unsteady if there is accumulation or depletion of mass in a control volume
$$\sum_{in}\dot{m}_i-\sum_{out}\dot{m}_e=\frac{dm_{cv}}{dt}$$
If we account for the conservation of energy we get the non-steady flow energy equation:
$$\delta Q-\delta W_x=\delta E_{cv}+\sum_{out}\delta m_e (h_e+\frac{1}{2}V_e^2 +gz_e)-\sum_{in}\delta m_i (h_i+\frac{1}{2}V_i^2 +gz_i)$$
Where $h=u+pv$ is the specific enthalpy, which accounts for all the displacement work

$Q$ and $W$ follow the sign convention previously established
$W_x$ may include electrical power output
If the flow is steady, then the term $\frac{dE_{cv}}{dt}=0$

Both $u$ and $h$ have arbitrary constants, defined at absolute zero, so $u=u_0+c_vT$ and $h=h_0 +c_pT$ but this can be manipulated to give $h=u_0 + c_pT$, allowing them to be compared without worrying about constants

## Steady Flow

Steady implies no accumulation of mass, energy or entropy inside the device

$\sum_{in}\dot{m}=\sum_{out}\dot{m}$
For just one stream, $\dot{m}_i=\dot{m}_e=\dot{m}=\rho A V_n$
Where $\rho$ is normally found by $p/RT$

The steady flow energy equation for a single stream:
$q-w_x=(h_e+\frac{1}{2}V_e^2 +gz_e)-(h_i+\frac{1}{2}V_i^2 +gz_i)$
Where $w_x$ is the net shaft work output per kg

The pitot pressure is the stagnation pressure, the static pressure due to depth plus the dynamic head due to velocity, whereas just tapping a pressure from the wall gives static pressure only

The shaft work output may not be as calculated because:
* The temperature and velocity profiles may not be uniform
* The mass flow rate may be less due to boundary layers on the wall

A throttling process is locally unsteady but globally steady, so can be treated as a steady flow process. There is no shaft work, and it's adiabatic, so is also isenthalpic

For throttling, all the change in entropy is irreversible change in entropy.

For a perfect gas, an isenthalpic process is also an isothermal one
For real gases it isn't, and the temperature may rise or fall

Turbines and compressors are globally steady flow devices
Turbines have a pressure drop through them and produce shaft work
Compressors have a pressure rise and absorb shaft work


If we apply the Second Law to the control volume, for an unsteady flow we get that:
$$\frac{dS_{CV}}{dt}+\sum_{out}\dot{m}_es_e-\sum_{in}\dot{m}_is_i=\sum\frac{\dot{Q}_j}{T_j}+\dot{S}_{IRREV}$$
If the flow is steady, then the first term disappears:
$$\sum_{out}\dot{m}_es_e-\sum_{in}\dot{m}_is_i=\sum\frac{\dot{Q}_j}{T_j}+\dot{S}_{IRREV}$$
With just one inflow and outflow:
$$s_e-s_i=\sum\frac{q_j}{T_j}+s_{IRREV}$$
If we want to determine the direction of flow in a pipe, we can start by assuming it's going one way, then evaluate $s_{IRREV}$. If this is negative, we know it must be going the other way

For a steady and reversible flow in a control volume, with one inlet and outlet:
$s_e-s_i=\sum \frac{q_j}{T_j}$, which is just $ds=\frac{dq}{T}$

If we use this, integrate the Tds equation, and sub into the SFEE:
$-w_x=\int_i^e vdp +(\frac{1}{2}V_e^2+gz_e)-(\frac{1}{2}V_i^2+gz_i)$
This shows that shaft work is related to $\int vdp$

For an incompressible fluid, $\rho$ is constant, so $v=\frac{1}{\rho}$ is a constant, so $\int vdp = \frac{p_e-p_i}{\rho}$

The flow is incompressible when the working fluid is a liquid, or when the working fluid is a gas with a small velocity
$V < 0.3\times \sqrt{\gamma RT}$, so 0.3 times the speed of sound

With a bit of rearranging, this also means that $\frac{\Delta p}{\rho} < 5\% \frac{p}{\rho}$

The difference between actual power input and minimum power input, $\dot{W}_{act}-\dot{W}_{min}=\dot{m}T\Delta s$, so proportional to the increase in specific entropy

If the flow is steady, reversible, and adiabatic, then the equation simplifies to $s_e=s_i$, so is also isentropic

We are going to assume turbines and compressors are reversible for this year, and the processes happen fast so adiabatic, so we can use the reversible isentropic relations





