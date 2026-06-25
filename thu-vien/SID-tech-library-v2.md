# SID Technique Library v2

## Structured Intelligence Design — Technique Library theo progression chuẩn

Tài liệu này là thư viện kỹ thuật thực hành của SID, được thiết kế để đi cùng SID Syllabus như một bộ công cụ tra cứu, luyện tập và triển khai.

- Nó **không phải** danh sách mẹo prompt rời rạc.  
- Nó là một **progression library**: kỹ thuật được sắp từ nền tảng đến kiến trúc, gắn với level năng lực, mục tiêu tư duy, tình huống sử dụng, anti-pattern, tiêu chí đánh giá và ứng dụng thực chiến.

---

## 1. Vai trò của SID Technique Library v2

SID Technique Library v2 có 5 vai trò:

1. **Làm bộ công cụ cốt lõi của khóa học**  
   Mỗi session trong SID Syllabus chọn ra một tập kỹ thuật từ library này.

2. **Làm bản đồ progression**  
   Người học biết nên học kỹ thuật nào trước, kỹ thuật nào sau, và kỹ thuật nào chỉ nên dùng khi đã có nền.

3. **Làm tài liệu tra cứu sau khóa**  
   Sau khi học xong, học viên có thể quay lại tra cứu nhanh theo nhóm kỹ thuật, level, hoặc bài toán.

4. **Làm cầu nối giữa tư duy và thực hành**  
   Kỹ thuật không bị dạy như thủ thuật, mà gắn với bài toán nhận thức, cấu trúc thông tin, và logic triển khai.

5. **Làm nền cho Expert Builder Track**  
   Một số kỹ thuật trong library này là tiền đề để đi tiếp sang Gems, GPTs, RAG, tutors, assistants.

---

## 2. Cách đọc library này

Mỗi kỹ thuật trong library được mô tả theo cùng một schema chuẩn:

| Trường                | Ý nghĩa                                                     |
| --------------------- | ----------------------------------------------------------- |
| Tên kỹ thuật          | Tên chuẩn của kỹ thuật                                     |
| Tier                  | Tầng progression                                           |
| Level SID             | Level phù hợp trong SID                                    |
| Định nghĩa ngắn       | Kỹ thuật là gì                                             |
| Dùng để làm gì        | Bài toán mà kỹ thuật giải quyết                            |
| Dùng khi nào          | Tình huống phù hợp                                         |
| Không nên dùng khi nào| Tình huống không phù hợp                                   |
| Prompt / Usage Pattern| Mẫu dùng điển hình                                         |
| Failure Modes / Anti-patterns | Lỗi thường gặp                                     |
| Evaluation Criteria   | Tiêu chí đánh giá xem dùng tốt chưa                        |
| Kỹ thuật liên quan    | Kỹ thuật nên học cùng hoặc sau đó                          |
| Builder Relevance     | Liên hệ với Expert Builder Track                           |

---

## 3. Progression tổng thể của thư viện

SID Technique Library v2 được chia thành 4 tiers.

| Tier   | Tên                         | Mục tiêu                                          | Level SID |
| ------ | --------------------------- | ------------------------------------------------- | --------- |
| Tier 1 | Core Framing & Structuring | Định khung và cấu trúc hóa bài toán              | L1–L2     |
| Tier 2 | Analytical & Exploratory   | Mở rộng miền và điều khiển phân tích             | L3        |
| Tier 3 | Validation & Synthesis     | Kiểm định và tổng hợp thành tri thức có cấu trúc | L4–L5     |
| Tier 4 | Architect & Transfer       | Thiết kế hệ, workflow, domain knowledge use      | L6        |

Ngoài 4 tiers chính, cuối tài liệu có một phần:

- **Bridge to Expert Builder Track**

để chỉ ra kỹ thuật nào là nền cho các hệ Gem / GPT / RAG / tutor / assistant.

---

## 4. Tier 1 — Core Framing & Structuring

Tier 1 là nền tảng.  
Nếu thiếu Tier 1, người học sẽ:

- Hỏi lan man  
- Nhảy vào prompt phức tạp quá sớm  
- Có đầu ra dài nhưng thiếu đúng trọng tâm  
- Không dựng được hệ tri thức rõ ràng  

### 4.1. Problem Framing

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Problem Framing                                                                                   |
| Tier                         | Tier 1                                                                                            |
| Level SID                    | L1                                                                                                |
| Định nghĩa ngắn             | Xác định đúng bài toán cốt lõi cần AI hỗ trợ giải quyết                                          |
| Dùng để làm gì               | Làm rõ câu hỏi thật sự nằm ở đâu                                                                 |
| Dùng khi nào                 | Khi yêu cầu còn mơ hồ, quá rộng, hoặc lẫn nhiều mục tiêu                                         |
| Không nên dùng khi nào       | Khi bài toán đã được định nghĩa rất rõ và chỉ cần thực thi nhanh                                |
| Prompt / Usage Pattern       | “Trước khi trả lời, hãy giúp tôi xác định bài toán cốt lõi, mục tiêu chính, phạm vi và đầu ra phù hợp nhất.” |
| Failure Modes / Anti-patterns | Nhầm triệu chứng với bài toán; hỏi theo chủ đề thay vì theo vấn đề; gộp nhiều bài toán trong một prompt |
| Evaluation Criteria          | AI có làm rõ được mục tiêu, ranh giới, và outcome mong muốn không?                             |
| Kỹ thuật liên quan           | Goal Framing, Scope Design                                                                       |
| Builder Relevance            | Nền để viết system prompt và AI role definition                                                 |

