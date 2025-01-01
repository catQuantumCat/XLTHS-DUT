>[!info] Phương pháp chống [[Hiện tượng chồng phổ]]

>**Nyquist/Shannon sampling theory**
>*An analog signal with maximum frequency of B must be sampled at least 2B times per second*

- Tần số lấy mẫu Nyquist: Tần số tối thiểu để khôi phục hoàn hảo tín hiệu liên tục input
	- Liên tục: 22kHz -> phải lấy mẫu 44kHz
- Tần số lấy mẫu Nyquist xác định chất lượng âm thanh lấy được:
	- Nếu lấy mẫu với tần số lấy mẫu 10Hz -> có thể khôi phục được các tần số 5Hz
	- Xác định chất lượng xử lý tín hiệu số

- **Nynquist frequency**: $\frac{fs}{2}$ with $fs$ being sample frequency
- Filter frequencies above **Nynquist frequency**: use [[Anti-aliasing filter]]

![[Pasted image 20240819110813.png]]

