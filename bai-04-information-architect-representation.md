# Buổi 4 — Information Architecture & Representation  
> Biến bản đồ tri thức thành cấu trúc dễ dạy, dễ so sánh, dễ dùng

---

## 0. Bạn đã có gì trước Buổi 4?

Từ Buổi 1–3, bạn (lý tưởng) đã có:

1. **Framing Brief** cho 1 domain thật.  
2. **Prompt Stack V1** cho domain đó.  
3. **Decomposition Tree** 3–4 tầng (≥20 node).  
4. **Functional map hoặc Stakeholder map**.

Buổi 4 sẽ dùng các artifact trên để:

- chọn **dạng biểu diễn** (representation) phù hợp,
- dựng **taxonomy**, **hierarchy**, và **bảng/matrix**,
- làm ra 1 **IA Pack** có thể dùng cho:
  - dạy học,  
  - thiết kế assistant/GPT,  
  - trình bày với stakeholder.

---

## 1. Mục tiêu Buổi 4

Sau buổi này, bạn có thể:

1. Phân biệt rõ:
   - **Taxonomy** vs **Hierarchy** vs **Ontology thinking** vs **Table** vs **Matrix**.
2. Biết **khi nào dùng dạng nào**, theo mục tiêu:
   - học nhanh,
   - so sánh,
   - ra quyết định,
   - thiết kế khóa học.
3. Chuyển Decomposition Tree thành:
   - **Taxonomy** (phân loại theo tiêu chí),
   - **Hierarchy** (outline dạy học),
   - 1 **bảng** hoặc **matrix so sánh** có ý nghĩa.
4. Tạo được **IA Pack** cho domain của bạn:
   - 1 taxonomy,
   - 1 hierarchy,
   - 1 table/matrix.

---

## 2. Vấn đề: cùng 1 nội dung, nhiều cách biểu diễn – không phải cách nào cũng tốt

### 2.1. Biểu diễn không phải chuyện… trang trí

Cùng 1 tập tri thức, bạn có thể:

- viết thành đoạn văn dài,
- bullet list,
- cây phân cấp,
- bảng so sánh,
- matrix 2 chiều,
- sơ đồ flow,
- concept map.

**Nhưng**:

- dạng trình bày **ảnh hưởng trực tiếp** đến:
  - tốc độ hiểu,
  - khả năng nhớ,
  - khả năng so sánh,
  - khả năng dạy lại.

### 2.2. Vấn đề hay gặp (giống user AI 1–3 năm)

- Dùng **bullet list** cho mọi thứ:
  - dù cần so sánh,
  - dù cần phân loại.
- Dùng **bảng** nhưng:
  - cột đặt tùy hứng,
  - không rõ tiêu chí,
  - người đọc không thấy “ra quyết định gì” từ đó.
- Nhầm lẫn:
  - Taxonomy = Hierarchy,
  - mọi cây phân cấp đều là “outline”.

---

## 3. Bảng khái niệm Buổi 4

| Khái niệm         | Mô tả ngắn                                                                                 |
|-------------------|--------------------------------------------------------------------------------------------|
| Taxonomy          | Hệ **phân loại** theo 1 tiêu chí rõ (VD: loại kỹ thuật, loại năng lực, loại use case…)   |
| Hierarchy         | Cấu trúc **cha–con** (outline dạy học, index sách, mục lục documentation)                |
| Ontology thinking | Cách nghĩ về **thực thể–thuộc tính–quan hệ–phụ thuộc** (không cần vẽ RDF để có giá trị)  |
| Table schema      | Thiết kế cấu trúc bảng (cột) trước khi yêu cầu AI điền nội dung                          |
| Matrix            | Bảng 2 chiều có ý nghĩa trên cả 2 trục (VD: kỹ thuật × mục tiêu, facet × độ sâu)         |
| Representation fit| Dùng đúng dạng biểu diễn với mục tiêu nhận thức                                           |

---

## 4. Khi nào dùng cái gì? (quick guide)

