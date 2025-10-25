For an asymptotically stable system:
When we input a sinusoidal signal into an LTI system, the output (after transience has decayed) is a similar sinusoid but with:
1) Magnitude scaled by $|G(j\omega)|$
2) Phase shift by arg $G(j\omega)$

This can be proven by setting the input of a system of differential equations to $u=e^{j\omega t}$ and its output to $y(t)=Ye^{j\omega t}$
Solving for $Y$ gives it to be the same as the transfer function $G(s)$ but with $s$ set to $j\omega$
