Câu hỏi trắc nghiệm Buổi 4 
> Information Architecture & Representation

1-C. Trang trí nội dung cho “đẹp mắt” và sinh động hơn  
2-B. Taxonomy dựa trên **một tiêu chí phân loại rõ**, hierarchy dựa trên **trật tự cha–con để dạy/học**  
3-B. Để tránh việc trộn nhiều tiêu chí trên cùng một chiều, làm người đọc khó hiểu và khó dạy lại  
4-B. Đặt cột theo ngẫu hứng, không có tiêu chí, khiến người đọc không rút ra được quyết định gì  
5-C. Vì schema chính là nơi mã hóa **tiêu chí so sánh/quyết định**, nếu làm sau thì bảng dễ trở nên “cho có”, thiếu ý nghĩa  
6-C. Ưu tiên “mạch học hợp lý” (logic học cái gì trước – sau, cognitive load mỗi mục lớn) hơn là trung thành tuyệt đối với cấu trúc cây ban đầu  
7-C. Vì thứ tự này tuân theo nguyên tắc: khái niệm nền → ứng dụng → đánh giá → đạo đức & policy → dạy lại  
8-B. Khi muốn thể hiện **giao cắt 2 chiều có ý nghĩa**, ví dụ “nhóm năng lực × giai đoạn”  
9-B. Giúp nhìn đa chiều: cùng một năng lực, xuất hiện khác nhau ở các giai đoạn, hỗ trợ ưu tiên thiết kế training/assistant  
10-C. Giúp thấy các **phụ thuộc giữa năng lực/khái niệm**, từ đó biết nên học/built assistant theo chuỗi nào  
11-C. Mỗi hàng/nhóm tuân theo **một tiêu chí phân loại rõ**, không trộn nhóm với cá nhân hay trộn nhiều tiêu chí trong cùng một chiều  
12-B. Vì mỗi dạng biểu diễn phục vụ một mục tiêu nhận thức khác: taxonomy để phân loại, hierarchy để dạy/học theo mạch, bảng/matrix để so sánh/ra quyết định  
13-B. IA Pack có trung thành với Framing Brief & scope domain đã định, tránh lan man vượt khung hay lệch mục tiêu hay không  
14-A. “Mục tiêu chính của năng lực” 
15-C. Dùng **đúng dạng biểu diễn** (taxonomy, hierarchy, table, matrix, flow,…) phù hợp với mục tiêu nhận thức cụ thể (học nhanh, so sánh, ra quyết định, thiết kế khóa học)  


## 9. Bài tập Buổi 4
### 9.1. Bài tập 1 — Taxonomy cho domain của bạn

**Mục tiêu**  
Phân loại 1 tập thành phần/năng lực trong Decomposition Tree theo 1 tiêu chí rõ.

**Bước 1**: Chọn tiêu chí phân loại:

- theo giai đoạn,
- theo mục tiêu,
- theo loại năng lực (nhận thức / kỹ thuật / đạo đức / dạy lại),
- v.v.

**Bước 2**: Lấy các node cấp 2–3 quan trọng trong cây, gán vào nhóm.

**Bước 3**: Viết lại dạng bảng taxonomy:

```markdown
### Taxonomy — [Tên]

| Nhóm chính       | Thành phần thuộc nhóm                      | Ghi chú ngắn               |
|------------------|---------------------------------------------|----------------------------|
| [Nhóm A]         | item 1, item 2, item 3                     |                            |
| [Nhóm B]         | ...                                         |                            |
| ...              |                                             |                            |
```

---

### 9.2. Bài tập 2 — Hierarchy dạy học (outline nhiều tầng)

**Mục tiêu**  
Từ cây decomposition → tạo 1 **outline dạy/học** 3–4 tầng.

**Bước 1**: Quyết định số “chương/mục lớn” (vd 4–6).

**Bước 2**: Gắn node vào cấu trúc I, II, III,… như 1 syllabus:

```markdown
I. [Mục lớn 1]
   I.1. [...]
   I.2. [...]
   I.3. [...]
II. [Mục lớn 2]
   ...
```

**Bước 3**: Đảm bảo:

- có thể map **1 mục lớn = 1 buổi / 1 module**,
- thứ tự học hợp lý.

---

### 9.3. Bài tập 3 — Bảng hoặc Matrix

Chọn **một**:

1. **Comparison table**:
   - So sánh 3–7 năng lực / kỹ thuật / module theo 3–4 tiêu chí hữu ích (mục tiêu, context, rủi ro…).

2. **Matrix**:
   - 2 chiều có ý nghĩa (VD: nhóm năng lực × giai đoạn; kỹ thuật × loại bài toán; v.v.).

---

## 10. Assignment Buổi 4 — IA Pack cho domain của bạn

### 10.1. Đề bài

Tạo 1 **IA Pack** dạng markdown, gồm:

1. **Taxonomy** (theo tiêu chí bạn chọn).
2. **Hierarchy dạy học** (outline 3–4 tầng).
3. **1 comparison table hoặc matrix**.
4. 1 đoạn ngắn (150–250 từ) trả lời:
   - Bạn sẽ dùng IA Pack này vào việc gì? (dạy, viết sách, thiết kế assistant, xây khóa nội bộ…)
   - Vì sao bạn chọn dạng biểu diễn như vậy (thay vì dạng khác)?

### 10.2. Gợi ý rubric tự chấm

| Tiêu chí             | Mô tả                                                                                 | Điểm (0–5) |
|----------------------|----------------------------------------------------------------------------------------|------------|
| Taxonomy clarity     | Tiêu chí phân loại rõ? Nhóm logic? Không trộn nhiều tiêu chí trong 1 taxonomy?       | /5         |
| Hierarchy coherence  | Outline có mạch? Các mục lớn đồng đẳng? Dạy/học theo thứ tự này có hợp lý?           | /5         |
| Table/Matrix usefulness | Bảng/matrix giúp nhìn ra quyết định/góc nhìn gì? Có cột/hàng vô nghĩa không?     | /5         |
| Connection to real use| IA Pack gắn với cách bạn thực sự sẽ dùng (dạy, build assistant, handbook…)?         | /5         |
| Alignment với Frame  | IA Pack vẫn tôn trọng Framing Brief & scope đã định?                                 | /5         |
| Clarity & readability| Đọc dễ, rõ, không rối; từng phần có heading, giải thích ngắn gọn?                     | /5         |

---

## 11. Sau Buổi 4 – Bạn đã có gì?

Nếu bạn hoàn thành Buổi 4:

- Bạn không chỉ có “cây tri thức” (Buổi 3),
- Mà còn có:

  - **Taxonomy**: phân loại các phần với 1 tiêu chí phù hợp,
  - **Hierarchy dạy học**: sườn 1 handbook/khóa học,
  - **Bảng/matrix**: công cụ so sánh, ra quyết định.

Tức là domain của bạn:

- đã có **bản đồ** (Buổi 3),
- và **có cách trình bày có chủ đích** (Buổi 4).

Buổi 5 sẽ mở rộng **chiều rộng & chiều sâu nghiên cứu**:

- quét rộng (breadth-first),
- mở rộng từ khóa,
- faceted exploration,
- chọn node đào sâu,
- thiết kế research path.

---