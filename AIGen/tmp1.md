Recall that the DTFT of a sequence x[n] is defined as:

$X(e^{jω}) = \sum_{n=-\infty}^{\infty} x[n] e^{-jωn}$

1.

Substitute the given sequence:

2.

For x[n] = a<sup>n</sup> u[n], the DTFT becomes:

3.

$X(e^{jω}) = \sum_{n=-\infty}^{\infty} a^n u[n] e^{-jωn}$

4.

Apply the unit step function:

5.

The unit step function u[n] is zero for n < 0 and one for n ≥ 0. Therefore, the summation simplifies to:

6.

$X(e^{jω}) = \sum_{n=0}^{\infty} a^n e^{-jωn}$

7.

Recognize the geometric series:

8.

This is an infinite geometric series with the first term being 1 and the common ratio being $ae^{-jω}$.

9.

Apply the formula for infinite geometric series:

10.

The sum of an infinite geometric series converges if the magnitude of the common ratio is less than 1. In this case, the series converges if $|ae^{-jω}| < 1$, which simplifies to $|a| < 1$.

11.

When the series converges, its sum is given by:

12.

$\sum_{n=0}^{\infty} r^n = \frac{1}{1-r}$, for $|r| < 1$

13.

Applying this formula to our DTFT expression:

14.

$X(e^{jω}) = \frac{1}{1-ae^{-jω}}$, for |a| < 1

Therefore, the DTFT of x[n] = an u[n] is:

$X(e^{jω}) = \frac{1}{1-ae^{-jω}}$, for |a| < 1