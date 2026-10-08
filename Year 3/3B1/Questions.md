Why do we need to impedance match our antennas? What does it do to our VSWR?

To prevent reflection of our signal waves. VSWR is Vmax/Vmin due to the reflection, so we want it to be small, as close to 1 as possible.

Why do we need to modulate our signal before transmitting, and how to we modulate it?

We must modulate our signal as an antenna suited for long wavelength waves would be massive. In AM, we modulate it with a carrier of the form $\cos(\omega t)$. We apply a DC offset to our signal $x(t)$ and then multiply with the carrier to get: $[a_0+x(t)]\cos(\omega t)$

What is the modulation index in AM?

The peak amplitude of $x(t)/a_0$. It is the variation of the carrier amplitude, so $\pm 50\%$ if $0.5$. You find it by $\frac{A_{max}-A_{min}}{A_{max}+A_{min}}$, and should be between 0 and 1 for normal AM
