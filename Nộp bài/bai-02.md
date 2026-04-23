# Trắc nghiệm

1- B
2- D
3- B
4- C
5- B
6- B
7- C
8- A
9- C
10- C



# Bài tập

## Bài tập 1 — RTC-COE Lab: “Mổ xẻ & viết lại 2 prompt dài-sai”

**Mục tiêu**  
Luyện thói quen nhìn prompt theo cấu trúc, không viết theo cảm tính.

=== Prompt 1 ===
```


```

**Đánh giá**

| Thành phần | Có/Không | Nhận xét ngắn                                         |
|-----------|----------|-------------------------------------------------------|
| Role      |          | Vai trò rõ hay mơ hồ?                                 |
| Task      |          | Có trộn bao nhiêu loại task?                          |
| Context   |          | Bối cảnh, audience, thời gian, domain có rõ không?    |
| Constraints |        | Có ràng buộc cụ thể, hữu ích không?                   |
| Output    |          | Output là artifact cụ thể hay chỉ “trả lời kỹ”?       |
| Evaluation|          | Có tiêu chí "tốt/kém" không?                          |

**Viết lại một phiên bản prompt mới:**

```
```
=== Prompt 2 ===

```


```

**Đánh giá**

| Thành phần | Có/Không | Nhận xét ngắn                                         |
|-----------|----------|-------------------------------------------------------|
| Role      |          | Vai trò rõ hay mơ hồ?                                 |
| Task      |          | Có trộn bao nhiêu loại task?                          |
| Context   |          | Bối cảnh, audience, thời gian, domain có rõ không?    |
| Constraints |        | Có ràng buộc cụ thể, hữu ích không?                   |
| Output    |          | Output là artifact cụ thể hay chỉ “trả lời kỹ”?       |
| Evaluation|          | Có tiêu chí "tốt/kém" không?                          |

**Viết lại một phiên bản prompt mới:**

```
```




## Prompt Stack V1 — AI hỗ trợ xây hệ thống nội dung & kênh cá nhân cho Leader hệ thống

### Context (tóm tắt Framing Brief)

- **Topic**: Ứng dụng AI vào xây dựng thương hiệu cá nhân cho Leader MLM/Đại lý mạng lưới
- **Problem**: Leader giỏi truyền lửa offline nhưng tốn thời gian thể hiện chuyên môn lên mạng xã hội để mở rộng đội nhóm
- **Audience**: Leader/Boss hệ thống tự chủ hoàn toàn, không có trợ lý, rất bận, cần kênh TikTok/Facebook
- **Scope**: Content Matrix, Workflow tái chế bài giảng, Playbook Prompt — không đi vào tool spam, bắt trend giải trí, lách luật quảng cáo
- **Output ưu tiên**: Content Matrix 30 ngày, Workflow tái chế, Playbook Prompt mẫu

---

### Prompt 0 — Grounding Brief

*Task type chính: grounding (thiết lập bối cảnh)*

```
Sắp gửi một Framing Brief mô tả chủ đề, bài toán, đối tượng, phạm vi và output mong muốn.

Yêu cầu:
- Chỉ sử dụng brief này làm nguồn thông tin chính về bối cảnh.
- Nếu các prompt sau có nội dung mâu thuẫn với brief, hãy báo lại để kiểm tra.
- Giữ đúng domain MLM/Đại lý mạng lưới/Bán hàng trực tiếp — không lệch sang kinh doanh truyền thống.

Đây là Framing Brief:

[DÁN FRAMING BRIEF TỪ BÀI 01 VÀO ĐÂY]

Nhiệm vụ:
- Xác nhận đã hiểu bối cảnh.
- Tóm tắt lại ngắn gọn theo cách diễn đạt của bạn để kiểm tra mức độ hiểu framing.
Chưa cần giải bài toán chính.
```

---

### Prompt 1 — Làm rõ bài toán (Clarify)

*Task type chính: explain + diagnose*

