Top level hierarchy of processing functions in design:
* Primary shaping
* Secondary processes
* Joining 
* Surface treatment

For primary shaping processes, the most important attributes that we will have to consider:
Technical attributes:
* Material class: Materials to which processes can be applied to
* Shape class: Shapes the process can make
* Mass: Limit on mass the process can handle
* Section thickness: Upper and lower dimensional limits
* Tolerance: Dimensional precision
* Roughness: Surface finish

To find information about these and to eliminate certain processes, look in the materials data book
Production outside of the given ranges is still possibly, just a lot more expensive

Shape-process compatibility:
* Prismatic shapes: Rolling, extrusion
* Sheet: Sheet metal forming
* 3D: Casting, forging, powder, moulding, machining

The general cost equation:
Cost per part = $C=C_m+\frac{C_c}{n}+\frac{\dot{C_L}}{\dot{n}}$
Where:
* Material cost, $C_m$ - includes consumables
* Tooling cost, $C_c$ - dedicated tooling
* Overhead cost, $\dot{C_l}$
* Batch size, $n$ - total number being made
* Production rate, $\dot{n}$ - number/hour which can be made

Different processes can have different costs per part based on the batch size so you will have to take this into account

The consumption rate, C is modelled as an exponential grown
The growth rate is $r\%$ per year
$\frac{dC}{dt}=\frac{r}{100}C$
Initial consumption = $C_0$ at time $t_0$
This gives $C=C_0\exp{(\frac{t(t-t_0)}{100})}$



