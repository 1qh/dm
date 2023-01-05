# Discreet Math

## Count

- 32 xâu nhị phân độ dài 5
- 16 xâu nhị phân độ dài 5 sao cho bít đầu = bít cuối
- $2^5 + 2^5 - 2^3 = 56$ xâu nhị phân 7bit hoặc bắt đầu bằng 10 hoặc kết thúc bằng 00 (hoặc + hoặc - và)
- Hoán vị tiếp theo của 45827631 theo thứ tự từ điển: 45831267
- 15 nam vào 15 nữ. 15C1 x 15C2 cách bầu 1 nam và 2 nữ
- Có thể chọn nhiều nhất 4 việc để phân cho thợ sao cho mỗi việc chỉ được thực hiện bởi duy nhất 1 thợ và mỗi thợ ko thực hiện quá 1 việc
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
