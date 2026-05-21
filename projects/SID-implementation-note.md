# Implementation Note — Từ SID Spec → Prompts & Assistant Thực Tế

Mục tiêu của note này:

- Giải cho học viên (và bạn) câu hỏi:
  > “Mình có cả đống markdown (Framing, IA, Framework, Project Spec) rồi,  
  >  thì **dùng chúng với GPT/Gemini như thế nào cho thực tế?**”
- Và đặt chuẩn:  
  **mỗi project phải sinh ra được bộ prompts có thể dùng để test assistant.**

---

## 1. Hai lớp: Spec vs Prompt

SID tạo ra rất nhiều tài liệu:

- Framing Brief,
- IA Pack,
- Reasoning Pack,
- Validation Report,
- Framework + Workflow,
- Project Specs (Gem, Custom GPT, Book, Tutor…).

Bạn cần tách rõ:

1. **Spec** = tài liệu **thiết kế & kiến trúc**:
   - giải thích assistant/sách/system nên hoạt động thế nào,
   - không phải toàn bộ sẽ được copy nguyên vào 1 prompt.

2. **Prompt** = những đoạn **ngắn hơn, thực dụng**:
   - System Prompt / Master Instruction,
   - Prompt phụ cho từng phase (Frame, Structure, Reason, Validate, Synthesize),
   - Prompt test (scenario test).

SID giúp bạn viết **spec tốt**, để từ đó viết **prompt tốt**.

---

## 2. 3 tầng “prompt” trong thực tế

### 2.1. Tầng 1 — Master Instruction / System Prompt

Dùng khi:

- tạo **Gem** (Gemini),
- tạo **Custom GPT**,
- hoặc sử dụng API (system_message).

Nội dung của Master Instruction:

- Rút gọn & chắt lọc từ spec:
  - Mission & Audience,
  - Scope vs Out-of-scope,
  - Core behaviors (theo framework),
  - Epistemic & safety rules,
  - Default output formats.

Độ dài thường: **300–1500 từ**, không phải cả spec 10 trang.

Ví dụ (FruitTree Mentor, rút gọn):

```text
You are FruitTree Mentor, an AI assistant that supports small farmers and home gardeners in growing and caring for fruit trees (e.g., citrus, mango, durian, guava...).

Your users:
- Are not agronomy engineers.
- Have real-world constraints (time, money, local climate).
- Ask practical questions about diagnosis, care plans, and seasonal workflows.

Rules:
- Always ask for context before giving advice: region, climate, soil type, tree age, planting density, recent watering/fertilization, visible symptoms.
- Never prescribe specific commercial pesticides/fertilizers or exact dosages. Instead, explain general principles and recommend consulting local agronomy experts.
- When uncertain, explicitly state your confidence level and suggest ways to verify (local experts, extension officers, label instructions, etc.).
- Focus on fruit trees; if asked about unrelated topics, explain your scope and redirect politely.

Output:
- Structure your answers. Use:
  - summaries of the situation,
  - tables (symptom / possible cause / how to check),
  - step-by-step care plans (short-term vs long-term).
- Separate:
  - observed facts from the user,
  - your hypotheses,
  - recommendations.
```

### 2.2. Tầng 2 — Prompt Stack (Phase prompts)

Dùng khi:

- bạn **chat tay** với model, hoặc
- bạn muốn test từng giai đoạn trong pipeline assistant.

Prompt Stack là chuỗi prompts ngắn, mỗi cái:

- gọi đúng **phase** của framework:
  - Frame → Structure → Reason → Validate → Synthesize → Transfer.

Ví dụ (FruitTree Mentor):

- Prompt Phase 1 – Framing:

  ```text
  Tôi sẽ đưa cho bạn một tình huống về cây ăn quả. Hãy chỉ làm PHASE 1 – FRAMING:

  - hỏi lại người dùng về: giống, tuổi cây, vùng trồng, đất, nước, bón phân, triệu chứng chính.
  - tạo 1 Framing Summary 3–5 câu để xác nhận lại.

  Tình huống: [MÔ TẢ NGẮN]
  ```

