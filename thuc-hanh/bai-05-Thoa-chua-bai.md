# Dùng các prompt nâng cao để khai thác assignment bài 5

> PROMPT 1
```text
Giải thích ngắn gọn bằng 3 gạch đầu dòng xem bạn hiểu OUTPUT của file này là gì? 
Phản biện cho từng gạch đầu dòng đó theo hướng:

* Điểm tốt = ? %
* Điểm yếu = ? %
* Bổ sung gì.
```
## OUTPUT
**File này là kết quả của một quy trình nghiên cứu có cấu trúc**, không phải là chương trình học hè thật — nó là bản thiết kế *cách tiếp cận* để tạo ra chương trình đó.


### OUTPUT 1: Một bản đồ tư duy phân loại nội dung (Exploration Map + Keyword Matrix + Facet Matrix)
Xác định cái gì Core, Near, Extended, Out-of-scope — và từ khóa nào dùng để đi tìm tài liệu tiếp theo.

- Điểm tốt: **70%** — Phân loại rõ ràng, có lý do, có sanity check, tránh được bẫy "ôm quá nhiều".
- Điểm yếu: **30%** — Vẫn mang tính lý thuyết, chưa kiểm chứng bằng thực tế. Ví dụ: phân loại "kỹ thuật dựng video = Extended" nhưng nếu con lớp 6 hứng thú với clip thì có thể cần nâng lên sớm hơn dự kiến.
- Bổ sung: Nên có một vòng hỏi nhanh hai con xem chúng thích/sợ hoạt động nào trước khi chốt Core.

### OUTPUT 2: Một khung nghiên cứu 3 pha (Research Path v1)
Pha 1 quét rộng → Pha 2 chọn node → Pha 3 đào sâu thành deliverable thật. Có checkpoint và tiêu chí pivot rõ ràng.

- Điểm tốt: **65%** — Có logic rõ, tránh sa đà, biết khi nào dừng và đổi hướng.
- Điểm yếu: **35%** — Checkpoint A và B đặt câu hỏi hay nhưng *không có câu trả lời* — tức là vẫn đang hỏi, chưa thực sự kiểm tra. Đây vẫn là kế hoạch nghiên cứu, chưa phải kết quả nghiên cứu.
- Bổ sung: Mỗi checkpoint cần ghi thêm "đã làm gì và kết quả là gì" thay vì chỉ liệt kê câu hỏi sẽ hỏi.

### OUTPUT 3: Một danh sách deliverable tương lai (chưa hoàn thành)
Cuối Pha 3 có hứa hẹn: khung 24 buổi, template buổi học, bộ prompt AI cho mẹ, checklist phản hồi, dự án cuối khóa — nhưng tất cả vẫn ở dạng *mô tả sẽ làm*, không phải nội dung thật.

- Điểm tốt: **50%** — Biết mình cần gì, deliverable được gắn rõ với node nghiên cứu nào tạo ra nó.
- Điểm yếu: **50%** — File kết thúc đúng lúc chuẩn bị bước vào phần có giá trị nhất. Người đọc không dùng được gì ngay lập tức.
- Bổ sung: Cần ít nhất một buổi học mẫu hoàn chỉnh làm "nguyên mẫu" để kiểm tra toàn bộ khung trước khi triển khai 24 buổi.

---

> PROMPT 2
```text
CoT lại file ban đầu
Bản chất file này là định hướng nghiên cứu, không phải là một kế hoạch sản xuất nên không có đầu ra cụ thể.
Tuy nhiên điểm mơ hồ ở OUTPUT số 3 cần được định hình lại ra sao theo hướng ITTO
I = Input 
T = Technique
T = Transition
O = Output

Từ đó OUTCOME rõ ràng hơn. 
Trả lời ITTO dạng bảng
Cung cấp thêm SWOT của OUTCOME
Làm rõ những develiries dành cho đối tượng người sử dụng.
```

## OUTPUT
## CoT — Định vị lại bản chất file

File này là **Research Design Document**, không phải Production Plan. Mục đích đúng của nó là: *biết cần nghiên cứu gì, theo thứ tự nào, dừng ở đâu.* Việc không có đầu ra cụ thể là đúng bản chất — nhưng OUTPUT 3 bị mơ hồ vì nó **liệt kê deliverable như thể đã xong**, trong khi thực ra chỉ là đích đến của Pha 3.

Định hình lại theo ITTO giúp làm rõ: deliverable đó *đến từ đâu, qua bước nào, và trông như thế nào khi hoàn thành.*

