# Discreet Math

## Count

- 32 xâu nhị phân độ dài 5

- 16 xâu nhị phân độ dài 5 sao cho bít đầu = bít cuối

- $2^5 + 2^5 - 2^3 = 56$ xâu nhị phân 7bit hoặc bắt đầu bằng 10 hoặc kết thúc bằng 00 (hoặc + hoặc - và)

- Số xâu nhị phân độ dài 5 ko chứa 2 bít 1 đứng cạnh nhau

  - Nếu bit cuối (n) = 0
    - bit n – 1 có thể = 1 or 0
  - Nếu bit cuối (n) = 1
    - bit n – 1 chỉ có thể = 0
    - bit n – 2 có thể = 1 or 0
  - &rarr; $f_n = f_{n-1} + f_{n-2}$
    - $f_1 = 2$
    - $f_2 = 3$
    - $f_3 = 5$
    - $f_4 = 8$
    - **$f_5 = 13$**

- Có **42** cách phân tích 10 thành tổng của các số nguyên dương

  - Số cách phân tích n thành tổng $X1 + X2 + ... + Xk$
    - với $1 \le X1 \le X2 \le ... \le Xk$
  - Số cách phân tích $n$ thành tổng các số nguyên dương $\ge q$
  - $F(q,n) = 1 + F(q,n-q) + F(q+1, n-q-1) + F(q+2, n-q-2) + ...$
    - $F(q,n) = 1$ nếu $n = q$
    - $F(q,n) = 0$ nếu $n < q$
  - $F(1,10) = 1 + F(1,9) + F(2,8) + F(3,7) + F(4,6) + 1$

- Có **$4.2^3 = 32$** bộ có thứ tự (A, B) sao cho:

  - A, B là 2 tập con của {1, 2, 3, 4}
  - Số phần tử của A hợp với B là 4
  - Số phần tử của A giao B là 1
  - &rarr; 4 cách chọn 1 phần tử giao nhau, 3 phần tử còn lại được chia vào 2 tập

- Hoán vị tiếp theo của 45827631 theo thứ tự từ điển: 45831267

- 15 nam vào 15 nữ. 15C1 x 15C2 cách bầu 1 nam và 2 nữ

- $X1 + X2 + X3 + X4 = 11$ có **$C^3_{10} = 120$** nghiệm nguyên dương

- Có thể chọn nhiều nhất **4 việc** để phân cho thợ sao cho mỗi việc chỉ được thực hiện bởi duy nhất 1 thợ và mỗi thợ ko thực hiện quá 1 việc
  - thợ 1 việc 4
  - thợ 2 việc 1 or 5
  - thợ 3 việc 4
  - thợ 4 việc 2 or 3
  - thợ 5 việc 1 or 5

## Graph

- 1

  - V = {1, 2, 3, 4, 5, 6}
  - E = {(1,2),(1,3),(1,6),(2,3),(2,5),(2,6),(4,5),(4,6),(5,6)}
    - G KHÔNG phải là đồ thị đầy đủ

- 2

  - V = {1,2,3,4,5,6,7,8}
  - E = {(1,2),(1,3),(1,6),(2,3),(2,5),(4,5),(4,6),(5,6),(7,8)}.
  - ít nhất cần bổ sung thêm 3 cạnh (1,8), (5,7), (2,6)
    - G trở thành đồ thị Euler

- duyệt theo chiều sâu trên G từ đỉnh s luôn cho ta đường đi ngắn nhất theo số cạnh từ s đến tất cả các đỉnh cùng thành phần liên thông với s
  - sai
