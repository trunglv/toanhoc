---
title: "Monty Hall: đổi cửa hay giữ cửa?"
date: 2026-11-14 09:00:00 +0700
categories: [xac-suat]
lang: vi
---

Bạn đang trong một chương trình truyền hình. Có ba cánh cửa. Sau một cửa là chiếc xe, sau hai cửa còn lại là dê. Bạn chọn cửa số 1.

Người dẫn chương trình, người biết rõ cửa nào có xe, mở một cửa khác, cửa số 3, và cho bạn thấy có một con dê. Anh ta hỏi: bạn có muốn đổi sang cửa số 2 không?

Nhiều người trả lời ngay là "không quan trọng", vì còn hai cửa, mỗi cửa xác suất $\frac{1}{2}$. Trực giác này sai.

## Lập luận đơn giản

Lúc đầu, cửa bạn chọn có xác suất $\frac{1}{3}$ chứa xe. Vậy xác suất xe nằm ở hai cửa còn lại là $\frac{2}{3}$.

Người dẫn chương trình luôn mở một cửa có dê. Anh ta không thay đổi xác suất đó, chỉ loại bỏ một lựa chọn. Toàn bộ $\frac{2}{3}$ ấy dồn về cửa còn lại. Vì vậy đổi cửa thắng với xác suất $\frac{2}{3}$, giữ cửa chỉ thắng với xác suất $\frac{1}{3}$.

## Kiểm tra bằng công thức Bayes

Gọi $C$ là vị trí xe, $H$ là sự kiện người dẫn mở cửa 3. Giả sử bạn chọn cửa 1.

- Nếu xe ở cửa 1, người dẫn có hai lựa chọn (cửa 2 hoặc 3): $P(H \mid C=1) = \frac{1}{2}$.
- Nếu xe ở cửa 2, người dẫn buộc phải mở cửa 3: $P(H \mid C=2) = 1$.
- Nếu xe ở cửa 3, người dẫn không thể mở cửa 3: $P(H \mid C=3) = 0$.

Xác suất mở cửa 3 là

<div class="math-block">
$$P(H) = \frac{1}{2}\cdot\frac{1}{3} + 1\cdot\frac{1}{3} + 0\cdot\frac{1}{3} = \frac{1}{2}$$
</div>

Theo Bayes, xác suất xe ở cửa 2 khi biết người dẫn đã mở cửa 3 là

<div class="math-block">
$$P(C=2 \mid H) = \frac{P(H \mid C=2)\,P(C=2)}{P(H)} = \frac{1 \cdot \frac{1}{3}}{\frac{1}{2}} = \frac{2}{3}$$
</div>

Kết quả khớp với lập luận đơn giản.

## Tự kiểm tra bằng mô phỏng

Nếu vẫn chưa tin, hãy chạy thử. Đoạn Python ngắn sau mô phỏng chương trình hàng trăm nghìn lần:

```python
import random

def play(switch):
    car = random.randrange(3)
    pick = random.randrange(3)
    opened = next(d for d in range(3) if d != pick and d != car)
    if switch:
        pick = next(d for d in range(3) if d != pick and d != opened)
    return pick == car

n = 100_000
print("đổi cửa:", sum(play(True) for _ in range(n)) / n)   # xấp xỉ 0.667
print("giữ cửa:", sum(play(False) for _ in range(n)) / n)  # xấp xỉ 0.333
```

<div class="note">
<span class="note-label">Vì sao trực giác sai</span>
<p>Ta dễ nghĩ rằng sau khi một cửa bị mở, bài toán "reset" thành hai cửa 50/50. Nhưng người dẫn mở cửa không phải ngẫu nhiên: anh ta luôn biết và luôn tránh cửa có xe. Thông tin đó chính là thứ làm thay đổi xác suất.</p>
</div>