### 4.2. Goal Framing

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Goal Framing                                                                                     |
| Tier                         | Tier 1                                                                                           |
| Level SID                    | L1                                                                                               |
| Định nghĩa ngắn             | Chỉ rõ mình muốn AI tạo ra loại giá trị nào: hiểu, so sánh, ra quyết định, dạy lại, triển khai |
| Dùng để làm gì               | Tránh output đúng chủ đề nhưng sai mục tiêu                                                     |
| Dùng khi nào                 | Gần như luôn luôn, đặc biệt khi chủ đề lớn                                                      |
| Không nên dùng khi nào       | Hầu như không có trường hợp loại bỏ hoàn toàn                                                   |
| Prompt / Usage Pattern       | “Mục tiêu của tôi không phải hiểu chung, mà là tạo một framework ra quyết định / một playbook / một plan triển khai.” |
| Failure Modes / Anti-patterns | Không nói rõ output cuối cùng; thay đổi mục tiêu giữa chừng; yêu cầu vừa học vừa triển khai vừa phản biện nhưng không ưu tiên |
| Evaluation Criteria          | Output có đúng loại giá trị cần thiết không?                                                    |
| Kỹ thuật liên quan           | Output Framing, Audience Framing                                                                |
| Builder Relevance            | Rất quan trọng khi thiết kế task modes cho Gems / GPTs                                          |

### 4.3. Audience Framing

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Audience Framing                                                                                 |
| Tier                         | Tier 1                                                                                           |
| Level SID                    | L1                                                                                               |
| Định nghĩa ngắn             | Xác định người đọc / người dùng của đầu ra                                                      |
| Dùng để làm gì               | Điều chỉnh độ sâu, từ vựng, ví dụ, format và mức giả định kiến thức                             |
| Dùng khi nào                 | Khi cần giải thích, dạy, soạn tài liệu, hoặc tạo output cho người khác                          |
| Không nên dùng khi nào       | Khi output chỉ dành cho chính mình và mức độ người dùng đã rõ                                  |
| Prompt / Usage Pattern       | “Hãy trình bày cho người đã có 1–3 năm dùng AI nhưng chưa có framework hệ thống.”              |
| Failure Modes / Anti-patterns | Nói “giải thích đơn giản” nhưng không chỉ rõ đơn giản cho ai; trộn audience novice và expert trong cùng output |
| Evaluation Criteria          | Output có đúng độ sâu và đúng ngôn ngữ cho audience mục tiêu không?                            |
| Kỹ thuật liên quan           | Goal Framing, Teaching Translation                                                              |
| Builder Relevance            | Quan trọng khi thiết kế AI tutor, coach, assistant theo persona                                |

### 4.4. Scope Design

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Scope Design                                                                                     |
| Tier                         | Tier 1                                                                                           |
| Level SID                    | L1                                                                                               |
| Định nghĩa ngắn             | Xác lập biên của chủ đề: cái gì trong phạm vi, cái gì ngoài phạm vi                             |
| Dùng để làm gì               | Tránh lan man và tránh “mở rộng vô hạn”                                                          |
| Dùng khi nào                 | Khi chủ đề rộng, có nhiều nhánh, hoặc dễ lạc khỏi mục tiêu                                      |
| Không nên dùng khi nào       | Khi chỉ hỏi một tác vụ vi mô rất hẹp                                                             |
| Prompt / Usage Pattern       | “Giới hạn phạm vi ở: tư duy khai thác thông tin từ AI, không đi sâu vào coding implementation hay policy.” |
| Failure Modes / Anti-patterns | Phạm vi quá rộng; phạm vi thay đổi liên tục; bỏ sót biên ngoài phạm vi                         |
| Evaluation Criteria          | AI có giữ được sự tập trung và loại bỏ được phần ngoài phạm vi không?                           |
| Kỹ thuật liên quan           | Problem Framing, Decomposition                                                                   |
| Builder Relevance            | Rất quan trọng cho domain-bounded assistants                                                     |

### 4.5. Output Framing

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Output Framing                                                                                   |
| Tier                         | Tier 1                                                                                           |
| Level SID                    | L1                                                                                               |
| Định nghĩa ngắn             | Chỉ định rõ hình dạng của đầu ra                                                                |
| Dùng để làm gì               | Ép AI tạo ra output có cấu trúc dùng được                                                       |
| Dùng khi nào                 | Khi output cần dùng lại, đánh giá, hoặc chuyển thành tài liệu / workflow                        |
| Không nên dùng khi nào       | Khi chỉ cần brainstorming thô                                                                    |
| Prompt / Usage Pattern       | “Hãy trả lời dưới dạng bảng gồm: khái niệm, định nghĩa, ứng dụng, sai lầm phổ biến.”           |
| Failure Modes / Anti-patterns | Chọn format sai với bản chất thông tin; ép bảng khi dữ liệu dị loại; yêu cầu quá nhiều format cùng lúc không có ưu tiên |
| Evaluation Criteria          | Output có đúng format và format đó có hỗ trợ mục tiêu không?                                    |
| Kỹ thuật liên quan           | Representation Design, Table Schema Design                                                       |
| Builder Relevance            | Rất quan trọng cho response contracts trong GPT/Gem                                             |

### 4.6. Top-down Decomposition

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Top-down Decomposition                                                                           |
| Tier                         | Tier 1                                                                                           |
| Level SID                    | L2                                                                                               |
| Định nghĩa ngắn             | Chia một chủ đề lớn thành các nhánh nhỏ từ trên xuống                                           |
| Dùng để làm gì               | Quét rộng, tránh bỏ sót, tạo roadmap đào sâu                                                     |
| Dùng khi nào                 | Nghiên cứu chủ đề mới, xây outline, framework, syllabus                                         |
| Không nên dùng khi nào       | Khi bài toán đã rất vi mô hoặc khi cần bottom-up synthesis từ dữ liệu cụ thể                    |
| Prompt / Usage Pattern       | “Hãy bóc tách chủ đề này thành 4–6 nhánh lớn, rồi chia mỗi nhánh thành 3–5 tiểu mục.”          |
| Failure Modes / Anti-patterns | Chia trùng lặp; chia theo cảm tính; lẫn cấp độ trừu tượng                                      |
| Evaluation Criteria          | Các nhánh có đủ bao quát, ít chồng lấn và có thể đào sâu tiếp không?                           |
| Kỹ thuật liên quan           | Taxonomy Building, Hierarchy Design                                                             |
| Builder Relevance            | Dùng để thiết kế capability map cho AI systems                                                  |

