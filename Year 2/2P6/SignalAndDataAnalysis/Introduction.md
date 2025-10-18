Nyquist sampling theorem - Shows it is possible to reconstruct an original analogue signal perfectly from correctly digitised data

The total energy of a signal $f(t)$: $E_f=\int_{-\infty}^{\infty}|f(t)|^2dt$
Often more convenient to compute as a limit: 
$E_f=\lim_{T\rightarrow \infty}\int_{-T/2}^{+T/2}|f(t)|^2dt$

Average power estimated over the whole time interval:
$P_f=\lim_{T\rightarrow \infty}\frac{1}{T}\int_{-T/2}^{+T/2}|f(t)|^2dt$

For a decaying signal, energy is well defined but power goes to zero.
For a constant signal, energy is infinite but power is well defined.
For a signal with unbounded growth, energy is infinite and power is undefined

Delta functions are key to signal analysis. Infinitely narrow and infinitely tall, with an area of 1 under the spike.

Ideal sampling tool, picking out the value of a function at a specific point.
Sifting property:
$\int_{-\infty}^{\infty} g(t) \delta (t-a)dt=g(a)$

Other functions in their limit become the delta function. For example if we consider $sinc(t)$, that is $\frac{\sin(t)}{t}$.
$\frac{\sin(at)}{\pi t}$ becomes the delta function as $a \rightarrow \infty$

We can use this result to evaluate the following integral:
$I=\int_{-\infty}^{\infty}\exp(j\omega t)d\omega=\lim_{A\rightarrow \infty}\int_{-A}^{A} \exp(j\omega t)d\omega$

Standard integration gives $\lim_{A\rightarrow \infty}(a\frac{\sin(At)}{t})$
Which is $2\pi \delta(t)$

This turns on oscillating function into a generalised delta function at the limit:
$\int_{-\infty}^{\infty}\exp(j\omega t)d\omega=2\pi \delta(t)$




