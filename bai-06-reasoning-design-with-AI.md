# Buổi 6 — Reasoning Design with AI  
> Điều khiển cách AI suy luận: tuyến tính, đa nhánh, giả thuyết, nhân quả, so sánh

---

## 0. Bạn cần chuẩn bị gì trước Buổi 6?

Từ Buổi 5, bạn nên đã có:

1. **Exploration Map** (core/near/extended/out-of-scope).  
2. **Keyword Expansion Matrix**.  
3. **Facet Matrix**.  
4. **Node Prioritization Table**:
   - bạn đã chọn **1–2 node “đáng đào sâu”** cho domain mình.  
5. **Research Path v1**:
   - Pha breadth, selection, depth.

Buổi 6 sẽ dùng **1 node ưu tiên** làm “case chính” để luyện reasoning.

---

## 1. Mục tiêu của Buổi 6

Sau buổi này, bạn:

1. Phân biệt được 5 mode reasoning chính:
   - **CoT** (Chain of Thought) – tuyến tính,
   - **ToT** (Tree of Thought) – đa nhánh,
   - **Hypothesis-driven reasoning** – giả thuyết & kiểm định,
   - **Causal reasoning** – nguyên nhân–hệ quả, root cause,
   - **Comparative reasoning** – so sánh có tiêu chí.
2. Biết **khi nào dùng mode nào** cho loại bài toán gì.
3. Dùng AI để:
   - sinh chuỗi CoT có ý nghĩa (không chỉ “viết dài”),
   - mở 3–5 nhánh ToT khác nhau thật sự,
   - đặt & đánh giá 3–5 giả thuyết,
   - vẽ causal chain đơn giản,
   - so sánh các lựa chọn theo tiêu chí bạn đặt.
4. Tạo được **Reasoning Pack** cho 1 node trong domain thật:
   - CoT analysis,
   - ToT branches,
   - Hypothesis table,
   - Causal chain,
   - Comparative table (nếu phù hợp).

---

## 2. Vấn đề: “CoT” không phải là “viết dài ra”

Người dùng AI 1–3 năm thường:

- nghe nói CoT là “hãy suy nghĩ từng bước”,
- thêm câu: “Hãy giải thích từng bước chi tiết” vào prompt,
- nhận về:
  - 4–7 bước “một câu/1 bullet” nhưng:
    - mỗi bước chỉ lặp lại điều hiển nhiên,
    - không có “logic chuyển tiếp”.

**CoT đúng** phải:

- chỉ rõ:
  - bước này dựa trên dữ kiện/gỉa định nào,
  - tại sao dẫn đến bước sau,
- có thể **soát, sửa và phản biện** từng bước.

Buổi 6 không dừng ở “gọi tên CoT/ToT”, mà dạy **cách thiết kế reasoning**.

---

## 3. Bản đồ khái niệm Buổi 6

| Kỹ thuật                 | Dùng khi nào                                                                 |
|--------------------------|------------------------------------------------------------------------------|
| Chain of Thought (CoT)   | Bài toán tuyến tính, cần giải thích/chỉ đường từng bước                     |
| Tree of Thought (ToT)    | Bài toán mở, có nhiều hướng, cần khám phá không gian giải pháp              |
| Hypothesis-driven        | Nhiều khả năng nguyên nhân/giải thích, cần đặt & kiểm giả thuyết            |
| Causal reasoning         | Cần tìm root cause, hiểu “vì sao xảy ra”                                    |
| Comparative reasoning    | Cần chọn giữa A/B/C theo tiêu chí, tránh chọn theo cảm tính                 |

Ta sẽ luyện tất cả trên **1 node ưu tiên** bạn đã chọn.

---

## 4. Chọn “node để luyện” cho Buổi 6

Trước khi đi tiếp, hãy xác định:

- Node bạn muốn đào sâu ở Buổi 6 là gì?

Ví dụ (minh họa):

- “Đánh giá & kiểm định output AI trong dạy học”
- hoặc
- “Dùng AI thiết kế outline bài giảng”
- hoặc
- “Đảm bảo đạo đức & an toàn khi dùng AI trong giảng dạy”

Từ đây, tôi sẽ lấy ví dụ với node:

> “Đánh giá & kiểm định output AI trong dạy học”  
> (bạn hãy mentally thay bằng node của bạn khi đọc).

---

## 5. Chain of Thought (CoT) – tuyến tính có căn cứ

### 5.1. Khi nào dùng CoT?

