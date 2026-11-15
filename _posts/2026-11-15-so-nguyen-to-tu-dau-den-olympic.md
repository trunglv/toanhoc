---
title: "Số nguyên tố: từ dễ hiểu đến các bài olympic"
date: 2026-11-15 09:00:00 +0700
categories: [so-hoc]
lang: vi
---

Bạn có thể chia hết cho 1 và chính mình. Nhưng số 7 chỉ chia hết cho 1 và 7, còn số 6 thì chia hết cho 1, 2, 3, 6. Sự khác nhau nhỏ đó là ý tưởng của bài này: **số nguyên tố**.

## 1. Số nguyên tố là gì?

<div class="note">
<span class="note-label">Định nghĩa</span>
<p><strong>Số nguyên tố</strong> là số tự nhiên lớn hơn 1, chỉ có đúng hai ước là 1 và chính nó.</p>
</div>

Ví dụ: 2, 3, 5, 7, 11, 13 đều là số nguyên tố.

Ngược lại, số lớn hơn 1 mà không phải số nguyên tố gọi là **hợp số**. Ví dụ 4 có ước 1, 2, 4; 9 có ước 1, 3, 9.

Hai số cần chú ý đặc biệt:

- **Số 0 và số 1 không phải số nguyên tố.** Số 1 chỉ có một ước là chính nó, không đủ hai ước.
- **Số 2 là số nguyên tố chẵn duy nhất.** Mọi số chẵn lớn hơn 2 đều chia hết cho 2 nên đều là hợp số.

## 2. Liệt kê các số nguyên tố nhỏ hơn 50

Để kiểm tra một số có phải số nguyên tố hay không, ta thử chia nó cho các số nhỏ: 2, 3, 5, 7, ... Nếu có một phép chia hết (ngoài 1 và chính nó) thì đó là hợp số.

Với các số nhỏ, bảng sau giúp bạn nhớ nhanh:

| Khoảng | Các số nguyên tố |
|---|---|
| 1 – 10 | 2, 3, 5, 7 |
| 11 – 20 | 11, 13, 17, 19 |
| 21 – 30 | 23, 29 |
| 31 – 40 | 31, 37 |
| 41 – 50 | 41, 43, 47 |

Có tất cả **15 số nguyên tố nhỏ hơn 50**.

## 3. Mẹo: sàng Eratosthenes

Cách tìm nhiều số nguyên tố cùng lúc rất đơn giản:

1. Viết các số từ 2 đến 50 ra giấy.
2. Gạch các bội của 2 (trừ 2 chính nó): 4, 6, 8, ...
3. Số đầu tiên còn lại là 3. Gạch các bội của 3 (trừ 3): 6, 9, 12, ...
4. Số đầu tiên còn lại là 5. Gạch các bội của 5.
5. Làm tiếp với 7. Các số không bị gạch là số nguyên tố.

Bạn chỉ cần thử đến 7 vì $7 \cdot 7 = 49 < 50$, còn $11 \cdot 11 = 121$ đã vượt quá 50.

## 4. Phân tích ra thừa số nguyên tố

Mọi số tự nhiên lớn hơn 1 đều viết được thành tích các số nguyên tố, và cách viết đó là duy nhất (không tính thứ tự).

Ví dụ: $2024 = 2 \cdot 1012 = 2 \cdot 2 \cdot 506 = 2 \cdot 2 \cdot 2 \cdot 253 = 2^3 \cdot 11 \cdot 23$.

Cách làm: chia dần cho số nguyên tố nhỏ nhất có thể, cho đến khi không chia được nữa.

<div class="note note-try">
<span class="note-label">Thử sức</span>
<p>Phân tích $360$ ra thừa số nguyên tố. Đáp số: $360 = 2^3 \cdot 3^2 \cdot 5$.</p>
</div>

## 5. Có vô số số nguyên tố không?

Có. Đây là chứng minh của Euclid, khoảng 300 năm trước Công nguyên, và nó vẫn rất dễ hiểu:

Giả sử chỉ có hữu hạn số nguyên tố, ví dụ: 2, 3, 5, 7, 11, 13. Nhân chúng lại rồi cộng thêm 1:

<div class="math-block">
$$2 \cdot 3 \cdot 5 \cdot 7 \cdot 11 \cdot 13 + 1 = 30031$$
</div>

Số 30031 không chia hết cho 2, 3, 5, 7, 11, 13 (luôn dư 1). Vậy nó có ước nguyên tố khác. Ví dụ $30031 = 59 \cdot 509$, và 59 không nằm trong danh sách. Điều này mâu thuẫn với giả sử ban đầu, nên số nguyên tố là vô hạn.

