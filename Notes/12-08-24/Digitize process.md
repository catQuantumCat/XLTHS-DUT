- Input: Tín hiệu liên tục [[Analog signal|Tín hiệu liên tục]]
- Có thể lấy đều/không đều (**nên lấy đều**)

Giả sử: TH liên tục $xa(t)$ với t thuộc R
Nếu lấy mẫu với [[Chu kỳ lấy mẫu|chu kỳ]] $Ts$ giây -> thu được [[Discrete signal|tín hiệu rời rạc]]: $x[n] = xa(t)$ với $t = n* Ts$ thuộc $xa(n*Ts)$; n thuộc Z

- Tại mỗi bội của [[Chu kỳ lấy mẫu]] $T$ được chọn -> bắt dữ liệu tại thời điểm đó ^d370df
	-  $-1T, 0, T, 2T, 3T,...$ ->  $nT$
	- Tín hiệu này chỉ được xác định trên khoảng $n$

>[!warning] Chu kỳ $Ts$ khác nhau -> Tín hiệu rời rạc duy nhất

^de1c30

- Chọn $Ts$ như thế nào cho hợp lý?




1. Signal acquisition: transform into mesurable quantities
2. [[Analog signal|Contiguous]] -> [[Digital Signal|digital]] ^f99ced
	- Time-axis (sampling)
	- Amplitude-axis (quantization)
	- Coding