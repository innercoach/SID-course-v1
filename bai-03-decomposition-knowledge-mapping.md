# Buổi 3 — Decomposition & Knowledge Mapping  
> Bóc tách chủ đề thành bản đồ tri thức nhiều tầng

---

## 0. Bạn cần chuẩn bị gì trước Buổi 3?

Từ Buổi 1–2, bạn nên đã có:

1. **Framing Brief** cho 1 domain thật:
   - Topic, Problem, Audience, Scope, Output, Task type.
2. **Prompt Stack V1**:
   - Ít nhất 1 prompt để **bóc khung thành phần/năng lực**,
   - 1 prompt để **rút gọn/tinh luyện**,
   - (tuỳ chọn) 1 prompt **tự phản biện**.

Kết quả thường là:

- 1 bảng khung thành phần/năng lực / module / nhóm nội dung (sơ bộ).

Buổi 3 sẽ dùng chính bảng này để:

- bóc tách thành **cây 3–4 tầng**,
- nhìn domain từ **nhiều logic**: khái niệm, chức năng, stakeholder,
- tạo **Decomposition Tree + 1 map bổ sung**.

---

## 1. Mục tiêu Buổi 3

Sau buổi này, bạn sẽ:

1. Hiểu tại sao **decomposition** là nền của mọi bước tiếp theo:
   - Information Architecture (Buổi 4),
   - Reasoning (Buổi 6),
   - Synthesis (Buổi 8).
2. Bóc được 1 chủ đề lớn thành:
   - **cây 3–4 tầng**, không trùng cấp, không chồng ý quá nhiều.
3. Phân biệt 3 kiểu decomposition:
   - **Top-down** (từ tổng quan đến chi tiết),
   - **Functional** (theo chức năng/khâu trong hệ),
   - **Stakeholder-based** (theo vai trò liên quan).
4. Tạo được 2 artifact:
   - **Decomposition Tree** (3–4 tầng),
   - **Functional map hoặc Stakeholder map** cho chính domain của bạn.

---

## 2. Vì sao phải học Decomposition?

### 2.1. Không decomposition → không kiến trúc được

Nếu bạn chỉ hỏi AI “giải thích”, “liệt kê”, “tóm tắt”, bạn nhận về:

- danh sách ý tưởng,
- đoạn văn dài,
- nhưng:
  - không biết **bức tranh toàn bộ**,
  - không rõ **đâu là khối lớn, đâu là chi tiết**,
  - khó xây syllabus, handbook, framework.

Decomposition cho bạn:

- “bản đồ tri thức” của domain,
- chỗ đứng rõ cho từng khái niệm, quy trình, kỹ thuật, use case.

### 2.2. Một domain không có **1** decomposition duy nhất

Ví dụ: “AI literacy cho giảng viên” có thể bóc:

- Theo **khái niệm** (conceptual): hiểu AI, hiểu dữ liệu, kỹ năng đánh giá, đạo đức, sư phạm với AI,…
- Theo **chức năng** (functional): dùng AI để soạn bài, chấm bài, phản tư, cá nhân hoá học tập,…
- Theo **stakeholder**: nhìn từ giảng viên, sinh viên, khoa, ban giám hiệu,…

Không có “cách chia duy nhất đúng”;  
có cách **phù hợp nhất với bài toán & audience của bạn**.

---

## 3. Bản đồ khái niệm Buổi 3

### 3.1. Khái niệm chính

| Khái niệm                 | Vai trò                                                         |
|---------------------------|-----------------------------------------------------------------|
| Decomposition             | Bóc chủ đề lớn thành nhiều phần/cấp độ                         |
| Top-down Decomposition    | Chia từ tổng quan → miền chính → nhóm con → node cụ thể       |
| Functional Decomposition  | Chia theo chức năng / khâu trong hệ (input → process → output)|
| Conceptual Decomposition  | Chia theo khái niệm nền, khái niệm trung gian, ứng dụng       |
| Stakeholder Decomposition | Chia theo các bên liên quan (learner, teacher, manager…)     |
| MECE-ish Thinking         | Cố gắng “không trùng lớn, không thủng lớn”                     |
| Node                      | Một “khối” trong cây tri thức (nhánh, lá, cụm nội dung)       |

