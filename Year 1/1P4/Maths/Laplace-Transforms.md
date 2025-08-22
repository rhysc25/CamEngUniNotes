Laplace Transforms convert linear differential equations in to algebraic equations

Consider the function $g(t)$ which is defined for all $t\geq 0$, and 0 or undefined for $t < 0$
The Laplace transform of $g(t)$:
$$\overline{g}(s)=G(s)=L\{g(t)\}=\int_0^\infty g(t)e^{-st}dt$$
The lower limit of 0 is important in problems with boundary conditions
In general, $G(s)$ is a function of the complex variable s

E.g. if $g(t)=H(t)$, the Heaviside function, $G(s)=\frac{1}{s}$, where $\Re \{s\} >0$, so that the exponential converges
Or if $g(t)=e^{at}$, then $G(s)=\frac{1}{s-a}$, provided $\Re \{s\} >a$

All of the Laplace transforms are found in the data book

If we convert sines and cosines into exponentials we can simplify the transforming, as Laplace transforms are linear operations

The function $g(t)$ is uniquely defined by its Laplace Transform: $g(t) \leftrightarrow G(s)$ provided $g(t)=L^{-1}\{G(s)\}$

The derivative rule: We can evaluate $L\{\frac{dg}{dt}\}$ using the by parts formula, giving:
$$L\{\frac{dg}{dt}\}=sG(s)-g(0)$$
And subsequently:
$$L\{\frac{d^2g}{dt^2}\}=s^2G(s)-sg(0)-\dot{g}(0)$$

To solve differential equations: convert everything in the equation into its Laplace transform
Then rearrange the equation into a form that can be converted back

The Laplace Transform for a shift in s:
$L\{e^{-at}g(t)\}=G(s+a)$

The Laplace Transform for $t\times g(t)$:
$L\{tg(t)\}=-\frac{d}{ds}G(s)$

This can be shown pretty simply by $\frac{d}{ds}G(s)=\frac{d}{ds}\int_0^\infty g(t)e^{-st}dt=\int_0^\infty g(t)\frac{d}{ds}(e^{-st})dt$

In general $L\{t^n\}=\frac{n!}{s^{n+1}}$

## Partial Fractions

Only when the order of the polynomial on the denominator is larger than that of the numerator can we convert into partial fractions

Use the cover up rule!!

If the fraction comprises two even polynomials, substitute the variable, let $r=s^2$, and repeat as normal

With a repeated factor, e.g. $\frac{s+\alpha}{(s+a)^2}=\frac{A_1}{(s+a)}+\frac{A_2}{(s+a)^2}$

To evaluate these, we can find the coefficient of highest order using the cover up rule, then subtract that, simplify and repeat

If the numerator is of larger order than the denominator, we need to do polynomial division
To do this, quantify the expression when s is very large, e.g. $\frac{5s^3+2}{(s+1)(s+2)} \approx \frac{5s^3}{s^2} = 5s$
Subtract this, simplify and repeat, until you have something like $5s-15+\frac{32+35s}{(s+1)(s+2)}$

## Delta Functions

In order to allow us to use Laplace Transforms with delta impulse functions, we need to redefine the Laplace transform: $L\{g(t)\}=\int_{0^-}^\infty g(t)e^{-st}dt$
This subtle change to $0^-$ means we are evaluating functions in the limit of 0 from the negative side, so the delta function equals 1

Using this, we know that $L\{\delta (t)\}=\int_{0^-}^\infty \delta(t)e^{-st}dt=e^{-s 0^{-}}=1$

Now whenever we evaluate functions we must use the $0^{-}$ convention
To apply a time shift of time $T$ we must multiply the transform by $e^{-sT}$, so  $e^{-sT}G(s)$

If we want a time pulse, we can use a superposition of two step function transforms, so $\frac{1}{s}-\frac{1}{s}e^{-Ts}$

We can solve simultaneous differential equations with Laplace transforms quite simply, by turning both into purely algebraic simultaneous equations, and solving for one of the variables

If we apply the Laplace Transform to the convolution integral, we get:
$$L\{\int_0^t f(\tau)g(t-\tau)d\tau\}=L\{f(t)\}L\{g(t)\}$$
So you just simply multiply the transforms of the two functions together





