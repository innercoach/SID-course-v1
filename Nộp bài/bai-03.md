# Trắc nghiệm

1-B Bóc chủ đề lớn thành bản đồ tri thức nhiều tầng, rõ khối lớn/khối nhỏ  
2-B Không có bức tranh toàn bộ, khó thấy đâu là khối lớn, đâu là chi tiết  
3-C Không có cách chia duy nhất đúng; quan trọng là phù hợp với bài toán & audience  
4-B Cố gắng “không trùng lớn, không thủng lớn” giữa các phần  
5-C Một “khối” trong cây tri thức (nhánh, lá, cụm nội dung)  
6-C Chia từ tổng quan → miền chính → nhóm con → node cụ thể  
7-B Các chức năng/khâu trong hệ theo dòng thời gian hoặc pipeline  
8-B “Chủ đề này trông thế nào từ góc nhìn mỗi bên liên quan?”  
9-A Giảng viên, sinh viên, khoa/bộ môn, ban giám hiệu,… 
10-B Khái niệm nền, khái niệm trung gian, ứng dụng  
11-C 3–7 miền chính, có cùng tiêu chí chia  
12-B Chia theo cảm tính, node cùng cấp nhưng bản chất khác nhau (khái niệm lẫn quy trình, lỗi, công cụ)  
13-B Các node cấp 1 phải thuộc cùng loại (vd: đều là nhóm năng lực, không trộn chức năng/lỗi) 
14-A Hai node khác tên nhưng đề cập cùng một nội dung/vai trò  
15-B Nhìn vào cây, bạn có thể dạy 4–5 buổi logic theo thứ tự được không  
16-B Thiết kế workflow, thiết kế assistant/agent  
17-C Xác định “quy trình” trung tâm cần phân tích (input → output)  
18-C. Bổ sung sub-function để làm rõ các khâu nhỏ bên trong một chức năng  
19-B. Nó giúp nối decomposition với thao tác cụ thể, workflow thực tế  
20-B. Dòng bước/bullet từ 1 → n, có thể kèm sub-function (1.1, 1.2, …)  
21-B. Kỳ vọng gì, sợ điều gì, cần năng lực/tri thức gì, dùng AI vào việc gì  
22-A. Cây tri thức nhiều tầng  
23-B. Stakeholder  
24-B. Giúp thiết kế module, content, ưu tiên khác nhau cho từng vai trò  
25-B. Ít nhất 3 miền chính, tổng số node ≥ 20  
26-B. Có 3–4 tầng tổng, tránh lẫn lộn khái niệm/quy trình/lỗi trên cùng 1 cấp  
27-B. Chọn 1 workflow thực, liệt kê các chức năng từ input → output, có thể bóc sub-function  
28-B. Một đoạn 150–250 từ giải thích tiêu chí cấp 1 và cách dùng cây này (syllabus/assistant/khóa học)  
29-B. Map có phản ánh thực tế, giúp hiểu system/people hơn không  
30-B. Một bản đồ tri thức đầu tiên cho domain, gồm phía nội dung (cây) và phía vận hành/con người (functional/stakeholder)  

## 7. Bài tập tự học Buổi 3

### 7.1. Bài tập 1 — Decomposition Tree 3–4 tầng

**Mục tiêu**  
Bóc domain của bạn thành cây nhiều tầng dễ dạy, dễ dùng.

---

**Bước 1 — Bảng khung thành phần từ Prompt Stack V1 (Buổi 2)**

