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
- Tốt nếu ví dụ đề cập ít nhất 1 trong: tuyển sỉ, tuyến dưới F1/F2, buổi Zoom đào tạo, commission, hệ thống đại lý.
- Kém nếu ví dụ dùng ngành khác thay thế (cửa hàng cà phê, freelancer, kinh doanh thông thường...).
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
- Bảng với 5–7 hàng (mỗi hàng = 1 loại nội dung), 8 cột theo thứ tự:

  | Loại nội dung | Mô tả | Ví dụ (MLM/Đại lý) | Mục đích | Tần suất | Kênh | Độ khó | Hành động ngay (<30') |
  |---|---|---|---|---|---|---|---|
  | (điền) | ... | ... | ... | ... | ... | ... | ... |

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
2. Liệt kê tất cả điểm yếu hoặc lỗ hổng tìm được, bao gồm:
   - Loại nội dung nào dễ gây hiểu nhầm hoặc mất thiện cảm với người lạ
   - Rủi ro vi phạm pháp lý hoặc chính sách nền tảng (TikTok/Facebook)
   - Loại nội dung nào khó duy trì với người tự làm một mình
   - Chỗ nào còn thiếu để xây dựng lòng tin trước khi tuyển người
   Sau đó tổng kết: 3 điểm ưu tiên giải quyết trước.

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
2. Danh sách điểm yếu/lỗ hổng (toàn bộ, mỗi điểm kèm gợi ý cải thiện cụ thể)
   → Tổng kết: 3 điểm ưu tiên giải quyết trước
3. Bảng tóm tắt rủi ro pháp lý:
   - Loại nội dung | Rủi ro | Mức độ | Cách phòng tránh
4. Bảng chấm điểm Content Matrix theo tiêu chí:
   - Tính khả thi | Tính tin cậy với người lạ | Tính tuân thủ pháp lý | Dễ duy trì một mình

[Evaluation]
- Tốt nếu danh sách điểm yếu toàn diện, không bỏ sót loại nội dung nào trong bảng.
- Tốt nếu 3 điểm ưu tiên được chọn có lý do rõ ràng — không chọn ngẫu nhiên.
- Tốt nếu bảng rủi ro pháp lý thực tế với nền tảng TikTok/Facebook tại Việt Nam.
- Kém nếu phê bình chung chung mà không có gợi ý cải thiện cụ thể.
```

---

### Prompt 5 — Phiên bản A/B & Lịch content 30 ngày (Design)

*Task type chính: design + synthesize*

```
[Role] Coach xây dựng lịch content thực chiến cho Leader MLM/Đại lý 
tự vận hành kênh cá nhân.

[Task]
1. Từ kết quả phân tích ở Prompt 4, đề xuất 2 phiên bản điều chỉnh:
   - Phiên bản A: rút gọn cho Leader mới bắt đầu — nêu rõ đặc điểm 
     + kèm lịch tuần mẫu 7 ngày
   - Phiên bản B: mở rộng cho Leader đã có nền tảng và muốn scale — 
     nêu rõ đặc điểm + kèm lịch tuần mẫu 7 ngày
2. Dựa trên phiên bản Leader xác nhận ([CHỌN: A / B] — điền trước 
   khi gửi prompt này):
   Thiết kế lịch content 30 ngày đầy đủ. Với mỗi ngày, chỉ rõ:
   - Loại content
   - Kênh đăng (TikTok / Facebook / cả hai)
   - Gợi ý chủ đề cụ thể (1 dòng)

[Context]
- Dựa trên bảng nội dung (Prompt 3) và kết quả phân tích (Prompt 4).
- Phiên bản A/B được trình bày ở bước 1 — Leader xác nhận chọn 
  trước khi AI thiết kế lịch 30 ngày đầy đủ.
- Leader tự làm một mình, không trợ lý, thời gian hạn chế.
- Mục tiêu tháng đầu: xây dựng thói quen đăng đều đặn — không cần 
  hoàn hảo, cần bền vững.

[Constraints]
- Tối đa 1 bài/ngày — không được vượt quá.
- Phải có ít nhất 2 ngày nghỉ/tuần — không đăng bài.
- Không lặp cùng 1 loại content 2 ngày liên tiếp.
- Tuần 1 chỉ dùng các loại content có độ khó "Dễ" — tăng dần từ tuần 2.
- Trình bày dạng bảng, chia làm 4 tuần.

[Output]
Phiên bản A — [tóm tắt đặc điểm, 2–3 dòng]
  Lịch tuần mẫu: | Ngày | Loại content | Kênh | Gợi ý chủ đề |

Phiên bản B — [tóm tắt đặc điểm, 2–3 dòng]
  Lịch tuần mẫu: | Ngày | Loại content | Kênh | Gợi ý chủ đề |

─── [Tôi chọn Phiên bản: ___ ] ───

Lịch 30 ngày (phiên bản đã chọn), chia theo tuần:

  Tuần 1 — [Tên chủ đề tuần]
  | Ngày | Loại content | Kênh | Gợi ý chủ đề |
  |------|-------------|------|--------------|
  | Thứ Hai | ... | ... | ... |
  | ...

  (lặp lại cho Tuần 2, 3, 4)

Tổng kết cuối bảng:
  - Tổng số bài/tháng
  - Phân bổ theo loại content (%)
  - Phân bổ theo kênh (%)

[Evaluation]
- Tốt nếu 2 phiên bản A/B khác biệt rõ ràng về mức độ yêu cầu — 
  không chỉ là "ngắn hơn/dài hơn".
- Tốt nếu lịch 30 ngày có thể in ra và dùng ngay mà không cần 
  chỉnh sửa thêm.
- Tốt nếu tuần 1 đủ nhẹ để Leader mới bắt đầu không bỏ cuộc.
- Tốt nếu có sự đa dạng — không có tuần nào toàn 1 loại content.
- Kém nếu lịch dày đặc đến mức Leader tự làm một mình không thể 
  duy trì.
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
[Role] Chuyên gia thiết kế quy trình content cho cá nhân và doanh nghiệp nhỏ trong lĩnh vực MLM/Đại lý mạng lưới.

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

### Tiêu chí tự chấm Prompt Stack V2 (rubric gợi ý)

| Tiêu chí              | Mô tả                                                                                                           | Điểm (0–5) |
|-----------------------|-----------------------------------------------------------------------------------------------------------------|-----------|
| Alignment với Brief   | Stack bám sát output "Workflow tái chế bài giảng", đúng audience Leader tự chủ không trợ lý                    | 4/5        |
| Cấu trúc RTC-COE      | Mỗi prompt có Role, Task, Context, Constraints, Output rõ ràng                                                  | 5/5        |
| Tách phase hợp lý     | P1 kiểm kê kho → P2 bóc tách luồng → P3 SOP → P4 phản biện → P5 template — không lặp task giữa các bước       | 4/5        |
| Tính SOP              | Cấu trúc Phần Chung + Luồng A/B đủ rõ để F1/F2 làm theo mà không cần hỏi Leader; checklist tự QC có ở mỗi luồng | 4/5        |
| Tính tái sử dụng      | Stack có thể áp dụng cho bất kỳ hệ thống nào cần tái chế "1 nội dung gốc → nhiều định dạng"                    | 4/5        |
| Chuẩn bị cho Buổi 3–4 | SOP và Template là dạng decomposition thực tế; cây 2 luồng từ P2 có thể dùng làm case study cho IA             | ?/5        |

---



## Prompt Stack V3 — Playbook Prompt mẫu cho Leader MLM/Đại lý

### Context (tóm tắt Framing Brief)

- **Topic**: Bộ prompt mẫu giúp Leader MLM/Đại lý dùng AI tạo content mà không cần biết viết prompt
- **Problem**: Leader không có hệ thống prompt — mỗi lần cần content lại phải nghĩ từ đầu, mất thời gian và output không nhất quán
- **Audience**: Leader/Boss hệ thống tự chủ hoàn toàn, không có trợ lý, cần công cụ dùng lại được
- **Scope**: 8 tình huống — viết caption lifestyle, caption tái chế bài giảng, post quan điểm nghề, story đội nhóm, trả lời inbox/bình luận, viết bio kênh, tạo ảnh minh họa, viết kịch bản video ngắn (< 1 phút 30 giây)
- **Output ưu tiên**: Cẩm nang 1 trang — toàn bộ prompt mẫu, tra cứu nhanh, in được

> **Lưu ý khi dùng**: Dùng chung Prompt 0 — Grounding Brief từ Stack 1.
> Sau khi nhận output Prompt 1, trả lời 5 câu hỏi làm rõ trước khi gửi Prompt 2.

---

### Prompt 1 — Làm rõ nhu cầu Playbook (Clarify)

*Task type chính: explain + diagnose*

```
[Role] Chuyên gia tư vấn thiết kế hệ thống prompt cho Leader 
MLM/Đại lý tự vận hành.

[Task]
1. Tóm tắt lại bài toán Playbook Prompt từ Framing Brief.
2. Liệt kê 5–7 giả định về cách Leader hiện đang viết prompt 
   (copy paste từ mạng, viết thủ công mỗi lần, không có hệ thống...).
3. Đề xuất 5 câu hỏi cần làm rõ về nhu cầu và thói quen 
   dùng prompt của Leader trước khi thiết kế Playbook.

[Context]
- Đây là bước làm rõ yêu cầu, chưa bước vào thiết kế prompt.
- Domain: Leader MLM/Đại lý, 8 tình huống đã xác định:
  viết caption lifestyle, caption tái chế bài giảng, post quan điểm 
  nghề, story đội nhóm, trả lời inbox/bình luận, viết bio kênh, 
  tạo ảnh minh họa, viết kịch bản video ngắn (< 1 phút 30 giây).
- Leader tự chủ hoàn toàn, không trợ lý.

[Constraints]
- Không thiết kế prompt mẫu ở bước này — chỉ làm rõ nhu cầu 
  và đặt câu hỏi.
- Ngôn ngữ đơn giản, tránh thuật ngữ kỹ thuật AI.
- Giả định và câu hỏi phải phản ánh đúng thực tế người tự làm 
  một mình, không rành viết prompt.
- Trình bày dạng đầu mục + gạch đầu dòng.

[Output]
1. Tóm tắt bài toán Playbook (3–5 câu)
2. Danh sách "Giả định hiện tại" (5–7 giả định)
3. Danh sách "Câu hỏi cần làm rõ" (5 câu hỏi)

[Evaluation]
- Tốt nếu giả định phản ánh đúng thực tế Leader chưa có hệ 
  thống prompt, không giả định đã thành thạo.
- Tốt nếu câu hỏi giúp phát hiện điểm tắc nghẽn thực tế 
  (tình huống hay gặp nhất, loại output cần nhất, thời gian sẵn sàng).
- Tốt nếu không có câu hỏi thừa hoặc quá hiển nhiên.
- Kém nếu lệch sang domain kinh doanh truyền thống.
- Kém nếu dùng thuật ngữ kỹ thuật AI mà Leader không hiểu.
```

---

### Prompt 2 — Bóc tách tình huống & biến số (Structure)

*Task type chính: design (extract & structure)*

```
[Role] Người sắp xếp tri thức chuyên phân loại tình huống sử 
dụng prompt cho Leader MLM/Đại lý mạng lưới.

[Task]
- Dựa trên kết quả làm rõ từ Prompt 1.
- Phân loại 8 tình huống thành 3–4 nhóm lớn theo mục đích.
- Với mỗi tình huống, xác định rõ:
  - Đầu vào cần có (Leader phải cung cấp gì trước khi dùng prompt)
  - Đầu ra mong muốn (output AI cần tạo ra)
  - Biến số cần điền (tối đa 3 biến/tình huống)

[Context]
- Dựa trên kết quả từ Prompt 1 (giả định, câu hỏi đã làm rõ).
- 8 tình huống: viết caption lifestyle, caption tái chế bài giảng, 
  post quan điểm nghề, story đội nhóm, trả lời inbox/bình luận, 
  viết bio kênh, tạo ảnh minh họa, viết kịch bản video ngắn 
  (< 1 phút 30 giây).
- Leader tự chủ, không trợ lý — biến số phải đơn giản, 
  dễ điền.

[Constraints]
- Không thêm tình huống ngoài 8 cái đã xác định.
- Tối đa 3–4 nhóm lớn — các nhóm không chồng chéo về mục đích.
- Mỗi biến số phải đặt tên đơn giản, dễ hiểu 
  (ví dụ: [TÊN SẢN PHẨM], [KẾT QUẢ CỤ THỂ], [TÊN THÀNH VIÊN]).
- Trình bày dạng cây phân cấp, tách rõ từng nhóm.

[Output]
- Cây phân cấp:
  Nhóm A: [Tên nhóm — mục đích]
    Tình huống 1:
      - Đầu vào: ...
      - Đầu ra: ...
      - Biến số: [BIẾN 1], [BIẾN 2], [BIẾN 3]
    Tình huống 2: ...
  Nhóm B: ...

[Evaluation]
- Tốt nếu 3–4 nhóm có mục đích khác biệt rõ ràng, không chồng chéo.
- Tốt nếu biến số đặt tên dễ hiểu, Leader điền được ngay.
- Tốt nếu đầu vào/đầu ra phản ánh đúng thực tế từng tình huống.
- Kém nếu có tình huống nào thiếu biến số hoặc biến số quá phức tạp.
- Kém nếu lệch sang domain kinh doanh truyền thống.
```

---

### Prompt 3 — Viết prompt template (Refine)

*Task type chính: refine + design*

```
[Role] Chuyên gia viết prompt template có thể chuyển giao cho 
Leader MLM/Đại lý tự vận hành.

[Task]
1. Từ cây phân cấp ở Prompt 2, viết prompt template cho 
   từng tình huống.
2. Mỗi template bao gồm:
   - Tên tình huống (ngắn gọn 2–4 từ)
   - Prompt mẫu với [BIẾN] được đánh dấu rõ
   - Gợi ý điền [BIẾN] (ví dụ cụ thể trong domain MLM/Đại lý)
   - Ví dụ prompt đã điền hoàn chỉnh

[Context]
- Dựa trên cây phân cấp từ Prompt 2.
- Leader không rành viết prompt — template phải đủ đơn giản 
  để điền [BIẾN] vào là dùng được ngay.
- Mục tiêu: Leader dùng được mà không cần hiểu cách hoạt 
  động của AI.

[Constraints]
- Mỗi prompt tối đa 100 từ — ngắn gọn, không lan man.
- Tối đa 3 biến số mỗi prompt.
- Mỗi [BIẾN] phải có gợi ý ví dụ ngay bên cạnh 
  (ví dụ: [TÊN THÀNH VIÊN — ví dụ: "chị Lan"]).
- Không dùng thuật ngữ kỹ thuật AI trong prompt.
- Ngôn ngữ tự nhiên, giống cách Leader nói chuyện thật.

[Output]
- Bảng prompt template:
  | Tình huống | Prompt mẫu (có [BIẾN]) | Gợi ý điền | Ví dụ đã điền | Đầu ra kỳ vọng |

[Evaluation]
- Tốt nếu Leader điền [BIẾN] vào là ra content dùng được ngay.
- Tốt nếu ví dụ đã điền phản ánh đúng domain MLM/Đại lý, 
  không chung chung.
- Kém nếu có biến số nào khó hiểu hoặc không biết điền gì.
- Kém nếu prompt dài quá 100 từ sau khi điền biến.
- Kém nếu quy trình chỉ phù hợp với 1 người — người mới 
  bắt đầu phải dùng được.
```

---

### Prompt 4 — Phản biện & Kiểm định Playbook (Critique)

*Task type chính: critique*

```
[Role] Chuyên gia QC hệ thống prompt cho cá nhân tự chủ 
trong lĩnh vực MLM/Đại lý mạng lưới.

[Task]
1. Chỉ ra 2–3 điểm mạnh của bộ prompt template (về tính 
   đơn giản, tính dùng lại, tính domain-specific).
2. Chỉ ra ít nhất 5 điểm yếu/lỗ hổng, bao gồm:
   - Prompt nào dễ ra output chung chung không dùng được
   - Biến số nào khó điền với người không rành domain MLM
   - Tình huống nào thiếu ví dụ cụ thể hoặc ví dụ không sát thực tế
   - Prompt nào dễ gây bỏ cuộc nhất — và lý do cụ thể tại sao
   - Chỗ nào Playbook chưa đủ phổ quát để người mới dùng được
3. Đề xuất 2 phiên bản:
   - Phiên bản A: bộ prompt tối giản (3–4 tình huống cốt lõi) 
     cho Leader mới bắt đầu
   - Phiên bản B: bộ prompt đầy đủ (cả 8 tình huống) cho 
     Leader đã quen dùng AI

[Context]
- Dựa trên bảng prompt template từ Prompt 3.
- Leader tự chủ, không trợ lý, không rành kỹ thuật AI.
- Playbook cần chuyển giao được cho F1/F2.
- Domain: MLM/Đại lý mạng lưới/Bán hàng trực tiếp.

[Constraints]
- Tập trung vào tính khả thi thực tế, không phê bình lý thuyết.
- Nếu chỗ nào chưa tốt phải giải thích cụ thể lý do và đưa 
  gợi ý cải thiện luôn.
- Không viết lại toàn bộ Playbook — chỉ chỉ ra vùng cần 
  điều chỉnh.
- Trình bày dạng đầu mục + gạch đầu dòng.

[Output]
1. Điểm mạnh (2–3 điểm)
2. Điểm yếu/lỗ hổng (ít nhất 5 điểm + gợi ý cải thiện cụ thể)
3. Bảng rủi ro prompt:
   - Tình huống | Rủi ro output kém | Mức độ | Cách phòng tránh
4. Bảng chấm điểm Playbook theo tiêu chí:
   - Tính đơn giản | Tính dùng lại | Domain-specific | 
     Dễ chuyển giao cho F1/F2
5. Phiên bản A — tối giản (3–4 tình huống cốt lõi)
6. Phiên bản B — đầy đủ (cả 8 tình huống)

[Evaluation]
- Tốt nếu điểm yếu nêu cụ thể, có dẫn chứng từ prompt 
  template, không nói chung chung.
- Tốt nếu 2 phiên bản A/B có thể triển khai ngay mà không 
  cần hỏi thêm.
- Tốt nếu bảng rủi ro thực tế với domain MLM/Đại lý.
- Kém nếu phê bình chung chung mà không có gợi ý cải thiện.
- Kém nếu Playbook chỉ phù hợp với 1 người — người mới 
  bắt đầu phải dùng được.
```

---

### Prompt 5 — Cẩm nang 1 trang (Design)

*Task type chính: design + synthesize*

```
[Role] Template designer chuyên thiết kế tài liệu tham khảo 
nhanh cho Leader MLM/Đại lý tự vận hành.

[Task]
1. Đóng gói toàn bộ prompt template thành Cẩm nang 1 trang 
   dạng bảng tra cứu nhanh.
2. Bố cục theo nhóm tình huống từ Prompt 2.
3. Mỗi ô trong bảng gồm:
   - Tên tình huống
   - Prompt mẫu rút gọn (có [BIẾN] được đánh dấu)
   - 1 gợi ý điền [BIẾN] ngắn

[Context]
- Dựa trên bảng prompt template (Prompt 3) và phiên bản A/B 
  (Prompt 4).
- Mục tiêu: Leader mở Cẩm nang ra là tìm được prompt cần 
  dùng trong 30 giây, không cần đọc toàn bộ.
- Dùng được cả khi in ra hoặc lưu trên điện thoại.

[Constraints]
- Toàn bộ nội dung phải vừa 1 trang A4 hoặc 1 màn hình 
  điện thoại (khi phóng to vừa đủ đọc).
- Mỗi ô prompt không quá 3 dòng.
- Sắp xếp theo nhóm mục đích — không sắp xếp ngẫu nhiên.
- Font/bố cục phải in được rõ ràng, không cần màu sắc 
  phức tạp.
- Cuối trang có ô ghi chú trống để Leader tự thêm prompt 
  của riêng mình.

[Output]
CẨM NANG PROMPT — Leader MLM/Đại lý
(1 trang A4 — bảng tra cứu nhanh)

┌─────────────────────────────────────────┐
│ NHÓM A: [Tên nhóm]                      │
├──────────────┬──────────────────────────┤
│ Tình huống 1 │ Prompt: ...              │
│              │ Điền: [BIẾN] = ví dụ... │
├──────────────┼──────────────────────────┤
│ Tình huống 2 │ ...                      │
└──────────────┴──────────────────────────┘

[lặp lại cho các nhóm B, C, D]

┌─────────────────────────────────────────┐
│ GHI CHÚ — Prompt của tôi:               │
│ ___________________________________     │
└─────────────────────────────────────────┘

[Evaluation]
- Tốt nếu Leader tìm được prompt cần dùng trong 30 giây 
  mà không cần đọc toàn bộ.
- Tốt nếu bố cục in ra rõ ràng trên A4, không bị chật chội.
- Tốt nếu ô ghi chú giúp Leader cá nhân hóa Playbook 
  theo thời gian.
- Kém nếu prompt nào thiếu gợi ý điền [BIẾN].
- Kém nếu bố cục không in được vừa 1 trang A4.
- Kém nếu không có ô ghi chú để Leader tự thêm vào.
```

### Tiêu chí tự chấm Prompt Stack V3 (rubric gợi ý)

| Tiêu chí              | Mô tả                                                                                                      | Điểm (0–5) |
|-----------------------|------------------------------------------------------------------------------------------------------------|-----------|
| Alignment với Brief   | Stack bám sát output "Playbook Prompt mẫu", 8 tình huống đúng domain MLM/Đại lý trong Framing Brief       | 4/5        |
| Cấu trúc RTC-COE      | Mỗi prompt có Role, Task, Context, Constraints, Output rõ ràng                                             | 5/5        |
| Tách phase hợp lý     | P1 clarify → P2 phân nhóm + biến số → P3 viết template → P4 phản biện → P5 Cẩm nang — mỗi phase khác nhiệm vụ | 5/5        |
| Tính domain-specific  | Template prompt gắn chặt với domain MLM/Đại lý — [BIẾN] được đặt tên theo ngữ cảnh thực chiến             | 4/5        |
| Tính tái sử dụng      | Cấu trúc [BIẾN] giúp Leader dùng lại prompt không cần viết từ đầu; Cẩm nang có thể chuyển giao cho F1/F2  | 5/5        |
| Chuẩn bị cho Buổi 3–4 | Cẩm nang 1 trang là artifact có thể phân tích theo IA; cây phân nhóm ở P2 là dạng decomposition thực tế   | ?/5        |

---