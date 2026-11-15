---
title: "Định lý Pythagoras: chứng minh bằng diện tích"
date: 2026-11-12 09:00:00 +0700
categories: [hinh-hoc]
lang: vi
---

Mọi người đều học định lý Pythagoras: trong tam giác vuông có hai cạnh góc vuông $a$, $b$ và cạnh huyền $c$ thì

<div class="math-block">
$$a^2 + b^2 = c^2$$
</div>

Nhưng học thuộc công thức khác với hiểu vì sao nó đúng. Bài này chứng minh bằng một hình vuông và vài tam giác, không cần đại số phức tạp.

## Ý tưởng

Lấy một hình vuông có cạnh $a + b$. Trong hình vuông lớn này, đặt bốn tam giác vuông giống hệt nhau, mỗi tam giác có cạnh góc vuông là $a$ và $b$, sao cho chúng vây quanh một hình vuông nhỏ ở giữa.

Hình vuông ở giữa có cạnh là cạnh huyền $c$, nên diện tích của nó là $c^2$.

## Tính diện tích theo hai cách

Cách 1: diện tích hình vuông lớn là bình phương cạnh.

<div class="math-block">
$$S = (a+b)^2 = a^2 + 2ab + b^2$$
</div>

Cách 2: cộng diện tích bốn tam giác và hình vuông ở giữa. Mỗi tam giác có diện tích $\frac{ab}{2}$, nên

<div class="math-block">
$$S = 4 \cdot \frac{ab}{2} + c^2 = 2ab + c^2$$
</div>

Cả hai cách đều tính cùng một diện tích, nên

<div class="math-block">
$$a^2 + 2ab + b^2 = 2ab + c^2$$
</div>

Trừ $2ab$ ở hai vế, ta được $a^2 + b^2 = c^2$. Xong.

<div class="note">
<span class="note-label">Điểm đáng nhớ</span>
<p>Chứng minh này không dùng đến tính chất của số. Nó chỉ dựa vào việc diện tích không đổi khi ta sắp xếp lại các mảnh. Đó là lý do nhiều người xem nó là một trong những chứng minh đẹp nhất của định lý.</p>
</div>

## Định lý đảo và các hệ quả

Ngược lại, nếu $a^2 + b^2 = c^2$ thì tam giác có ba cạnh $a$, $b$, $c$ là tam giác vuông. Vì vậy bộ ba $(3, 4, 5)$ dùng được để dựng góc vuông chính xác khi xây móng nhà: đo $3$ m, $4$ m, $5$ m, và góc giữa hai cạnh ngắn sẽ là góc vuông.

Lịch sử của định lý dài hơn hình vẽ này rất nhiều. Đã có hàng trăm cách chứng minh được ghi lại, từ những chứng minh bằng hình đến cách dùng đồng dạng và đại số. Chọn cách nào tùy vào điều bạn muốn thấy rõ nhất.

<div class="note note-try">
<span class="note-label">Thử sức</span>
<p>Một tam giác vuông có cạnh góc vuông là $6$ cm và $8$ cm. Tính cạnh huyền.</p>
<p>Đáp số: $10$ cm, vì $6^2 + 8^2 = 36 + 64 = 100$.</p>
</div>
