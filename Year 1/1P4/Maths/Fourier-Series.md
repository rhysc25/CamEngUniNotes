# Fourier Series

We want to express functions as a linear combination of sines and cosines, ie. a Fourier series.

We want to represent $f(t)$ in the range $-\pi$ to $\pi$ using orthogonal basis functions. To represent functions we need an infinite number of basis functions, $\cos(nt)$ and $\sin(nt)$ where n is an integer.

All are essentially periodic with a period of $2\pi$.

Functions, $p(t)$ and $q(t)$ have infinite components. The equivalent to a dot product, summed over all elements, is $\int^\pi_{-\pi}p(t)q(t)dt$

The Fourier series, to represent $f(t)$ between $-\pi$ and $+\pi$:

$f(t)=\sum a_n \cos(nt)+\sum b_n \sin(nt)+d$

To find the coefficients:

$a_n=\frac{\int_{-\pi}^\pi \cos(nt)f(t)dt}{\int_{-\pi}^\pi \cos(nt)\cos(nt)dt}=\frac{1}{\pi}\int_{-\pi}^\pi \cos(nt)f(t)dt$

$b_n=\frac{1}{\pi}\int_{-\pi}^\pi \sin(nt)f(t)dt$

$d=\frac{1}{2\pi}\int_{-\pi}^\pi f(t)dt$

Any range of length $2\pi$ will do, like $0$ to $2\pi$. However, we are only modelling the function in this range, and the Fourier model will repeat this with a period of $2\pi$. If the function we are modelling is not periodic this will obviously be incorrect.

The $a_n$ terms model all the even components in the function. If there is no even component, all $a_n=0$.

The $b_n$ terms model all the odd components in the function. If there is no odd component, all $b_n=0$.

If the function we are modelling has a mean of 0 in the specified range of the Fourier series, then $d=0$.

We are considering the odd or even characteristics of the function we are modelling, not the Fourier series it will become.

Obviously if the function you are modelling can already be converted to $\cos(nt)$ or $\sin(nt)$ using a trigonometric identity, do it.

In order to model a function over an arbitrary range $L$, we make the substitution $\frac{2\pi x}{L}=t$, and $\frac{2\pi}{L}dx=dt$.

This makes the coefficients: $a_n= \frac{2}{L}\int_{0}^L \cos(\frac{2\pi nx}{L})f(x)dx$ and so on.

The fraction $\frac{2\pi}{L}$ is often written as $\omega_0$ and called the fundamental angular frequency.

The Fourier series will repeat every $L$.

For certain functions, such as a sawtooth function, it may be easier to differentiate twice, obtaining an impulse function. This will most likely have a mean of zero, and will either be odd or even, so you will only have to consider $a_n$ or $b_n$.

We do not want to choose an integration range where there is an impulse function on the boundary, so we can just shift the integration range.

This will be an easier integration, as the sifting theorem applies, so you will most likely just be integrating a sinusoid.

3 ways to find the Fourier series for an arbitrary period: Direct integration using the coefficient equations. Determining the second derivative, an impulse function, finding the Fourier series and integrating. Using the data book.

When we use the data book cases, we may have to change the range, or shift the function, or scale it.

For many sinusoidal cases, symmetry may mean that eg. $b_n=0$ when $n$ is even. This will simplify your analysis.

If only the odd terms are non-zero, in the formula for $b_n$, we can replace $n$ with $2m-1$.

Fourier series for delta functions don't converge.

If the function is value discontinuous, eg. square wave, the Fourier series converges as $\frac{1}{n}$.

If the function is gradient discontinuous, eg. triangular wave, the Fourier series converges as $\frac{1}{n^2}$.

If the function has a discontinuous second derivative, the Fourier series converges as $\frac{1}{n^3}$.

The smoother the function, the faster the Fourier series converges.

If we only care what our function does within specific bounds, we can choose any function with the same behaviour in that interval, but so as to make the series converge faster, eg. continuous.

Pick the Fourier series period so as to get good convergence and a series that is easy to calculate.

Instead of sinusoidal basis functions, we can replace them all with $e^{int}$, with n taking integer values from $-\infty$ to $\infty$.

This is easier to evaluate.

$f(x)=\sum_{-\infty}^\infty c_ne^{inx\frac{2\pi}{L}}$

$c_n=\frac{1}{L}\int_0^Le^{-inx\frac{2\pi}{L}}f(x)dx$

$$c_n= \begin{cases} 
      d & , n = 0  \\
      (a_n-ib_n)/2) & , n = 1,2,3... \\
      (a_{-n}+ib_{-n})/2 & , n = -1, -2, -3...
   \end{cases}$$

From this we can see that:

$a_n=2\Re(c_n)$

$b_n=-2\Im(c_n)$

$d=c_0$
