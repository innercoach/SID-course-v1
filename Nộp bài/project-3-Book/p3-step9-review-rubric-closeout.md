---
project: Book Architect Pro (Project 3)
step: 9
artifact: Review, Acceptance Rubric & Close-out
sid_techniques: [Validation, Self-Critique, Iterative Synthesis]
grounding_mode: OFF
status: draft-for-verify
closes: SID build process (Step 1-9)
---

# Step 9 — Review, Rubric nghiệm thu & Đóng quy trình

## 1. Xử lý defect (vòng sửa 1)

| Defect | Cách sửa | Vá vào |
|---|---|---|
| **D1** — thiếu fallback input lệch vocab | thêm luật: input rõ → map lệnh gần nhất; input mơ hồ → hỏi 1 câu + giữ ngữ cảnh + đề 2–3 hướng | `KB2_flow.md` (mục FALLBACK) |
| **D2** — WRITE-DRAFT thiếu precondition | chỉ nháp section đã outline; chưa outline → đề nghị outline/drill trước | `KB6_stacks.md` (WRITE-DRAFT) |
| **D3** — ledger drift (chưa test được) | soạn kịch bản hội thoại dài để chạy thật (mục 4) | chờ test thực địa |

**Re-test nhanh (dry-run) sau vá:**
- S8 (input lệch vocab): giờ assistant hỏi làm rõ + giữ ngữ cảnh → **PASS**.
- S9 (draft chưa outline): giờ assistant đề nghị outline trước → **PASS**.

→ **9/9 PASS** ở dry-run. D3 còn treo cho test thực địa.

---

## 2. Self-review (góc evaluator)

**Chỗ tốt**
- An toàn đặt đúng chỗ: gate cross-cutting, touch-to-trigger, user không tắt được.
- Kiến trúc modular sạch: router mỏng + 6 KB theo chức năng + precedence rõ.
- Transfer trọn: từ problem note → prompt stack → test log → deploy-ready.
- Test có giá trị thật: lộ 2 defect thay vì PASS hình thức.

**Chỗ còn mỏng**
- **Ledger cách (a)** là điểm yếu kiến trúc còn lại — chưa validate hội thoại dài.
- **Ops rubric vận hành** (khác rubric nghiệm thu thiết kế) chưa có — cần khi
  dùng thật, đo chất lượng output theo thời gian.
- Chưa **deploy thật** với một tác giả thật.

**5 việc nên làm tiếp (ngoài phạm vi build này)**
1. Chạy kịch bản test dài (mục 4) → đo drift.
2. Nếu drift đáng kể → nâng ledger sang cách (b) block ẩn.
3. Thêm ops rubric vận hành cho bản deploy.
4. Bổ sung vài ca test: "đổi concept giữa chừng", "outline nhiều chương".
5. Thử nghiệm thực địa với 1 tác giả, 1 chủ đề nhạy cảm.

---

## 3. Rubric nghiệm thu thiết kế (thang 0–3)

| Tiêu chí | 0 | 1 | 2 | 3 | Chấm | Lý do |
|---|---|---|---|---|---|---|
| **Framing** | mơ hồ | có | khá rõ | rõ, 2 tầng audience | **3** | tác giả/người đọc tách rõ, concept branching |
| **Structure / IA** | rối | có tầng | khá logic | rõ từ concept→section | **3** | flow 6 phase, hub, MECE |
| **Tone / Safety** | thiếu | có nhắc | khá ổn | chặt, dùng được | **3** | gate touch-to-trigger, value boundaries, epistemic |
| **Chapter design** | yếu | có form | tạm ổn | rõ, không generic | **3** | Chapter Arc 6 nhịp + biến thể vai trò |
| **Testability** | chưa | ít test | có test | test tốt + revise | **3** | 9 scenario, defect log, vòng sửa |
| **Consistency / Ledger** | không | có ý | có cơ chế | validated | **2** | có cơ chế (cách a) nhưng D3 chưa test thật |

**Tổng: 17/18.** Đạt ngưỡng nghiệm thu thiết kế. Điểm trừ duy nhất là Ledger —
đúng điểm yếu đã biết, chờ test thực địa.

---

## 4. Kịch bản test hội thoại dài (cho D3 — anh chạy thật)

Chạy liền mạch trên Custom GPT để đo drift của ledger cách (a):

```
1.  Sách quản lý tài chính cá nhân cho người mới đi làm
2.  chọn 1
3.  dựng mục lục
4.  chương 1
5.  sâu phần 1.2
6.  chương khác
7.  chương 4
8.  sâu phần 4.1
9.  đang chốt gì rồi      <- kiểm: title/độc giả/tone/mục lục còn đúng?
10. chương 2
11. sâu phần 2.3
12. viết thử phần 2.3
13. chương 6
14. đang chốt gì rồi      <- kiểm: có nhất quán thuật ngữ đã dùng ở chương 1–2?
```
**Đạt nếu:** ở lượt 9 và 14, snapshot vẫn đúng title/độc giả/tone; thuật ngữ
không bị định nghĩa lại; Gate vẫn bật (chủ đề tài chính = nhạy cảm).

---

## 5. Checklist đóng quy trình (Step 1–9)

- [x] Step 1 — Author Problem Note
- [x] Step 2 — Framing Brief (rules → KB1)
- [x] Step 3 — Audience/Value Boundary map
- [x] Step 4 — Work Architecture (flow 6 phase)
- [x] Step 5 — Chapter Framework
- [x] Step 6 — Master Instruction (gộp)
- [x] Step 7 — Prompt Stack + bộ file (Master Instruction + KB1–6)
- [x] Step 8 — Scenario test log (9 ca)
- [x] Step 9 — Review + rubric + defect vá (D1, D2)

**Trạng thái: THIẾT KẾ HOÀN TẤT — sẵn sàng deploy bản test.**
Còn 1 việc thực địa: chạy kịch bản mục 4 (D3). Ops rubric vận hành là bước
sau khi dùng thật.

---

## Checkpoint tự đánh giá

Đối chiếu checkpoint mẫu (Project 2, Step 9):

- [x] Chỉ ra chỗ tốt / chỗ mỏng / chỗ lệch → ĐẠT (mục 2).
- [x] Sau 1 vòng sửa: output không sensational, đúng audience, structure tốt →
  ĐẠT (D1/D2 vá, 9/9 PASS).
- [x] Có rubric nghiệm thu định lượng → ĐẠT (mục 3, 17/18).
- [x] Đề xuất chỉnh sửa cụ thể tiếp theo → ĐẠT (mục 2, 5 việc).

**Tự đánh giá: ĐẠT checkpoint Step 9. Quy trình đóng.**

## Điểm cần anh verify

1. Rubric 17/18 (Ledger để 2) — anh đồng ý mức này, hay muốn ép test D3 xong
   mới coi là đóng?
2. Deploy: anh muốn mình gộp toàn bộ Step 1–9 thành **1 tài liệu bàn giao**
   (handoff doc) để lưu/nộp không?
3. Ops rubric vận hành — làm luôn, hay để sau khi anh chạy thử thực địa?
