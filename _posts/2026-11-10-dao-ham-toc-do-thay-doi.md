---
title: "Đạo hàm: tốc độ thay đổi nhìn bằng hình"
date: 2026-11-10 09:00:00 +0700
categories: [giai-tich]
lang: vi
---

Một chiếc xe đi trên đường. Sau 2 giờ nó đã đi được 100 km. Vậy nó chạy với vận tốc bao nhiêu?

Câu trả lời "50 km/h" đúng, nhưng chỉ là vận tốc **trung bình**. Trong hai giờ đó, lúc thì xe chậm lại ở đèn đỏ, lúc thì tăng tốc trên đường cao tốc. Khi bạn nhìn lên đồng hồ tốc độ, kim chỉ một con số tại đúng thời điểm đó. Đạo hàm là công cụ để nói về con số thứ hai ấy.

## Từ cát tuyến đến tiếp tuyến

Gọi $s(t)$ là quãng đường xe đi được sau $t$ giờ. Trên khoảng từ $t$ đến $t + h$, vận tốc trung bình là

<div class="math-block">
$$\frac{s(t+h) - s(t)}{h}$$
</div>

Trên đồ thị, đây là **độ dốc của cát tuyến**: đường thẳng nối hai điểm $(t, s(t))$ và $(t+h, s(t+h))$. Khi $h$ nhỏ dần về 0, hai điểm ấy dồn lại gần nhau, cát tuyến xoay dần và tiến đến **tiếp tuyến**, đường chỉ chạm đồ thị đúng tại một điểm.

Vận tốc tức thời là giới hạn đó:

<div class="math-block">
$$s'(t) = \lim_{h \to 0} \frac{s(t+h) - s(t)}{h}$$
</div>

Đây chính là định nghĩa đạo hàm. Với một hàm $f(x)$ bất kỳ, $f'(x)$ là độ dốc của tiếp tuyến tại điểm $x$.

## Ví dụ: $f(x) = x^2$

Tính trực tiếp:

<div class="math-block">
$$\frac{(x+h)^2 - x^2}{h} = \frac{2xh + h^2}{h} = 2x + h$$
</div>

Khi $h \to 0$ biểu thức còn lại $2x$. Vậy $(x^2)' = 2x$. Ở $x = 3$, đồ thị có độ dốc $6$; ở $x = 0$, độ dốc bằng $0$, đúng với hình dạng của parabol tại đỉnh.

<div class="note">
<span class="note-label">Ghi nhớ</span>
<p>Đạo hàm đo <em>tốc độ thay đổi tức thời</em>. Nếu đại lượng không đổi, đạo hàm bằng 0. Nếu đại lượng tăng, đạo hàm dương.</p>
</div>

## Vì sao nó hữu ích

Đạo hàm cho ta cách tìm cực trị. Tại đỉnh của một đường cong trơn, tiếp tuyến nằm ngang, nên $f'(x) = 0$. Đó là chỗ để bắt đầu tìm giá trị lớn nhất hoặc nhỏ nhất, từ bài toán tối ưu chi phí đến thiết kế hộp đựng có thể tích lớn nhất với lượng tôn cho trước.

Vài quy tắc cơ bản để tính nhanh:

- $(x^n)' = n x^{n-1}$
- $(\sin x)' = \cos x$
- $(e^x)' = e^x$

Bước tiếp theo thường là học quy tắc tích, quy tắc chuỗi, và cách dùng đạo hàm để vẽ phác đồ thị. Nhưng ý tưởng cốt lõi vẫn là bài toán chiếc xe ở trên: nhìn đoạn đường ngắn lại càng ngắn, và xem điều gì xảy ra ở giới hạn.

<div class="note note-try">
<span class="note-label">Thử sức</span>
<p>Tính đạo hàm của $f(x) = x^3$ bằng định nghĩa, theo đúng các bước như ví dụ $x^2$ ở trên. Gợi ý: khai triển $(x+h)^3$ rồi chia cho $h$.</p>
<p>Kiểm tra: kết quả đúng là $3x^2$.</p>
</div>
