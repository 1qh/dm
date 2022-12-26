# Discreet Math Cheat Sheet

## Count

- 32 xâu nhị phân độ dài 5
- $2^5 + 2^5 - 2^3 = 56$ xâu nhị phân 7bit hoặc bắt đầu bằng 10 hoặc kết thúc bằng 00 (hoặc + hoặc - và)

## Graph

- 1

  - V = {1,2,3,4,5,6,7,8}
  - E = {(1,2),(1,3),(1,6),(2,3),(2,5),(4,5),(4,6),(5,6),(7,8)}.
  - ít nhất cần bổ sung thêm 3 cạnh (1,8), (5,7), (2,6)
    - G trở thành đồ thị Euler

- 2

  - V = {1, 2, 3, 4, 5, 6}
  - E = {(1,2),(1,3),(1,6),(2,3),(2,5),(2,6),(4,5),(4,6),(5,6)}
    - G KHÔNG phải là đồ thị đầy đủ

- duyệt theo chiều sâu trên G từ đỉnh s luôn cho ta đường đi ngắn nhất theo số cạnh từ s đến tất cả các đỉnh cùng thành phần liên thông với s
  - sai
