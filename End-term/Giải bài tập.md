
Câu 13
1) $x[n] = \frac{1}{2}^{|n|} \cos\left( \frac{\pi (n-1)}{8} \right)$
$$
\begin{align}
x[n] &= \frac{1}{2}^{|n|} \frac{1}{2}(e^{j \pi (n-1)/8} + e^{-j \pi (n-1)/8}) \\
&= \frac{1}{2}^{|n|}\left( \frac{1}{2}e^{j\pi n/8}e^{-j\pi/8} \right)  
+ \frac{1}{2}^{|n|}\left( \frac{1}{2}e^{-j\pi n/8}e^{j\pi/8} \right) \\
&= (\frac{1}{2}^{|n|} \frac{1}{2}e^{j\pi n/8})e^{-j\pi/8}  +  
(\frac{1}{2}^{|n|} \frac{1}{2}e^{-j\pi n/8})e^{j\pi/8}  
\end{align}
$$
Tính DTFT của $\frac{1}{2} ^{|n|}$:
$$
\begin{align}
\sum _{n = -\infty}^{\infty} \frac{1}{2}^{|n|} e^{-j\omega n} &= 
\sum_{-\infty}^{-1} \frac{1}{2}^{-n} e^{-j\omega n} + 
\sum_{n=0}^{\infty} \frac{1}{2}^{n} e^{-j\omega n}  \\
&= \sum_{m=1}^{\infty} \left( \frac{e^{j\omega }}{2} \right)^{m} + \frac{1}{1 - \frac{1}{2}e^{-j\omega}} (\text{thay m = -n}) \\ 
&= \sum_{m=0}^{\infty} \left( \frac{e^{j\omega }}{2} \right )^{m}-1 + \frac{1}{1 - \frac{1}{2}e^{-j\omega}}  \\
&= \frac{1}{1 - \frac{1}{2}e^{j\omega} } - 1 + \frac{1}{1 - \frac{1}{2}e^{-j\omega}} \\
&= \frac{\frac{3}{4}}{\frac{5}{4} - \cos \omega}

\end{align}

$$
Áp dụng tính dịch tần số: ![[Tổng hợp công thức#^c4d990]]
Kết quả: 
$$
\frac{1}{2} e^{-j \pi/8} \frac{\frac{3}{4}}{\frac{5}{4} -\cos(\omega - \frac{\pi}{8})} +
\frac{1}{2} e^{j \pi/8} \frac{\frac{3}{4}}{\frac{5}{4} -\cos(\omega +\frac{\pi}{8})}
$$