### 4.7. Taxonomy Building

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Taxonomy Building                                                                                |
| Tier                         | Tier 1                                                                                           |
| Level SID                    | L2                                                                                               |
| Định nghĩa ngắn             | Xây hệ phân loại các khái niệm trong một miền                                                   |
| Dùng để làm gì               | Tạo cấu trúc khái niệm và language map                                                           |
| Dùng khi nào                 | Khi chủ đề có nhiều thuật ngữ, biến thể, trường phái, use case                                  |
| Không nên dùng khi nào       | Khi chủ đề chỉ là một tác vụ đơn giản, không cần phân loại                                      |
| Prompt / Usage Pattern       | “Hãy xây taxonomy 2–3 tầng cho chủ đề này, tách rõ khái niệm nền, kỹ thuật, ứng dụng và đánh giá.” |
| Failure Modes / Anti-patterns | Phân loại lẫn lộn; chồng tầng; trộn loại thực thể khác nhau vào cùng nhóm                     |
| Evaluation Criteria          | Taxonomy có rõ nhóm, rõ cấp, ít trùng và có ích cho học / triển khai không?                    |
| Kỹ thuật liên quan           | Hierarchy Design, Ontology Thinking                                                             |
| Builder Relevance            | Dùng để thiết kế knowledge schemas cho assistants                                               |

### 4.8. Hierarchy Design

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Hierarchy Design                                                                                 |
| Tier                         | Tier 1                                                                                           |
| Level SID                    | L2                                                                                               |
| Định nghĩa ngắn             | Tổ chức thông tin theo quan hệ cha-con, từ tổng quát đến chi tiết                               |
| Dùng để làm gì               | Giúp trình bày, dạy học, đào sâu có kiểm soát                                                    |
| Dùng khi nào                 | Outline, bullets, manuals, course materials                                                      |
| Không nên dùng khi nào       | Khi quan hệ thông tin là mạng lưới đa chiều, không phải cây                                     |
| Prompt / Usage Pattern       | “Hãy tổ chức nội dung theo 3 tầng: nguyên lý → thành phần → kỹ thuật / ví dụ.”                |
| Failure Modes / Anti-patterns | Nhảy cấp; các ý cùng cấp không đồng đẳng; ý con không giải thích ý cha                         |
| Evaluation Criteria          | Hierarchy có mạch, nhất quán cấp độ và dễ đọc không?                                            |
| Kỹ thuật liên quan           | Taxonomy, Representation Design                                                                  |
| Builder Relevance            | Dùng cho instruction hierarchy trong system prompts                                              |

### 4.9. Table Schema Design

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Table Schema Design                                                                              |
| Tier                         | Tier 1                                                                                           |
| Level SID                    | L2                                                                                               |
| Định nghĩa ngắn             | Thiết kế logic hàng-cột phù hợp trước khi yêu cầu AI tạo bảng                                   |
| Dùng để làm gì               | Tránh bảng lộn xộn hoặc méo logic                                                                |
| Dùng khi nào                 | Khi cần so sánh thực thể cùng lớp hoặc chuẩn hóa thông tin                                      |
| Không nên dùng khi nào       | Khi dữ liệu chưa cùng lớp hoặc quá narrative                                                     |
| Prompt / Usage Pattern       | “Tạo bảng với hàng là kỹ thuật, cột là: mục tiêu, khi dùng, sai lầm, level phù hợp.”           |
| Failure Modes / Anti-patterns | Hàng không cùng loại; cột không cùng tiêu chí; bảng chỉ để nhìn gọn                            |
| Evaluation Criteria          | Bảng có giúp so sánh, ra quyết định hoặc học nhanh hơn không?                                   |
| Kỹ thuật liên quan           | Output Framing, Matrix Design                                                                   |
| Builder Relevance            | Quan trọng cho structured outputs và evaluation sheets                                          |

---

## 5. Tier 2 — Analytical & Exploratory Techniques

Tier 2 dành cho người đã có nền framing và structuring.  
Mục tiêu là biết:

- Quét rộng đúng cách  
- Đào sâu đúng điểm  
- Điều khiển kiểu suy luận  
- Không bị một chiều  

### 5.1. Breadth-first Exploration

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Breadth-first Exploration                                                                       |
| Tier                         | Tier 2                                                                                           |
| Level SID                    | L3                                                                                               |
| Định nghĩa ngắn             | Quét rộng toàn bộ miền trước khi chọn điểm đào sâu                                              |
| Dùng để làm gì               | Tránh đi sâu sai chỗ từ quá sớm                                                                  |
| Dùng khi nào                 | Gặp chủ đề mới, nhiều nhánh, nhiều trường phái                                                  |
| Không nên dùng khi nào       | Khi phạm vi đã rất hẹp và mục tiêu rất cụ thể                                                   |
| Prompt / Usage Pattern       | “Trước khi đi sâu, hãy quét toàn bộ chủ đề, chỉ ra các nhánh chính, trường phái, tranh luận và hướng ứng dụng lớn.” |
| Failure Modes / Anti-patterns | Quét quá rộng nhưng không chốt được điểm sâu; biến quét rộng thành liệt kê dài vô ích         |
| Evaluation Criteria          | Output breadth có tạo được bản đồ để chọn hướng đào sâu không?                                  |
| Kỹ thuật liên quan           | Depth-first Exploration, Query Expansion                                                        |
| Builder Relevance            | Dùng trong discovery phase cho domain assistants                                                |

### 5.2. Depth-first Exploration

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Depth-first Exploration                                                                         |
| Tier                         | Tier 2                                                                                           |
| Level SID                    | L3                                                                                               |
| Định nghĩa ngắn             | Chọn một nhánh rồi đi sâu theo nhiều tầng                                                       |
| Dùng để làm gì               | Chuyển từ overview sang mastery cục bộ                                                          |
| Dùng khi nào                 | Sau khi đã quét rộng và xác định nhánh trọng tâm                                               |
| Không nên dùng khi nào       | Khi chưa có bản đồ toàn cục                                                                     |
| Prompt / Usage Pattern       | “Hãy đào sâu nhánh này theo 12 mục: định nghĩa, bối cảnh, cấu trúc, cơ chế, use case, trade-off, sai lầm, đánh giá…” |
| Failure Modes / Anti-patterns | Đi sâu quá sớm; đi sâu mà không giữ cấu trúc; lặp nội dung                                    |
| Evaluation Criteria          | Output depth có thật sự tăng hiểu biết cơ chế và ứng dụng không?                               |
| Kỹ thuật liên quan           | Breadth-first, Probe Each Node                                                                  |
| Builder Relevance            | Dùng trong domain deep-spec và failure analysis                                                 |