```
[Role] Chuyên gia tư vấn xây dựng hệ thống nội dung & kênh mạng xã hội cá nhân.

[Task]
1. Tóm tắt lại bài toán, đối tượng, phạm vi và output từ Framing Brief bằng ngôn ngữ đơn giản.
2. Liệt kê 5–7 giả định ngầm về Leader (tần suất đăng bài, thời gian mỗi ngày, có trợ lý hay tự làm…).
3. Đề xuất 5 câu hỏi cần làm rõ trước khi thiết kế hệ thống content.

[Context]
- Đây là bước làm rõ yêu cầu, chưa bước vào thiết kế giải pháp.
- Domain: Leader hệ thống MLM/Đại lý, kênh TikTok/Facebook.
- Bối cảnh: kinh doanh khởi nghiệp — Leader hoạt động hoàn toàn tự chủ, không có trợ lý.

[Constraints]
- Không đề xuất giải pháp hay hệ thống content ở bước này.
- Ngôn ngữ đơn giản, tránh thuật ngữ marketing phức tạp.
- Leader hoạt động hoàn toàn tự chủ, không có trợ lý — giả định và câu hỏi phải phản ánh điều này.
- Trình bày theo đầu mục rõ ràng, nội dung dạng gạch đầu dòng, ngắn gọn.

[Output]
- Đoạn tóm tắt bài toán (5–7 câu).
- Danh sách "Giả định hiện tại" (5–7 giả định).
- Danh sách "Câu hỏi cần làm rõ" (5 câu hỏi).

[Evaluation]
- Tốt nếu giả định phản ánh đúng thực tế Leader tự chủ, không có trợ lý.
- Tốt nếu câu hỏi chỉ ra được điểm mờ thực sự (tần suất, thời gian, nền tảng ưu tiên…).
- Tốt nếu không có câu hỏi thừa hoặc quá hiển nhiên.
- Kém nếu lệch sang bối cảnh kinh doanh truyền thống — phải giữ đúng domain MLM/Đại lý mạng lưới/Bán hàng trực tiếp.
```

---

### Prompt 2 — Bóc tách cấu trúc hệ thống content (Structure)

*Task type chính: design (extract & structure)*

```
[Role] Người sắp xếp tri thức chuyên tổ chức và phân loại hệ thống nội dung cho Leader MLM/Đại lý mạng lưới.

[Task]
- Liệt kê các thành phần của hệ thống content cho Leader MLM/Đại lý, 
  phân tích theo 6 chiều: loại nội dung, kênh phân phối, đối tượng, 
  tần suất, quy trình sản xuất, mục đích.
- Nhóm các thành phần thành 3–5 nhóm lớn phục vụ cho việc xây khung 
  hệ thống content ở bước sau.

[Context]
- Dựa trên kết quả tóm tắt, giả định và câu hỏi làm rõ từ Prompt 1.
- Audience: Leader MLM/Đại lý tự chủ hoàn toàn, không có trợ lý.
- Mục tiêu: tạo "bản đồ thô" toàn bộ hệ thống content — chưa cần tối ưu hay thiết kế chi tiết.

[Constraints]
- Mỗi thành phần cần có mô tả ngắn + ví dụ cụ thể trong domain MLM/Đại lý.
- Không thêm nội dung đã xác định là out-of-scope (bắt trend giải trí, tool spam, lách luật quảng cáo).
- Tần suất đề xuất phải thực tế với người tự làm một mình — tối đa 1 bài/ngày, 
  không tạo áp lực "con nợ nội dung" cho nền tảng.
- Mỗi nhóm phải có mục đích khác biệt rõ ràng — nêu rõ lý do tách nhóm, không để 2 nhóm cùng nhắm một đối tượng và mục đích.
- Trình bày dạng đầu mục + gạch đầu dòng.

[Output]
- Cấu trúc dạng cây phân cấp:
  - Nhóm lớn (3–5 nhóm)
    - Thành phần con: mô tả ngắn
      - Ví dụ cụ thể trong domain MLM/Đại lý

[Evaluation]
- Tốt nếu cây bao quát đủ 6 chiều đã xác định, không bỏ sót.
- Tốt nếu ví dụ gắn với thực tế Leader MLM/Đại lý, không chung chung.
- Tốt nếu các nhánh không chồng chéo — mỗi thành phần chỉ thuộc một nhóm duy nhất.
- Có thể dùng cây này làm xương sống cho Prompt 3.
```