| Mục tiêu chính                            | Dạng phù hợp nhất                 |
|-------------------------------------------|-----------------------------------|
| Muốn phân loại các loại / nhóm            | Taxonomy                          |
| Muốn thiết kế outline / syllabus / mục lục| Hierarchy                         |
| Muốn thấy quan hệ “là gì – bao gì – phụ thuộc gì” | Ontology thinking         |
| Muốn so sánh nhiều đối tượng theo tiêu chí| Table (schema tốt)                |
| Muốn nhìn giao cắt 2 chiều                | Matrix                            |
| Muốn mô tả quy trình/flow                 | Flowchart / process diagram       |

---

## 5. Kỹ thuật 1 — Từ Decomposition Tree → Taxonomy

### 5.1. Cốt lõi

**Taxonomy** = phân loại thành **nhóm**, theo 1 tiêu chí nhất định.

Ví dụ, với domain “kỹ thuật khai thác tri thức với AI”, bạn có thể có taxonomy theo:

- Mục tiêu (`framing, decomposition, IA, reasoning, expansion, validation, synthesis, transfer`).
- Hoặc theo mức độ (basic / intermediate / advanced / expert).

Trong Buổi 4, ta tập trung vào **taxonomy theo mục tiêu / chức năng** vì nó dễ dùng nhất.

### 5.2. Cách làm step-by-step

Giả sử bạn đã có Decomposition Tree từ Buổi 3.  
Ta sẽ trích ra 1 taxonomy từ đó.

**Bước 1 — Chọn tiêu chí phân loại**

Hỏi: “Tôi muốn phân loại **cái gì theo cái gì**?”

Ví dụ:

- “Các năng lực AI literacy của giảng viên” **theo**:
  - nhóm mục tiêu (nhận thức / ứng dụng / đánh giá / dạy lại),
  - hoặc theo giai đoạn dạy học (trước giờ, trong giờ, sau giờ).

Giả sử bạn chọn:

- Tiêu chí: **giai đoạn dạy học** (before class / in-class / after class).

**Bước 2 — Liệt kê thành phần cần phân loại**

Lấy tất cả node “năng lực” từ Decomposition Tree:

- Problem framing với AI,
- Thiết kế outline bài giảng với AI,
- Tạo câu hỏi/bài tập,
- Đánh giá output AI,
- Đảm bảo đạo đức & an toàn,
- Dạy sinh viên dùng AI có trách nhiệm,
- …

**Bước 3 — Gán vào nhóm**

Ví dụ:

- **Before class**:
  - Problem framing với AI,
  - Thiết kế outline bài giảng với AI,
  - Tạo tài liệu/học liệu với AI.
- **In-class**:
  - Thiết kế hoạt động sử dụng AI trong lớp,
  - Hướng dẫn sinh viên đặt câu hỏi với AI,
  - Điều phối thảo luận quanh output AI.
- **After class**:
  - Dùng AI phản tư, phân tích log hoạt động lớp,
  - Dùng AI gợi ý cải tiến bài giảng,
  - Cập nhật tài liệu dựa trên phản hồi.

**Bước 4 — Viết bảng taxonomy**

Dạng:

```markdown
### Taxonomy — Năng lực AI literacy theo giai đoạn dạy học

| Giai đoạn      | Năng lực chính                              | Ghi chú ngắn                          |
|----------------|---------------------------------------------|---------------------------------------|
| Before class   | Problem framing với AI                      | Xác định đúng nhiệm vụ bài học       |
|                | Thiết kế outline bài giảng với AI           | Dùng AI gợi ý cấu trúc hợp lý        |
|                | Tạo tài liệu/học liệu với AI                | Slide, handout, ví dụ, case study    |
| In-class       | Thiết kế hoạt động sử dụng AI trong lớp     | Ví dụ: thảo luận nhóm với AI         |
|                | Hướng dẫn sinh viên đặt câu hỏi với AI      | Tư duy prompt & framing cho sinh viên|
|                | Điều phối thảo luận quanh output AI         | Giải thích, phản biện, so sánh       |
| After class    | Dùng AI phản tư & phân tích phản hồi        | Rút kinh nghiệm, pattern học tập     |
|                | Dùng AI gợi ý cải tiến bài giảng            | Iterate giáo án                       |
|                | Cập nhật tài liệu với AI                    | Sửa bài, tạo phiên bản mới           |
```