- Khi bài toán:
  - có **bước rõ ràng** (1 → 2 → 3 → 4),
  - cần giải thích hoặc “walk through” một quy trình/chuỗi lập luận,
- Ví dụ:
  - “Làm sao giảng viên nên đánh giá 1 câu trả lời của AI cho đề bài X?”
  - “Quy trình kiểm định output AI trước khi đưa vào slide dạy.”

### 5.2. Prompt CoT chuẩn (tránh “viết dài vô nghĩa”)

Với node “đánh giá output AI”, ta có thể viết:

```text
Chủ đề: đánh giá & kiểm định output AI trong bối cảnh giảng dạy đại học.

Hãy phân tích quy trình mà một giảng viên nên đi qua khi kiểm định một đoạn trả lời của AI dùng trong bài giảng.

Yêu cầu:
1. Trình bày theo dạng Chain of Thought rõ ràng.
2. Mỗi bước phải nêu:
   - Mục tiêu của bước,
   - Dữ kiện hoặc giả định đang dùng,
   - Tiêu chí để chuyển sang bước tiếp theo.
3. Tổng số bước từ 5–9, không ít hơn nếu không đủ ý.

Trả ra:
- Danh sách các bước, đánh số 1, 2, 3,...
- Cuối cùng, ghi chú ngắn: "Bước yếu nhất trong chuỗi này là bước nào và vì sao".
```

### 5.3. Bạn làm gì với CoT nhận được?

- Check từng bước:
  - có **mục tiêu rõ** không?
  - có **dựa trên gì** (data/assumption/principle) không?
- Đánh dấu 1–2 bước mơ hồ → note lại cho Buổi 7 (Validation).

**Mini-bài tập:**  
Chạy prompt trên với node của bạn.  
Copy kết quả, đánh dấu 1–2 bước bạn thấy mơ hồ, comment tại sao.

---

## 6. Tree of Thought (ToT) – mở không gian suy nghĩ

### 6.1. Khi nào dùng ToT?

- Khi bài toán:
  - không có 1 đường duy nhất,
  - cần **3–5 chiến lược** hoặc **3–5 lời giải thích** khác nhau.
- Ví dụ:
  - “Có những chiến lược nào để nâng chất lượng đánh giá output AI của giảng viên?”
  - “3 hướng thiết kế module dạy AI literacy cho giảng viên như thế nào?”

### 6.2. Prompt ToT chuẩn (tránh “3 nhánh khác câu chữ nhưng cùng ý”)

Ví dụ:

```text
Chủ đề: nâng cao năng lực đánh giá & kiểm định output AI của giảng viên đại học.

Hãy phân tích ít nhất 3 NHÁNH tiếp cận khác nhau (Tree of Thought) cho bài toán:
"làm thế nào để một khoa/đại học nâng năng lực này trong 1 năm tới".

Yêu cầu:
1. Mỗi nhánh phải đại diện cho MỘT chiến lược khác thật sự, không chỉ đổi câu chữ. Ví dụ: nhánh tập trung vào training tập trung, nhánh tập trung vào mentoring tại chỗ, nhánh tập trung vào thay đổi policy + tool.
2. Với mỗi nhánh, trình bày:
   - Giả định nền của nhánh đó,
   - Các bước/hoạt động chính,
   - Ưu điểm,
   - Hạn chế,
   - Bối cảnh nào phù hợp nhất.
3. Cuối cùng, so sánh 3 nhánh theo ít nhất 3 tiêu chí: tốc độ, chi phí, độ bền vững.

Trả ra có heading rõ: "Nhánh 1: ...", "Nhánh 2: ...", "Nhánh 3: ...".
```

### 6.3. Bạn làm gì với ToT nhận được?

- Nhìn xem:
  - Có **nhánh nào thực ra giống nhau** không? (nếu có, prompt chưa đủ ràng buộc).
- Hỏi tiếp:
  - “Nhánh nào phù hợp nhất với bối cảnh của mình?” (dựa trên Framing Brief).
  - Ghi chú: bạn chọn nhánh nào là trọng tâm → liên kết với Research Path.

---

## 7. Hypothesis-driven Reasoning – tư duy theo giả thuyết

### 7.1. Khi nào dùng?

- Khi bạn muốn giải thích:
  - **vì sao** 1 hiện tượng xảy ra,
  - có **nhiều nguyên nhân khả dĩ**.
- Ví dụ:
  - “Vì sao nhiều giảng viên dùng AI rồi vẫn không nâng được chất lượng dạy?”
  - “Vì sao dù có policy, sinh viên vẫn lạm dụng AI để làm bài?”