---

### Prompt 3 — Tinh chỉnh thành Content Matrix (Refine)

*Task type chính: refine + design*

```
[Role] Chuyên gia thiết kế chương trình & hệ thống nội dung có thể chuyển giao 
cho Leader MLM/Đại lý tự vận hành.

[Task]
1. Từ cây phân cấp ở Prompt 2, gom và tinh giản thành 5–7 loại nội dung cốt lõi 
   cho Content Matrix của Leader MLM/Đại lý.
2. Với mỗi loại nội dung, bổ sung:
   - Tên ngắn gọn (2–4 từ)
   - Mô tả 1–2 câu
   - Ví dụ bài cụ thể trong domain MLM/Đại lý
   - Hành động Leader có thể làm ngay (dưới 30 phút)

[Context]
- Dựa trên cây phân cấp từ Prompt 2.
- Mục tiêu: tạo Content Matrix có thể dùng ngay và dạy lại cho tuyến dưới (F1/F2).
- Leader tự làm hoàn toàn, không trợ lý, thời gian & ngân sách hạn chế.

[Constraints]
- Chỉ giữ lại 5–7 loại nội dung cốt lõi — không thêm mới ngoài cây Prompt 2.
- Ưu tiên dạng nội dung dễ bắt đầu: không cần thiết bị đắt tiền, không cần kỹ năng 
  chỉnh sửa phức tạp, không tốn quá 30 phút/bài.
- Không đề xuất nội dung đòi hỏi ekip, studio, hay ngân sách quảng cáo.

[Output]
- Bảng Content Matrix với các cột:
  1. Loại nội dung (tên ngắn 2–4 từ)
  2. Mô tả
  3. Ví dụ cụ thể trong domain MLM/Đại lý
  4. Mục đích (tuyển người / bán hàng / truyền cảm hứng…)
  5. Tần suất (ngày/tuần/tháng)
  6. Kênh phù hợp (TikTok / Facebook / cả hai)
  7. Độ khó (Dễ / Trung bình / Khó)
  8. Hành động Leader có thể làm ngay (dưới 30 phút)

[Evaluation]
- Tốt nếu bảng có thể in ra và dùng ngay làm lịch content tháng đầu mà không cần chỉnh sửa thêm.
- Tốt nếu mọi loại nội dung đều khả thi với Leader mới bắt đầu, tự làm một mình.
- Kém nếu có bất kỳ loại nội dung nào đòi hỏi ekip, thiết bị chuyên nghiệp hoặc ngân sách quảng cáo.
```

---

### Prompt 4 — Phản biện & Kiểm định (Critique)

*Task type chính: critique*