### 5.3. Check nhanh

- Một taxonomy tốt:
  - mỗi hàng/nhóm tuân theo **1 tiêu chí** rõ,
  - không trộn **nhóm** với **cá nhân** (vd: “giảng viên” + “before class” trên cùng 1 chiều),
  - giúp bạn dạy hoặc quyết định **một điều gì đó** (vd: dạy theo giai đoạn).

---

## 6. Kỹ thuật 2 — Hierarchy để dạy & thiết kế tài liệu

### 6.1. Cốt lõi

**Hierarchy** = outline nhiều tầng:

- từ “mục I, II, III”
- đến “I.1, I.2,…”
- đến “I.1.1, I.1.2,…”

Đây là cách:

- tổ chức 1 cuốn sách,
- 1 handbook,
- 1 syllabus,
- 1 module đào tạo.

### 6.2. Từ Decomposition Tree → Hierarchy dạy học

Khác biệt:

- Decomposition tree có thể chứa **nhiều loại node** (khái niệm, kỹ năng, quy trình, lỗi,…).
- Hierarchy dạy học nên được sắp thành **một thứ tự hợp lý để học**.

**Bước 1 — Xác định “tuyến nội dung” chính**

Dựa trên cây + Framing Brief, bạn chọn 4–6 mục lớn để dạy.

Ví dụ (cho khóa 4 buổi):

```markdown
I. Gốc rễ: AI & AI literacy trong bối cảnh trường đại học
II. Dùng AI cho soạn dạy & thiết kế bài giảng
III. Đánh giá & phản biện output AI
IV. Đạo đức, an toàn & chính sách dùng AI
V. Dạy sinh viên dùng AI có trách nhiệm
```

**Bước 2 — Gắn node decomposition vào mục lớn**

Ví dụ:

```markdown
II. Dùng AI cho soạn dạy & thiết kế bài giảng
   II.1. Bóc tách chủ đề & mục tiêu học tập với AI
   II.2. Thiết kế outline bài giảng (lesson plan) với AI
   II.3. Tạo câu hỏi, bài tập, ví dụ, case study
   II.4. Dùng AI tạo variation cho lớp có năng lực khác nhau
```

**Bước 3 — Chia sâu khi cần (tới 3–4 tầng)**

Nhưng nhớ:

- Hierarchy = **outline dạy học**, không nhất thiết phải phản chiếu toàn bộ decomposition tree.
- Nó ưu tiên:
  - mạch logic (học cái gì trước, sau),
  - cognitive load (mỗi mục-lớn ~1 buổi).

### 6.3. Check nhanh

Tự hỏi:

1. Nếu tôi phải dạy khóa 4 buổi, mạch này có **đủ tự nhiên**, không nhảy lung tung?
2. Mỗi mục lớn có thể trở thành **1 buổi** hoặc **1 chương** không?
3. Có mục nào nên đổi thứ tự để:
   - “khái niệm trước – ứng dụng sau”,
   - “AI literacy trước – policy sau”…?

---

## 7. Kỹ thuật 3 — Table & Matrix (so sánh có ý nghĩa)

### 7.1. Bảng so sánh — tránh bảng “cho có”

Bảng hữu ích khi:

- bạn muốn **so sánh** 3–5 thứ theo cùng tiêu chí:
  - kỹ thuật,
  - phương pháp,
  - level,
  - stakeholder,
  - v.v.

Sai lầm thường gặp:

- tự nghĩ cột 1 cách tùy tiện,
- mỗi hàng một kiểu, mỗi cột một kiểu,
- nhìn xong **không ra quyết định gì**.

### 7.2. Thiết kế schema bảng trước

Giả sử bạn muốn so sánh **các năng lực AI literacy** theo:

- mục tiêu,
- ngữ cảnh dùng,
- rủi ro nếu thiếu.

Schema đề xuất:

```markdown
| Năng lực                 | Mục tiêu chính                    | Context dùng mạnh nhất           | Rủi ro nếu thiếu            |
|--------------------------|-----------------------------------|----------------------------------|-----------------------------|
| Problem framing với AI   | Đặt bài toán đúng                 | Soạn dạy, nghiên cứu, tư vấn    | Dùng AI cho sai việc       |
| Đánh giá output AI       | Tách đúng/sai/hợp-ngữ cảnh       | Chấm bài, đọc báo cáo, thiết kế | "Nghe hay là dùng bừa"     |
| ...                      | ...                               | ...                              | ...                         |
```

Bạn có thể nhờ AI giúp nghĩ schema:

```text
Tôi muốn thiết kế một bảng so sánh các năng lực AI literacy của giảng viên theo mục tiêu, context sử dụng và rủi ro nếu thiếu.

Hãy đề xuất 2–3 phương án schema bảng (tức là bộ cột), giải thích ưu/nhược từng phương án.
Sau đó chọn một schema tối ưu nếu mục tiêu của tôi là: 
"giúp hiệu trưởng/khoa/bộ môn quyết định xem nên ưu tiên đào tạo năng lực nào trước".
```

### 7.3. Matrix — khi cần **2 chiều**

Ví dụ: bạn muốn xem:

- hàng: nhóm năng lực chính (Nền tảng, Ứng dụng, Đánh giá, Đạo đức, Dạy lại)
- cột: giai đoạn (Before class / In-class / After class)

Matrix:

```markdown
| Nhóm năng lực \ Giai đoạn | Before class                 | In-class                         | After class                    |
|---------------------------|------------------------------|----------------------------------|--------------------------------|
| Nền tảng & nhận thức      | Hiểu LLM, giới hạn, bias     | Nhắc lại khái niệm cho sinh viên| Phản tư: LLM giúp/giảm giá trị|
| Ứng dụng soạn dạy         | Thiết kế outline với AI      | Điều chỉnh ví dụ theo phản ứng  | Cập nhật tài liệu             |
| Đánh giá & phản biện      | Chuẩn bị rubic & tiêu chí    | Chữa bài cùng AI                | Phân tích kết quả với AI      |
| Đạo đức & an toàn         | Chọn công cụ, policy         | Nhắc nhở guideline               | Review vi phạm/edge case      |
| Dạy lại / mentoring       | Thiết kế activity về AI      | Hướng dẫn prompt & kiểm định    | Coaching 1–1 với AI hỗ trợ    |
```

Matrix này:

- giúp nhìn **đa chiều**,
- hữu ích khi:
  - ưu tiên thiết kế training,
  - thiết kế assistant hỗ trợ từng giai đoạn.

---

## 8. Ontology thinking (nhẹ) – để hiểu “quan hệ & phụ thuộc”

Không cần vẽ graph phức tạp, nhưng bạn nên:

- liệt kê **thực thể** chính trong domain,
- cho mỗi thực thể:
  - thuộc tính chính,
  - quan hệ với thực thể khác (is-a, part-of, depends-on, influences…).

Ví dụ đơn giản:

```markdown
Thực thể: Năng lực "Đánh giá output AI"
- Thuộc tính:
  - yêu cầu AI literacy nền,
  - yêu cầu kỹ năng fact-check,
  - gắn với rủi ro sử dụng sai thông tin.
- Quan hệ:
  - depends-on: "Problem framing đúng" (nếu frame sai, đánh giá sai bối cảnh),
  - influences: "Chất lượng dạy & đánh giá sinh viên",
  - part-of: nhóm năng lực "Đánh giá & phản biện".
```

Điều này giúp:

- bạn thấy **phụ thuộc**:
  - học cái gì trước để hỗ trợ cái gì,
  - nếu build assistant, cần chain bước nào trước.

---

## 9. Bài tập Buổi 4

### 9.1. Bài tập 1 — Taxonomy cho domain của bạn

**Mục tiêu**  
Phân loại 1 tập thành phần/năng lực trong Decomposition Tree theo 1 tiêu chí rõ.

**Bước 1**: Chọn tiêu chí phân loại:

- theo giai đoạn,
- theo mục tiêu,
- theo loại năng lực (nhận thức / kỹ thuật / đạo đức / dạy lại),
- v.v.

**Bước 2**: Lấy các node cấp 2–3 quan trọng trong cây, gán vào nhóm.

**Bước 3**: Viết lại dạng bảng taxonomy:

```markdown
### Taxonomy — [Tên]

| Nhóm chính       | Thành phần thuộc nhóm                      | Ghi chú ngắn               |
|------------------|---------------------------------------------|----------------------------|
| [Nhóm A]         | item 1, item 2, item 3                     |                            |
| [Nhóm B]         | ...                                         |                            |
| ...              |                                             |                            |
```

---

### 9.2. Bài tập 2 — Hierarchy dạy học (outline nhiều tầng)

**Mục tiêu**  
Từ cây decomposition → tạo 1 **outline dạy/học** 3–4 tầng.

**Bước 1**: Quyết định số “chương/mục lớn” (vd 4–6).

**Bước 2**: Gắn node vào cấu trúc I, II, III,… như 1 syllabus:

```markdown
I. [Mục lớn 1]
   I.1. [...]
   I.2. [...]
   I.3. [...]
II. [Mục lớn 2]
   ...
```

**Bước 3**: Đảm bảo:

- có thể map **1 mục lớn = 1 buổi / 1 module**,
- thứ tự học hợp lý.

---

### 9.3. Bài tập 3 — Bảng hoặc Matrix

Chọn **một**:

1. **Comparison table**:
   - So sánh 3–7 năng lực / kỹ thuật / module theo 3–4 tiêu chí hữu ích (mục tiêu, context, rủi ro…).

2. **Matrix**:
   - 2 chiều có ý nghĩa (VD: nhóm năng lực × giai đoạn; kỹ thuật × loại bài toán; v.v.).

---

## 10. Assignment Buổi 4 — IA Pack cho domain của bạn

### 10.1. Đề bài

Tạo 1 **IA Pack** dạng markdown, gồm:

1. **Taxonomy** (theo tiêu chí bạn chọn).
2. **Hierarchy dạy học** (outline 3–4 tầng).
3. **1 comparison table hoặc matrix**.
4. 1 đoạn ngắn (150–250 từ) trả lời:
   - Bạn sẽ dùng IA Pack này vào việc gì? (dạy, viết sách, thiết kế assistant, xây khóa nội bộ…)
   - Vì sao bạn chọn dạng biểu diễn như vậy (thay vì dạng khác)?

### 10.2. Gợi ý rubric tự chấm

| Tiêu chí             | Mô tả                                                                                 | Điểm (0–5) |
|----------------------|----------------------------------------------------------------------------------------|------------|
| Taxonomy clarity     | Tiêu chí phân loại rõ? Nhóm logic? Không trộn nhiều tiêu chí trong 1 taxonomy?       | /5         |
| Hierarchy coherence  | Outline có mạch? Các mục lớn đồng đẳng? Dạy/học theo thứ tự này có hợp lý?           | /5         |
| Table/Matrix usefulness | Bảng/matrix giúp nhìn ra quyết định/góc nhìn gì? Có cột/hàng vô nghĩa không?     | /5         |
| Connection to real use| IA Pack gắn với cách bạn thực sự sẽ dùng (dạy, build assistant, handbook…)?         | /5         |
| Alignment với Frame  | IA Pack vẫn tôn trọng Framing Brief & scope đã định?                                 | /5         |
| Clarity & readability| Đọc dễ, rõ, không rối; từng phần có heading, giải thích ngắn gọn?                     | /5         |

---

## 11. Sau Buổi 4 – Bạn đã có gì?

Nếu bạn hoàn thành Buổi 4:

- Bạn không chỉ có “cây tri thức” (Buổi 3),
- Mà còn có:

  - **Taxonomy**: phân loại các phần với 1 tiêu chí phù hợp,
  - **Hierarchy dạy học**: sườn 1 handbook/khóa học,
  - **Bảng/matrix**: công cụ so sánh, ra quyết định.

Tức là domain của bạn:

- đã có **bản đồ** (Buổi 3),
- và **có cách trình bày có chủ đích** (Buổi 4).

Buổi 5 sẽ mở rộng **chiều rộng & chiều sâu nghiên cứu**:

- quét rộng (breadth-first),
- mở rộng từ khóa,
- faceted exploration,
- chọn node đào sâu,
- thiết kế research path.

---