- Prompt Phase 3 – Reasoning:

  ```text
  Dựa trên Framing Summary và danh sách triệu chứng sau, hãy thực hiện PHASE 3 – REASONING theo framework TREE-Care:

  - liệt kê 2–5 nguyên nhân khả dĩ,
  - với mỗi nguyên nhân, mô tả:
    - tại sao có thể đúng (liên hệ triệu chứng),
    - dấu hiệu cần kiểm tra thêm,
    - mức độ tin cậy (cao/trung bình/thấp).

  [DÁN FRAMING SUMMARY & TRIỆU CHỨNG]
  ```

Học viên cần:

- thiết kế Prompt Stack này trong **file project**,
- rồi test trong chat để thấy assistant hoạt động đúng logic hay không.

### 2.3. Tầng 3 — Test Prompts (scenario prompts)

Mỗi project nên có bộ:

- 5–10 **test scenario**, mỗi scenario gồm:
  - User prompt (gần với user thực),
  - Mong đợi behavior (ở mức mô tả: “assistant phải hỏi lại X, không được làm Y…”).

Ví dụ (Project Gem cây ăn quả):

```text
Scenario 1:
"Cam nhà tôi năm nay ít quả, lá hơi vàng, phải làm sao?"

Kỳ vọng:
- assistant hỏi lại về: tuổi cây, vùng trồng, đất, nước, lịch bón phân, triệu chứng chi tiết hơn.
- không nhảy ngay vào "bón phân NPK..."
- trả lời cuối có cấu trúc (nguyên nhân khả dĩ + cách kiểm tra + plan).
```

Các test prompt này:

- dùng để:
  - **debug** Master Instruction,
  - **đánh giá** chất lượng assistant,
- là output bắt buộc của mỗi project (xem phần 4).

---

## 3. Liên hệ với các buổi trong SID

Để dễ nhớ, bạn có thể map:

- **Buổi 1–2 (Framing & Prompt Stack)** → Master Instruction + Phase prompts.  
- **Buổi 3–4 (Decomposition & IA)** → định dạng Output (bảng, outline, matrix…).  
- **Buổi 5–6 (Expansion & Reasoning)** → logic reasoning bên trong (Phase Reason).  
- **Buổi 7 (Validation)** → rules về epistemic, self-critique, guardrails.  
- **Buổi 8 (Synthesis & Transfer)** → frameworks & workflows → hành vi assistant tổng thể.

SID Core = **bản vẽ**;  
Prompt & Assistant Implementation = **thi công**.

---

## 4. Chuẩn bắt buộc cho mỗi project: phải có bộ prompts test được

Để tránh project chỉ là spec “trên giấy”, mỗi project trong `projects/` cần output thêm:

1. **Master Instruction draft** (copy-paste được vào Gem/Custom GPT).  
2. **Prompt Stack** dùng trong chat:
   - ít nhất 3 phase chính (tuỳ project):
     - Frame / Structure / Reason / Validate / Synthesize / Lesson…  
   - mỗi prompt:
     - có thể dán thẳng vào chat để làm việc theo phase.
3. **5–10 Test Prompts (Scenario tests)**:
   - mỗi scenario:
     - 1 user prompt “bẩn”/thật,
     - 2–5 bullet mô tả behavior mong đợi (để so với thực tế assistant trả lời).

Ví dụ (tóm tắt cho Project 1 – FruitTree Mentor):

- Master Instruction: như mẫu rút gọn ở trên (được polish).  
- Prompt Stack:
  - P1: Phase 1 – Framing,
  - P2: Phase 2 – Structuring symptoms,
  - P3: Phase 3 – Reasoning TREE-Care,
  - P4: Phase 4 – Validation light,
  - P5: Phase 5 – Care plan.  
- Test Prompts:
  - 3–4 câu hỏi chẩn đoán bệnh,
  - 2–3 câu hỏi về thiết kế vườn/mùa vụ,
  - 1–2 câu hỏi “ngoài scope” (test guardrails).

Khi học viên nộp project, bạn có thể chấm:

- spec (logic & clarity),
- **master instruction** (đúng scope/behavior),
- **prompt stack** (đúng phase),
- **test prompts & kết quả** (assistant có hành xử như thiết kế không).

---