### 3.2. 3 mô hình bạn cần nắm

1. **Cây 3–4 tầng (Top-down)**

Ví dụ (rút gọn) cho “AI literacy cho giảng viên”:

- AI literacy cho giảng viên  
  - Hiểu công cụ AI  
    - Loại công cụ & giới hạn  
    - Khả năng & lỗi thường gặp  
  - Kỹ năng dùng AI trong thiết kế bài giảng  
    - Soạn đề cương  
    - Tạo câu hỏi & bài tập  
    - Tạo ví dụ, case study  
  - Kỹ năng đánh giá & phản biện output AI  
  - Kỹ năng đạo đức & an toàn dữ liệu  
  - Kỹ năng dạy sinh viên dùng AI đúng cách  

2. **Functional flow**

Ví dụ (functional decomposition) – “quy trình dùng AI cho thiết kế bài giảng”:

- Xác định mục tiêu học tập →  
- Bóc chủ đề →  
- Thiết kế cấu trúc bài →  
- Dùng AI gợi ý nội dung & hoạt động →  
- Dùng AI phản biện & kiểm định →  
- Chỉnh sửa & cá nhân hoá cho lớp học thật.

3. **Stakeholder lens**

Ví dụ (stakeholder decomposition):

- Giảng viên: năng lực A, B, C…
- Sinh viên: năng lực X, Y, Z…
- Khoa/Bộ môn: chính sách, tài nguyên…
- Ban giám hiệu: định hướng, KPI, rủi ro…

---

## 4. Kỹ thuật 1 — Top-down Decomposition

### 4.1. Cốt lõi

- Bắt đầu từ **một khối rất rộng** (chủ đề tổng),
- Chia thành 3–7 **miền chính**,
- Mỗi miền chính lại chia thành **nhóm con**,
- Mỗi nhóm con lại chia thành **node cụ thể** (kỹ thuật, khái niệm, use case, lỗi, v.v.).

### 4.2. Sai lầm phổ biến (rất giống người dùng 1–3 năm)

- Chia **theo cảm tính**: nhảy lung tung, không cùng tiêu chí.
- Node ở cùng cấp nhưng bản chất khác nhau:
  - “Khái niệm” nằm cạnh “quy trình” nằm cạnh “lỗi”.
- Node trùng ý:
  - “Đánh giá output AI” và “kiểm định AI” lặp lại nhau, nhưng vẫn tách riêng.

### 4.3. Cách làm có kỷ luật (self-study)

Giả sử bạn đang làm với domain trong Framing Brief.

**Bước 1 — Lấy artifact từ Buổi 2**

- Lấy bảng khung năng lực/thành phần bạn đã tạo bằng Prompt Stack V1.

Ví dụ (giản lược), bảng có các năng lực:

- “Đặt bài toán & framing câu hỏi với AI”  
- “Dùng AI thiết kế & chỉnh sửa tài liệu giảng dạy”  
- “Đánh giá & kiểm định output AI”  
- “Thiết kế hoạt động học tập có AI hỗ trợ”  
- “Đảm bảo đạo đức & an toàn khi dùng AI”  
- “Dạy sinh viên dùng AI có trách nhiệm”

**Bước 2 — Chọn tiêu chí chia cấp 1**

Hỏi:

- Cấp 1 của tôi nên là gì?
  - giai đoạn trong workflow,
  - nhóm kỹ năng,
  - nhóm phạm vi nội dung?

Ví dụ, quyết định: cấp 1 = **nhóm năng lực lớn**.

- Nền tảng & nhận thức
- Ứng dụng vào soạn dạy
- Đánh giá & phản biện
- Đạo đức & an toàn
- Dạy lại / mentoring sinh viên

**Bước 3 — Gắn năng lực vào nhóm cấp 1**

