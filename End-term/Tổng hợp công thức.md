## Phương trình phân tích, bào chế
![[Pasted image 20241225143501.png]]
## Năng lượng, công suất
Bản thân công thức bỏ đi phần $e$ của các cặp công thức biến đổi tương ứng

| Fourier Transform | Signal Type | Energy                                                                                                     | Average Power                                                                                  |     |
| :---------------- | :---------- | :--------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------- | --- |
| **CTFS**          | Periodic    | 0                                                                                                          | $P_{av} = \frac{1}{T_0}\int_{T_0} \|x(t)\|^2dt = \sum\limits_{k=-\infty}^{\infty}\|c_k\|^2$    |     |
| **CTFT**          | Aperiodic   | $E = \int_{-\infty}^{\infty} \|x(t)\|^2dt = \int_{-\infty}^{\infty} \|X(j2πF)\|^2dF$                       |                                                                                                |     |
| **DTFS**          | Periodic    | 0                                                                                                          | <br>$P_{av} = \frac{1}{N}\sum\limits_{n=0}^{N-1}\|x[n]\|^2 = \sum\limits_{k=0}^{N-1}\|c_k\|^2$ |     |
| **DTFT**          | Aperiodic   | $E_x = \sum\limits_{n=-\infty}^{\infty}\|x[n]\|^2 = \frac{1}{2\pi}\int_{2\pi} \|X(e^{j\omega})\|^2d\omega$ |                                                                                                |     |
|                   |             |                                                                                                            |                                                                                                |     |

	$n(u[n+3] - u[n-4])$

### Công suất trung bình đặc biệt
- Với hàm sine: $P_{av} = \frac{1}{2} A^2$

## Các biến đổi đáng chú ý
- Các tính chất biến đổi DTFT:![[Pasted image 20241225140330.png]]
- Câu 5, [[Applied Digital Signal Processing.pdf#page=211|chap 4]]: $$
 |cos(2\pi x)|, T_{0} = 1 \to cos(2\pi x), T_{1} = \frac{1}{2} = \frac{T_{0}}{2}
$$
- Câu 9, [[Applied Digital Signal Processing.pdf#page=211|chap 4]], ý c: ![[Cách tính phổ pha#^9dbf06]]
- Câu 11, ý a: Góc của phổ pha là hệ tọa độ của 
- Câu 13a:
	- Áp dụng tính dịch chuyển tần số: $$x[n] \xrightarrow{\text{DTFT}} X(\omega) \
\text{then} \ x[n]e^{j \omega_{0}n} \xrightarrow{\text{DTFT}} X(\omega - \omega_{0}) $$ ^11
	- Phép tách sigma:$$\sum_{n=1}^{\infty} e^n = \sum_{n=0}^{\infty}e^n \ -e^0$$ ^c4d990
- Đối với DTFS và DFT:
	- Chú ý công thức chuỗi hình học - chuỗi cấp số nhân: 
		- Điều kiện: $0<|r| < 1$
		- Cận hữu hạn: $\sum^{N -1}_{n = 0} ar^n = a\frac{1 - r^N}{1- r}$
		- Cận vô hạn: $\sum^{\infty}_{n = 0} r^n = \frac{1}{1 - r}$
	- Công thức biến đổi để ghép về sine 
	- $$e^{-j\frac{2\pi}{N}kn} = e^{j\frac{2\pi}{N}k(N - n)}= e^{j\frac{2\pi}{N}(N-k)n}$$

## Công thức Euler

$$
e^{jx} = j\sin x  + \cos x
$$



