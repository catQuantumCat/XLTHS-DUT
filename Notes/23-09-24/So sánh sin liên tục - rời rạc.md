
#### Kết luận
*Xét trường hợp 1 liên tục và 1 rời rạc không tiên quan tới nhau*

|                       | Liên tục                                                                                                  | Rời rạc                                                                                                    |
| --------------------- | --------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Chu kỳ cơ bản         | Tuần hoàn                                                                                                 | Tuần hoàn khi $f_0=\frac{n}{kN_0}$ là phân số tối giản                                                     |
| Tính tuần hoàn tần số | - Không tuần hoàn<br>- Với mọi $\Omega_0$ khác nhau đều tương ứng với các tín hiệu sin phân biệt với nhau | Tuần hoàn với $2\pi$                                                                                       |
| Tốc độ tần số         | $\Omega_0$ càng lớn $\to$ $x(t)$ đổi (giao động) càng nhanh                                               | - $\omega_0$ lân cận mà lẻ $\pi$ : Tần số cao nhất<br>- $\omega_0$ lân cận mà chẵn $\pi$: Tần số thấp nhất |
___
>[!Info] Kết luận về chu kỳ
> $x[n]$ không phải lúc nào cũng tuần hoàn $\leftrightarrow$ chỉ tuần hoàn khi $f_0=\frac{n}{kN_0}$ là phân số tối giản

___
>[!Warning] Kết luận từ [[So sánh sin liên tục - rời rạc#^c643ae|tính tuần hoàn tần số]] của Sin rời rạc:
> Các tần số
> $$F_k = F_0 + kF_s$$
> Đều là các bản sao của $F_0$ khi được lấy mẫu với $F_s$

^f886fa
### Chứng minh
*Xét trường hợp 1 liên tục và 1 rời rạc không liên quan tới nhau*
#### Đối với tín hiệu Sin liên tục
- **Chu kỳ cơ bản**: $T_0 = \frac{2\pi}{\Omega} = \frac{1}{F_0}$
	Do $x(t) = x(t + KT_0), \forall k \in Z, t \in R, \Omega_0 \in R$ ==hay $x(t)$ luôn tuần hoàn==
- **Tính tuần hoàn về tần số**
	$\Omega_0$ không có tính tuần hoàn nên mọi $\Omega_0$ khác nhau đều tương ứng với các tín hiệu sin phân biệt với nhau
- **Tốc độ thay đổi của tín hiệu**
	$\Omega_0$ càng lớn $\to$ $x(t)$ đổi (giao động) càng nhanh
	- $\Omega_{min} = 0$
	- $\Omega_{max} = \Omega$
#### Đối với tín hiệu Sin rời rạc
- **Chu kỳ cơ bản:** $\exists N_0 \in Z$
	$$
	\begin{align}
	 x[n] &= x[n + kN_0] (\forall n \in Z) \\
	\leftrightarrow cos (\omega_0n + \varphi) &= cos[\omega_0(n+kN_0) + \varphi] (\forall n \in Z) \\
	\leftrightarrow \omega_0n + k\omega_0N_0 + \varphi &= \omega_0n + \varphi + n2\pi \\
	\leftrightarrow k\omega_0N_0 &= n2\pi \\ 
	\leftrightarrow N_0 &= \frac{n2\pi}{k2\pi f_0} \\ &= \frac{n}{kf_0}\\
	\end{align}
	$$
	$\to$ $\exists m; k \in Z$ sao cho $N_0 = \frac{m}{Kf_0}$ là số nguyên dương
- **Tính tuần hoàn về tần số**
	$\omega_0$ tuần hoàn với chu kỳ $2\pi$, vì:
	$$  
	\begin{align}  
	x[n]_k &= Acos[(\omega_0 + k2\pi)n + \varphi] (k \in Z) \\
		&= Acos[\omega_0 + n + \varphi] (k \in Z)\\
		 &=x[n]
	\end{align}  
	$$
	
	^c643ae
	
	$\to$ các TH sin rời rạc mang $\omega$ khác nhau $k2\pi$ đều không phân biệt được
- **Tốc độ thay đổi của tần số:**
	- $\omega_0$ lân cận mà lẻ $\pi$ : Tần số cao nhất
	- $\omega_0$ lân cận mà chẵn $\pi$: Tần số thấp nhất
### Xét trường hợp phụ thuộc - Xét tần số Nyquist
Giả sử $x[n]$ lấy mẫu từ $x(t)$ là sin liên tục với $F_s$ là tần số lấy mẫu:
- $\omega_0 = \frac{\Omega_0^`}{F_s} = 2\pi \frac{F_0^`}{F_s}$ 
- $\to F_0'[0; \frac{F_s}{2})$
- Đây là tần số [[Định lý lấy mẫu Nyquist - Shannon|Tần số Nyquist]]
### Ví dụ
![[IMG_0013 1.jpeg]]
