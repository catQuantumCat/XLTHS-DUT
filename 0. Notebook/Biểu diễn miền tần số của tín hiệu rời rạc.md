**Lấy** mẫu tín hiệu liên tục $x_{[n]} \to X(\omega)$, sau đó biến đổi về $X(F)$, thông qua DTFS và DTFT
## So sánh CTFS - DTFS

|                        | CTFS với $\tilde{x(t)}$ liên tục tuần hoàn                                                           | DTFS với $\tilde{x[n]}$ rời rạc tuần hoàn                                                                                                          |
| ---------------------- | ---------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| Chu kỳ cơ bản          | $T_0(s) \in R: (\tilde{x}(t) = \tilde{x }(t + kT_0)\forall K \in Z)$                                 | N(mẫu) :$\in Z \leftrightarrow \tilde{x}[n] =  \tilde{x}[n + kN] \forall k \in Z$                                                                  |
| Tần số cơ bản          | $\Omega_0 = 2\pi F_0 = \frac{2pi}{T_0}$ (rad/s) ($F_0$: Hz)                                          | $\omega_0 = 2\pi f_0 = \frac{2\pi}{N_0}$ (rad) ($f_0$: không đơn vị)                                                                               |
| Sóng hài               | Vô số sóng hài: $s_k(t) = e^{K\Omega_0t}$ (biến $\Omega$ không tuần hoàn); $K \in (-\infty, \infty)$ | Chỉ có N sóng hài: $s_{k}[n] = e^{jK\omega_0n}$ (hay $K\omega_0 = k\frac{2\pi}{N} \in (0; 2\pi]$); ($\omega$ tuần hoàn $2\pi$); $K \in [0, N - 1]$ |
| PT tổng hợp            | $\tilde{x}(t)=\sum_{K = -\infty}^{\infty}c_k e^{jK\Omega_0 t}$                                       | $\tilde{x}[n] = \sum^{N - 1}_{K = 0}{\tilde{c}_k e^{jK\omega_0n}}$                                                                                 |
| PT Phân tích           | $C_K = \frac{1}{T_0}\int_{T_0}^{}{\tilde{x}(t)e^{-jK\Omega_0t}~dt}; K \in (-\infty, \infty)$         | $C_K = \frac{1}{N}\sum_{n = 0}^{N - 1}{\tilde{x}[n]e^{-jK\omega_0n}}; K \in [0, N - 1]$                                                            |
| Phổ, phổ biên, phổ pha | $C_k = C(k\omega_0), \|C_k\|, \angle {C_k}$; $K \in (-\infty, \infty)$                               | $\tilde{C}_k = \tilde{C}(k\Omega_0), \|\tilde{C}_k\|, \angle {\tilde{C}_k}$; $K \in [0, N - 1]$                                                    |
| T/C phổ                | Phổ vạch, rời rạc, không tuần hoàn                                                                   | Phổ vạch, rời rạc, tuần hoàn với chu kỳ $N$ (vì $\tilde{c}_k = \tilde{c}_{ktmN}$)                                                                  |
| Phổ pha                | $\|C_k\|^{2}$                                                                                        | $\|\tilde{C}_k\|^{2}$                                                                                                                              |
| Parsevalfdsfjdsklgfds  | $P_\tilde{x} = \frac{1}{T_0}\int_{0}^{T_0}{\|x(t)\|^2dt} = \Sigma_{k = -\infty}^{\infty} \|C_k\|^2$  | $\frac{1}{N} \sum_{n = 0}^{N - 1}\|\tilde{x}[n]\|^2 = \sum_{k = 0}^{N - 1}{\|C_k\|^2}$                                                             |
|                        |                                                                                                      |                                                                                                                                                    |

## So sánh CTFT - DTFT
|                                  | CTFT với $x(t)$ liên tục, không tuần hoàn                                                               | DTFT với $x[t]$ rời rạc, không tuần hoàn                                                                         |     |
| -------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | --- |
| Điều kiện tồn tại của biến đổi F | $\int_{-\infty}^{\infty}{\|x(t)\|dt} < \infty \leftrightarrow$ $\int_{-\infty}^{\infty}{\|x(t)\|^2 dt}$ | $\sum_{-\infty}^{\infty}{\|x[n]\|dt} < \infty \leftrightarrow$ $\sum_{-\infty}^{\infty}{\|x[t]\|^2 dt < \infty}$ |     |
| PT tổng hợp                      | $x(t) \frac{1}{2\pi}$                                                                                   |                                                                                                                  |     |
|                                  |                                                                                                         |                                                                                                                  |     |
|                                  |                                                                                                         |                                                                                                                  |     |
![[IMG_0436.jpeg]]
![[IMG_0437.jpeg]]

HW: 
- Tìm quan hệ giữa phổ (DTFT) của x[n] và phổ CTFT của x(t) với giả sử
	- x[n] là phiên bản lấy mẫu với chu kỳ lấy mẫu Ts của x(t)
- Làm 4 ví dụ slide chap 4 (7, 10, 11. 12) - thay  \Omega = \omega
![[IMG_0449.jpeg]]
![[IMG_0450.jpeg]]
	![[IMG_0451.jpeg]]
![[IMG_0452.jpeg]]
![[IMG_0453.jpeg]]
- Phổ năng lượng tập trung tại tần số thấp; càng về tần số cao 
- Giải tần chạy vô hạn

$$X(\omega) = F_s \sum_{k = -\infty} ^{\infty} X_a(F-kF_s)$$


