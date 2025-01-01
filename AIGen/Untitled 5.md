The **synthesis equation of the DFT** describes how to reconstruct the original time-domain sequence, _x[n]_, from its DFT coefficients, _X[k]_. It uses the **same twiddle factor, $W_N$,** but with a positive exponent and a scaling factor of 1/N:

$\mathbf{x[n] = \frac{1}{N} \sum_{k=0}^{N-1} X[k] W_N^{-kn}}$

**Explanation:**

- The equation sums over all _k_ frequency components, from 0 to _N_-1.
- Each DFT coefficient _X[k]_ is multiplied by the complex conjugate of the twiddle factor raised to the power _kn_. This reverses the phase shift introduced in the analysis equation.
- The 1/_N_ factor normalises the result.

**Key Points about the Twiddle Factor:**

- **Periodicity:** $W_N^{kn} = W_N^{k(n+N)} = W_N^{(k+N)n}$. This periodicity is important for understanding the properties and computational efficiency of the DFT.
- **Symmetry:** $W_N^{kn} = (W_N^{-kn})^*$. The twiddle factors in the analysis and synthesis equations are complex conjugates of each other.

**Relationship Between Analysis and Synthesis:**

The analysis equation transforms a time-domain sequence into its frequency-domain representation, while the synthesis equation performs the inverse operation. They form a DFT pair, allowing you to move between the time and frequency domains.