Three main aspects are:
1. Generation
2. Transmission and distribution
3. Utilisation

The common thread which links all of them is the use of balanced three-phase a.c. systems at 50Hz

**Star-connected load**
![[StarConnected.png]]

The resulting three-phase supply is star-connected. The centre of the star is at 0V.

Consists of three voltages of equal magnitude, but differing in phase by 120 degrees with respect to each other.

We can draw a phase diagram where:
$\tilde{V}_A=Ve^{j0}=V$, $\tilde{V}_B=Ve^{-j\frac{2\pi}{3}}$, and $\tilde{V}_C=Ve^{j\frac{2\pi}{3}}$

Line voltages: Voltages between pairs of lines, e.g. 
$\tilde{V}_{AB}=\tilde{V}_A-\tilde{V}_B$

$|\tilde{V}_{AB}|=2|\tilde{V}_A|\sin(60)=\sqrt{3}V$
and $\angle \tilde{V}_{AB}=\angle \tilde{V}_A + 30\degree = 30\degree$
Line voltage = $\sqrt{3} \space \times$ phase voltage 

All of the loads are balanced too, with magnitude: $\overline{Z}$
So $\overline{I}_A=\frac{\overline{V}_A}{\overline{Z}}$, and $\overline{I}_B=\overline{I}_A e^{-j\frac{2\pi}{3}}$ and similar for $\overline{I}_C$

The current form a balanced three-phase set, and line current = phase current
All these currents sum to zero, so the current flowing from the centre of the impedance star to the centre of the supply star is zero.
So for a balanced 3-phase load it doesn't matter whether or not the neutral conductor is connected

If we consider the complex volt-amps in each phase, they are both equal to $\tilde{V}_A \tilde{I}_A^*=\overline{S}_A$
Therefore, for a balanced 3-phase load: P, Q and S are identical in each phase
$\overline{S}_{TOTAL}=3\overline{S}_A$

Total 3-phase P = 3 times P per phase
Total 3-phase Q = 3 times Q per phase
Total 3-phase S = 3 times S per phase

As each phases behaves identically, we only need to analyse one of them
![[SinglePhaseRepresentation.png]]

**Delta-connected load**

![[DeltaConnectedLoad.png]]
It is clear that the voltage across each phase of the load equals the line voltage

The load currents will form a balanced 3-phase set
$\tilde{I}_1=I$, $\tilde{I}_2=Ie^{-j\frac{2\pi}{3}}$, $\tilde{I}_3=Ie^{j\frac{2\pi}{3}}$
Trigonometry shows that the line currents (that is $\overline{I}_A$ for example) is $\sqrt{3}$ times the phase current.

![[StarDeltaComparison.png]]

Similarly, the supply could also be connected in delta since $\tilde{V}_A+\tilde{V}_B+\tilde{V}_C=0$
![[DeltaConnectSupply.png]]

The star-delta and delta-star transformations can be found in the data book.
For balanced loads: $\overline{Z}_{delta}=3\overline{Z}_{star}$

For both star-connected and delta-connected, $P=\sqrt{3}V_lI_l\cos(\theta)$, where $V_l$ and $I_l$ are the line quantities
Similar results apply to Q and S