- “Đặt bài toán & framing câu hỏi với AI”  
  → Nhóm “Nền tảng & nhận thức”.
- “Dùng AI thiết kế & chỉnh sửa tài liệu giảng dạy”  
  → Nhóm “Ứng dụng vào soạn dạy”.
- “Đánh giá & kiểm định output AI”  
  → Nhóm “Đánh giá & phản biện”.
- “Thiết kế hoạt động học tập có AI hỗ trợ”  
  → Nhóm “Ứng dụng vào soạn dạy”.
- “Đảm bảo đạo đức & an toàn khi dùng AI”  
  → Nhóm “Đạo đức & an toàn”.
- “Dạy sinh viên dùng AI có trách nhiệm”  
  → Nhóm “Dạy lại / mentoring sinh viên”.

**Bước 4 — Bổ sung tầng dưới (3–4 tầng tổng)**

Ví dụ (text-tree):

```markdown
AI literacy cho giảng viên đại học
  1. Nền tảng & nhận thức
     1.1. Phân biệt AI generative / không generative
     1.2. Hiểu giới hạn & lỗi thường gặp của LLM
     1.3. Problem framing & đặt câu hỏi với AI
  2. Ứng dụng vào soạn dạy
     2.1. Thiết kế outline bài giảng với AI
     2.2. Tạo câu hỏi & bài tập với AI
     2.3. Sử dụng AI để gợi ý ví dụ, case study
  3. Đánh giá & phản biện
     3.1. Kiểm tra fact vs hallucination
     3.2. Đánh giá sự phù hợp với mục tiêu học tập
     3.3. Dùng AI để tự phản biện output AI
  4. Đạo đức & an toàn
     4.1. Quyền riêng tư & dữ liệu sinh viên
     4.2. Minimize bias trong nội dung AI sinh ra
     4.3. Quy tắc sử dụng AI trong đánh giá sinh viên
  5. Dạy lại / mentoring sinh viên
     5.1. Dạy sinh viên đặt câu hỏi
     5.2. Dạy sinh viên kiểm định output AI
     5.3. Chính sách lớp học về dùng AI
```

### 4.4. Check nhanh chất lượng cây

Tự hỏi:

1. Cấp 1 có đang “đồng đẳng” không? (đều là nhóm năng lực / nhóm miền lớn?)
2. Cấp 2 có lẫn “khái niệm” với “hoạt động” với “công cụ” không? (nếu có, xem lại tiêu chí).
3. Có node nào trùng ý ở cấp 2–3 không?
4. Nhìn vào cây, **tôi có thể dạy 4–5 buổi logic theo thứ tự được không?**

---

## 5. Kỹ thuật 2 — Functional Decomposition

### 5.1. Cốt lõi

Functional decomposition trả lời:

> “Hệ thống/quy trình này phải làm những **chức năng** gì, theo dòng thời gian hoặc pipeline?”

Ví dụ: quy trình **“dùng AI để thiết kế 1 module dạy học”**:

- Nhận yêu cầu / mục tiêu học tập;
- Phân tích đối tượng học;
- Bóc tách chủ đề;
- Thiết kế outline;
- Dùng AI generate nội dung gợi ý;
- Dùng AI tự phản biện & refine;
- Dùng con người chỉnh sửa cuối & chuẩn bị tài liệu.

### 5.2. Vì sao functional view quan trọng?

- Nó giúp bạn:
  - hiểu **workflow thực tế**,
  - gắn decomposition với **thao tác cụ thể**,
  - chuẩn bị tốt cho:
    - design workflow,
    - design assistant/agent (sau này).

### 5.3. Cách làm tự học

Tiếp tục với domain của bạn.

**Bước 1 — Xác định “quy trình” trung tâm**

Ví dụ: “Quy trình sử dụng AI trong thiết kế bài giảng”.

**Bước 2 — Hỏi: từ input đến output, cần chức năng nào?**

Đặt câu hỏi:

- Đầu vào là gì? (vd: đề cương môn học, chuẩn đầu ra)
- Đầu ra là gì? (vd: slide, handout, bài tập, rubric)
- Giữa chừng có những khâu gì?

