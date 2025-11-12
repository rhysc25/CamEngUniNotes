Can we design an ideal power plant using steam as the working fluid?
Problems: developing pumps that work in the 2 phase region
Heat is transferred from hot combustion products that are at constant p

To stop the first problem, we create the Rankine cycle:
![[Pasted image 20251030200424.png]]
However the turbine is still largely in the two phase region, so we go for the superheated Rankine cycle
![[Pasted image 20251030200517.png]]
This is much better now, also because the average temperature at which heat is added is higher, so the cycle is much more efficient

We are trying to reject heat at the coldest temperature possible, as close to $T_{atm}$

All steam cycles are based on the Rankine cycle which is a true thermodynamic cycle. This is used in many things - combustion of fossil fuels, nuclear reactors

How to perform calculations throughout the Rankine cycle:
* Pump 1-2: $w_p=h_2-h_1$
* Boiler 2-3: $q_{in}=h_3-h_2$
* Turbine 3-4: $w_t=h_3-h_4$
* Condenser 4-1: $q_{out}=h_1-h_4$
$\eta_{thermal}=\frac{w_t-w_p}{q_{in}}=\frac{w_{net}}{q_{in}}$
This is all assuming that the turbine and pump 

State 1: Saturated liquid - Just look up $h_1$
State 1-2: Assume density is constant: $-w_x=h_2-h_1=\int vdp = v_{f1}(p_2-p_1)$
Then calculate $h_2=h_1+w_p$
State 2-3: Superheated steam at 20MPa and a given temp. Look up in table to find $h_3$, then $q_23=h_3-h_2$
State 3-4: Isentropic so $s_4=s_3$
From tables get $s_3$. From tables at $p_4$, find $s_f$ and $s_g$
$x=\frac{s_4-s_f}{s_g-s_f}$ from the lever rule
Then do $h_4=h_f+xh_g$ to find $h_4$, then $w_t=h_3-h_4$
Now we can find $\eta_{thermal}$

The work input required to compress the liquid water is very much less than the work output of the turbine, $w_p<<w_t$
$T_{hot}$ is quite low, but this is compensated by the fact that the temperature at which heat is rejected is also very low

**Irreversible Rankine cycle**
![[Pasted image 20251030213205.png]]
We can calculate $h_4$ using $h_{4s}$ and the isentropic efficiency

Alternatively we can use a h-s diagram to simplify the analysis. 
![[Pasted image 20251030213501.png]]
Find where p=const and T=const lines meet at 3, trace down to $p_4$, to find $h_{4s}$.
Use this and the efficiency equation to find $h_4$. Follow this to $p_4$ line and then read off dryness fraction x

There are two ways to increase the efficiency of the cycle:
1) Raise the temperature where Q is added and lower the temperature where Q is rejected. 
2) Reduce irreversibility

Steps:
* Lower the condenser pressure: Lowers the temperature at which heat is rejected. This is good, but there's a limit to how low it can go. There is a possibility of air leaking in if we lower it below $p_{atm}$. It also means the turbine becomes more two phase

* Superheat the steam to higher temperatures: Average temperature of $Q_{in}$ rises. This makes the turbine become less two phase. However there is a limit on how high the temperature can go before the metal melts

* Increase the boiler pressure: Raises the temperature of $Q_{in}$. However the peak T is limited so the turbine operates more in the two phase region.
![[Pasted image 20251031163745.png]]

**The Ideal Reheat Rankine cycle**
If we let the temperature fall a bit at point 3, then we extract work, then we put it back into the boiler, we can make sure the turbine is working less in the two phase region. It also means the average temperature at which heat is added is greater.

The optimal reheat pressure is about a quarter of the max pressure

Any more than 2 reheats has diminishing returns, and becomes too complex to design, so cost would start to outweigh benefit

**Second Law Analysis**

Shaft power = transfer of available power due to heat transfer - lost available power due to irreversibilities
$\dot{W}_x=\int (1-\frac{T_0}{T})d\dot{Q}-T_0\dot{S}_{irrev}$

Considering irreversibilities:
Assuming pump and turbine are isentropic:
$T_0s_{irrev(1-2)}=T_0s_{irrev(3-4)}=0$
$T_0s_{irrev(2-3)}=T_0(-\frac{q_{in}}{T_{hot}}+(s_3-s_2))$
$T_0s_{irrev(4-1)}=T_0(\frac{q_{in}}{T_{cold}}+(s_1-s_4))$

The way we increase efficiency further is by providing the heat using a gas turbine. This is the combined Gas-vapour cycle.
![[Pasted image 20251031165319.png]]
The heat transfer happens in a HRSG, a heat recovery steam generator. One is heated while the other is cooled
Inside the HRSG:
![[Pasted image 20251031165522.png]]
X is the fraction of heat transferred. The pinch point is the point at which the temperatures are closest. You can see from 2-3, the liquid undergoes a phase transformation to vapour.