### 5.3. Query Expansion

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Query Expansion                                                                                  |
| Tier                         | Tier 2                                                                                           |
| Level SID                    | L3                                                                                               |
| Định nghĩa ngắn             | Mở rộng tập thuật ngữ, từ khóa, góc nhìn hoặc biến thể của câu hỏi                              |
| Dùng để làm gì               | Tăng recall và tránh bị giới hạn bởi từ ngữ ban đầu                                              |
| Dùng khi nào                 | Khi cảm thấy output hẹp, lặp lại, hoặc có khả năng bỏ sót miền liên quan                        |
| Không nên dùng khi nào       | Khi chủ đề đã được khóa scope rất chặt                                                           |
| Prompt / Usage Pattern       | “Hãy mở rộng câu hỏi này thành các hướng truy vấn liên quan: thuật ngữ thay thế, góc nhìn liền kề, câu hỏi phản biện, ứng dụng thực tế.” |
| Failure Modes / Anti-patterns | Mở rộng vô tội vạ; mất scope; đẩy AI ra ngoài chủ đề chính                                     |
| Evaluation Criteria          | Query expansion có giúp phát hiện góc mù hoặc khái niệm liền kề quan trọng không?              |
| Kỹ thuật liên quan           | Breadth-first, Adjacent-domain Exploration                                                      |
| Builder Relevance            | Quan trọng trong retrieval query design và knowledge coverage                                   |

### 5.4. Comparative Reasoning

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Comparative Reasoning                                                                            |
| Tier                         | Tier 2                                                                                           |
| Level SID                    | L3                                                                                               |
| Định nghĩa ngắn             | Phân tích bằng cách so sánh hai hoặc nhiều phương án / trường phái / kỹ thuật                  |
| Dùng để làm gì               | Thấy trade-off, ranh giới ứng dụng, khác biệt bản chất                                           |
| Dùng khi nào                 | Đánh giá framework, mô hình, lựa chọn giải pháp                                                  |
| Không nên dùng khi nào       | Khi đối tượng chưa cùng lớp để so sánh                                                           |
| Prompt / Usage Pattern       | “So sánh A và B theo: mục tiêu, cơ chế, điều kiện dùng, ưu điểm, giới hạn, failure modes.”      |
| Failure Modes / Anti-patterns | So sánh táo với cam; tiêu chí không đồng nhất; kết luận theo cảm tính                          |
| Evaluation Criteria          | So sánh có công bằng, rõ tiêu chí và chỉ ra được trade-off thật không?                         |
| Kỹ thuật liên quan           | Table Schema Design, Trade-off Analysis                                                          |
| Builder Relevance            | Quan trọng cho model/tool selection                                                              |

### 5.5. Causal Reasoning

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Causal Reasoning                                                                                 |
| Tier                         | Tier 2                                                                                           |
| Level SID                    | L3                                                                                               |
| Định nghĩa ngắn             | Phân tích nguyên nhân – cơ chế – hệ quả thay vì chỉ mô tả hiện tượng                             |
| Dùng để làm gì               | Đi sâu bản chất, giải thích vì sao, dự đoán hệ quả                                               |
| Dùng khi nào                 | Khi cần hiểu cơ chế hoạt động hoặc vấn đề gốc                                                    |
| Không nên dùng khi nào       | Khi không có đủ ngữ cảnh hoặc đối tượng vốn mang tính mô tả / taxonomy thuần túy                |
| Prompt / Usage Pattern       | “Giải thích mối quan hệ nhân quả giữa các yếu tố, phân biệt nguyên nhân gốc, nguyên nhân gần và tác động hệ quả.” |
| Failure Modes / Anti-patterns | Nhầm tương quan với nhân quả; suy diễn quá mức; thiếu điều kiện bối cảnh                      |
| Evaluation Criteria          | Causal chain có hợp lý, đủ điều kiện và không nhảy bước không?                                  |
| Kỹ thuật liên quan           | Hypothesis-driven Reasoning, Failure Analysis                                                    |
| Builder Relevance            | Quan trọng trong troubleshooting AI systems                                                      |

### 5.6. Hypothesis-driven Reasoning

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Hypothesis-driven Reasoning                                                                      |
| Tier                         | Tier 2                                                                                           |
| Level SID                    | L3                                                                                               |
| Định nghĩa ngắn             | Đặt giả thuyết rồi dùng AI để kiểm tra, phản biện hoặc tinh chỉnh                               |
| Dùng để làm gì               | Chuyển từ hỏi lan man sang inquiry có định hướng                                                 |
| Dùng khi nào                 | Khi cần phân tích vấn đề, ra quyết định, tìm nguyên nhân, hoặc nghiên cứu có kiểm soát         |
| Không nên dùng khi nào       | Khi chưa có đủ hiểu biết nền để tạo giả thuyết có ích                                           |
| Prompt / Usage Pattern       | “Giả thuyết của tôi là X. Hãy kiểm tra giả thuyết này bằng các dấu hiệu ủng hộ, phản ví dụ, điều kiện đúng-sai và dữ kiện cần thêm.” |
| Failure Modes / Anti-patterns | Bias xác nhận; ép AI chứng minh giả thuyết thay vì kiểm tra; giả thuyết quá mơ hồ             |
| Evaluation Criteria          | AI có xét cả evidence thuận và nghịch, và nêu điều kiện giới hạn không?                        |
| Kỹ thuật liên quan           | Causal Reasoning, Validation Techniques                                                          |
| Builder Relevance            | Quan trọng khi debug prompt systems, RAG behaviors                                               |

