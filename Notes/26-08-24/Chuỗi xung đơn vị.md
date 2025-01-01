*Unit impulse signal*
Tín hiệu chỉ có ở 1 thời điểm, còn lại không có tín hiệu
 >[!Warning] Chú ý
 >Mọi tín hiệu rời rạc đều có thể biểu diễn -> tổ hợp tuyến tính chuỗi này với gtri khác 0
 >- $x[n]\to\sum_{n=-\infty}^\infty x[k] *\delta[n - k]$ -> phức tạp hoá
 >- $x[n]\leftarrow\sum_{n=-\infty}^\infty x[k] *\delta[n - k]$ ->  đơn giản hoá
^b03a75
## Dạng thường
![[Pasted image 20240825085213.png]]
____
## Dạng dịch chuyển thời gian
![[Pasted image 20240825085255.png]]
- [[Biến đổi thời gian]]: Dịch sang phải (trái, nếu âm) một đoạn $n0$
- [[Mối quan hệ Unit impulse, unit step]]

### VD:
Có $x[n] = \delta [n]$
- $x1[n] = 2 \delta [n - 3]$ -> chỉ có tín hiệu ở $n = 3$ và biên độ = 2
- [[IMG_1792.jpeg]]
- $x2[n] = -2 \delta [n + 1]$ -> có tín hiệu ở $n = -1$ và biên độ = 2
- [[IMG_1793.jpeg]]