---

## ITTO — OUTPUT 3 được định hình lại

| | Nội dung |
|---|---|
| **INPUT** | • Exploration Map đã sanity check (Core/Near/Extended) |
| | • Keyword Shortlist 13 term |
| | • Facet Matrix 7 góc nhìn |
| | • Node Prioritization Table (5 node, điểm 4 tiêu chí) |
| | • Adjacent-domain Map |
| | • Bộ nguyên tắc dùng AI ban đầu với con |
| **TECHNIQUE** | • Quick-scan 5 node → chấm điểm Centrality / Dependency / Applicability / Confusion risk |
| | • Đào sâu 3 node flagship: khung chương trình, phân hóa độ tuổi, quy trình AI |
| | • Template hóa từng buổi học theo cấu trúc cố định |
| | • Differentiated task design: cùng chủ đề, hai mức nhiệm vụ |
| | • Prompt engineering cho phụ huynh không chuyên |
| **TRANSITION** | • Từ nghiên cứu → bản nháp khung 8 tuần |
| | • Từ bản nháp → chạy thử 1 buổi mẫu |
| | • Từ buổi mẫu → điều chỉnh → nhân ra 24 buổi |
| **OUTPUT** | • Khung lịch 8 tuần / 24 buổi có chủ đề từng tuần |
| | • Template buổi học: mục tiêu, vật quan sát, câu hỏi gợi mở, nhiệm vụ lớp 2, nhiệm vụ lớp 6, sản phẩm đầu ra |
| | • Bộ prompt AI cho mẹ (trước / trong / sau buổi học) |
| | • Checklist phản hồi tích cực không chấm điểm |
| | • Kế hoạch dự án cuối khóa "Mùa hè em quan sát Việt Nam" |

---

## OUTCOME

> Mẹ có thể mở file vào tối hôm trước, đọc template 5 phút, dùng 1–2 prompt AI để chuẩn bị, rồi dạy buổi hôm sau mà không cần soạn từ đầu — hai con có nhiệm vụ phù hợp độ tuổi và có sản phẩm cụ thể sau mỗi buổi.

---

## SWOT của OUTCOME

| | Nội dung |
|---|---|
| **Strengths** | Cấu trúc rõ, mẹ bận vẫn dùng được. Phân hóa lớp 2 / lớp 6 tránh bé quá dễ, bé quá khó. Prompt AI giúp tiết kiệm thời gian chuẩn bị. Sản phẩm thật sau mỗi buổi tạo động lực cho con. |
| **Weaknesses** | Chưa có buổi mẫu thật để kiểm chứng template. Prompt AI chưa được test với đối tượng mẹ không rành AI. Checklist phản hồi chưa biết có phù hợp văn hóa gia đình Việt không. |
| **Opportunities** | Có thể scale thành tài liệu dùng cho nhiều gia đình tương tự. Dễ điều chỉnh chủ đề (không chỉ thiên nhiên Việt Nam). Dự án cuối khóa có thể thành kỷ niệm gia đình thật sự. |
| **Threats** | Mẹ mất động lực nếu 2–3 buổi đầu con không phản hồi tốt. Hai con chênh lệch độ tuổi có thể tạo cạnh tranh thay vì hợp tác. AI có thể bị dùng sai hướng — làm thay con thay vì hỗ trợ mẹ. |

---

## Deliveries làm rõ theo đối tượng người dùng

| Đối tượng | Họ cần gì | Delivery cụ thể |
|---|---|---|
| **Mẹ (người triển khai)** | Dùng nhanh, không cần đọc dài, không cần hiểu sâu lý thuyết | Template buổi học 1 trang. Bộ 4–5 prompt AI copy-paste được. Checklist chuẩn bị tối hôm trước. |
| **Con lớp 2** | Nhiệm vụ rõ, cụ thể, có thể làm ngay, không đọc nhiều | Thẻ nhiệm vụ: "Em vẽ lại 1 chiếc lá em thấy hôm nay và nói 2 điều em để ý." |
| **Con lớp 6** | Thách thức vừa đủ, có không gian tự quyết, không bị coi là "học hè bình thường" | Nhiệm vụ mở hơn: "Viết đoạn mô tả 5 câu + quay clip 30 giây giới thiệu như một nhà khoa học nhí." |
| **Cả hai con (chung)** | Thấy mình đang làm dự án thật, không phải bị kiểm tra | Dự án cuối khóa có tên, có sản phẩm trưng bày, mẹ đóng vai "khán giả" không phải "giám khảo". |