### 5.7. Tree of Thought (Basic)

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Tree of Thought (Basic)                                                                          |
| Tier                         | Tier 2                                                                                           |
| Level SID                    | L3                                                                                               |
| Định nghĩa ngắn             | Yêu cầu AI xem xét nhiều hướng suy nghĩ song song trước khi kết luận                            |
| Dùng để làm gì               | Tránh suy luận một đường duy nhất                                                                |
| Dùng khi nào                 | Vấn đề phức tạp, nhiều phương án, cần phân nhánh                                                 |
| Không nên dùng khi nào       | Tác vụ đơn giản, đã có quy trình rõ                                                              |
| Prompt / Usage Pattern       | “Hãy tạo 3 hướng tiếp cận khác nhau, đánh giá ưu nhược điểm của từng hướng rồi mới khuyến nghị.” |
| Failure Modes / Anti-patterns | Tạo nhánh giả tạo; quá nhiều nhánh gây loãng; không có bước chọn lọc sau cùng                 |
| Evaluation Criteria          | Các nhánh có thực sự khác nhau và giúp mở rộng phương án không?                                |
| Kỹ thuật liên quan           | Comparative Reasoning, Prompt Stack                                                              |
| Builder Relevance            | Dùng trong planning prompts cho assistants                                                       |

---

## 6. Tier 3 — Validation & Synthesis Techniques

Tier 3 là phần thường bị người dùng AI bỏ qua nhất.  
Đây là nơi chuyển người dùng “dùng được” thành người dùng “đáng tin cậy”.

### 6.1. Self-critique Prompting

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Self-critique Prompting                                                                          |
| Tier                         | Tier 3                                                                                           |
| Level SID                    | L4                                                                                               |
| Định nghĩa ngắn             | Yêu cầu AI tự xem lại và chỉ ra điểm yếu của câu trả lời vừa tạo                                 |
| Dùng để làm gì               | Tăng chất lượng đầu ra và giảm tự tin giả                                                        |
| Dùng khi nào                 | Gần như luôn nên dùng với output quan trọng                                                      |
| Không nên dùng khi nào       | Với tác vụ rất nhỏ, chi phí nhận thức không đáng                                                 |
| Prompt / Usage Pattern       | “Hãy tự phản biện câu trả lời trên: chỉ ra điểm mơ hồ, chỗ thiếu, chỗ có thể gây hiểu sai, và viết lại tốt hơn.” |
| Failure Modes / Anti-patterns | Phản biện hời hợt; chỉ sửa câu chữ; không chạm vào giả định cốt lõi                            |
| Evaluation Criteria          | Self-critique có phát hiện lỗi cấu trúc, logic, hoặc thiếu sót thực sự không?                  |
| Kỹ thuật liên quan           | Contradiction Check, Gap Detection                                                               |
| Builder Relevance            | Nền cho eval loops và self-revision patterns                                                     |

### 6.2. Contradiction Check

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Contradiction Check                                                                              |
| Tier                         | Tier 3                                                                                           |
| Level SID                    | L4                                                                                               |
| Định nghĩa ngắn             | Kiểm tra xem output có tự mâu thuẫn hoặc mâu thuẫn với premise không                            |
| Dùng để làm gì               | Tăng tính logic nội tại                                                                          |
| Dùng khi nào                 | Khi output dài, nhiều phần, nhiều khẳng định                                                    |
| Không nên dùng khi nào       | Khi output chỉ là một trả lời ngắn rất đơn giản                                                  |
| Prompt / Usage Pattern       | “Hãy kiểm tra các phần trên xem có mâu thuẫn nội tại, nhảy logic hoặc thay đổi định nghĩa không.” |
| Failure Modes / Anti-patterns | Chỉ soi câu chữ; không phát hiện mâu thuẫn ngầm; bỏ qua thay đổi cấp độ khái niệm              |
| Evaluation Criteria          | Có phát hiện được inconsistency thật sự không?                                                  |
| Kỹ thuật liên quan           | Assumption Check, Logic Validation                                                              |
| Builder Relevance            | Quan trọng cho consistency testing trong system outputs                                         |

### 6.3. Assumption Check

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Assumption Check                                                                                 |
| Tier                         | Tier 3                                                                                           |
| Level SID                    | L4                                                                                               |
| Định nghĩa ngắn             | Bóc tách các giả định ẩn đằng sau câu trả lời hoặc khuyến nghị                                   |
| Dùng để làm gì               | Tránh dùng output đúng trong một thế giới giả định nhưng sai ngoài thực tế                     |
| Dùng khi nào                 | Ra quyết định, thiết kế framework, chiến lược, tư vấn                                           |
| Không nên dùng khi nào       | Khi chỉ cần tóm tắt mô tả đơn giản                                                               |
| Prompt / Usage Pattern       | “Hãy liệt kê các giả định ngầm trong phân tích này và cho biết nếu giả định nào sai thì kết luận nào sụp đổ.” |
| Failure Modes / Anti-patterns | Chỉ nêu assumption hiển nhiên; không liên hệ assumption với hệ quả                             |
| Evaluation Criteria          | Assumption có đủ cụ thể và cho thấy điểm dễ gãy của lập luận không?                            |
| Kỹ thuật liên quan           | Hypothesis-driven Reasoning, Boundary Testing                                                   |
| Builder Relevance            | Rất quan trọng trong safety, guardrails, domain boundaries                                      |

### 6.4. Gap Detection

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Gap Detection                                                                                    |
| Tier                         | Tier 3                                                                                           |
| Level SID                    | L4                                                                                               |
| Định nghĩa ngắn             | Tìm ra phần quan trọng còn thiếu trong cấu trúc hoặc phân tích                                  |
| Dùng để làm gì               | Tăng độ đủ và độ bao quát                                                                        |
| Dùng khi nào                 | Khi xây framework, syllabus, playbook, checklist                                                |
| Không nên dùng khi nào       | Output rất hẹp, không cần bao quát                                                               |
| Prompt / Usage Pattern       | “Nếu xem đây là một framework hoàn chỉnh, phần nào đang bị thiếu hoặc chưa được phát triển đủ?” |
| Failure Modes / Anti-patterns | Thêm cho nhiều nhưng không đúng trọng yếu; lẫn ‘thiếu’ với ‘muốn thêm cho hay’                |
| Evaluation Criteria          | Gap được chỉ ra có thật sự quan trọng với mục tiêu không?                                      |
| Kỹ thuật liên quan           | Breadth-first Exploration, Self-critique                                                         |
| Builder Relevance            | Giúp phát hiện missing modes trong GPT/Gem designs                                              |

