The DTFT of a sequence $x[n]$ is given by:

$\tilde{X}(e^{j\omega}) = \sum_{n=-\infty}^{\infty} x[n]e^{-j\omega n}$1

Given the sequence $x[n] = n(0.9)^n u[n]$, we can calculate its DTFT $\tilde{X}(e^{j\omega})$:

●

$\tilde{X}(e^{j\omega}) = \sum_{n=-\infty}^{\infty} n(0.9)^n u[n]e^{-j\omega n}$

Since $u[n] = 0$ for $n<0$, we can change the limits of summation:

●

$\tilde{X}(e^{j\omega}) = \sum_{n=0}^{\infty} n(0.9)^n e^{-j\omega n}$

This summation can be solved using the following formula from the geometric series:

●

$\sum_{n=0}^{\infty} na^n = \frac{a}{(1-a)^2}$ for $|a| < 1$

In this case, $a = 0.9e^{-j\omega}$. Since $|0.9e^{-j\omega}| = 0.9 < 1$, we can apply the formula:

●

$\tilde{X}(e^{j\omega}) = \frac{0.9e^{-j\omega}}{(1-0.9e^{-j\omega})^2}$

Therefore, the DTFT of $x[n]$ is:

●

$\tilde{X}(e^{j\omega}) = \frac{0.9e^{-j\omega}}{(1-0.9e^{-j\omega})^2}$