Communication: Process of delivering information from source to destination through a communication channel

Multiple access channel: Multiple sources to one destination
Broadcast channel: One source to multiple destinations

Transmitter: translates information into a suitable signal
Channel: Medium used to transmit signal
Receiver: reconstructs the information from the received signal

Important properties of signals for communication:
1. Power
2. Bandwidth

**Signal Energy**
The energy of a signal $x(t)$ is defined as:
$E_x=\int_{-\infty}^{\infty}|x(t)|^2dt$
Squaring magnitude gives instantaneous power or something analogous

If $X(\omega)$ is the Fourier transform of $x(t)$, from Parseval's theorem we know that:
$E_x=\int_{-\infty}^{\infty}|x(t)|^2dt=\frac{1}{2\pi}\int_{-\infty}^{\infty}|X(\omega)|^2d\omega=\int_{-\infty}^{\infty}|X(\omega)|^2df$

$|X(f)|^2$ is the energy spectral density.
We can this of $|X(f)|^2df$ as the energy of the signal in the frequency band $[f,f+df]$

**Signal Power**
For a signal $x(t)$ whose energy is infinite, the power is defined as:
$P_x=\lim_{T\rightarrow \infty} \frac{1}{T}\int_{-T/2}^{T/2}|x(t)|^2dt$

Signal power is important because:
* We usually care about transmit power, the energy of the transmitted signal per unit time
* Lower transmit power means longer battery life
* Lower transmit power also makes signal harder to detect at the receiver in the presence of noise
* Need clever Tx + Rx designs that make judicious use of available transmit power

**Bandwidth**
The bandwidth of a signal is roughly the range of frequencies over which its spectrum (Fourier transform) is non-zero

Fourier Transforming the signal: $X(f)=\int x(t)e^{-j2\pi ft}dt$
Similarly: $X^*(f)=\int x^*(t)e^{j2\pi ft}dt$
From this we can see that is $x(t)$ is real, then $X^*(f)=X(-f)$

**Baseband**
![[BandwidthSignal.png]]

For real signals, bandwidth measured as the range of positive frequencies as $|X(f)|$ is symmetric around 0. Specified in Hz

A signal is called low-pass or baseband if its spectral content is centred around $f=0$.
The bandwidth of the baseband signal above is W

**Passband**
![[Passband.png]]
