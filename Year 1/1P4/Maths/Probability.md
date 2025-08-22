# Probability

$P(A \cup B)=P(A)+P(B)-P(A\cap B)$

$P(A \cap B)=P(B|A)P(A)$

The number of different orders in which n unique objects can be placed is $n!$.

The number of ways of choosing r items from n when the order of the chosen items matter $_nP_r=\frac{n!}{(n-r)!}$

The number of ways of choosing r items from n when the order of the chosen items does not matter $_nC_r=\frac{n!}{(n-r)!r!}$

Probability of r things from n things: $_nC_r p^r (1-p)^{n-r}$

Variance = $\sigma^2$, where $\sigma$ is the population standard deviation

Sample variance = $s^2$

Sample standard deviation, $s=\sqrt{\frac{\sum x_i^2-\mu (\sum x_i)^2}{n-1}}$

For a probability distribution:

Mean = $\mu=\sum x_j P(x_j)$

Variance = $\sigma^2=\sum (x_j-\mu)^2P(x_j)$

For a continuous probability distribution:

The probability of $(a \leq x \leq b)=\int_a^b f_x(x)dx$

The total integral should equal 1.

Mean = $\mu=\int_{-\infty}^{+\infty} x f_x(x)dx$

Variance = $\sigma^2=\int_{-\infty}^{+\infty} (x-\mu)^2f_x(x)dx$

Suppose x is a random variable with mean $\mu$ and standard deviation $\sigma$. We have n samples of x, where $\bar{x}$ is the average of these samples.

$\bar{x}$ is now a random variable. The mean of $\bar{x}$ is $\mu$. The standard deviation of $\bar{x}$ is $s_{(\bar{x})}=\frac{\sigma}{\sqrt{n}}$

The Normal distribution is a symmetric distribution with two parameters, its mean $\mu$ and standard deviation $\sigma$.

$P(z)=\frac{1}{\sqrt{2\pi\sigma^2}}\exp(-\frac{(z-\mu)^2}{2\sigma^2})$

The central limit theorem: if you add together a bunch of random variables, the sum will conform to this.

$95\%$ of the area lies within 2 standard deviations from the mean.
