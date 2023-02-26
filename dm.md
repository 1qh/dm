# Discreet Math

## Count

- Có **50 + 33 - 16 = 67** số tự nhiên 1 - 100 hoặc chia hết cho 2 hoặc chia hết cho 3

- 32 xâu nhị phân độ dài 5

- 16 xâu nhị phân độ dài 5 sao cho bít đầu = bít cuối

- $2^5 + 2^5 - 2^3 = 56$ xâu nhị phân 7bit hoặc bắt đầu bằng 10 hoặc kết thúc bằng 00 (hoặc + hoặc - và)

- Số xâu nhị phân độ dài 5 ko chứa 2 bít 1 đứng cạnh nhau

  - Nếu bit cuối (n) = 0
    - bit n - 1 có thể = 1 or 0
  - Nếu bit cuối (n) = 1
    - bit n - 1 chỉ có thể = 0
    - bit n - 2 có thể = 1 or 0
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

- Có 6.5.4.3.5! = **43200**
  - cách sắp xếp 5 nam và 4 nữ trên một hàng ngang sao cho ko có 2 nữ nào cạnh nhau
  - hoán vị của 1, 2, 3, 4, 5, 6, 7, 8, 9 sao cho ko có 2 chẵn nào cạnh nhau
- $X1 + X2 + X3 + X4 = 11$ có **$C^3_{10} = 120$** nghiệm nguyên dương

- Có thể chọn nhiều nhất **4 việc** để phân cho thợ sao cho mỗi việc chỉ được thực hiện bởi duy nhất 1 thợ và mỗi thợ ko thực hiện quá 1 việc

  - thợ 1 việc 4
  - thợ 2 việc 1 or 5
  - thợ 3 việc 4
  - thợ 4 việc 2 or 3
  - thợ 5 việc 1 or 5

- 10 số 1-10 xếp trên đường thẳng theo thứ tự từ trái qua phải.

  - **35** cách chọn ra 4 phần tử sao cho ko có 2 phần tử nào đứng cạnh nhau cùng được chọn
    - $1 \le x1 \le x2+1 \le x3+2 \le x4+3 \le 10 $
    - $1 \le x1 < x2 < x3 < x4 \le 7$
    - $C^4_7 = 35$

- Hỏi có bao nhiêu bộ có thứ tự (A, B) sao cho:
  A, B là 2 tập con của {1, 2, 3, 4}
  Số phần tử của A hợp với B là 4
  Số phần tử của A giao B là 1

  - $2^3 * 4 = 32$

- Có bao nhiêu cách chọn ra 4 phần tử từ 7 số 1, 2, …, 7 sao cho luôn có 2 số liên tiếp nhau cùng được chọn?

  - 34
  - chi co 1 day 1357
  - 7C4 - 1

- Cho 6 chi tiết sản phẩm 1, 2, …, 6 cần được gia công trên 2 máy A và B với thời gian gia công trên máy A lần lượt là 3, 2, 5, 4, 6, 7 và trên máy B lần lượt là 1, 2, 4, 3, 7, 4.

  - Mỗi chi tiết sản phẩm cần hoàn thành gia công trên máy A thì mới chuyển sang gia công trên máy B
  - Mỗi thời điểm, mỗi máy chỉ thực hiện gia công được nhiều nhất 1 chi tiết sản phẩm

  - Hãy xác định thời gian sớm nhất hoàn thành việc gia công 6 chi tiết sản phẩm trên 2 máy A và B.

    - ko cung luc lam 2 viec
    - xong A moi sang B
    - algo
      - chia thanh 2 loai
        - a >= b (loai 1)
        - a < b (loai 2)
      - lam loai 1 thu tu A tang
      - lam loai 2 thu tu B giam
      - tinh tong
        - prefix[i] theo thu tu A lam (tren xuong duoi)
        - suffix[i] theo thu tu B lam (duoi len tren)
      - ans = max(prefix[i] + suffix[i])
    - 28

## Graph

- 1

  - V = {1, 2, 3, 4, 5, 6}
  - E = {(1,2),(1,3),(1,6),(2,3),(2,5),(2,6),(4,5),(4,6),(5,6)}
    - G KHÔNG phải là đồ thị đầy đủ
    - vi do thi du phai co n \* (n-1) / 2 canh
      - 15 canh