```
[Role] Chuyên gia QC nội dung có kinh nghiệm thực chiến xây kênh cá nhân 
trong lĩnh vực MLM/Đại lý mạng lưới.

[Task]
1. Chỉ ra 2–3 điểm mạnh của Content Matrix (về tính thực tế, tính dễ làm, tính nhất quán…).
2. Chỉ ra ít nhất 5 điểm yếu hoặc lỗ hổng, bao gồm:
   - Loại nội dung nào dễ gây hiểu nhầm hoặc mất thiện cảm với người lạ
   - Rủi ro vi phạm pháp lý hoặc chính sách nền tảng (TikTok/Facebook)
   - Loại nội dung nào khó duy trì với người tự làm một mình
   - Chỗ nào còn thiếu để xây dựng lòng tin trước khi tuyển người
3. Đề xuất 2 phiên bản điều chỉnh:
   - Phiên bản A: rút gọn cho Leader mới bắt đầu (tuần đầu tiên)
   - Phiên bản B: mở rộng cho Leader đã có nền tảng và muốn scale

[Context]
- Dựa trên Content Matrix đã tạo ở Prompt 3.
- Audience: Leader MLM/Đại lý tự chủ hoàn toàn, không có trợ lý.
- Domain: MLM/Đại lý mạng lưới/Bán hàng trực tiếp — không lệch sang kinh doanh truyền thống.

[Constraints]
- Tập trung vào tính khả thi thực tế, không phê bình lý thuyết chung chung.
- Nếu chỗ nào chưa tốt phải giải thích cụ thể lý do và đưa ra gợi ý cải thiện luôn.
- Không viết lại toàn bộ Content Matrix — chỉ chỉ ra vùng cần điều chỉnh.
- Trình bày dạng đầu mục + gạch đầu dòng.

[Output]
1. Điểm mạnh (2–3 điểm)
2. Điểm yếu/lỗ hổng (ít nhất 5 điểm + gợi ý cải thiện cụ thể)
3. Bảng tóm tắt rủi ro pháp lý:
   - Loại nội dung | Rủi ro | Mức độ | Cách phòng tránh
4. Bảng chấm điểm Content Matrix theo tiêu chí:
   - Tính khả thi | Tính tin cậy với người lạ | Tính tuân thủ pháp lý | Dễ duy trì một mình
5. Phiên bản A — rút gọn cho Leader mới bắt đầu (kèm bảng lịch tuần cụ thể)
6. Phiên bản B — mở rộng cho Leader đã có nền tảng (kèm bảng lịch tuần cụ thể)

[Evaluation]
- Tốt nếu điểm yếu nêu cụ thể, có dẫn chứng từ Content Matrix, không nói chung chung.
- Tốt nếu bảng rủi ro pháp lý thực tế với nền tảng TikTok/Facebook tại Việt Nam.
- Tốt nếu 2 phiên bản A/B có thể triển khai ngay mà không cần hỏi thêm.
- Kém nếu phê bình chung chung mà không có gợi ý cải thiện cụ thể.
```

---

### Prompt 5 — Thiết kế lịch content 30 ngày (Design)

*Task type chính: design + synthesize*

```
[Role] Coach xây dựng lịch content thực chiến cho Leader MLM/Đại lý 
tự vận hành kênh cá nhân.

[Task]
Dựa trên Content Matrix từ Prompt 3 và phiên bản điều chỉnh đã chọn 
từ Prompt 4 (A hoặc B):
1. Thiết kế lịch content 30 ngày cụ thể theo từng ngày.
2. Với mỗi ngày, chỉ rõ:
   - Loại content (từ Content Matrix)
   - Kênh đăng (TikTok / Facebook / cả hai)
   - Gợi ý chủ đề cụ thể (1 dòng)

[Context]
- Dựa trên Content Matrix (Prompt 3) và phiên bản A hoặc B (Prompt 4).
- Leader tự làm một mình, không trợ lý, thời gian hạn chế.
- Mục tiêu tháng đầu: xây dựng thói quen đăng đều đặn — không cần hoàn hảo, 
  cần bền vững.

[Constraints]
- Tối đa 1 bài/ngày — không được vượt quá.
- Phải có ít nhất 2 ngày nghỉ/tuần — không đăng bài.
- Không lặp cùng 1 loại content 2 ngày liên tiếp.
- Tuần 1 chỉ dùng các loại content có độ khó "Dễ" — tăng dần từ tuần 2.
- Trình bày dạng bảng, chia làm 4 tuần.

[Output]
- Bảng lịch 30 ngày chia theo tuần:

  Tuần 1 — [Tên chủ đề tuần]
  | Ngày | Loại content | Kênh | Gợi ý chủ đề |
  |------|-------------|------|--------------|
  | Thứ Hai | ... | ... | ... |
  | ...

  (lặp lại cho Tuần 2, 3, 4)

- Tổng kết cuối bảng:
  - Tổng số bài/tháng
  - Phân bổ theo loại content (%)
  - Phân bổ theo kênh (%)

[Evaluation]
- Tốt nếu lịch có thể in ra và dùng ngay mà không cần chỉnh sửa thêm.
- Tốt nếu tuần 1 đủ nhẹ để Leader mới bắt đầu không bỏ cuộc.
- Tốt nếu có sự đa dạng — không có tuần nào toàn 1 loại content.
- Kém nếu lịch dày đặc đến mức Leader tự làm một mình không thể duy trì.
```

### Tiêu chí tự chấm Prompt Stack V1 (rubric gợi ý)

