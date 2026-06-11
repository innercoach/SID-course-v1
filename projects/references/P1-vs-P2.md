# So sánh Project 1 và Project 2 theo khung SID

> P1 và P2 cùng dùng khung SID 9 bước, nhưng bản chất bài toán khác nhau hoàn toàn — một bên là chẩn đoán dưới bất định, một bên là sản xuất dưới áp lực sáng tạo. Sự khác biệt kỹ thuật xuất phát từ đó, không phải ngẫu nhiên.

---

## 1. Nền tảng bài toán

| Chiều so sánh | P1 — FruitTree Mentor | P2 — Family/Finance Content Engine |
|---|---|---|
| **Bản chất nhiệm vụ** | Chẩn đoán & tư vấn dưới bất định — sự thật chỉ có một nhưng dữ kiện thường thiếu | Sản xuất nội dung sáng tạo — không có "đáp án đúng", chỉ có quality & fit |
| **Người dùng của assistant** | Nông dân / người trồng cây ăn quả — trình độ kỹ thuật không đồng đều | Creator — người dùng cuối lại là khán giả kênh, tạo ra lớp "user kép" |
| **Rủi ro chính nếu sai** | Chẩn đoán sai → can thiệp sai → cây chết, mất tiền, ngộ độc hóa chất | Nội dung sai tone → blame/shame/sensationalism → tổn hại tâm lý khán giả |
| **Loại output** | Structured diagnosis report — ổn định, lặp lại được | Creative content layers — biến thiên theo channel, series, episode |

---

## 2. Kỹ thuật SID — mức độ áp dụng

Ký hiệu: **✓** = áp dụng rõ · **~** = có nhưng chưa là trọng tâm

| Buổi SID | P1 — FruitTree Mentor | P2 — Content Engine |
|---|---|---|
| **Buổi 1 — Framing** | ✓ Rất rõ — audience 1 lớp, scope cứng, rủi ro thiếu context được mã hóa vào behavior | ✓ Rất rõ — audience 2 lớp (creator + viewer), tone/boundaries là trọng tâm của brief |
| **Buổi 2 — Prompt Stack** | ✓ Stack theo phase chẩn đoán: Frame → Cause → Validate → Plan → Monitor | ✓ Stack theo tầng sản xuất: Channel → Series → Episode → Script → Tone review |
| **Buổi 3 — Decomposition** | ~ Trung bình — phân tầng domain (cây/đất/nước/dinh dưỡng) nhưng chủ yếu phục vụ diagnosis, không đi sâu cấu trúc | ✓ Mạnh hơn — decomposition theo chiều dọc: channel → series → episode → script skeleton — đây là xương sống của toàn bộ hệ thống |
| **Buổi 4 — Info Architecture** | ✓ Schema cứng: triệu chứng → nguyên nhân → kiểm tra → rationale + monitoring table | ✓ IA theo tầng nội dung: Channel Brief → Series Map → Episode Outline → Script Skeleton |
| **Buổi 5 — Expansion / Research Depth** | ~ Nhẹ — liệt kê 2–5 nguyên nhân khả dĩ, nhưng expansion là phụ — mục tiêu là thu hẹp về chẩn đoán đúng | ~ Nhẹ — mở nhiều series / góc nội dung, nhưng thiên về production workflow hơn là research depth thực sự |
| **Buổi 6 — Reasoning Design** | ✓ Rất mạnh — hypothesis-driven, causal reasoning, confidence labeling, fact/assumption/hypothesis/recommendation | ~ Trung bình — reasoning về message value và tone, nhưng không triển khai đa nhánh — logic sản xuất không cần CoT/ToT nặng |
| **Buổi 7 — Validation / Epistemic Control** | ✓ Rất mạnh — tầng epistemic tách bạch: 5 nhãn, confidence, prompt validation riêng, không kết luận khi thiếu dữ kiện | ✓ Validation thiên về tone & safety — checkpoint blame/shame/oversell, auto-review sau mỗi output |
| **Buổi 8 — Synthesis / Transfer** | ✓ TREE-Care + Monitoring — workflow tuần tự, học từ thực nghiệm, chuyển về nông dân | ✓ Mạnh hơn — framework EPISODE-Flow có thể tái dụng cho nhiều kênh, nhiều creator, nhiều domain |

