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

> **Lưu ý khi dùng**: Chờ AI xác nhận và tóm tắt lại đúng bối cảnh trước khi gửi Prompt 1.
> Nếu AI tóm tắt sai → chỉnh brief rồi gửi lại Prompt 0, không tiếp tục stack.

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

> **Lưu ý khi dùng**: Sau khi nhận output Prompt 1, **trả lời 5 câu hỏi làm rõ** trước khi gửi Prompt 2.
> Ví dụ: tần suất có thể cam kết, nền tảng ưu tiên, số lượng video Zoom sẵn có...
> Bỏ qua bước này → Prompt 2 sẽ dựa trên giả định thay vì thông tin thật của bạn.

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
- Mục tiêu tháng đầu: xây thói quen đăng đều — không cần hoàn hảo, 
  cần bền vững.

[Constraints]
- Tối đa 1 bài/ngày — không được vượt quá.
- Phải có ít nhất 2 ngày nghỉ/tuần — không đăng bài.
- Không lặp cùng 1 loại content 2 ngày liên tiếp.
- Tuần 1 chỉ dùng các loại content có độ khó "Dễ" — tăng dần từ tuần 2.
- Trình bày dạng bảng, chia theo 4 tuần.

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