Viết ra dạng bullet:

```markdown
Quy trình "dùng AI thiết kế bài giảng":
  1. Làm rõ mục tiêu học tập & audience của môn
  2. Bóc tách chủ đề môn thành các chủ đề con
  3. Thiết kế cấu trúc buổi học (outline)
  4. Dùng AI gợi ý nội dung, ví dụ, bài tập
  5. Dùng AI phản biện & kiểm định nội dung
  6. Con người chỉnh sửa cuối & lên tài liệu dạy
```

**Bước 3 — Bổ sung sub-function nếu cần**

Ví dụ, bước 4 có thể bóc:

- 4.1. Prompt AI xây khung nội dung
- 4.2. Prompt AI bổ sung ví dụ phù hợp ngành
- 4.3. Prompt AI gợi ý hoạt động nhóm

Bạn vừa tạo:

- 1 functional decomposition,
- rất hữu ích khi thiết kế:
  - workflow dạy học,
  - AI助手/tutor cho giảng viên.

---

## 6. Kỹ thuật 3 — Stakeholder Decomposition

### 6.1. Cốt lõi

Trả lời:

> “Chủ đề này trông thế nào từ góc nhìn **mỗi bên liên quan**?”

Ví dụ, với “AI literacy trong trường đại học”, stakeholder có thể là:

- Giảng viên,
- Sinh viên,
- Khoa / Bộ môn,
- Ban giám hiệu,
- Phòng công nghệ thông tin,
- Phòng đảm bảo chất lượng.

Mỗi bên:

- quan tâm điều gì,
- sợ điều gì,
- cần năng lực/tri thức gì.

### 6.2. Cách làm

**Bước 1 — Liệt kê stakeholder chính**

Dựa trên Framing Brief + hiểu biết thực tế.

**Bước 2 — Với mỗi stakeholder, trả lời 4 câu hỏi:**

1. Họ **kỳ vọng gì** từ chủ đề này?
2. Họ **sợ điều gì** nếu chủ đề này bị làm sai?
3. Họ cần **năng lực/tri thức** nào?
4. Họ sẽ dùng AI **vào việc gì**?

Ví dụ (giản lược):

```markdown
Giảng viên:
  - Kỳ vọng: dạy tốt hơn, bớt tốn thời gian soạn bài.
  - Sợ: bị thay thế, đánh giá sai vì AI sai, sinh viên lạm dụng.
  - Cần: framing, thiết kế bài giảng, kiểm định output, đạo đức.
  - Dùng AI: soạn bài, chấm bài, phản tư.

Sinh viên:
  - Kỳ vọng: học nhanh hơn, có trợ lý học tập.
  - Sợ: phụ thuộc, mất kỹ năng tư duy độc lập.
  - Cần: kỹ năng hỏi AI, kiểm định, dùng AI cho assignment đúng quy định.
  - Dùng AI: làm bài tập, ôn thi, tra cứu.

Ban giám hiệu:
  - Kỳ vọng: nâng chất lượng dạy & học, không scandal.
  - Sợ: vi phạm đạo đức, lộ dữ liệu, chất lượng sa sút.
  - Cần: policy, training, đánh giá mức sử dụng AI.
  - Dùng AI: ra chiến lược, đọc báo cáo, phân tích số liệu.
```

Stakeholder map này:

- không phải “cây tri thức”,
- nhưng giúp bạn:
  - thiết kế module khác nhau,
  - chọn content/priority theo vai trò,
  - gắn decomposition với **con người thật**.

---

## 7. Bài tập tự học Buổi 3

### 7.1. Bài tập 1 — Decomposition Tree 3–4 tầng

**Mục tiêu**  
Bóc domain của bạn thành cây nhiều tầng dễ dạy, dễ dùng.

**Bước 1**: Lấy bảng khung năng lực/thành phần từ Buổi 2.

**Bước 2**: Chọn **tiêu chí cho cấp 1** (vd: nhóm năng lực, giai đoạn workflow, miền nội dung).