## 6. Các dạng toán nâng cao (olympic và học sinh giỏi)

Các bài dưới đây dùng đúng kiến thức ở trên, nhưng cần thêm một ý tưởng: **xét số dư khi chia cho 3**.

### Bài 1: Ba số cách đều nhau

Tìm tất cả số nguyên tố $p$ sao cho $p + 2$ và $p + 4$ cũng là số nguyên tố.

<div class="note">
<span class="note-label">Gợi ý</span>
<p>Hãy xét ba số $p$, $p+2$, $p+4$. Chúng có số dư khác nhau khi chia cho 3. Trong ba số này phải có một số chia hết cho 3.</p>
</div>

**Lời giải.** Nếu $p = 2$ thì $p + 2 = 4$ không là số nguyên tố, loại. Vậy $p$ là số lẻ.

Ba số $p$, $p+2$, $p+4$ có số dư khi chia cho 3 lần lượt là $r$, $r+2$, $r+1$ (với $r$ là số dư của $p$), tức là ba số dư khác nhau. Nên đúng một trong ba số chia hết cho 3. Vì chúng đều là số nguyên tố, số chia hết cho 3 đó phải bằng 3. Mà $p \ge 3$ nên chỉ có thể $p = 3$.

Thử lại: 3, 5, 7 đều là số nguyên tố. **Đáp số: $p = 3$.**

### Bài 2: Số nguyên tố và bình phương

Tìm tất cả số nguyên tố $p$ sao cho $p^2 + 2$ cũng là số nguyên tố.

**Lời giải.** Nếu $p = 2$ thì $p^2 + 2 = 6$, là hợp số, loại.

Nếu $p \ne 3$ thì $p$ không chia hết cho 3, nên $p \equiv 1$ hoặc $2 \pmod 3$, và khi đó $p^2 \equiv 1 \pmod 3$. Suy ra $p^2 + 2 \equiv 0 \pmod 3$, tức là $p^2 + 2$ chia hết cho 3. Vì $p^2 + 2 > 3$ nên nó là hợp số, loại.

Vậy $p = 3$, và $3^2 + 2 = 11$ là số nguyên tố. **Đáp số: $p = 3$.**

### Bài 3: Hai số nguyên tố có tổng bằng 2023?

Có tồn tại hai số nguyên tố có tổng bằng 2023 hay không?

**Lời giải.** Giả sử $a + b = 2023$ với $a, b$ là số nguyên tố. Tổng 2023 là số lẻ, nên một trong hai số phải chẵn. Số nguyên tố chẵn duy nhất là 2. Giả sử $a = 2$, khi đó $b = 2021$.

Mà $2021 = 43 \cdot 47$ không phải số nguyên tố. Vậy **không tồn tại** hai số nguyên tố như vậy.

<div class="note note-try">
<span class="note-label">Thử sức</span>
<p>Có tồn tại hai số nguyên tố có tổng bằng 2024 không? Gợi ý: 2024 là số chẵn, nên có thể cả hai số đều là số lẻ.</p>
</div>

### Bài 4: Số nhỏ nhất có đúng 6 ước

Tìm số tự nhiên nhỏ nhất có đúng 6 ước.

**Lời giải.** Nếu $n = p^a$ với $p$ là số nguyên tố thì $n$ có $a + 1$ ước. Nếu $n = p^a \cdot q^b$ với $p$, $q$ là hai số nguyên tố khác nhau thì $n$ có $(a+1)(b+1)$ ước.

Để có đúng 6 ước, ta có hai khả năng:

- $n = p^5$: số nhỏ nhất là $2^5 = 32$.
- $n = p^2 \cdot q$ (vì $(a+1)(b+1) = 3 \cdot 2 = 6$): số nhỏ nhất là $2^2 \cdot 3 = 12$.

So sánh, $12 < 32$. **Đáp số: 12.** Kiểm tra: các ước của 12 là 1, 2, 3, 4, 6, 12, đúng 6 ước.

## Tóm tắt

- Số nguyên tố: lớn hơn 1, chỉ có hai ước là 1 và chính nó.
- Số 2 là số nguyên tố chẵn duy nhất.
- Mọi số lớn hơn 1 phân tích được thành tích các số nguyên tố, và cách phân tích là duy nhất.
- Có vô số số nguyên tố.
- Trong các bài olympic, xét số dư khi chia cho 2 và cho 3 là cách thường gặp nhất.
