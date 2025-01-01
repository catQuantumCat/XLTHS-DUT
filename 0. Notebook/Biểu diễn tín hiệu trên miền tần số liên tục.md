## Khái niệm tần số của tín hiệu liên tục
*Một tín hiệu liên tục bất kỳ có vô số tần số riêng lẻ*
- **[[Dải tần]]**: Tập hợp các tần số riêng lẻ của tín hiệu
- [[Sin signal]]: Mang 1 tần số riêng lẻ duy nhất $\to$ Tín hiệu liên tục được tạo thành từ nhiều (vô số) tín hiệu sin khác nhau
> [!info] Khi đề cập đến một tần số = xét tín hiệu sin mang tần số đó

- Việc tìm dải tần và phân bố năng lượng/công suất của một tín hiệu liên tục trên dải tần = [[Phân tích phổ]]
- Sử dụng chuỗi Fourier 
### Phân biệt tần số tín hiệu liên tục - rời rạc
Tần số lấy mẫu $F_s$:![[Tần số lấy mẫu#^f02d1d]]
![[Tần số chuẩn hoá - tần số góc chuẩn hoá#^7e2b93]]

### [[So sánh sin liên tục - rời rạc]]
![[So sánh sin liên tục - rời rạc#Kết luận]]

### [[So sánh sin thực - phức]]
![[So sánh sin thực - phức#Kết luận]]

### Năng lượng và công suất của tín hiệu
Giả sử tín hiệu liên tục, không tuần hoàn $x_a(t)$ và rời rạc, không tuần hoàn $x[n]$
Giả sử tín hiệu liên tục, tuần hoàn $\tilde{x}_a(t)$ và rời rạc, không tuần hoàn $\tilde{x}[n]$
- Tính năng lượng tín hiệu - miền thời gian
	- $\int_{-\infty}^{+\infty} x^2(t) \,dt; E_{x[n]} = \sum_{n=-\infty}^{\infty} {|x[n]|^2}$
	- $E_x = +\infty$ thì tín hiệu có năng lượng vô hạn -> không biểu diễn được phổ
	- $E_x < +\infty$ có năng lượng hữu hạn -> biểu diễn được phổ, là năng lượng có biểu diễn phổ, công suất = 0

- Tính công suất của tín hiệu - miền thời gian
	- $P_x = \lim \frac{\int_{-T}^{+T} x^2(t) \,dt}{2T}$
	- $P_x = lim_{N \to \infty} \frac{1}{2N + 1} \sum_{n = -N}^{N}{x[n]^2}$
Xét lớp tín hiệu có năng lượng vô hạn nhưng có công suất hữu hạn khác không -> là tín hiệu tuần hoàn

- Giả sử $\tilde{x}(t)$ tuần hoàn với chu kỳ cơ bản $T_0 \leftrightarrow \tilde{x}(t) = \tilde{x}(t + kT_0)\forall K \in Z$
- Giả sử $\tilde{x}(t)$ tuần hoàn với chu kỳ cơ bản $N_0$ mẫu $\leftrightarrow \tilde{x}[n] = \tilde{x}[n + kN_0] \forall K \in Z$
- Công suất hữu hạn được tính:
	- $P_\tilde{x} = \frac{1}{T_0}\int_{0}^{T_0}{|x(t)|^2dt}$
		- $x[t]$ là tín hiệu phức; việc lấy trị đối của phức khác với tín hiệu thực
	- $P_\tilde{x} = \frac{1}{N_0}\sum_{n=0}^{N_0 - 1}{x^2[n]}$
>[!info] Công thức Parseval - tính công suất trung bình của tín hiệu phức
>$$
>P_\tilde{x} = \frac{1}{T_0}\int_{0}^{T_0}{|x(t)|^2dt} = \Sigma_{k = -\infty}^{\infty} |C_k|^2
>$$
- Phân tích phổ tính hiệu: tìm phân bố của năng lượng (hay công suất) của tín hiệu theo tần số
	- Chỉ quan tâm đến 2 loại TH:
		- **Phổ năng lượng**: Không tuần hoàn, có năng lượng hữu hạn: Phổ là phân bố **năng lượng** theo tần số
		- **Phổ công suất**: Tuần hoàn, có công suất hữu hạn: Phổ là phân bố **công suất** theo tần số
- Các trường hợp
	- Liên tục, tuần hoàn
	- Liên tục, không tuần hoàn
	- Rời rạc, tuần hoàn
	- Rời rạc, không tuần hoàn

### Biểu diễn phổ công suất của tín hiệu liên tục, tuần hoàn bằng chuỗi Fourier CTFS
*hay Continuous-time Fourier (CTFS)*
Xét tín hiệu liên tục tuần hoàn $\tilde{x}(t)$ với chu kỳ cơ bản $T_0(s)$
- Tần số cơ bản $F_0 = \frac{1}{T_0}(Hz)$
Hài bậc K (Kth harmonic) của tín hiệu trên là [[Sin signal|tín hiệu sin]] mang tần số $kF_0 (K \in Z, K\ne 0)$
Với tín hiệu sin trên thì có [[So sánh sin thực - phức|sin phức]] tương ứng: $s_k(t) = e^{jK\Omega_0t} = e^{jK2\pi F_0t}$

Cặp phương trình CTFS của $\tilde{x}(t)$ là:
- CTFS: $\tilde{x}(t)=\sum_{K = -\infty}^{\infty}c_k e^{jK\Omega_0 t}$
	- $C_K$: biên độ phức của sóng hài bậc $K$ - **là giá trị duy nhất**
- $\tilde{x}(t)$ được tạo nên từ vô số sóng hài bậc $K$ (hay vô số tín hiệu sin phức mang tần số $K\Omega_0$)
- Inverse-CTFT: $C_K(K=-\infty, +\infty)$: 
$$
C_K = \frac{1}{T_0}\int_{T_0}^{}{\tilde{x}(t)e^{-jK\Omega_0t}~dt}
$$
Theo phương trình tổng hợp: $\tilde{x}(t)$ là tổ hợp tuyến tính của vó số sóng hài bậc K
- Công suất của sóng hài K: 
$$
| C_K|^2
$$

![[IMG_0236.jpeg]]
- Các hệ số $C_K$ là các hệ số của chuỗi Fourier của $\tilde{x}(t)$, mang các thông tin về tần số của tín hiệu:
	- Công suất
	- Biên độ
	- Pha

### Chứng minh công thức tính công suất trung bình
![[IMG_0289.jpeg]]
Đối với tín hiệu sine tuần hoàn -> công suất là $A^2/2$

### Công thức Euler
>[!info] Tổng quát
>$$
>e^{i\alpha}=cos(\alpha) + isin(\alpha)
>$$

Biến đổi lượng giác:
- $Cos(\alpha) = \frac{e^{i\alpha} + e^{-i\alpha}}{2}$
- $Sin(\alpha) = \frac{e^{i\alpha} - e^{-i\alpha}}{2i}$

### Bài tập
HW: 
1. **Vẽ đồ thị phổ biên độ/phổ pha/phổ công suất** theo trục tần số F của tín hiệu xung chữ nhật tuần hoàn: [[Chapter3_FREQUENCY-DOMAIN REPRESENTATION OF SIGNALS.pdf#page=19|Silde 19, chương 3]], xét phân bố công suất này theo tần số
2. Áp dụng công thức Euler cho câu trên với $\tilde{x}(t) = \frac{1}{3}Cos(2\pi F_0 t) + \frac{1}{10}Cos(6\pi F_0 t + \pi) + \frac{1}{20}Cos(10\pi F_0 t + \frac{\pi}{6})$

Giải: [[Giải Ck.pdf]]
- Bài 1
	- Nháp tính lại công thức [[IMG_0240.jpeg]]
	- [[IMG_0290.jpeg|Sửa bài 1]] $\to$ dùng hàm sinc để đưa ra kết luận

Bài 2:
- [[IMG_0246.jpeg]]
- [[IMG_0247.jpeg]]


## Biểu diễn phổ công suất của tín hiệu liên tục, không tuần hoàn với CTFT
Xét $x(t)$ không tuần hoàn, thoả điều kiện khả tích tuyệt đối, tức có năng lượng hữu hạn
$$\int_{-\infty}^{+\infty} |x(t)| \,dt < \infty$$
Lớp các tín hiệu này có thể biểu diễn bởi cặp CTFT sau:
- PT tổng hợp/PT bào chế (1): 
$$

\begin{align}  
x(t) &= \frac{1}{2\pi} \int_{-\infty}^{\infty} {x(j\Omega)e^{j\Omega t} d\Omega} \\
 &= \frac{1}{2\pi} \int_{-\infty}^{\infty} {x(j2 \pi F_0)e^{j 2\pi F_0 t} dF} 
  \\
 
&= \frac{1}{2\pi} \sum_{ k = -\infty}^{\infty} {x(j2 \pi F_K)e^{j 2\pi F_K t} \Delta F_k}  
\end{align}
$$
$\to$ $x(t)$ được tạo nên từ vô số tín hiệu phức có tần số $F$ biến thiên liên tục $\in (-\infty, \infty)$ với ${x(j2 \pi F_K)}$ là biên độ phức của thành phần sin phức mang tần số $F_k$

- PT phân tích (2): 
$$ 
\begin {align}
X(j\Omega) &= \int_{-\infty}^{\infty}{e^{-j\Omega t} dt} \\ 
X(j2\pi F) &= \int_{-\infty}^{\infty}{x(t)e^{-j2\pi F t} dt}

\end {align}
$$
	-  Cho phép xác định biên độ phức với hàm số $F_k$ trong phương trình tổng hợp
>[!Info] Mối quan hệ (1) và (2)
>(1) -> (2): Công thức Inverse-CTFT
>(2) -> (1): Công thức CTFT
>$X(j2\pi F)$ hay $X(j\Omega)$ là phổ của $x(t)$

- $|X(j\Omega)|$ phổ biên độ
- góc $X(j\Omega)$: phổ pha
- ${x(j\Omega)e^{j\Omega t} d\Omega }$
-> Cho biết biên độ/pha của thành phần sin mang tần số $\Omega$ trong $x(t)$

>[!Info] Định lý Parseval
>$$
>\begin{align}
>E_x &= \int_{-\infty}^{\infty}{|x(t)|^2 dt} (trên \ miền\ thời \ gian)\\
> &=\int_{-\infty}^{\infty}{|x(t)e^{-j2\pi F t}|^2} dF \\
> &= \frac{1}{2\pi} \int_{-\infty}^{\infty} {|x(j\Omega)e^{j\Omega t} d\Omega|^2 } d\Omega (trên \ miền\ tần  \ số)
> \end{align}
>$$


![[IMG_0351.jpeg]]
### So sánh CTFT và CTFS
Định ti
![[IMG_0354.jpeg]]

![[IMG_0355.jpeg]]

#### Tạo lập mối quan hệ giữa CTFT và CTFS
![[IMG_0379.jpeg]]

### Bài tập CTFT
[[Chapter3_FREQUENCY-DOMAIN REPRESENTATION OF SIGNALS.pdf#page=24]]
![[IMG_0378.jpeg]]
![[Scanned Documents.pdf]]