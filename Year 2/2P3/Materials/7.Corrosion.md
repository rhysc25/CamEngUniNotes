Corrosion is the progressive attack of materials, typically metals, due to chemical interactions
Consider due to: Safety, economic cost, conservation.

In a solution, metallic ions will detach from the metal surface, leaving free electrons at the surface. If the electrons remain at the surface, an electric field develops and attracts back the ions towards the metal. This favours the inverse reaction until an equilibrium is reached.
The development of the electric field implies that the electrode takes a potential with respect to the solution.

**Measuring the Electrode Potential**
The potential will depend on the metal and its environment. To measure the surface potential one needs a reference electrode, such as the standard hydrogen electrode.
The standard potential $E^0$ is defined by the potential of a metal in a solution of its ions at a concentration of one mole per litre.

If you connect an electrode with a potential of +1 to one of -1 there will be a potential difference of 2V, provided a salt bridge acts across solutions to complete the circuit, allowing ions to flow one way as electrons flow the other.

In a half cell:
One compound is oxidised meaning that it is losing electrons, taking place at the anode.
One compound is reduced, meaning that it is gaining electrons, taking place at the cathode.

In the Daniell Cell:
Anode: $Zn\rightarrow Zn^{2+}+2e^-$
Cathode: $Cu^{2+}+2e^-\rightarrow Cu$
Overall reaction: $Cu^{2+}+Zn\rightarrow Zn^{2+} + Cu$

In a lemon, the cathodic reaction involves hydrogen ions

**Corrosion of Reactive Metals in Water**
Considering iron:
With acidic solutions, $H^+$ ions receive electrons, giving off $Fe^{2+}$
In neutral environments, overall reaction: $O_2+2H_2O+2Fe\rightarrow 2Fe^{2+}+4OH^-$

**Rust**
Iron corrosion in the presence of water and oxygen results in the formation of a solid oxide called rust
Iron ions and hydroxide ions first form together a ferrous hydroxide precipitate that deposits on the metal. This reacts with water to form a hydrated ferric oxide. This oxide adheres very poorly to the metal surface so flakes off.
$Fe^{2+}+2OH^-\rightarrow Fe(OH)_2$
$2Fe(OH)_2+(x-1)H_2O\rightarrow Fe_2O_3 \cdot xH_2O + 2H^+ + 2e^-$

In principle, the lower the standard potential, the more the metal will corrode. Aluminium has a very low potential, but is still strong, due to how strongly the oxide layer binds to the surface

Localised corrosion occurs when sites of the material promote the anodic reaction. This could be due to:
Defects in a protective coating, leading to pitting. Electrolyte present in crevices. Corrosion directly promotes crack growth.

To prevent corrosion:
Displace the anodic reaction
Control the environment so that the cathodic reaction is avoided
Insulating the path between the anodic and cathodic sites
Avoid water accumulation and salty environments

**Galvanic Corrosion**
If two metals of different electro-potential are connected in an electrolyte, the metal with the lower potential will be oxidised

Galvanic Compatibility -
To reduce this effect, we can try to only have contact between metals/alloys of a similar electro-potential

Galvanic Protection -
Coat a metal with a protective layer of zinc - as it has a very low potential. As long as the zinc is present, it will be preferentially corroded.

Sacrificial anodes -
A lump of zinc, with a very negative electro-potential, is electrically connected to another metal surface. This lump of zinc will end up corroding instead.

Impressed current protection -
For very large structures, sacrificial anodes are costly and may fail to deliver the necessary current to protect the cathode
Use a voltage source to generate the potential required. This makes the impressed current anode corrode. This can be replaced much easier than the main body

**Oxide Layers**
Thermodynamic considerations -
The standard Gibbs free energy of reaction, $\Delta G^0(P,T)$ = Energy of the product - Energy of the reactants
If $\Delta G^0(P,T)>0$, the reaction will not spontaneously happen, and the metal surface is stable

However, in a lot of cases, the size of $\Delta G^0(P,T)$ doesn't directly correlate to the rate of reaction. We must consider the kinetics of the oxidation formation

Three types of evolution that can be observed:
1) Linear loss: When the oxide does not stay at the surface or is volatile
2) Parabolic gain: When the oxide adheres to the metal and provides a barrier to the diffusion of reactants. The thicker the reactant, the slower it grows
3) Linear gain: When the oxide stays on the metal surface but cracks and allows oxygen to reach freely the metallic surface for further oxidation
![[Pasted image 20251103135022.png]]

Consider the formation of silicon oxide for use in MOSFETs:
The gas diffused through the oxide layer, and more oxide is formed at the oxide-silicon interface. There is an infinite supply of gas at constant concentration at the gas-oxide interface

We can say that $J_{diff}=J_{react}$. The diffusive flux of gas must balance the rate of reaction.
Considering Fick's law: $J_{diff}=D_{ox}\frac{c_g-c_s}{h}$
$J_{react}=kc_s$
From the definition of $J$: $dN=J_{react}Adt$ as J is per area per time
The volume $Adh$ of $dN$ moles of oxide is $Adh=\frac{M}{\rho}dN$
Combining all these equations we get: $h(t)=D_{ox}(\sqrt{\frac{2Mc_g}{\rho D_{ox}}t+\frac{1}{k^2}}-\frac{1}{k})$

Non-dimensionalising we get $\tilde{h}=(\sqrt{\tilde{t}+1}-1)$
If $\tilde{t}<<1$, the reaction rate is limited and $h$ grows linearly
If $\tilde{t}>>1$, the diffusion is limited, $h^2\propto t$, so parabolic profile
![[Pasted image 20251103140630.png]]

Cons of metal oxide layers:
Reduces lifetime, oxides have poor chemical properties (brittle), heterogeneities in the oxide layer can initiate fatigue and cracks
Pros:
Protect from corrosion ($Al_2O_3$), provide thermal insulation, reduce the coefficient of friction

Some metals, such as copper and aluminium, spontaneously form protective oxide layers, called a passivation layer
**Hot bluing**: protects iron or steel by placing the metal in a hot alkaline solution followed by an oil coating

The chromium in stainless steel provides a good $Cr_2O_3$ barrier film which protects the metal both against hot oxidation and aqueous corrosion. This barrier is self-healing.