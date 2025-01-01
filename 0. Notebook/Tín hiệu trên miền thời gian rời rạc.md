
Discrete-time signal
![[Pasted image 20240821134844.png]]
## Tín hiệu rời rạc
![[Discrete signal#^bea4a0]]
#### Cách biểu diễn
- [[Discrete signal#^c78c14|Đồ thị]]
- [[Discrete signal#^a272fe|Chuỗi số]]
![[Chuỗi xung đơn vị#^b03a75|Công thức tách tuyến tính tín hiệu DT phức tạp -> tổng các chuỗi xung đơn vị  ]]
#### Chuyển đổi tín hiệu liên tục -> rời rạc thông qua lấy mẫu
![[Digitize process#^de1c30]]
![[Digitize process#^d370df]]

- Bài tập: [[Bài tập]]
## Các tín hiệu DT cơ sở
- [[Chuỗi nhảy bậc đơn vị]]
	- **Bài tập**: biểu diễn u\[n] dưới dạng 
		- Tổ hợp tuyến tính các xung đơn vị theo [[Chuỗi xung đơn vị#^b03a75|công thức]]
		- $u[n] = \sum_{k=0}^{\infty} \delta[n-k]$
- [[Chuỗi xung đơn vị]]
- [[Sin signal]]
- [[Chuỗi mũ thực]]
	- **Bài tập**: biểu diễn $x[n] = a^n u[n], a\in \mathbb{R}, a \neq 0$ trong 2 trường hợp
		- $-1 < a < 0$: 
		- $a < -1$
		- [[IMG_1849.jpeg]]
## Các phép biến đổi tín hiệu đơn giản
- [[Biến đổi thời gian]]
	- [[Biến đổi thời gian#Dịch thời gia|Dịch]]
	- [[Biến đổi thời gian#Đảo thời gian|Đảo]]
	- **Bài tập**: biểu diễn $x[n] = a^n u[-n], a\in \mathbb{R}, a \neq 0$ trong 2 trường hợp
		- $0 < a < 1$: [[Pasted image 20240831165320.png]]
		- $a > 1$: [[Pasted image 20240831165207.png]]
- [[Cộng - trừ tín hiệu]]
- **Bài tập**: biểu diễn $x[n] = a^n u[-n -2], a\in \mathbb{R}, a \neq 0$ trong 2 trường hợp
		- $0 < a < 1$: [[Pasted image 20240831170843.png]]
		- $a > 1$: [[Pasted image 20240831170913.png]]
		- Quy trình: $u[-n-2] = u[-(n + 2)]$, với $k = -2$ -> đảo và dịch sớm lên 2 đơn vị

### [[IMG_1934.jpeg|Giải bài tập]]
### [[Hiện tượng chồng phổ]]
### Bài tập
Vẽ đồ thị mô tả hiện tượng chồng phổ cho:
- F1: 50Hz
- F2: 10Hz
- Fs (lấy mẫu): 40Hz
Bài tập ví dụ: 1.1, 1.2, 1.3 (a, b) từ [[Bai Giang XLTHS.pdf#page=12]]
- [[9-9-24.pdf|Bài giải]]
- [[aliasing-fix.pdf|Bài fix]]