If we have a controller K and a plant G, we could try making an arbitrary transfer function by setting $K=F/G$. However this would never work in practice as the knowledge of the transfer function of G is only approximate, and also the effect of disturbances would never allow it to be accurate.
Therefore we need feedback

![[Pasted image 20251107112045.png]]

We know have that $\bar{y}=\frac{GK}{1+HGK}\bar{r}+\frac{1}{1+HGK}\bar{d}_0+\frac{G}{1+HGK}\bar{d}_i$
The term $1+HGK$ appears as the denominator of all the closed-loop transfer functions. Therefore it determines the poles and hence the stability of the system

We call $L(s)=HGK$, where L is the return ratio of the loop or the loop transfer function.
The closed loop characteristic equation is $1+L(s)=0$
