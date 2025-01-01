The magnitude and phase spectra of the signal $x_1(t) = (1 - t^2)[u(t) - u(t - 1)]$ can be determined by calculating its Fourier Transform $X(F)$ and then plotting its magnitude $|X(j2\pi F)|$ and phase $\angle X(j2\pi F)$.

Here are the steps:

●

Determine the Fourier Transform X(F) of x1(t):

●

The Fourier Transform of a continuous-time signal $x(t)$ is given by:

●

$X(F) = \int_{-\infty}^{\infty} x(t)e^{-j2\pi Ft}dt$

●

For $x_1(t)$, this becomes:

●

$X(F) = \int_{-\infty}^{\infty} (1-t^2)[u(t)-u(t-1)]e^{-j2\pi Ft}dt$

●

Since $u(t) - u(t-1)$ is 1 for 0 ≤ t ≤ 1 and 0 otherwise, the integral simplifies to:

●

$X(F) = \int_{0}^{1} (1-t^2)e^{-j2\pi Ft}dt$

●

Evaluating this integral, we get:

●

$X(F) = \frac{1}{j2\pi F} + \frac{2e^{-j2\pi F}}{(j2\pi F)^2} + \frac{2(e^{-j2\pi F}-1)}{(j2\pi F)^3}$

●

Compute the magnitude spectrum |X( j_2_πF)|:

●

The magnitude spectrum is the absolute value of the Fourier Transform:

●

$|X(j2\pi F)| = \left| \frac{1}{j2\pi F} + \frac{2e^{-j2\pi F}}{(j2\pi F)^2} + \frac{2(e^{-j2\pi F}-1)}{(j2\pi F)^3} \right|$

●

Compute the phase spectrum ∠_X_( j_2_πF):

●

The phase spectrum is the angle of the Fourier Transform:

●

$\angle X(j2\pi F) = arg\left( \frac{1}{j2\pi F} + \frac{2e^{-j2\pi F}}{(j2\pi F)^2} + \frac{2(e^{-j2\pi F}-1)}{(j2\pi F)^3} \right)$

●

Plot the magnitude and phase spectra:

●

Using the obtained expressions for the magnitude and phase spectra, we can plot them as functions of frequency F.

This problem is similar to problem 24(a) in the sources. Problem 24(a) asks for the magnitude and phase spectra of the signal $x_1(t) = (1 - t^2)[u(t) - u(t - 1)]$, and Figure 4.23 provides the corresponding plots. The source demonstrates how to find the Fourier Transform of a similar signal and then obtain the magnitude and phase spectra.