---

## 3. Điểm phân kỳ cốt lõi

| Chiều so sánh | P1 | P2 |
|---|---|---|
| **Trục chủ đạo** | Epistemic discipline — kiểm soát độ chắc chắn trước khi hành động | Production architecture — cấu trúc hóa quy trình sản xuất từ trên xuống |
| **Lý do reasoning nặng ở P1** | Sai lầm trong chẩn đoán có hậu quả vật chất không đảo ngược → phải slow down | Output content có thể revise nhiều vòng → không cần slow down ở reasoning layer |
| **Lý do decomposition nặng ở P2** | Domain cây ăn quả đã có taxonomy cứng → không cần phân tầng phức tạp | Content không có cấu trúc tự nhiên → phải tự tạo hierarchy từ channel xuống script |
| **Vị trí của safety** | Safety = hard boundary về thuốc/hóa chất, mã hóa vào reasoning rules | Safety = tone & value boundary, mã hóa vào audience map + episode framework |
| **Tính tái dụng** | Schema diagnosis có thể áp cho nhiều loại cây, nhưng domain-specific cao | EPISODE-Flow và content IA có thể transfer sang nhiều domain nội dung khác |

---

## 4. Tại sao kỹ thuật khác nhau — phân tích theo lý do thực sự

P1 và P2 đều dùng đủ 9 bước SID, nhưng trọng tâm kỹ thuật lệch nhau vì bản chất bài toán khác nhau theo hai trục:

**Trục 1 — Reversibility.** Khi nông dân phun sai thuốc vì chẩn đoán sai, hậu quả không đảo ngược được. Điều này ép P1 phải đầu tư vào reasoning layer — hypothesis, confidence, validation — để làm chậm assistant lại trước khi đưa ra kết luận. P2 không có áp lực này: creator có thể revise nội dung vô số lần, nên không cần tầng kiểm soát epistemic dày.

**Trục 2 — Cấu trúc có sẵn hay phải tự tạo.** Domain cây ăn quả đã có taxonomy tương đối cứng (đất, nước, dinh dưỡng, sâu bệnh...) — P1 chỉ cần mapping vào schema chẩn đoán. Ngược lại, content không có skeleton tự nhiên: một kênh có thể là bất kỳ thứ gì. P2 phải tự xây hierarchy từ channel-level xuống script skeleton — nên decomposition và IA trở thành trọng tâm.

---

## 5. Phản biện — những điểm có thể tranh luận

### Phản biện 1 — P2 thiếu reasoning quá mức

Tài liệu đánh giá P2 nhẹ ở Buổi 6, nhưng thực tế content về tài chính cá nhân có thể gây hại nghiêm trọng nếu lời khuyên sai — mức độ không thua P1 bao nhiêu. Một người xem làm theo lời khuyên đầu tư thiếu căn cứ có thể mất tiền thật. Lý do P2 thiếu reasoning có lẽ đúng về mặt production logic, nhưng chưa chắc đúng về mặt epistemic risk của domain tài chính.

### Phản biện 2 — P1 có thể overfit vào kỷ luật epistemic

Kỷ luật fact/assumption/hypothesis/recommendation rất mạnh trong môi trường học thuật, nhưng người dùng thực (nông dân ở vùng nông thôn Việt Nam) có thể bị nhầm lẫn hoặc cảm thấy assistant do dự quá mức. Kỷ luật epistemic cần được dịch lại cho audience cụ thể, không phải áp nguyên si.

### Phản biện 3 — Expansion (Buổi 5) yếu ở cả hai

Cả P1 lẫn P2 đều được đánh giá ở mức `~` cho Expansion. Đây là điểm cần lưu ý: P1 thiếu bước mở rộng tìm kiếm nguyên nhân từ các domain liền kề (khí hậu, thổ nhưỡng vùng), trong khi P2 thiếu research depth thực sự về audience insight. Cả hai có thể được củng cố ở bước này mà không phá vỡ logic hiện tại.