| Tiêu chí                 | Mô tả                                                                                          | Điểm (0–5) |
|--------------------------|------------------------------------------------------------------------------------------------|-----------|
| Alignment với Brief      | Stack bám sát problem, audience, scope, output trong Framing Brief                           | 4/5        |
| Cấu trúc RTC-COE         | Mỗi prompt có Role, Task, Context, Constraints, Output rõ ràng                               | 5/5        |
| Tách phase hợp lý        | Các prompt thực sự xử lý các nhiệm vụ khác nhau, không lặp lại cùng một task                 | 4/5        |
| Tính tái sử dụng         | Stack có thể áp dụng lại cho chủ đề khác trong cùng domain với ít chỉnh sửa                  | 4/5        |
| Chuẩn bị cho Buổi 3–4    | Output của stack có thể dùng làm input cho Decomposition & Information Architecture (IA)      | ?/5        |
| Clarity                  | Văn bản rõ ràng, dễ hiểu, tránh mơ hồ                                                         | 4/5        |

---


---

## Prompt Stack V2 — Workflow tái chế bài giảng → Post/Video

### Context (tóm tắt Framing Brief)

- **Topic**: Tái chế nội dung từ bài giảng offline/Zoom thành post text và short video
- **Problem**: Leader có kho file ghi âm offline và video Zoom nhưng chưa có quy trình biến thành content mạng xã hội
- **Audience**: Leader/Boss hệ thống tự chủ hoàn toàn, không có trợ lý, có máy tính + điện thoại + app miễn phí
- **Scope**: 2 luồng — Ghi âm offline → Post text/caption & Video Zoom → Short video TikTok/Reels
- **Output ưu tiên**: SOP 2 luồng + Template tái chế 1 trang phân tầng cơ bản/nâng cao

> **Lưu ý khi dùng**: Dùng chung Prompt 0 — Grounding Brief từ Stack 1.
> Sau khi nhận output Prompt 1, trả lời 5 câu hỏi làm rõ trước khi gửi Prompt 2.

---

### Prompt 1 — Kiểm kê kho nội dung (Clarify)

*Task type chính: explain + diagnose*

```
[Role] Thủ thư chuyên quản lý và phân loại kho nội dung đào tạo 
cho Leader MLM/Đại lý.

[Task]
1. Tóm tắt lại bài toán tái chế nội dung từ Framing Brief.
2. Liệt kê 5–7 giả định về kho nội dung của Leader (loại file, 
   số lượng, chất lượng, khả năng truy cập...).
3. Đánh giá tình trạng tổ chức & lưu trữ kho nội dung hiện tại 
   — có hệ thống hay lưu lung tung, đặt tên hay không, dễ tìm 
   lại hay không.
4. Đề xuất 5 câu hỏi làm rõ trước khi thiết kế quy trình tái chế.

[Context]
- Đây là bước kiểm kê đầu vào, chưa thiết kế quy trình tái chế.
- Domain: Leader MLM/Đại lý — kho nội dung gồm file ghi âm 
  chương trình offline và video ghi hình Zoom online.
- Leader tự chủ, không trợ lý — kho nội dung do 1 người quản lý.

[Constraints]
- Không đề xuất quy trình tái chế ở bước này — chỉ kiểm kê 
  và đặt câu hỏi.
- Câu hỏi phải thực tế với người không rành kỹ thuật — tránh 
  hỏi về cách thức xử lý dữ liệu hay thuật ngữ media chuyên môn 
  (bitrate, độ phân giải, codec...).
- Trình bày dạng đầu mục + gạch đầu dòng.

[Output]
1. Tóm tắt bài toán tái chế (3–5 câu)
2. Danh sách "Giả định về kho nội dung" (5–7 giả định)
3. Đánh giá tình trạng tổ chức & lưu trữ (ngắn gọn)
4. Danh sách "Câu hỏi cần làm rõ" (5 câu hỏi)

[Evaluation]
- Tốt nếu giả định phản ánh đúng thực tế file ghi âm offline 
  + Zoom, không giả định kho "sạch".
- Tốt nếu câu hỏi giúp phát hiện điểm tắc nghẽn thực tế 
  (chất lượng âm, cách lưu trữ, khả năng tìm lại).
- Kém nếu hỏi về các cách thức xử lý dữ liệu.
- Kém nếu đưa thuật ngữ chuyên môn media vào câu hỏi 
  (bitrate, độ phân giải, codec...).
- Kém nếu lệch sang domain kinh doanh truyền thống.
```

