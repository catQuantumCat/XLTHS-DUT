
### Với DTFS
Các giá trị Ck tính được sau khi phân tích Fourier bản chất là một số ảo. Tính góc thông qua hệ tọa độ số ảo ^9dbf06

Như ví dụ 11a, chương 4: $C_k = \{0.5, 2/3, 0, -5/6, 0, 2/3\}$

Tại $k = 3$ giá trị âm, với giá trị $(x, y)=(-5/6, 0)$ với $x, y$ lần lượt là giá trị trên trục thực và trục ảo

$arctan(C_3)$ sẽ là góc giữa trục $x$ dương và giá trị trên, tức $\pi$
![[Pasted image 20241222145416.png]]

### LLM
The phase spectra for a given $k$ value can be obtained by calculating the angle of the complex DTFS coefficient, $c_k$. The following steps outline the process for the given signal $x_2[n] = {1, 2, -1, 0, -1, 2}$, $0 \leq n \leq 5$ (one period):

1. **Calculate the DTFS Coefficients:** The formula for the $k$th DTFS coefficient, $c_k$, for a discrete-time periodic signal $x[n]$ with period $N$ is:
    
    $c_k = \frac{1}{N} \sum^{N-1}_{n=0} x[n]e^{-j2\pi kn/N}$
    
    Given that $x_2[n]$ has a period of $N=6$, calculate $c_k$ for each value of $k$ from 0 to 5. This results in a set of complex numbers that represent the frequency components of the signal.
    
    For example, for $k=4$:
    
    $c_4 = \frac{1}{6} ( 1e^{-j2\pi 4(0)/6} + 2e^{-j2\pi 4(1)/6} - 1e^{-j2\pi 4(2)/6} + 0e^{-j2\pi 4(3)/6} - 1e^{-j2\pi 4(4)/6} + 2e^{-j2\pi 4(5)/6})$
    
    Repeat this calculation for each $k$ value to find all the DTFS coefficients.
    
2. **Determine the Phase:** The phase spectrum, for a specific $k$ value, is the angle of the corresponding DTFS coefficient, $c_k$. This is represented as:
    
    $\textbf{Phase}[k] = \angle c_k$
    
    Calculate this angle using the arctangent function (typically _atan2_ in programming languages), using the imaginary and real parts of $c_k$.
    
    For instance, to find the phase of the previously calculated $c_4$:
    
    $\textbf{Phase} = \angle c_4 = atan2(Im(c_4), Re(c_4))$
    
    This provides the phase angle in radians, which indicates the phase shift of the $k$th harmonic component of the signal.
    
3. **Repeat for All $\textbf{k}$ Values:** Repeat the process for each $k$ value in the range $0 \leq k \leq N-1$ to obtain the complete phase spectrum. This spectrum provides insights into the relative timing or displacement of the various frequency components within the signal.
    

**Figure 4.10** in the sources provides a visual example of magnitude and phase spectra for a periodic sequence.


At $K = 3$, the calculation for the phase value is as follows:

1. **Calculate the DTFS coefficient, $c_3$**:
    
    $c_3 = \frac{1}{6} (1e^{-j2\pi 3(0)/6} + 2e^{-j2\pi 3(1)/6} - 1e^{-j2\pi 3(2)/6} + 0e^{-j2\pi 3(3)/6} - 1e^{-j2\pi 3(4)/6} + 2e^{-j2\pi 3(5)/6})$ $= \frac{1}{6} (1 + 2e^{-j\pi} - 1e^{-j2\pi} + 0 - 1e^{-j4\pi} + 2e^{-j5\pi})$ $= \frac{1}{6} (1 - 2 - 1 + 0 - 1 - 2)$ $= -5/6$
    
2. **Determine the phase**:
    
    $\textbf{Phase} = \angle c_3 = \text{atan2}(Im(c_3), Re(c_3)) = \text{atan2}(0, -5/6) = \boldsymbol{\pi} \textbf{ radians}$
    

Therefore, at $K = 3$, the phase value is $\boldsymbol{\pi}$ **radians**.