### 7.2. Prompt Hypothesis chuẩn

Ví dụ:

```text
Chủ đề: giảng viên đã dùng AI 1–2 năm nhưng năng lực đánh giá output AI vẫn yếu.

Hãy tiếp cận vấn đề này theo hướng hypothesis-driven reasoning.

Yêu cầu:
1. Đề xuất ít nhất 3 giả thuyết khả dĩ (H1, H2, H3) giải thích hiện tượng trên.
2. Với mỗi giả thuyết, phân tích:
   - Bằng chứng ủng hộ (điều gì khiến chúng ta nghĩ giả thuyết này đúng),
   - Bằng chứng phản bác / trường hợp nó không đúng,
   - Dữ liệu nào cần thu thập thêm để kiểm chứng,
   - Nếu giả thuyết này đúng, ta nên can thiệp như thế nào.
3. Cuối cùng, xếp hạng các giả thuyết theo "độ hợp lý hiện tại" dựa trên thông tin bạn có.

Trả ra dạng bảng: H, mô tả, ủng hộ, phản bác, kiểm chứng thêm, hướng can thiệp.
```

### 7.3. Tại sao điều này quan trọng?

- Nó:
  - tách “ý kiến” khỏi “giả thuyết có thể kiểm chứng”,
  - chuẩn bị cho Buổi 7:
    - **Validation**: phân biệt fact vs assumption vs hypothesis.

---

## 8. Causal Reasoning – nguyên nhân, hệ quả, root cause

### 8.1. Khi nào dùng?

- Khi bạn cần đi từ **triệu chứng → nguyên nhân gốc**.
- Ví dụ:
  - “Vì sao chất lượng output AI trong bài giảng thấp?”
  - “Vì sao sinh viên lệ thuộc AI?”

### 8.2. Prompt Causal chuẩn

Ví dụ:

```text
Chủ đề: chất lượng đánh giá output AI của giảng viên thấp, dẫn tới việc dùng nội dung sai hoặc lệch trong bài giảng.

Hãy phân tích vấn đề này bằng causal reasoning.

Yêu cầu:
1. Phân biệt rõ:
   - Triệu chứng (symptoms),
   - Nguyên nhân trực tiếp (direct causes),
   - Nguyên nhân gốc (root causes),
   - Hệ quả downstream (downstream effects).
2. Vẽ (bằng text) một causal chain hoặc causal tree:
   - từ root cause đến symptoms,
   - và đến các hệ quả.
3. Chỉ ra:
   - 2 điểm can thiệp có leverage cao nhất,
   - 1–2 điểm mà nhiều người hay can thiệp sai chỗ (chữa triệu chứng, không chữa gốc).

Trả ra:
- Danh sách các lớp nguyên nhân/hệ quả,
- 1 causal chain dạng bullet,
- đề xuất can thiệp.
```

### 8.3. Bạn làm gì với causal map?

- Kết nối với Research Path & IA:
  - nơi nào bạn cần training,
  - nơi nào là policy/structure issue,
  - nơi nào có thể dùng AI để hỗ trợ.

---

## 9. Comparative Reasoning – so sánh có tiêu chí

### 9.1. Khi nào dùng?

- Khi bạn phải chọn giữa A/B/C:
  - 3 cách triển khai,
  - 3 module ưu tiên,
  - 3 chiến lược đào tạo,…
- Mục tiêu:
  - giảm **chọn theo cảm tính**,
  - tăng **ra quyết định có cấu trúc**.

### 9.2. Prompt Comparative chuẩn

Ví dụ:

```text
Giả sử tôi có 3 cách để nâng cao năng lực đánh giá output AI của giảng viên:
- Phương án A: khóa tập huấn tập trung 2 ngày
- Phương án B: mentoring tại chỗ từng khoa trong 3 tháng
- Phương án C: xây AI tutor hỗ trợ giảng viên tự luyện

Hãy giúp tôi so sánh 3 phương án này bằng comparative reasoning.

Yêu cầu:
1. Đề xuất bộ tiêu chí so sánh phù hợp với mục tiêu:
   "tăng năng lực thực tế trong 1 năm, trong bối cảnh trường có ngân sách hạn chế".
2. Với mỗi tiêu chí:
   - giải thích nó quan trọng thế nào,
   - rồi cho điểm hoặc mô tả A/B/C theo tiêu chí đó.
3. Cuối cùng:
   - tóm tắt trade-off,
   - đề xuất trong bối cảnh [mô tả bối cảnh của bạn], nên ưu tiên phương án nào và vì sao.

Trả ra dạng bảng + đoạn kết luận.
```

