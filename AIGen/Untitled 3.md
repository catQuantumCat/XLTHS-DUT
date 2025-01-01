The CTFS of a periodic signal $\tilde{x}_c(t)$ is given by:

$c_k = \frac{1}{T_0} \int_{T_0} \tilde{x}_c(t) e^{-jk\Omega_0 t}dt$12

where:

●

$T_0$ is the fundamental period.

●

$\Omega_0 = \frac{2\pi}{T_0}$ is the fundamental frequency.

Given the periodic signal $\tilde{x}_c(t) = e^{-t}$, $0 ≤ t ≤ 5$ with fundamental period $T_0 = 5$, we can calculate its CTFS coefficients $c_k$:

●

$c_k = \frac{1}{5} \int_{0}^{5} e^{-t} e^{-jk \frac{2\pi}{5} t}dt$

This simplifies to:

●

$c_k = \frac{1}{5} \int_{0}^{5} e^{-(1+jk \frac{2\pi}{5})t} dt$

Evaluating the integral, we get:

●

$c_k = \frac{1}{5} [\frac{-1}{1+jk\frac{2\pi}{5}} e^{-(1+jk\frac{2\pi}{5})t}]_{0}^{5}$

●

$c_k = \frac{1-e^{-5}}{5+j2\pi k}$



It appears you are asking for clarification on evaluating the limits of integration for the CTFS coefficient we just derived. To be sure, you are asking to evaluate the following:

●

$c_k = \frac{1}{5} [\frac{-1}{1+jk\frac{2\pi}{5}} e^{-(1+jk\frac{2\pi}{5})t}]_{0}^{5}$

To evaluate this, we can substitute the limits of integration:

●

$c_k = \frac{1}{5} [\frac{-1}{1+jk\frac{2\pi}{5}} e^{-(1+jk\frac{2\pi}{5})5} - \frac{-1}{1+jk\frac{2\pi}{5}} e^{-(1+jk\frac{2\pi}{5})0}]$

Simplifying this yields:

●

$c_k = \frac{1}{5} [\frac{-1}{1+jk\frac{2\pi}{5}}e^{-5} + \frac{1}{1+jk\frac{2\pi}{5}}]$

This further simplifies to the expression for the CTFS coefficient $c_k$:

●

$c_k = \frac{1-e^{-5}}{5+j2\pi k}$


You are asking how the following simplification was made:

●

$c_k = \frac{1}{5} [\frac{-1}{1+jk\frac{2\pi}{5}} e^{-(1+jk\frac{2\pi}{5})5} - \frac{-1}{1+jk\frac{2\pi}{5}} e^{-(1+jk\frac{2\pi}{5})0}]$ simplifies to $c_k = \frac{1}{5} [\frac{-1}{1+jk\frac{2\pi}{5}}e^{-5} + \frac{1}{1+jk\frac{2\pi}{5}}]$

Let's break down the simplification process:

●

Step 1: Distribute the exponent

●

The exponent, $-(1 + jk\frac{2 \pi}{5})5$, can be distributed as follows:

○

$-(1 + jk\frac{2 \pi}{5})5 = -5 - j5k \frac{2\pi}{5} = -5 -j2 \pi k$.

●

Step 2: Simplify the exponential term

●

The exponential term can now be written as $e^{-5-j2 \pi k}$. Using the properties of exponents, we can separate this into a product of two exponentials:

○

$e^{-5 - j2 \pi k} = e^{-5}e^{-j2 \pi k}$

●

Step 3: Apply Euler's formula

●

Euler's formula states that $e^{jθ} = cos θ + j sin θ$. Therefore:

○

$e^{-j2 \pi k} = \cos(-2 \pi k) + j \sin(-2 \pi k)$

●

Since cosine and sine are periodic functions with a period of $2 \pi$:

○

$ \cos(-2 \pi k) = cos(0) = 1$

○

$ \sin(-2 \pi k) = sin(0) = 0$

●

Therefore, $e^{-j2 \pi k} = 1$

●

Step 4: Substitute the simplified term

●

Substituting this back into the original expression, we get:

○

$c_k = \frac{1}{5}[\frac{-1}{1+jk\frac{2 \pi}{5}}e^{-5} * 1 - \frac{-1}{1+jk\frac{2 \pi}{5}}e^{0}]$

Simplifying this gives us:

●

$c_k = \frac{1}{5} [\frac{-1}{1+jk\frac{2\pi}{5}}e^{-5} + \frac{1}{1+jk\frac{2\pi}{5}}]$

Therefore, the simplification arises from applying the properties of exponents and Euler's formula to the exponential term. The term $e^{-j2 \pi k}$ evaluates to 1, leaving only $e^{-5}$ in the expression.