- 2

  - V = {1,2,3,4,5,6,7,8}
  - E = {(1,2),(1,3),(1,6),(2,3),(2,5),(4,5),(4,6),(5,6),(7,8)}.
  - ít nhất cần bổ sung thêm 3 cạnh (1,8), (5,7), (2,6)
    - G trở thành đồ thị Euler
    - Vi Euler phai co tat ca cac dinh bac chan va lien thong
      - deg(1) = 3
      - deg(2) = 3
      - deg(3) = 2
      - deg(4) = 2
      - deg(5) = 3
      - deg(6) = 3
      - deg(7) = 1
      - deg(8) = 1

- duyệt theo chiều sâu trên G từ đỉnh s luôn cho ta đường đi ngắn nhất theo số cạnh từ s đến tất cả các đỉnh cùng thành phần liên thông với s

  - sai
  - vi duyet theo chieu ngang moi dung - BFS

- Cho đồ thị vô hướng trọng số trên cạnh G = (V,E) trong đó V = {1,2,3,4,5,6} và E = {(1,2),(1,3),(1,6),(2,3),(2,5),(2,6),(4,5),(4,6),(5,6)}. Trọng số trên cạnh w(1,2) = 1, w(1,3) = 1, w(1,6) = 4, w(2,3) = 1, w(2,5) = 2, w(2,6) = 2, w(4,5) = 3, w(4,6) = 5, w(5,6) = 2.

  - Hỏi cây khung nhỏ nhất của G có trọng số bằng bao nhiêu?

    - sort trong so tu be den lon
    - build graph sao cho ko co cycle
    - tinh tong trong so

  - Hỏi có tồn tại cây khung nhỏ nhất của G chứa cạnh (4,6) hay không?
    - KHÔNG
    - khi them canh (x,y) vao cay khung nho nhat
      - bo canh lon nhat tren duong di ngan nhat tu x -> y
      - so sanh canh do voi (x,y)
        - chi co the ton tai khi bang nhau

- Cho đồ thị vô hướng G=(V,E) trong đó tập đỉnh V = {1, 2, 3, 4, 5, 6} và tập cạnh E = {(1,4),(1,6),(2,5),(2,6),(3,4),(3,5),(3,6)}. Hỏi G có phải là đồ thị hai phía hay không?

  - CÓ
  - 2 phia ko co cycle le (tam giac, ngu giac)

- Cho đồ thị vô hướng G=(V,E) trong đó tập đỉnh V = {1, 2, 3, 4, 5, 6} và tập cạnh E ={(1,2),(,1,3),(1,6),(2,3),(2,5),(2,6),(4,5),(4,6),(5,6)}. Hỏi G có phải là đồ thị Euler hay không?

  - KHÔNG vi co dinh bac le

- Cho đồ thị vô hướng trọng số trên cạnh G = (V,E) trong đó V = {1,2,3,4,5,6} và E = {(1,2),(1,3),(1,6),(2,3),(2,5),(2,6),(4,5),(4,6),(5,6)}. Trọng số trên cạnh w(1,2) = 1, w(1,3) = 1, w(1,6) = 4, w(2,3) = 1, w(2,5) = 2, w(2,6) = 2, w(4,5) = 3, w(4,6) = 5, w(5,6) = 2. Hỏi cây khung nhỏ nhất của G có bao nhiêu cạnh?

  - 5
  - ko can quan tam trong so
  - cay khung nho nhat co n dinh -> n - 1 canh

- Cho đồ thị vô hướng G=(V,E) trong đó tập đỉnh V = {1, 2, 3, 4, 5, 6} và tập cạnh E ={(1,2),(,1,3),(1,6),(2,3),(2,5),(2,6),(4,5),(4,6),(5,6),(1,5)}. Hỏi chu trình nào dưới đây là chu trình Euler?

  - chu trinh Euler: xuat phat tai 1 dinh va ket thuc tai dinh do, di qua moi canh duy nhat 1 lan
    - -> dem so canh tren chu trinh == E thi dung
  - 3 - 2 - 1 - 5 - 2 - 6 - 5 - 4 - 6 - 1 - 3

- Cho đồ thị vô hướng G=(V,E) trong đó tập đỉnh V = {1, 2, 3, 4, 5, 6} và tập cạnh E ={(1,2),(,1,3),(1,6),(2,3),(2,5),(2,6),(4,5),(4,6),(5,6),(1,5)}. Hỏi chu trình nào dưới đây là chu trình Hamilton?

  - 1 - 3 - 2 - 5 - 4 - 6 - 1
  - Hamilton xuat phat & ket thuc cung 1 dinh, di qua tat ca cac dinh duy nhat 1 lan