---

### Prompt 2 — Bóc tách quy trình tái chế (Structure)

*Task type chính: design (extract & structure)*

```
[Role] Chuyên gia thiết kế quy trình content cho cá nhân và 
doanh nghiệp nhỏ trong lĩnh vực MLM/Đại lý mạng lưới.

[Task]
- Dựa trên kết quả kiểm kê kho nội dung từ Prompt 1.
- Bóc tách các bước xử lý theo 2 luồng song song:
  - Luồng A: File ghi âm offline → Post text/caption
  - Luồng B: Video Zoom → Short video (TikTok/Reels)
- Với mỗi luồng, liệt kê đầy đủ các bước từ đầu đến cuối.
- Nhóm các bước thành 3–5 giai đoạn lớn 
  (ví dụ: Chuẩn bị → Xử lý → Đóng gói → Đăng).

[Context]
- Dựa trên kết quả từ Prompt 1 (giả định, tình trạng kho, 
  câu hỏi đã làm rõ).
- Leader tự làm một mình, không có công cụ chuyên nghiệp — 
  có máy tính và các app miễn phí (bao gồm AI).
- Mục tiêu: tạo bản đồ thô đủ chi tiết để thiết kế SOP 
  ở Prompt 3.

[Constraints]
- Mỗi bước cần mô tả ngắn + công cụ miễn phí có thể dùng 
  (app, AI, phần mềm).
- Không đề xuất công cụ trả phí hoặc cần kỹ năng kỹ thuật cao.
- Không bỏ sót bước nào dù nhỏ — kể cả bước "nghe lại để 
  chọn đoạn hay".
- Trình bày dạng cây phân cấp, tách rõ 2 luồng A và B.

[Output]
Luồng A — Ghi âm offline → Post text/caption
  Giai đoạn 1: [Tên]
    - Bước 1: mô tả | công cụ | thời gian ước tính | định dạng đầu ra
    - Bước 2: mô tả | công cụ | thời gian ước tính | định dạng đầu ra
  Giai đoạn 2: ...

Luồng B — Video Zoom → Short video (TikTok/Reels)
  Giai đoạn 1: [Tên]
    - Bước 1: mô tả | công cụ | thời gian ước tính | định dạng đầu ra
    ...

[Evaluation]
- Tốt nếu cả 2 luồng đủ chi tiết để Leader làm theo mà không 
  cần hỏi thêm.
- Tốt nếu mọi công cụ đề xuất đều miễn phí và có trên điện 
  thoại hoặc máy tính thông thường.
- Tốt nếu tổng thời lượng thực hiện mỗi luồng không quá 
  1 giờ/ngày.
- Kém nếu bỏ sót bước quan trọng như nghe lại, chọn đoạn, 
  viết caption.
- Kém nếu 2 luồng có bước trùng lặp mà không gộp lại.
```

---

### Prompt 3 — Đóng gói thành SOP (Refine)

*Task type chính: refine + design*