**Bước 3**: Vẽ cây 3–4 tầng dạng markdown:

```markdown
[Chủ đề tổng]
  1. [Miền chính 1]
     1.1. [...]
     1.2. [...]
     ...
  2. [Miền chính 2]
     ...
  ...
```

**Yêu cầu tối thiểu**:

- Ít nhất **3** miền chính (cấp 1),
- Tổng số node tối thiểu **20**,
- Không lẫn lộn “khái niệm” với “quy trình” với “lỗi” trên cùng 1 cấp (trừ khi bạn có lý do rõ).

---

### 7.2. Bài tập 2 — Functional Map hoặc Stakeholder Map

Chọn **1 trong 2** (hoặc làm cả 2 nếu có thời gian):

#### A. Functional map

1. Chọn 1 workflow thực (vd: “dùng AI để…”, “khai thác AI cho…”).
2. Liệt kê các bước/chức năng từ input → output.
3. Nếu được, bóc 1–2 bước thành sub-function.

Dạng:

```markdown
Workflow: [tên]

1. [Chức năng 1]
2. [Chức năng 2]
   2.1. [Sub-function]
   2.2. ...
3. ...
```

#### B. Stakeholder map

1. Liệt kê 3–5 stakeholder chính trong domain.
2. Với mỗi stakeholder, trả lời 4 câu hỏi (kỳ vọng, sợ hãi, cần gì, dùng AI cho việc gì).

Dạng:

```markdown
Stakeholder 1 — [Tên]:
- Kỳ vọng:
- Sợ:
- Cần:
- Dùng AI để:

Stakeholder 2 — ...
```

---

## 8. Assignment Buổi 3 — Decomposition & Mapping cho domain của bạn

### 8.1. Đề bài

Viết 1 tài liệu ngắn (markdown) gồm:

1. **Decomposition Tree** (3–4 tầng, ≥20 node).
2. **Functional map hoặc Stakeholder map** (chọn 1).
3. 1 đoạn ngắn (150–250 từ) giải thích:
   - Vì sao bạn chọn tiêu chí như vậy cho cấp 1,
   - Bạn sẽ dùng cây này để:
     - thiết kế syllabus,
     - thiết kế assistant/GPT/Gem,
     - hay thiết kế khóa học… như thế nào.

### 8.2. Gợi ý rubric tự chấm

| Tiêu chí                 | Mô tả                                                                                  | Điểm (0–5) |
|--------------------------|-----------------------------------------------------------------------------------------|------------|
| Logic cấp 1              | Các miền chính có cùng loại (VD: đều là nhóm năng lực, không trộn chức năng/lỗi)?    | /5         |
| Độ đầy đủ (breadth)      | Cây có bao quát các phần quan trọng của domain?                                      | /5         |
| Độ rõ cấp 2–3            | Node cùng cấp có đồng đẳng? Ít trùng lặp?                                             | /5         |
| Functional/Stakeholder map| Map có phản ánh thực tế? Giúp hiểu system/people hơn không?                           | /5         |
| Tính dạy được            | Nhìn vào cây/map, bạn thấy dễ dạy, dễ giải thích hơn trước chưa?                      | /5         |
| Clarity tổng thể         | Tài liệu rõ ràng, đọc mạch lạc, dễ follow?                                            | /5         |

---

## 9. Sau Buổi 3 – Bạn đang có gì?

Nếu bạn hoàn thành:

1. Framing Brief (Buổi 1),
2. Prompt Stack V1 (Buổi 2),
3. Decomposition Tree + Functional/Stakeholder map (Buổi 3),

thì bạn đã:

- Thoát khỏi việc “thấy domain như một cục mù mờ”.
- Có **bản đồ tri thức** đầu tiên:
  - phía **nội dung** (cây),
  - phía **vận hành** hoặc **con người** (functional / stakeholder).

Buổi 4 sẽ dùng chính cây & map này để:

- chuyển thành **Information Architecture**:
  - taxonomy,
  - hierarchy “sạch”,
  - bảng & matrix so sánh.

---