| Loại nội dung         | Mô tả                                                    | Ví dụ (MLM/Đại lý)                                                   | Mục đích                                     | Tần suất      | Kênh                           | Độ khó     | Hành động ngay (<30')                                                  |
| --------------------- | -------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------- | ------------- | ------------------------------ | ---------- | ---------------------------------------------------------------------- |
| Cơ hội kinh doanh     | Giới thiệu mô hình thu nhập, cơ hội gia nhập đội nhóm    | Video 60s "Tại sao tôi chọn MLM sau 5 năm làm 3-4 việc đến kiệt sức" | Tuyển F1 mới                                 | 1–2 lần/tuần  | TikTok, Facebook Reels         | Thấp       | Mở camera, kể story 3 câu: Trước – Sau – Kêu gọi                       |
| Câu chuyện tuyến dưới | Testimonial thật từ F1/F2 đạt kết quả                    | "F1 của tôi đạt rank Silver tháng thứ 2" + screenshot thu nhập       | Social proof, tuyển dụng                     | 2–4 lần/tháng | Facebook, TikTok               | Thấp       | Nhắn tin xin phép F1, chụp màn hình kế quả đạt được, viết caption ngắn |
| Đào tạo tuyến dưới    | Bài giảng ngắn về kỹ năng khởi nghiệp cho F1 mới         | "3 bước đầu tiên sau khi ký hợp đồng đại lý"                         | Giữ chân & nâng cấp F1                       | 1 lần/tuần    | Facebook Group, YouTube Shorts | Trung bình | Dùng lại nội dung đã dạy trong Zoom, quay lại bằng điện thoại          |
| Uy tín & Quan điểm    | Chia sẻ góc nhìn về ngành, phản bác hiểu lầm             | "Sự thật về MLM mà không ai nói với bạn"                             | Brand building, lọc audience                 | 1 lần/tuần    | TikTok, Facebook cá nhân       | Trung bình | Chọn 1 câu hỏi/hiểu lầm hay gặp, trả lời thẳng trong 3 đoạn            |
| Review sản phẩm       | Trải nghiệm thực của Leader hoặc khách hàng              | "Dùng sản phẩm X 30 ngày - kết quả thật sự là…"                      | Bán hàng, tạo tin tưởng                      | 2 lần/tháng   | TikTok, Facebook               | Thấp       | Selfie với sản phẩm + kể 1 thay đổi cụ thể đã trải qua                 |
| Tái chế nội dung      | Biến bài giảng Zoom / câu hỏi group → clip/bài đăng ngắn | Lấy 3 phút hay nhất từ buổi Zoom → cắt đăng TikTok                   | Duy trì consistency không tốn thêm thời gian | 3-4 lần/tuần  | TikTok, Facebook Reels         | Rất thấp   | Xem lại recording Zoom, clip đoạn hay nhất, đăng ngay                  |
| Cột mốc & Hành trình  | Cột mốc cá nhân, rank mới, kỷ niệm đáng nhớ              | "Hôm nay tôi đạt Diamond - đây là điều tôi học được"                 | Brand authenticity, truyền cảm hứng          | 1 lần/tháng   | Facebook, TikTok               | Thấp       | Chụp hình lúc nhận phần thưởng, viết 3 bài học thật sự học được        |

---

**Bước 2 — Tiêu chí cấp 1**: Mục đích của nội dung (Tuyển dụng / Đào tạo / Brand / Bán hàng)

**Bước 3**: Vẽ cây 3–4 tầng dạng markdown:

```markdown
**Hệ thống Content cho Leader MLM/Đại lý — dùng AI hỗ trợ**

  1. [Nội dung Cơ hội Kinh doanh & Câu chuyện Tuyến dưới]
     1.1. Giới thiệu cơ hội kinh doanh
        1.1.1. Video 60s kể story cá nhân
        1.1.2. Bài viết so sánh "Trước – Sau khi gia nhập"
     1.2. Testimonial tuyến dưới (F1/F2)
        1.2.1. Screenshot thu nhập thực tế
        1.2.2. Video ngắn F1 chia sẻ cảm nhận
     1.3. Nội dung tái chế từ buổi Zoom chia sẻ cơ hội kinh doanh
        1.3.1. Highlight 3 phút hay nhất
        1.3.2. Q&A thường gặp sau buổi

  2. [Nội dung Đào tạo Tuyến dưới]
     2.1. Hướng dẫn khởi đầu cho F1 mới
        2.1.1. Checklist 30 ngày đầu
        2.1.2. Mô hình trả thưởng & thành tích /cấp độ
     2.2. Nội dung tái chế từ buổi đào tạo
        2.2.1. Cắt clip Zoom → TikTok/Reels
        2.2.2. Câu hỏi người tham dự → bài đăng FAQ

  3. [Nội dung Uy tín & Quan điểm]
     3.1. Uy tín & Quan điểm ngành
        3.1.1. Phản bác hiểu lầm về MLM
        3.1.2. Chia sẻ bài học thất bại/thành công
     3.2. Hành trình & Cột mốc Leader
        3.2.1. Cột mốc danh hiệu mới đạt được
        3.2.2. Behind-the-scenes ngày làm việc

  4. [Nội dung Sản phẩm]
     4.1. Review sản phẩm thực tế
        4.1.1. Trải nghiệm cá nhân 30 ngày
        4.1.2. Case study khách hàng
     4.2. Giải đáp Objection
        4.2.1. FAQ cho sản phẩm phổ biến
        4.2.2. So sánh với giải pháp thay thế khác có trên thị trường
```

---

### 7.2. Bài tập 2 — Functional Map & Stakeholder Map

#### A. Functional Map

**Workflow 1 — Tuyến Đào tạo**: Dùng AI tái chế bài giảng Zoom → Content TikTok/Facebook

> **Scope**: Workflow này phục vụ riêng tuyến *Đào tạo tuyến dưới* (node 2 trong Decomposition Tree). Các tuyến Uy tín & Quan điểm và Sản phẩm áp dụng quy trình tương tự, thay Input bằng nguồn nội dung tương ứng.

```markdown
Workflow 1: Tái chế bài giảng Zoom nội bộ → Content đào tạo tuyến dưới

Input: Recording buổi Zoom đào tạo nội bộ (60–90 phút)

1. [Transcript & tóm tắt]
   1.1. Dùng AI transcribe recording → văn bản thô
   1.2. Dùng AI tóm tắt → 5–7 key points chính của buổi
   1.3. Sắp xếp key point theo thứ tự giá trị

2. [Bóc content từ key point]
   2.1. Chọn 1 key point
   2.2. Dùng AI viết hook + 3 ý chính + CTA cho TikTok (60s-90s)
   2.3. Dùng AI viết bài Facebook dài hơn từ cùng key point đó
   2.4. Lặp lại cho các key point khác

3. [Chuẩn hóa giọng văn]
   3.1. Paste draft vào AI đã được train phong cách viết cá nhân, yêu cầu viết lại theo giọng Leader (thân mật, không spam)
   3.2. Kiểm tra: không dùng từ lách luật quảng cáo, không hứa hẹn thu nhập cụ thể
   3.3. Đối chiếu với tài liệu quy chuẩn sử dụng Mạng xã hội của công ty để tránh các lỗi có thể mắc phải

4. [Sản xuất material]
   4.1. Dùng AI để tạo hình ảnh đăng kèm trên Facebook
   4.2. Dùng AI để tạo video ngắn 60-90s đã lên ở phần 2.2

5. [Lên lịch & đăng]
   5.1. Chọn khung giờ đăng phù hợp với audience (TikTok: tối 20–22h)
   5.2. Đăng TikTok trước, cross-post Facebook sau 24h

Output: 1 clip TikTok + 1 bài Facebook từ 1 buổi Zoom, tổng thời gian tự làm < 30 phút
```

---

**Workflow 2 — Tuyến Tuyển dụng**: Dùng AI biến story cá nhân / testimonial → Content tuyển F1

```markdown
Workflow 2: Story cá nhân / Testimonial F1 → Content tuyển dụng

Input: Story thật của Leader hoặc F1/F2 đạt kết quả (kể miệng hoặc ghi chú thô)

1. [Thu thập & làm rõ câu chuyện]
   1.1. Leader kể lại story theo khung: Trước – Bước ngoặt – Sau – Bài học
   1.2. Nếu là testimonial F1: nhắn tin xin phép, hỏi 3 câu (Trước khi gia nhập bạn thế nào? Bước ngoặt là gì? Kết quả hiện tại?)
   1.3. Ghi chú thô hoặc voice note → paste vào AI để làm sạch

2. [Bóc content từ story]
   2.1. Dùng AI viết caption Facebook dạng storytelling (300–500 chữ)
   2.2. Dùng AI viết script TikTok 60s từ cùng story (hook mạnh + 3 điểm chính + CTA)
   2.3. Dùng AI tạo dạng Q&A ngắn để đăng story Instagram/Facebook

3. [Chuẩn hóa & kiểm tra]
   3.1. Kiểm tra không hứa hẹn thu nhập cụ thể, không dùng từ bị hạn chế quảng cáo
   3.2. Xác nhận lại với F1 nếu dùng testimonial của họ trước khi đăng

4. [Sản xuất & đăng]
   4.1. Chụp ảnh / quay video ngắn minh họa (screenshot kết quả, ảnh nhận thưởng)
   4.2. Đăng Facebook trước (audience rộng hơn cho tuyển dụng), TikTok sau

Output: 1 bài Facebook storytelling + 1 script TikTok, tổng thời gian < 30 phút
```

#### B. Stakeholder Map

```markdown
Stakeholder 1 — Leader/Boss hệ thống (người dùng trực tiếp)
- Kỳ vọng: Có kênh TikTok/Facebook chuyên nghiệp, tuyển được F1 mới mà không tốn quá nhiều thời gian
- Sợ: Bị hiểu lầm là spam/lừa đảo; làm content sai luật quảng cáo, quy chuẩn của công ty; tốn công mà không ra đơn
- Cần: Hệ thống làm content nhanh, có thể dạy lại cho tuyến dưới
- Dùng AI để: Tái chế bài giảng, viết caption, tóm tắt Zoom, tạo FAQ từ câu hỏi trong group

Stakeholder 2 — Tuyến dưới (F1/F2 — không phân biệt cấp, cùng nhu cầu)
- Kỳ vọng: Được đào tạo nhanh, có thu nhập trong 30–60 ngày đầu
- Sợ: Không biết bắt đầu từ đâu, sợ bị từ chối khi tiếp cận khách hàng, sợ không làm được
- Cần: Checklist rõ ràng, tài liệu đào tạo đơn giản, mẫu bài đăng để bắt đầu
- Dùng AI để: Tập viết caption, chuẩn bị câu trả lời xử lý từ chối, hiểu sản phẩm nhanh hơn

Stakeholder 3 — Khách hàng tiềm năng mua hàng
- Kỳ vọng: Sản phẩm hiệu quả, giá hợp lý, mua dễ dàng không bị ép buộc
- Sợ: Mua phải hàng kém chất lượng, bị chèo kéo gia nhập hệ thống sau khi mua
- Cần: Review trung thực, thông tin rõ ràng về sản phẩm, quy trình mua đơn giản
- Dùng AI để: (Không trực tiếp — hưởng lợi từ content review sản phẩm & FAQ mà Leader tạo bằng AI)

Stakeholder 4 — Khách hàng tiềm năng tuyển dụng (muốn có thêm thu nhập, chưa gia nhập)
- Kỳ vọng: Cơ hội kiếm thêm thu nhập thật sự, không phải mô hình lừa đảo
- Sợ: Mất tiền đầu tư ban đầu, bị ép mua hàng, mất quan hệ bạn bè vì chào mời
- Cần: Bằng chứng thu nhập thực tế, giải thích mô hình minh bạch, lộ trình rõ ràng để bắt đầu
- Dùng AI để: (Không trực tiếp — hưởng lợi từ content storytelling & testimonial Leader tạo bằng AI)

Stakeholder 5 — Công ty (nhà phân phối / brand chủ)
- Kỳ vọng: Leader đại diện thương hiệu đúng chuẩn, tăng doanh số, mở rộng mạng lưới bền vững
- Sợ: Leader đăng content sai quy chuẩn gây kiện tụng, hứa hẹn thu nhập không thực tế, làm xấu hình ảnh thương hiệu
- Cần: Leader tuân thủ policy truyền thông, dùng đúng tên/logo/hình ảnh được phép
- Dùng AI để: (Gián tiếp — công ty hưởng lợi khi Leader dùng AI làm content đúng chuẩn, nhất quán)
```

## 8. Assignment Buổi 3 — Decomposition & Mapping cho domain của bạn
### 8.1. Đề bài
1. Xem mục 7.1
2. Xem mục 7.2-A
3. Giải thích:
- Vì sao tôi chọn tiêu chí như vậy cho cấp 1:

```markdown
1. Chọn [Mục đích của nội dung] làm tiêu chí vì:
- Việc tạo nội dung là việc mà Leader/tuyến dưới cần thực hiện mỗi ngày và có tác dụng rất lớn trong việc xây dựng hình ảnh, tuyển dụng, tìm kiếm khách hàng. Tuy nhiên đây lại không phải là năng lực mà họ có sẵn / làm tốt. Vì vậy nếu không xác định rõ nội dung tạo ra để làm gì thì sẽ dẫn đến việc bỏ làm hoặc làm xong mà không biết mình làm để làm gì. Đồng thời việc làm nội dung không có quy trình hiệu quả gây tốn rất nhiều thời gian, ví dụ 2 tiếng đồng hồ để ra 1 video 90s, đăng bài facbeook xong lại đi sửa vì không có ai tương tác,...
- Ngoài ra, nếu không có hệ nội dung nhất quán dễ dẫn đến đăng quá nhiều / quá ít hoặc quá loạn nội dung dẫn đến công sức bỏ ra không đạt kết quả.

2. [Tôi sẽ dùng cây này để]
    1. Syllabus khoá học nội bộ, mỗi node cấp 1 là 1 bài, các node nhỏ hơn là nội dung bài tập.
    2. Thiết kế AI Assistant cho Leader — mỗi node tương ứng với một nhóm Prompt Template trong Playbook Template; hoặc được tạo thành các Gem
```

### 8.2. Gợi ý rubric tự chấm

| Tiêu chí                   | Mô tả                                                                             | Điểm (0–5) |
| -------------------------- | --------------------------------------------------------------------------------- | ---------- |
| Logic cấp 1                | Các miền chính có cùng loại (VD: đều là nhóm năng lực, không trộn chức năng/lỗi)? | 5/5        |
| Độ đầy đủ (breadth)        | Cây có bao quát các phần quan trọng của domain?                                   | 5/5        |
| Độ rõ cấp 2–3              | Node cùng cấp có đồng đẳng? Ít trùng lặp?                                         | 5/5        |
| Functional/Stakeholder map | Map có phản ánh thực tế? Giúp hiểu system/people hơn không?                       | 5/5        |
| Tính dạy được              | Nhìn vào cây/map, bạn thấy dễ dạy, dễ giải thích hơn trước chưa?                  | 5/5        |
| Clarity tổng thể           | Tài liệu rõ ràng, đọc mạch lạc, dễ follow?                                        | 4/5        |

---