```
[Role] Chuyên gia viết SOP content cho cá nhân tự vận hành 
trong lĩnh vực MLM/Đại lý mạng lưới.

[Task]
1. Từ bản đồ bước ở Prompt 2, thiết kế SOP theo cấu trúc:
   - Phần chung (áp dụng cả 2 luồng): các bước xử lý nội 
     dung gốc dùng chung — nghe lại, chọn đoạn hay, trích 
     ý chính
   - Luồng A (từ phần chung → Post text/caption): các bước riêng
   - Luồng B (từ phần chung → Short video TikTok/Reels): 
     các bước riêng
2. Tổng số bước mỗi luồng (bao gồm phần chung): không quá 7 bước
3. Mỗi bước ghi rõ: tên bước, mô tả ngắn, công cụ, thời gian 
   ước tính, đầu ra

[Context]
- Dựa trên bản đồ 2 luồng từ Prompt 2.
- Mục tiêu: Leader mở SOP ra là làm theo được, không cần 
  giải thích thêm.
- SOP đủ đơn giản để hướng dẫn lại cho F1/F2 mà không cần 
  Leader giải thích trực tiếp.
- Leader có máy tính + điện thoại + app miễn phí (bao gồm AI).

[Constraints]
- Không thêm bước mới ngoài bản đồ từ Prompt 2 — chỉ gom, 
  tinh giản, sắp xếp lại.
- Ngôn ngữ đời thường, tránh thuật ngữ kỹ thuật.
- Mỗi bước phải có đầu ra rõ ràng — biết bước này xong khi nào.
- Trình bày dạng đánh số, dễ in ra dùng.

[Output]
PHẦN CHUNG — Xử lý nội dung gốc
  Bước 1: tên | mô tả | công cụ | thời gian | đầu ra
  Bước 2: ...

LUỒNG A — Post text/caption
  Bước 3: tên | mô tả | công cụ | thời gian | đầu ra
  ...
  Checklist tự kiểm tra trước khi đăng (5–7 điểm)
  Lưu trữ: tên file | định dạng | thư mục/vị trí lưu

LUỒNG B — Short video (TikTok/Reels)
  Bước 3: tên | mô tả | công cụ | thời gian | đầu ra
  ...
  Checklist tự kiểm tra trước khi đăng (5–7 điểm)
  Lưu trữ: tên file | định dạng | thư mục/vị trí lưu

[Evaluation]
- Tốt nếu SOP đủ rõ để F1/F2 làm theo mà không cần hỏi Leader.
- Tốt nếu checklist phát hiện được lỗi phổ biến trước khi đăng.
- Tốt nếu hướng dẫn lưu trữ giúp tìm lại file dễ dàng sau 
  1 tháng.
- Kém nếu bước nào không rõ "xong khi nào".
- Kém nếu dùng thuật ngữ kỹ thuật mà Leader không hiểu.
- Kém nếu quy trình chỉ phù hợp với 1 người — người mới bắt 
  đầu phải làm được.
```

---

### Prompt 4 — Phản biện & Kiểm định SOP (Critique)

*Task type chính: critique*

```
[Role] Chuyên gia QC quy trình vận hành content cho cá nhân 
tự chủ trong lĩnh vực MLM/Đại lý mạng lưới.

[Task]
1. Chỉ ra 2–3 điểm mạnh của SOP (về tính rõ ràng, tính phổ 
   quát, tính chuyển giao).
2. Chỉ ra ít nhất 5 điểm yếu/lỗ hổng, bao gồm:
   - Bước nào dễ gây tắc nghẽn kỹ thuật với người không rành
   - Bước nào dễ bị bỏ qua nhất khi bận
   - Bước nào dễ gây bỏ cuộc nhất — và lý do cụ thể tại sao
   - Chỗ nào SOP chưa đủ phổ quát để người mới làm được
3. Đề xuất 2 phiên bản:
   - Phiên bản A: nhanh (dưới 30 phút/bài) cho người mới bắt đầu
   - Phiên bản B: sâu (dưới 60 phút/bài) cho người đã quen 
     quy trình

[Context]
- Dựa trên SOP 2 luồng từ Prompt 3.
- Leader tự chủ, không trợ lý, có máy tính + điện thoại + 
  app miễn phí.
- SOP cần chuyển giao được cho F1/F2.

[Constraints]
- Tập trung vào tính khả thi thực tế, không phê bình lý thuyết.
- Nếu chỗ nào chưa tốt phải giải thích cụ thể lý do và đưa 
  gợi ý cải thiện luôn.
- Không viết lại toàn bộ SOP — chỉ chỉ ra vùng cần điều chỉnh.
- Trình bày dạng đầu mục + gạch đầu dòng.

[Output]
1. Điểm mạnh (2–3 điểm)
2. Điểm yếu/lỗ hổng (ít nhất 5 điểm + gợi ý cải thiện cụ thể)
3. Bảng điểm tắc nghẽn & bỏ cuộc:
   - Bước | Lý do dễ bỏ cuộc | Mức độ rủi ro | Cách phòng tránh
4. Bảng chấm điểm SOP theo tiêu chí:
   - Tính rõ ràng | Tính phổ quát | Khả năng chuyển giao | 
     Dễ duy trì một mình
5. Phiên bản A — nhanh (dưới 30 phút/bài)
6. Phiên bản B — sâu (dưới 60 phút/bài)

[Evaluation]
- Tốt nếu bảng tắc nghẽn chỉ ra được bước cụ thể dễ gây bỏ 
  cuộc, có lý do thực tế.
- Tốt nếu 2 phiên bản A/B có thể triển khai ngay mà không 
  cần hỏi thêm.
- Tốt nếu điểm yếu nêu cụ thể, có dẫn chứng từ SOP, không 
  nói chung chung.
- Kém nếu phê bình chung chung mà không có gợi ý cải thiện 
  cụ thể.
- Kém nếu quy trình đề xuất vẫn đòi hỏi kỹ năng kỹ thuật cao.
- Kém nếu quy trình chỉ phù hợp với 1 người — người mới bắt 
  đầu phải làm được.
```