---

## 10. Bài tập Buổi 6 – Reasoning Pack cho node của bạn

### 10.1. Bài tập 1 — CoT + Causal cho node

1. Chọn node ưu tiên (từ Buổi 5).
2. Viết 1 prompt CoT (tuyến tính) để:
   - mô tả quy trình/chuỗi suy luận về node đó.
3. Viết 1 prompt causal:
   - phân tích nguyên nhân–hệ quả.

**Nộp**:  
- CoT output (copy + highlight 1–2 bước yếu),  
- Causal output (causal chain/cây).

---

### 10.2. Bài tập 2 — ToT + Hypothesis

1. Viết 1 prompt ToT:
   - 3–4 nhánh chiến lược/giải pháp liên quan node đó.
2. Viết 1 prompt hypothesis:
   - 3–5 giả thuyết giải thích một hiện tượng có liên quan tới node.

**Nộp**:  
- ToT output (có 3+ nhánh khác thật),  
- Hypothesis table (H, ủng hộ, phản bác, kiểm chứng, can thiệp).

---

### 10.3. Bài tập 3 — Comparative table (nếu phù hợp)

Chọn 2–4 phương án A/B/C/D liên quan node:

- so sánh bằng bảng criteria-driven (như ví dụ ở trên).

---

## 11. Assignment Buổi 6 — Reasoning Pack cho domain của bạn

### 11.1. Đề bài

Tạo 1 **Reasoning Pack** (markdown) cho **01 node** mà bạn đã chọn ở Buổi 5, gồm:

1. **CoT Analysis**:
   - Chuỗi bước logic (5–9 bước) cho 1 quy trình/bài toán liên quan node.
2. **ToT Branches**:
   - Ít nhất 3 nhánh suy nghĩ/chiến lược khác nhau, có ưu/nhược & bối cảnh phù hợp.
3. **Hypothesis Table**:
   - 3–5 giả thuyết giải thích 1 hiện tượng liên quan node; mỗi giả thuyết có ủng hộ/phản bác/kiểm chứng/can thiệp.
4. **Causal Chain/Tree**:
   - Phân biệt symptom/direct cause/root cause/downstream effects; đề xuất điểm can thiệp leverage cao.
5. **(Tuỳ chọn nhưng nên làm) Comparative Table**:
   - So sánh 2–4 phương án/cách tiếp cận liên quan node theo tiêu chí rõ ràng.

### 11.2. Rubric gợi ý

| Tiêu chí                   | Mô tả                                                                                 | Điểm (0–5) |
|----------------------------|----------------------------------------------------------------------------------------|------------|
| CoT quality                | Mỗi bước có mục tiêu & cơ sở rõ? Không chỉ lập lại hiển nhiên?                        | /5         |
| ToT diversity              | Các nhánh ToT khác thật, không chỉ đổi câu chữ?                                      | /5         |
| Hypothesis rigor           | Giả thuyết có thể kiểm chứng? Có ủng hộ / phản bác / kiểm chứng / can thiệp không?  | /5         |
| Causal clarity             | Phân biệt được symptom / direct cause / root cause / effect?                          | /5         |
| Comparative usefulness     | Nếu làm bảng so sánh: tiêu chí có ý nghĩa? Kết luận có bám tiêu chí?                 | /5         |
| Connection to domain       | Reasoning Pack bám sát domain & Framing Brief của bạn, không trôi sang generic?       | /5         |

---

## 12. Sau Buổi 6 – Bạn đã “điều khiển suy luận” tốt hơn chưa?

Nếu bạn làm đầy đủ:

- Bạn không còn chỉ “xin AI liệt kê và giải thích”.
- Bạn biết:

  - lúc nào cần chuỗi CoT để **trace logic**,
  - lúc nào cần ToT để **mở nhánh giải pháp**,
  - lúc nào cần giả thuyết & nhân quả để **chẩn đoán gốc rễ**,
  - lúc nào cần bảng so sánh theo tiêu chí để **chọn phương án**.

Buổi 7 sẽ lấy chính Reasoning Pack này để:

- **dán nhãn epistemic** (fact/interpretation/assumption/hypothesis/recommendation),
- ép AI **tự phản biện** (self-critique),
- làm **gap/contradiction check**,
- và **triangulation** nếu cần.

---
