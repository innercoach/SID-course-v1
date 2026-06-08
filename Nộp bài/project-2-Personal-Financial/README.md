## 2. Project 2 — Custom GPT: Content Engine cho video chủ đề gia đình / tài chính

**File:** `02-custom-gpt-content-engine.md`

### Bài toán & bối cảnh

Thiết kế 1 **Custom GPT** chuyên làm:

- **Content engine** cho video:
  - chủ đề **tài chính cá nhân/cơ bản** (quản lý chi tiêu, tiết kiệm, tư duy tiền,…).

Nó không chỉ “viết script”, mà:

- giúp chủ kênh:
  - lên chủ đề,
  - thiết kế series,
  - outline tập,
  - key message,
  - call-to-action,
  - gợi ý visual/shot.

### Yêu cầu chất lượng

- **Tone & values rõ**:
  - không sensational, không giật gân,
  - không cho lời khuyên tài chính vượt scope (“mua mã này, bán mã kia”…),
  - bám giá trị: trách nhiệm, bền vững, tôn trọng người xem.

- **IA content rõ**:
  - biết phân tầng nội dung:
    - top-of-funnel, mid, deep dive,
    - trình độ người xem,
  - biết cấu trúc 1 tập video:
    - hook → core → example → recap → CTA.

- **Workflow content**:
  - từ **idea bank** → **series** → **episode outline** → **script gợi ý**.

### Output project

1. **Spec cho Custom GPT Content Engine**:
   - System instructions (mission, boundaries, tone, values),
   - Supported workflows (ideation, series design, episode outline, script skeleton),
   - Input/Output schemas (vd: bảng lịch đăng video, outline, script format),
   - 3–5 scenario mẫu (user prompt → GPT output),
   - Safety & ethics rules (đặc biệt với tiền/bạo lực gia đình/khủng hoảng…).

2. (Tuỳ chọn) 1 pipeline mini:
   - ví dụ 1 series 5 video, mỗi video có outline sinh ra từ GPT.