### 6.5. Triangulation

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Triangulation                                                                                    |
| Tier                         | Tier 3                                                                                           |
| Level SID                    | L4                                                                                               |
| Định nghĩa ngắn             | Kiểm tra cùng một nội dung từ nhiều góc nhìn hoặc nhiều cấu trúc đánh giá                       |
| Dùng để làm gì               | Giảm lệ thuộc vào một framing duy nhất                                                           |
| Dùng khi nào                 | Khi cần độ tin cậy cao hoặc chủ đề có thể nhìn rất khác nhau                                    |
| Không nên dùng khi nào       | Khi bài toán rất đơn giản, chi phí không đáng                                                    |
| Prompt / Usage Pattern       | “Hãy đánh giá vấn đề này từ 3 góc nhìn: lý thuyết, thực hành, và phản biện.”                    |
| Failure Modes / Anti-patterns | Các góc nhìn không thực sự khác nhau; nhân bản cùng một ý dưới 3 nhãn khác nhau               |
| Evaluation Criteria          | Triangulation có tạo ra insight bổ sung và phát hiện điểm mù không?                            |
| Kỹ thuật liên quan           | Comparative Reasoning, Audience Framing                                                          |
| Builder Relevance            | Dùng trong eval suite cho assistants                                                             |

### 6.6. Confidence Labeling

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Confidence Labeling                                                                              |
| Tier                         | Tier 3                                                                                           |
| Level SID                    | L4                                                                                               |
| Định nghĩa ngắn             | Gắn nhãn mức chắc chắn cho các phần của output                                                  |
| Dùng để làm gì               | Tách phần chắc cao khỏi phần cần kiểm chứng                                                      |
| Dùng khi nào                 | Với output chiến lược, nghiên cứu, đánh giá, hoặc quyết định                                    |
| Không nên dùng khi nào       | Với nội dung hoàn toàn mô tả cơ bản ít rủi ro                                                    |
| Prompt / Usage Pattern       | “Hãy gắn cho mỗi phần một mức: chắc cao / trung bình / cần kiểm chứng, kèm lý do.”             |
| Failure Modes / Anti-patterns | Confidence quá chung chung; không gắn với lý do; nhầm tự tin với đúng                         |
| Evaluation Criteria          | Nhãn confidence có phân biệt được rõ các mức và hợp lý với nội dung không?                    |
| Kỹ thuật liên quan           | Self-critique, Source-demanding Prompting                                                        |
| Builder Relevance            | Quan trọng cho trustworthy AI UX                                                                 |

### 6.7. Pattern Extraction

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Pattern Extraction                                                                               |
| Tier                         | Tier 3                                                                                           |
| Level SID                    | L5                                                                                               |
| Định nghĩa ngắn             | Rút ra mẫu lặp lại từ nhiều ý, nhiều case, nhiều quan sát                                       |
| Dùng để làm gì               | Chuyển từ nhiều dữ kiện sang insight có tính hệ                                                 |
| Dùng khi nào                 | Sau khi đã có đủ material để tổng hợp                                                           |
| Không nên dùng khi nào       | Khi dữ liệu / input quá ít hoặc quá rời                                                          |
| Prompt / Usage Pattern       | “Từ các ví dụ / phần trên, hãy rút ra các pattern lặp lại và nêu hệ quả thực tiễn.”            |
| Failure Modes / Anti-patterns | Pattern giả; tổng quát hóa quá mức; pattern quá hiển nhiên                                     |
| Evaluation Criteria          | Pattern có lặp thật, có giải thích được nhiều trường hợp và có giá trị hành động không?       |
| Kỹ thuật liên quan           | Principle Extraction, Framework Synthesis                                                        |
| Builder Relevance            | Dùng trong extracting reusable workflows for AI products                                         |

### 6.8. Principle Extraction

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Principle Extraction                                                                             |
| Tier                         | Tier 3                                                                                           |
| Level SID                    | L5                                                                                               |
| Định nghĩa ngắn             | Rút nguyên lý nền đằng sau các kỹ thuật, hiện tượng hoặc framework                              |
| Dùng để làm gì               | Nâng người học từ ‘biết cách làm’ lên ‘biết tại sao’                                            |
| Dùng khi nào                 | Sau khi đã hiểu đủ ví dụ, kỹ thuật hoặc case                                                    |
| Không nên dùng khi nào       | Khi nền tảng vẫn mơ hồ, chưa có đủ chất liệu                                                    |
| Prompt / Usage Pattern       | “Hãy rút ra 3–5 nguyên lý nền tảng đứng sau các kỹ thuật này, và giải thích vì sao chúng quan trọng.” |
| Failure Modes / Anti-patterns | Nguyên lý quá chung; nghe hay nhưng không chỉ đạo được hành động                               |
| Evaluation Criteria          | Nguyên lý có giúp giải thích nhiều kỹ thuật và định hướng quyết định không?                    |
| Kỹ thuật liên quan           | Pattern Extraction, Abstraction                                                                  |
| Builder Relevance            | Dùng để thiết kế stable system behaviors thay vì prompt-by-prompt hacks                         |

### 6.9. Framework Synthesis

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Framework Synthesis                                                                              |
| Tier                         | Tier 3                                                                                           |
| Level SID                    | L5                                                                                               |
| Định nghĩa ngắn             | Tổng hợp nhiều ý, nhiều kỹ thuật thành một framework có tên, có bước, có logic                  |
| Dùng để làm gì               | Đóng gói tri thức thành tài sản có thể dạy lại và dùng lại                                      |
| Dùng khi nào                 | Cuối một chuỗi nghiên cứu, cuối khóa, cuối tài liệu, cuối workshop                             |
| Không nên dùng khi nào       | Khi material đầu vào còn quá rời hoặc thiếu validation                                          |
| Prompt / Usage Pattern       | “Từ toàn bộ nội dung trên, hãy tổng hợp thành một framework 5–7 bước, có tên, mục tiêu, logic từng bước và tình huống áp dụng.” |
| Failure Modes / Anti-patterns | Framework hóa quá sớm; đặt tên hay nhưng rỗng; bước chồng lặp                                   |
| Evaluation Criteria          | Framework có logic nội tại, dễ nhớ, dùng lại được và không chỉ là outline đổi tên không?      |
| Kỹ thuật liên quan           | Pattern Extraction, Workflow Design                                                              |
| Builder Relevance            | Nền để biến knowledge into AI product specifications                                            |

