
### 5b

Here's how to use the geometric series to solve the DFT of _x[n] = 4 sin(0.2πn)_, with _N = 10_:

**1. Express the Sine Function in Terms of Complex Exponentials**

Recall Euler's identity:

- $sin(\theta) = \frac{e^{j\theta} - e^{-j\theta}}{2j}$

Applying this to the given sequence:

- $x[n] = 4 sin(0.2\pi n) = 4 * \frac{e^{j0.2\pi n} - e^{-j0.2\pi n}}{2j} = \frac{2}{j} * (e^{j0.2\pi n} - e^{-j0.2\pi n})$

**2. Substitute into the DFT Formula**

The DFT formula is:

- $X[k] = \sum_{n=0}^{N-1} x[n] * e^{-j(\frac{2\pi}{N})kn}$

Substituting our expression for _x[n]_, with _N = 10_:

- $X[k] = \sum_{n=0}^{9} (\frac{2}{j} * (e^{j0.2\pi n} - e^{-j0.2\pi n})) * e^{-j(\frac{2\pi}{10})kn}$
- $X[k] = \frac{2}{j} * \sum_{n=0}^{9} (e^{j0.2\pi n} * e^{-j0.2\pi kn} - e^{-j0.2\pi n} * e^{-j0.2\pi kn})$
- $X[k] = \frac{2}{j} * \sum_{n=0}^{9} (e^{-j0.2\pi (k-1)n} - e^{-j0.2\pi (k+1)n})$

**3. Apply the Geometric Series Formula**

The finite geometric series formula is:

- $\sum_{n=0}^{M-1} a^{n} = \frac{1-a^{M}}{1-a}$

Applying this to our DFT expression:

- $X[k] = \frac{2}{j} * [\frac{(1 - e^{-j0.2\pi (k-1) * 10} )}{(1 - e^{-j0.2\pi (k-1)})} - \frac{(1 - e^{-j0.2\pi (k+1) * 10})}{(1 - e^{-j0.2\pi (k+1)})}]$

**4. Simplify**

Notice that terms like $e^{-j0.2\pi (k-1) * 10}$ simplify to 1 because the exponent is a multiple of _2π_. You can further simplify the expression using Euler's identity and trigonometric identities. However, the key point is that the geometric series formula helps you evaluate the summation in the DFT calculation when you have exponential terms.


4. Simplify

●

Recall the expression from step 3:

●

$X[k] = \frac{2}{j} * [\frac{(1 - e^{-j0.2\pi (k-1) * 10} )}{(1 - e^{-j0.2\pi (k-1)})} - \frac{(1 - e^{-j0.2\pi (k+1) * 10})}{(1 - e^{-j0.2\pi (k+1)})}]$

●

Since $e^{-j2\pi m} = 1$ for any integer m:

●

$X[k] = \frac{2}{j} * [\frac{(1 - 1)}{(1 - e^{-j0.2\pi (k-1)})} - \frac{(1 - 1)}{(1 - e^{-j0.2\pi (k+1)})}]$

●

This simplifies to:

●

$X[k] = \frac{2}{j} * = 0$, for $k \neq 1$ and $k \neq 9$

●

For the cases where k = 1 and k = 9, the denominator becomes zero, and we need to handle these separately.

5. Special Cases: k = 1 and k = 9

●

For k = 1:

●

$X1 = \frac{2}{j} * \sum_{n=0}^{9} (e^{-j0.2\pi (1-1)n} - e^{-j0.2\pi (1+1)n})$

●

$X1 = \frac{2}{j} * \sum_{n=0}^{9} (1 - e^{-j0.4\pi n})$

●

Since $\sum_{n=0}^{9} 1 = 10$ and the second summation is a geometric series, we get:

●

$X1 = \frac{2}{j} * [10 - \frac{(1 - e^{-j0.4\pi * 10})}{(1 - e^{-j0.4\pi})}] = \frac{20}{j}$

●

Similarly, for k = 9:

●

$X2 = \frac{2}{j} * \sum_{n=0}^{9} (e^{-j0.2\pi (9-1)n} - e^{-j0.2\pi (9+1)n})$

●

$X2 = \frac{2}{j} * \sum_{n=0}^{9} (e^{-j1.6\pi n} - e^{-j2\pi n})$

●

Simplifying and using the geometric series formula, we get:

●

$X2 = \frac{2}{j} * [\frac{(1 - e^{-j1.6\pi * 10})}{(1 - e^{-j1.6\pi})} - 10] = -\frac{20}{j}$

Therefore, the final result of the 10-point DFT is:

●

X[k] = 0, for k = 0, 2, 3, ..., 8

●

X1 = 20/j

●

X2 = -20/j