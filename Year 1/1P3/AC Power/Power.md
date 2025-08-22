# AC Power - Power

$v(t)=\hat{V}\cos(\omega t+\alpha)$, $i(t)=\hat{I}\cos(\omega t+\beta)$

In phasor notation: $\tilde{V}=V\exp(j\alpha)$, $\tilde{I}=I\exp(j\beta)$

In AC power the magnitude of phasors are always their RMS values.

$p(t)=v(t)i(t)$, having twice the frequency of the voltage.

With a bit of manipulation, $P=VI\cos(\alpha - \beta)=VI\cos(\phi)$

$\phi$ is the angle of the voltage with respect to the current.

The $\cos(\phi)$ term is the power factor.

Positive $\phi \Rightarrow$ I lags V. Inductive load

Negative $\phi \Rightarrow$ I leads V. V lags I. Capacitive load

Resolve the current into two components: one in phase with the voltage (the direct component) and one 90° out of phase with the voltage (the q component).

Active/real power = $P=VI\cos(\phi)$

Reactive power = $Q=VI\sin(\phi)$ Units: VAR

Apparent power = $\sqrt{P^2+Q^2}$. Units: VA.

Apparent power, $S$. $S\cos(\phi)=P$

Resistors do not consume any reactive power.

Inductors only consume reactive power.

Capacitors only generate reactive power.

![Power triangle](Power%20triangle.png)

"Power loss" refers solely to real power.

Reactance, X, of an inductor = $\omega L$. Reactance of a capacitor, $X_C = \frac{1}{\omega C} \Rightarrow Z_C=-jX_C$

First find the overall load current in polar form, then plug into reactive and real power equations.

Alternatively: Find P/Q = VI for the capacitor/resistor/inductor, as you know only resistor consumes real power, only inductor consumes reactive power, and only capacitor generates reactive power (using X, the reactance, instead of Z).

$\tilde{V}=Ve^{j\alpha}$, $\tilde{I}=Ie^{j\beta}$, $\tilde{I}^*=I e^{-j\beta}$

$\Rightarrow \tilde{V} \tilde{I}^*=P+Qj$

$\bar{S}$, apparent power (Unit: VA) $=P+Qj \Rightarrow |\bar{S}|=S=\sqrt{P^2+Q^2}$
