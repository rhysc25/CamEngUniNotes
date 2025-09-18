**Revision**

The ideal Gas Turbine (Joule Cycle): 
Reversible compressor -> Reversible heat addition -> Reversible turbine
$\eta = \frac{\dot{W}_x}{\dot{Q}}=1-\frac{1}{r_p^{(\gamma - 1)/\gamma}}$, where $r_p$ is the compressor pressure ratio

This year we consider the 'real', irreversible heat engines, where viscous dissipation occurs in both the compressor and turbine

Reversible process are the theoretical ideal limit. Irreversible processes create entropy. 
Entropy convects like smoke. It is being continually created wherever something deleterious to machine efficiency is taking place
The difference between ideal and real power is set by the increase in entropy from inlet to exit

**1st law (Quantity of Energy):** $\dot{m}(h_2-h_1) = \dot{m}((h_2+\frac{1}{2}v_e^2)-(h_1+\frac{1}{2}v_i^2))=\dot{Q}-\dot{W}_x$
Assume zero velocity at inlet and exit unless told otherwise

For ideal gases: $h_2-h_1=c_p(T_2-T_1)$

**2nd law (Quality of Energy):** 
$\dot{m}(s_2-s_1)=\int \frac{d\dot{Q}}{T}+\dot{S}_{irrev}$

Insight into entropy:
* Differences in velocity can be removed reversibly by placing a miniature paddle wheel between the regions of high and low velocity
* Differences in temperature can be removed reversibly by placing a miniature Carnot cycle between the regions of high and low temperature
* Differences in pressure can be removed reversibly by placing a piston between regions of high and low pressure and extracting work as it moves. 
If these ‘differences’ are instead allowed to disappear spontaneously, without work extraction, by energy dispersal, then the process is irreversible, and entropy is created.

The lower the entropy, the higher the potential to do work and therefore the higher the 'energy quality'

Entropy is a measure of the number of ways energy can be distributed in a system of molecules

Considering $\dot{m}(s_2-s_1)=\int \frac{d\dot{Q}}{T}+\dot{S}_{irrev}$
If heat is added the number of possible ways of distributing the energy goes up, due simply to the fact that there is more energy. If the heat is added at a high temperature then the increase in the number of possible ways of distributing the energy is smaller, and the entropy rise is small.

$S=k_B\ln(\Omega)$

3 flow processes which create entropy:
* Viscous dissipation in boundary layers
* Viscous mixing of flows of different velocity
* Heat transfer across a finite $\Delta T$

Even though the $Tds$ equations are derived for a reversible process, because entropy is a property of state, they can also be used for irreversible processes. The two $Tds$ equations are:
$Tds=du+pdv \qquad \qquad Tds = dh-vdp$

In the databook:
$\Delta s = c_v \ln(\frac{T_2}{T_1}+R\ln(\frac{v_2}{v_1}))$

**2nd Law Analysis**

The relative value of heat compared to work is dependent on the temperature from which it comes, $T$, and the temperature of the environment $T_0$: 
$d\dot{W}_x=(1-\frac{T_0}{T})d\dot{Q}$
If $T \rightarrow T_0$, then $\dot{Q}$ is useless

The magnitude of the heat flow to the environment, $\delta \dot{Q}_0$ is set by the requirement that heat transfer to the environment is reversible

The maximum available power can be achieved when the process is reversible
![[ExtractingMaxWork.png]]

From the first law: $\dot{m}(h_2-h_1) =-\dot{Q}_0-(\dot{W}_x+\dot{W}_Q)$
From the second law: $\dot{m}(s_2-s_1)=-\frac{\dot{Q}_0}{T_0}$ as reversible

Therefore the maximum available power of flow from state 1 to 2 is  $\dot{W}_x+\dot{W}_Q=\dot{m}[(h_2-h_1) - T_0(s_1-s_2)]$
Rewriting gives $\dot{W}_{max12}=\dot{m}(b_1-b_2)=\dot{m}[(h_1-T_0s_1) - (h_2-T_0s_2)]$
Where b is defined as the specific steady flow availability function

The decrease in b is the maximum available power which can be extracted between states 1 & 2 per kg mass flow rate
$b=h-T_0s$

b is not a thermodynamic property as depends on $T_0$

The dead state is when the fluid is in equilibrium with the environment $p_0, T_0$
The specific steady-flow exergy $e$ is the difference between $b$ and $b_0$. Hence $e_0=0$

$\dot{W}_{max}=(\dot{H}_1-\dot{H}_0)-\dot{Q}_0$
Max available power = difference in enthalpy flow rate from dead state - energy flow rate unavailable for work (transferred to env)

Entropy flow rate fixes the energy flow rate unavailable for work:
$\dot{Q}_0=T_0(\dot{S}_1-\dot{S}_0)$

Combining prior equations gives:
$\dot{m}(b_2-b_1)=-\dot{W}_x+\int (1-\frac{T_0}{T})d\dot{Q}-T_0\dot{S}_{irrev}$
So the decrease in max available power consists or shaft power output, transfer of available power into the control volume, and loss of available power due to irreversibilities

Importantly: Loss of available power due to the irreversibility is given by $T_0\dot{S}_{irrev}$

$\Delta$ energy = $\Delta$ available energy + $\Delta$ unavailable energy
$\Delta \dot{H}_{12}=\dot{m}\Delta  b_{12} + \Delta \dot{Q}_{0_{12}}$
where 1 is inlet and 2 is exit, and $\dot{Q}_{0_1}=T_0(\dot{S}_1-\dot{S}_0)$

**Gas Turbines**

Real gas turbines:
* 2-4% pressure drop in combustor 
* Combustion changes gas composition
* The compressor and turbine contain irreversibilities (This is the main effect in real gas turbines so will be focused on)

![[IdealVsRealGasTurbine.png]]
$(\dot{W}_T)_{real}=\eta_T \times (T_3-T_{4s})$

![[GasTurbineVsJetEngine.png]]
The difference between a gas turbine and a jet engine

