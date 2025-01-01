## Vì sao sử dụng DFT
- Trong thực tế, tín hiệu thường được phân tích trong 1 cửa sổ thời gian xác định
- Các biến thời gian và biến tần số đều hữu hạn/rời rạc
## Định nghĩa
>*Xét tín hiệu $x_{N}[n]$ có chiều dài hữu hạn $N$(mẫu)*
>*Một cách tổng quát, giả sử $x_{N}[n] = 0 \forall n\notin [0, N - 1]$*

>[!Info]  Cặp phương trình
>$x_N[n]$ được biểu diễn bởi cặp phương trình:
> - Tổng hợp: $$ x_{N}[n] = \frac{1}{N} \sum_{K = 0} ^{N - 1} X[k] e^{jk \frac{2\pi}{N}n} $$
> - Phân tích $$ X_[K] =  \sum_{K = 0} ^{N - 1} x_{N}[n] e^{-jk \frac{2\pi}{N}n} $$

^f8b8cc

**Chỉ có ý nghĩa về mặt toán học:**
- $x_N[n]$ và $X[k]$ xác định duy nhất lẫn nhau
- Có thể tính toán chính xác được
## Liên hệ với DTFS - DTFT
### DFT - DTFS
Xét 1 TH $\tilde{x}[n]$ tuần hoàn với N mẫu, với $x_{N}[n] (n \in [0, N - 1])$ là 1 chu kỳ thì DTFS của nó là:
$$C_k = \frac{1}{N}\sum_{n = 0}^{N - 1} \tilde{x}[n] e^{-jK\omega_0n}; \omega_0 = \frac{2\pi}{N} ; k \in [0, N - 1]$$
Từ công thức trên và [[Biến đổi fourier rời rạc - DFS#^f8b8cc|cặp phương trình DTF]], có:
$$X[k] = N c_k  ;k \in [0, N - 1]$$
Hay DFT N điểm của $x_{N}[n] = NX$ các hệ số DTFS của $\tilde{x}[n]$
### DFT - DTFT
*Lấy mẫu trên miền tần số*

$$
\begin{align}
X_N(\omega) &= \sum_{n = -\infty}^{\infty}{x_N[n] e ^{-j\omega n}}\\
&= \sum_{n = 0}^{n - 1}{x_N[n] e ^{-j\omega n}} \\
\end{align} 
$$
 ![[IMG_0479.jpeg]]
## Ảnh hưởng của số điểm tính DFT

*Xét tín hiệu $x_{L}[n]$ có chiều dài hữu hạn $L$(mẫu)*
>*Một cách tổng quát, giả sử $x_{L}[n] = 0 \forall n\notin [0, L - 1]$*

>[!Info]  Cặp phương trình
>$x_N[n]$ được biểu diễn bởi cặp phương trình:
> - Tổng hợp: $$ x_{N}[n] = \frac{1}{N} \sum_{K = 0} ^{N - 1} X[k] e^{jk \frac{2\pi}{N}n} $$
> - Phân tích $$ X_[K] =  \sum_{K = 0} ^{N - 1} x_{N}[n] e^{-jk \frac{2\pi}{N}n} $$




![[IMG_0480.jpeg]]

![[Pasted image 20241220163217.png]]
When performing a DFT, the choice of L, the number of points in the DFT, relative to N, the length of the sequence, has important implications for the interpretation and accuracy of the results.

### L < N

- **Time Domain Aliasing:** If L is chosen to be less than N, time domain aliasing occurs. This is because the DFT treats the input sequence as periodic with a period of L. When L < N, the shifted replicas of the sequence overlap, leading to distortion in the calculated DFT.
- **Loss of Information:** Choosing L < N results in a loss of information from the original sequence. The DFT only captures a portion of the data, and the missing information cannot be recovered.

### L = N

- **Accurate Representation:** If the sequence is actually periodic and L is chosen to be equal to N, then the DFT accurately represents one period of the sequence. This provides the correct frequency domain representation.
- **No Aliasing:** When L = N and the sequence is truly periodic, there is no time domain aliasing because the shifted replicas of the signal align perfectly.

### L > N

- **Zero-Padding:** Choosing L greater than N involves zero-padding the sequence, which means adding zeros to the end of the signal to extend its length.
- **Increased Frequency Resolution:** Zero-padding increases the number of frequency bins in the DFT output. This results in a more finely spaced frequency representation, leading to a smoother-looking spectrum. However, it does not enhance the inherent spectral resolution of the signal, which is determined by the original non-zero data.
- **Computational Complexity:** Increasing L beyond N increases the computational complexity of the DFT, particularly if L is large enough to warrant using an FFT algorithm. The execution time of an FFT is proportional to (L/2)Log2(L), meaning that larger values of L lead to longer computation times.

**In summary, selecting the appropriate value for L in relation to N is critical for obtaining an accurate and meaningful DFT. Choosing L < N leads to time domain aliasing and information loss, while L = N provides an accurate representation of a periodic signal. L > N, through zero-padding, enhances frequency domain representation density but does not improve the underlying spectral resolution.**