---

## 7. Tier 4 — Architect & Transfer Techniques

Tier 4 là nơi chuyển từ “người phân tích tốt” sang “người thiết kế hệ tri thức”.

### 7.1. Workflow Design

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Workflow Design                                                                                  |
| Tier                         | Tier 4                                                                                           |
| Level SID                    | L6                                                                                               |
| Định nghĩa ngắn             | Biến tri thức hoặc framework thành một chuỗi bước hành động có đầu vào, xử lý, đầu ra          |
| Dùng để làm gì               | Operationalize tri thức                                                                          |
| Dùng khi nào                 | Khi cần SOP, process, playbook, execution model                                                  |
| Không nên dùng khi nào       | Khi tri thức còn ở mức exploratory, chưa ổn định                                                |
| Prompt / Usage Pattern       | “Chuyển framework này thành workflow thực thi gồm: input, steps, checkpoints, outputs, common errors.” |
| Failure Modes / Anti-patterns | Workflow mơ hồ; thiếu checkpoint; không rõ ai làm gì; không có điều kiện dừng                 |
| Evaluation Criteria          | Workflow có thể được người khác làm theo không?                                                 |
| Kỹ thuật liên quan           | Framework Synthesis, Checklist Design                                                            |
| Builder Relevance            | Rất quan trọng cho assistants và agentic processes                                              |

### 7.2. Use-case Mapping

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Use-case Mapping                                                                                 |
| Tier                         | Tier 4                                                                                           |
| Level SID                    | L6                                                                                               |
| Định nghĩa ngắn             | Gắn tri thức / framework với các tình huống thực tế cụ thể                                      |
| Dùng để làm gì               | Đưa tri thức ra khỏi mức lý thuyết                                                               |
| Dùng khi nào                 | Trước khi chuyển thành giải pháp, sản phẩm, training, SOP                                       |
| Không nên dùng khi nào       | Khi bản thân framework còn chưa chín                                                             |
| Prompt / Usage Pattern       | “Hãy mapping framework này vào 3 bối cảnh: cá nhân, team nhỏ, tổ chức lớn; nêu điều kiện dùng, rủi ro và outcome kỳ vọng.” |
| Failure Modes / Anti-patterns | Ví dụ quá generic; không nói điều kiện dùng; use case không cùng lớp                           |
| Evaluation Criteria          | Use case có đủ cụ thể để thử nghiệm hoặc triển khai không?                                      |
| Kỹ thuật liên quan           | Workflow Design, Scenario Design                                                                 |
| Builder Relevance            | Nền cho domain-specific assistant design                                                         |

### 7.3. Checklist Design

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Checklist Design                                                                                 |
| Tier                         | Tier 4                                                                                           |
| Level SID                    | L6                                                                                               |
| Định nghĩa ngắn             | Nén một quy trình hoặc hệ tiêu chí thành danh sách kiểm ngắn gọn                               |
| Dùng để làm gì               | Giúp đánh giá nhanh, thực thi nhanh, review nhanh                                               |
| Dùng khi nào                 | Review output, audit quy trình, coaching, self-check                                            |
| Không nên dùng khi nào       | Khi vấn đề quá phức tạp cần giải thích dài                                                      |
| Prompt / Usage Pattern       | “Từ workflow này, hãy rút thành checklist 10 mục dùng để tự kiểm trước khi hoàn tất.”         |
| Failure Modes / Anti-patterns | Checklist quá dài; mục không kiểm được; quá trừu tượng                                        |
| Evaluation Criteria          | Người dùng có thể dùng checklist trong 1–3 phút không?                                          |
| Kỹ thuật liên quan           | Rubric Design, Workflow Design                                                                   |
| Builder Relevance            | Dùng trong eval checklists cho products                                                          |

### 7.4. Rubric Design

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Rubric Design                                                                                    |
| Tier                         | Tier 4                                                                                           |
| Level SID                    | L6                                                                                               |
| Định nghĩa ngắn             | Xây tiêu chí chấm hoặc đánh giá chất lượng theo mức độ                                          |
| Dùng để làm gì               | Đánh giá output, đánh giá học viên, đánh giá AI responses                                       |
| Dùng khi nào                 | Khi cần chất lượng có thể đo và lặp lại                                                         |
| Không nên dùng khi nào       | Khi chỉ brainstorming nhanh, chưa cần kiểm soát chất lượng                                      |
| Prompt / Usage Pattern       | “Hãy tạo rubric 5 tiêu chí, mỗi tiêu chí có 3 mức: yếu, đạt, mạnh.”                            |
| Failure Modes / Anti-patterns | Rubric quá chủ quan; tiêu chí chồng lặp; mức độ không phân biệt rõ                             |
| Evaluation Criteria          | Rubric có giúp hai người chấm gần giống nhau không?                                             |
| Kỹ thuật liên quan           | Checklist Design, Confidence Labeling                                                            |
| Builder Relevance            | Cực quan trọng cho evaluation suites của GPT/Gem/RAG                                            |

### 7.5. Teaching Translation

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Teaching Translation                                                                             |
| Tier                         | Tier 4                                                                                           |
| Level SID                    | L6                                                                                               |
| Định nghĩa ngắn             | Biến tri thức sâu thành dạng có thể dạy cho người khác mà không làm méo bản chất              |
| Dùng để làm gì               | Dạy lại, làm tài liệu, xây khóa học, làm tutor prompts                                          |
| Dùng khi nào                 | Khi cần giải thích cho audience khác mức độ                                                     |
| Không nên dùng khi nào       | Khi bản thân nội dung gốc còn chưa thật sự hiểu                                                |
| Prompt / Usage Pattern       | “Hãy viết lại nội dung này cho 3 audience: người mới, người đã dùng AI 1–3 năm, và người muốn đi expert.” |
| Failure Modes / Anti-patterns | Đơn giản hóa thành sai; ví dụ quá dễ dãi; mất cấu trúc nền                                    |
| Evaluation Criteria          | Người đọc mục tiêu có hiểu được mà vẫn giữ đúng logic chính không?                             |
| Kỹ thuật liên quan           | Audience Framing, Compression & Expansion                                                       |
| Builder Relevance            | Rất quan trọng trong AI tutor / coach design                                                    |

