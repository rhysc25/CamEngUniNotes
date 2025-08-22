# Functions and Series Approximations

Taylor series: $f(x)=f(a)+f'(a)(x-a)+\frac{f''(a)}{2!}(x-a)^2+...$
If $a=0$ it is a Maclaurin series.

Using series expansions as approximations:
Eg. if we want $1\%$ accuracy from our small angle approximation expression for $\cos(x)$, we would consider the next term:
$\frac{x^4}{24}<\cos(0) \times 0.01$

For very large $x$, create a series approximation in $y$, where $y=\frac{1}{x}$

To evaluate a limit, we can use L'Hopitals rule: $$\lim_{x \to 0}\frac{f(x)}{g(x)}=\frac{f'(x)}{g'(x)}$$
But this is rarely used, and most of the time we will just use series approximations to determine the limit.