- Cho đồ thị có hướng G = (V,E) trong đó tập đỉnh V = {1,2,3,4,5,6} và tập cung E = {(1,2),(2,5),(2,6),(3,1),(3,2),(5,4),(5,6),(6,1),(6,4)}. Hỏi có thể tiến hành sắp xếp TOPO các đỉnh trên G hay không?

  - KHÔNG
  - sap xep topo <=> kvck ko co chu trinh
  - tim chu trinh
    - bat dau tai 1 dinh, tim duong quay ve chinh no
    - neu co thi k duoc

- Cho đồ thị vô hướng G=(V,E) trong đó tập đỉnh V = {1, 2, 3, 4, 5, 6} và tập cạnh E ={(1,2),(,1,3),(1,6),(2,3),(2,5),(2,6),(4,5),(4,6),(5,6). Thực hiện phép duyệt đồ thị G theo chiều rộng (khi xét các đỉnh thì xét theo thứ tự từ điển). Hỏi đường đi từ đỉnh 1 đến đỉnh 4 trong phép duyệt theo chiều rộng là đường đi nào dưới đây?

  - 1 - 6 - 4
  - duong di ngan nhat co the tim duoc uu tien tu dien

- Cho đồ thị có hướng G = (V,E) trong đó tập đỉnh V = {1,2,3,4,5,6} và tập cung E = {(1,6),(2,1),(2,5),(2,6),(3,1),(3,2),(5,4),(5,6),(6,4)}. Thứ tự các đỉnh trong sắp xếp TOPO trên G là thứ tự nào sau đây?

  - 3, 2, 1, 5, 6, 4
  - thu tung canh trong E xem co xuat hien tu trai sang phai ko
    - neu co thi ok

- Cho mạng G = (V,E) trong đó tập đỉnh V = {1,2,3,4,5,6} và tập cung E = {(1,6),(2,1),(2,5),(2,6),(3,1),(3,2),(5,4),(5,6),(6,4)}. Khả năng thông qua trên các cung được cho như sau: c(1,6) = 6, c(2,1)=5, c(2,5) = 2, c(2,6) = 4, c(3,1) = 9, c(3,2) = 7, c(5,4) = 8, c(5,6) = 6, c(6,4) = 8. Hỏi luồng cực đại trên G có giá trị bằng bao nhiêu?

  - 10
  - cach tim luong cuc dai
    - tim source: ko co dinh nao di toi no
    - tim sink: ko co duong nao di tu no
    - tim lat cat cuc tieu
      - la tap cac cung sao cho ko co duong tu source -> sink
      - max flow = min(sum(kha nang thong qua tap cung do))
      - tim cac canh co tong be nhat ma khi xoa di ko co duong source -> sinh

- Đồ thị vô hướng có 10 đỉnh, bậc của mỗi đỉnh lớn hơn hoặc bằng 5. Hỏi phát biểu "G luôn là đồ thị liên thông" là đúng hay sai?

  - Đúng
  - Xet 1 dinh
    - noi voi 5 dinh khac
    - co 1 tp lien thong 6 dinh
    - max 4 dinh ko thuoc tp do
    - moi dinh do lai co tp lien thong voi 5 dinh khac
    - G lien thong

- G là một đồ thị phẳng (planar graph) và liên thông có 7 đỉnh và 12 cạnh, Hỏi đồ thị đó chia mặt phẳng thành mấy vùng?

  - V - E + f = 2
  - 7 - 12 + f = 2
  - f = 7

- Hỏi có tồn tại đồ thị phẳng liên thông sao cho mỗi đỉnh kề với ít nhất 6 đỉnh khác hay không?

  - Không
  - Dieu kien: e <= 3v - 6
  - e = 6v / 2 = 3v (ko thoa man)

- Có tồn tại đồ thị phẳng nào gồm 8 cạnh và chia mặt phẳng thành 6 vùng không?

  - v - e + f = 2
  - v - 8 + 6 = 2
  - v = 4
  - Dieu kien: e <= 3v - 6
  - 3v - 6 = 6
  - e = 8 ko thoa man

- Cho G là đồ thị vô hướng liên thông có 10 đỉnh, bậc của mỗi đỉnh là 5. Hỏi kết luận "Đồ thị G là đồ thị Hamilton (có chu trình Hamilton trên G)" đúng hay sai?

  - Đúng
  - deg(v) >= n / 2

- Tổng luồng đi ra khỏi đỉnh phát bằng tổng luồng đi vào đỉnh thu trên một mạng là ĐÚNG

- luồng trên mỗi cung luôn trong một mạng phải bằng khả năng thông qua của cung đó là SAI