---

### Prompt 5 — Template tái chế 1 trang (Design)

*Task type chính: design + synthesize*

```
[Role] Template designer chuyên thiết kế công cụ làm việc 
cho cá nhân tự vận hành trong lĩnh vực MLM/Đại lý mạng lưới.

[Task]
1. Thiết kế template theo cấu trúc phân tầng:
   - Phần cơ bản (Template A): xử lý nội dung gốc → ra post 
     text/caption — người mới bắt đầu hoàn thành được
   - Phần nâng cao (Template B): nối tiếp từ kết quả Template A 
     → ra script short video TikTok/Reels — dành cho người đã quen
2. Mỗi ô điền trong template cần có:
   - Tên ô + hướng dẫn ngắn (1 câu)
   - Ví dụ mẫu trong domain MLM/Đại lý
3. Đánh dấu rõ ranh giới giữa phần cơ bản và phần nâng cao.

[Context]
- Dựa trên SOP từ Prompt 3 và phiên bản A/B từ Prompt 4.
- Mục tiêu: Leader điền vào template là ra content, không cần 
  nghĩ thêm.
- Người mới chỉ cần hoàn thành phần cơ bản — đã có kết quả 
  dùng được.

[Constraints]
- Mỗi ô điền không quá 3 dòng — tránh template quá dài gây nản.
- Ngôn ngữ hướng dẫn đời thường, không dùng thuật ngữ kỹ thuật.
- Đánh dấu rõ ràng ranh giới "PHẦN CƠ BẢN — dừng ở đây nếu 
  mới bắt đầu" và "PHẦN NÂNG CAO".
- Template phải in ra được trên 1–2 trang A4.
- Cuối mỗi phần phải có checklist tự kiểm tra trước khi chuyển 
  sang bước tiếp theo.

[Output]
TEMPLATE TÁI CHẾ NỘI DUNG — Leader MLM/Đại lý

━━━ PHẦN CƠ BẢN (Post text/caption) ━━━
[Ô 1] Tên nội dung gốc: _______
       Hướng dẫn: ... | Ví dụ: ...
[Ô 2] Đoạn hay nhất: _______
       Hướng dẫn: ... | Ví dụ: ...
...
☑ Checklist trước khi đăng:
  □ ...
  □ ...
📁 Lưu trữ: tên file | định dạng | thư mục lưu

━━━ PHẦN NÂNG CAO (Short video) ━━━
[Ô X] Hook mở đầu: _______
       Hướng dẫn: ... | Ví dụ: ...
...
☑ Checklist trước khi đăng:
  □ ...
  □ ...
📁 Lưu trữ: tên file | định dạng | thư mục lưu

[Evaluation]
- Tốt nếu người mới chỉ làm phần cơ bản đã ra được post 
  dùng được.
- Tốt nếu template in vừa 1–2 trang A4, không bị chật chội.
- Tốt nếu checklist đủ để tự QC mà không cần hỏi ai.
- Tốt nếu ô lưu trữ giúp tìm lại file sau 1 tháng dễ dàng.
- Kém nếu ô điền nào không có ví dụ cụ thể trong domain 
  MLM/Đại lý.
- Kém nếu ranh giới cơ bản/nâng cao không rõ ràng.
```

---