### 7.6. Knowledge System Design (Basic)

| Trường                       | Nội dung                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Tên kỹ thuật                 | Knowledge System Design (Basic)                                                                 |
| Tier                         | Tier 4                                                                                           |
| Level SID                    | L6                                                                                               |
| Định nghĩa ngắn             | Tổ chức một miền tri thức thành một hệ có mục tiêu, cấu trúc, workflow và outputs              |
| Dùng để làm gì               | Đi từ tài liệu đơn lẻ sang hệ sử dụng lâu dài                                                   |
| Dùng khi nào                 | Cuối khóa, cuối dự án, khi xây playbook hoặc domain knowledge system                            |
| Không nên dùng khi nào       | Khi material còn rời rạc và chưa đủ chín                                                         |
| Prompt / Usage Pattern       | “Hãy thiết kế một knowledge system cho domain này gồm: audience, modules, workflows, artifacts, checklist và rubric.” |
| Failure Modes / Anti-patterns | Gom tài liệu chứ không thành hệ; thiếu mục tiêu; không có workflow sử dụng                     |
| Evaluation Criteria          | Hệ này có thể dùng lặp lại, dạy lại và mở rộng được không?                                      |
| Kỹ thuật liên quan           | Framework Synthesis, Workflow Design, Rubric Design                                             |
| Builder Relevance            | Cầu nối trực tiếp sang Expert Builder Track                                                     |

---

## 8. Bảng progression rút gọn toàn bộ library

| Tier   | Kỹ thuật cốt lõi                                                                                         | Output mong đợi                                                   |
| ------ | -------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| Tier 1 | Problem framing, goal framing, audience framing, scope design, decomposition, taxonomy, hierarchy, table schema | Prompt rõ, outline rõ, cấu trúc rõ                                |
| Tier 2 | Breadth-first, depth-first, query expansion, comparative, causal, hypothesis-driven, basic ToT           | Phân tích sâu và rộng đúng chỗ                                   |
| Tier 3 | Self-critique, contradiction check, assumption check, gap detection, triangulation, confidence labeling, pattern extraction, principle extraction, framework synthesis | Output đáng tin hơn và framework hóa được                        |
| Tier 4 | Workflow design, use-case mapping, checklist design, rubric design, teaching translation, knowledge system design | Tri thức dùng được, dạy được, vận hành được                      |

---

## 9. Cách gắn library này vào SID Syllabus

### Session 1–2

Dùng kỹ thuật Tier 1:

- Problem Framing  
- Goal Framing  
- Audience Framing  
- Scope Design  
- Output Framing  

### Session 3–4

Dùng kỹ thuật Tier 1 tiếp:

- Top-down Decomposition  
- Taxonomy Building  
- Hierarchy Design  
- Table Schema Design  

### Session 5–6

Dùng kỹ thuật Tier 2:

- Breadth-first Exploration  
- Depth-first Exploration  
- Query Expansion  
- Comparative Reasoning  
- Causal Reasoning  
- Hypothesis-driven Reasoning  
- Basic ToT  

### Session 7

Dùng kỹ thuật Tier 3:

- Self-critique  
- Contradiction Check  
- Assumption Check  
- Gap Detection  
- Triangulation  
- Confidence Labeling  

### Session 8

Dùng kỹ thuật Tier 3–4:

- Pattern Extraction  
- Principle Extraction  
- Framework Synthesis  
- Workflow Design  
- Use-case Mapping  
- Checklist / Rubric Design  

---

## 10. Bridge to SID Expert Builder Track

Một số kỹ thuật trong library này là cầu nối trực tiếp sang khóa expert.

| Kỹ thuật trong Library v2 | Ứng dụng ở Builder Track                       |
| ------------------------- | ---------------------------------------------- |
| Audience Framing          | Xác định người dùng của Gem / GPT             |
| Scope Design              | Xác định domain boundary                      |
| Output Framing            | Thiết kế response contract                    |
| Hierarchy Design          | Thiết kế instruction hierarchy                |
| Table Schema Design       | Thiết kế evaluation sheet                     |
| Query Expansion           | Retrieval query design                        |
| Comparative Reasoning     | Model/tool comparison                         |
| Assumption Check          | Safety / boundary analysis                    |
| Confidence Labeling       | Trustworthy answer design                     |
| Framework Synthesis       | System behavior design                        |
| Workflow Design           | Multi-step assistant flows                    |
| Rubric Design             | Evaluation and testing                        |
| Knowledge System Design   | Nền cho GPT / RAG / tutor architecture        |

---

## 11. Cách dùng library này để luyện thành kỹ năng thật

Người học không nên chỉ đọc library.  
Nên luyện theo 4 vòng:

### Vòng 1 — Nhận diện

- Kỹ thuật này giải quyết bài toán gì?  
- Tôi đang thiếu kỹ thuật nào?  

### Vòng 2 — Dùng riêng lẻ

- Áp một kỹ thuật vào một bài toán cụ thể  
- Xem output khác gì trước  

### Vòng 3 — Kết hợp kỹ thuật

- Framing + decomposition  
- Breadth + depth  
- Hypothesis + validation  
- Synthesis + workflow  

### Vòng 4 — Tái sử dụng có ý thức

- Biến thành template riêng  
- Biến thành prompt stack  
- Biến thành SOP cá nhân  
- Biến thành logic cho GPT/Gem/RAG  

---

## 12. Kết luận

SID Technique Library v2 không được thiết kế như một danh sách “mẹo prompt”.

Nó là một thư viện năng lực theo progression, giúp người học:

- Đặt câu hỏi đúng hơn  
- Cấu trúc thông tin rõ hơn  
- Suy luận sâu hơn  
- Kiểm định chặt hơn  
- Tổng hợp thành framework tốt hơn  
- Và tiến dần tới khả năng thiết kế hệ tri thức bằng AI  

Nói gọn:

- **Tier 1** dạy đặt khung đúng.  
- **Tier 2** dạy phân tích đúng.  
- **Tier 3** dạy nghi ngờ và tổng hợp đúng.  
- **Tier 4** dạy biến tri thức thành hệ dùng được.  

Đó là progression chuẩn của SID Technique Library v2.
