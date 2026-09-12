# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Trần Mạnh Tùng
- Mã học viên: 2A202602879
- Vai trò / bối cảnh (VD: sinh viên năm X, intern PM, ...): Sinh viên năm cuối ngành Trí tuệ Nhân tạo (AI), đang tham gia chương trình đào tạo & dự án "AI thực chiến" tại Vingroup (xây dựng các bài toán Computer Vision / NLP / LLM phục vụ sản phẩm thực tế).
- Công việc hằng tuần (3-5 gạch đầu dòng để soi problem):
  - Thu thập, làm sạch và khử trùng lặp dữ liệu thị giác / văn bản (Data cleansing & QA) trước khi nạp vào pipeline huấn luyện.
  - Xây dựng, tinh chỉnh và đánh giá chất lượng (Eval & Hallucination) cho các mô hình RAG / Chatbot tra cứu thông tin.
  - Huấn luyện thử nghiệm, tối ưu hóa và lượng tử hóa mô hình (TensorRT/ONNX) để chạy trên thiết bị nhúng / edge devices.
  - Đóng gói mô hình thành dịch vụ API backend (FastAPI) và phối hợp bàn giao cho nhóm phát triển Mobile/Web App.
  - Khảo sát các kiến trúc mô hình mã nguồn mở mới (Open-Source SOTA) trên Hugging Face để đề xuất giải pháp cho dự án.

---

## Phase 1 — Scan 5+ problems (tối thiểu 5, khuyến khích 8-10)

**Cách điền:** mỗi dòng = việc gì + ai chịu + đo bằng gì. Cột `Dấu hiệu thật` bắt buộc có số: mất bao lâu (bấm giờ mấy lần), mấy lần/tuần, bao nhiêu người gặp, log/ticket/quote nào.

| # | Lăng kính (Lặp lại / Tốn thời gian / AI có thể tốt hơn / Pain từ người khác) | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật (số + bằng chứng) |
|---|---|---|---|---|
| 1 | Tốn thời gian | Lọc và khử trùng lặp dữ liệu ảnh/video (Data De-duplication) trước khi gửi cho đội gán nhãn | Sinh viên AI phụ trách Data Pipeline | 10,000 frames trích từ video camera giao thông tĩnh có 70-80% frame trùng (xe dừng đèn đỏ); mất 3-4 tiếng/tuần lọc tay, gây phát sinh 30-40% chi phí và thời gian gán nhãn thừa |
| 2 | AI có thể tốt hơn | Đánh giá chất lượng và phát hiện ảo giác (Eval & Hallucination QA) cho mô hình Chatbot/RAG sau mỗi lần cập nhật prompt hoặc tài liệu | Sinh viên AI phát triển RAG/GenAI | Mất 2.5 tiếng/lần (2 lần/sprint) chấm điểm thủ công bộ 50 câu benchmark; người kiểm tra dễ mệt mỏi và bỏ sót lỗi hallucination ở các câu trả lời dài |
| 3 | Tốn thời gian | Benchmark độ trễ, RAM và độ suy giảm accuracy khi convert và lượng tử hóa mô hình (TensorRT/ONNX) cho thiết bị nhúng | Học viên AI phụ trách Edge Deployment | Mất 3-4 tiếng mỗi lần convert vì phải đo thủ công từng mức quantization (FP16/INT8) trên phần cứng target; lặp lại 2 lần/tuần trước hạn demo |
| 4 | Pain từ người khác | Nhóm Mobile/Frontend liên tục hỏi lại định dạng input/output API (schema mismatch) do tài liệu Notion lỗi thời so với code backend | Sinh viên AI & nhóm Mobile/Frontend (3-4 người) | Mất 30-45 phút mỗi lần họp sync (2-3 lần/tuần); 1-2 ngày trước hạn demo hay bị vỡ trận vì schema backend thay đổi nhưng tài liệu chưa cập nhật |
| 5 | Lặp lại | Khảo sát và lập bảng so sánh nhanh các mô hình Open-Source mới ra mắt trên Hugging Face (VRAM, license, benchmark tiếng Việt) | Sinh viên / Intern AI đề xuất kiến trúc | Mất 2-3 tiếng mỗi sáng thứ Hai lướt HuggingFace, PapersWithCode để trả lời câu hỏi của Tech Lead về khả năng ứng dụng model mới vào dự án |

**AI đã dùng ở Phase 1 (nếu có):**
- Prompt đã hỏi: *"Tôi là sinh viên năm cuối ngành AI đang tham gia chương trình AI thực chiến tại Vingroup, công việc liên quan đến CV, RAG, Edge Deployment và API handoff. Hãy gợi ý 5 vấn đề thực tế nhất bám sát 4 lăng kính: lặp lại, tốn thời gian, AI có thể tốt hơn, pain từ người khác, tuyệt đối không trùng với ví dụ Weekly Report."*
- Ý dùng được: Vấn đề khử trùng lặp ảnh camera giao thông (Data De-duplication) và đánh giá ảo giác RAG (Hallucination QA) — đây là hai bài toán rất đắt giá và đúng trọng tâm kỹ thuật hiện đại.
- Ý bỏ vì không phải pain thật: Ý tưởng *"AI tự động code hoàn chỉnh toàn bộ ứng dụng Mobile"* — bỏ vì không thực tế, sai phạm vi chuyên môn AI và mang tính giải pháp viển vông.

**Self-check Phase 1:**
- [x] Đủ 5+ dòng, mỗi dòng có actor + số đo cụ thể (đúng 5 vấn đề cốt lõi, không dàn trải)
- [x] Dùng ít nhất 3/4 lăng kính (bao phủ trọn vẹn cả 4 lăng kính: Lặp lại, Tốn thời gian, AI có thể tốt hơn, Pain từ người khác)
- [x] Không có dòng chung chung kiểu "mất nhiều thời gian" (mỗi dòng đều có số phút, số giờ, tần suất hoặc tỷ lệ % rõ ràng)

---

## Phase 2 — Top 3 Problem Cards

### 2.1. Chọn top 3

Giữ bài nào: actor cụ thể, workflow vẽ được 3-7 bước, bottleneck ở 1 bước, impact đo được. Loại bài quá rộng.

| Rank | Problem (copy từ bảng scan) | Vì sao chọn (2-3 ý) | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Đánh giá chất lượng và phát hiện ảo giác (Eval & Hallucination QA) cho mô hình Chatbot/RAG | Vấn đề sống còn của sản phẩm GenAI; đo lường được bằng thời gian test (từ 150' xuống 30') và tỷ lệ phát hiện hallucination; workflow đánh giá rất mạch lạc | Cần kiểm soát thiên kiến tự khen (self-preference bias) khi dùng LLM-as-a-Judge |
| 2 | Lọc và khử trùng lặp dữ liệu ảnh/video (Data De-duplication) trước khi gửi cho đội gán nhãn | Tiết kiệm trực tiếp 3-4 tiếng/tuần và giảm 30-40% chi phí gán nhãn; giải quyết triệt để nguyên tắc "Garbage in, Garbage out"; ranh giới thuật toán rất rõ | Cần chọn ngưỡng tương đồng (cosine similarity threshold) phù hợp để không xóa nhầm các mẫu edge cases hiếm |
| 3 | Nhóm Mobile/Frontend liên tục hỏi lại định dạng input/output API (schema mismatch) do tài liệu Notion lỗi thời | Giải quyết điểm nghẽn hand-off kinh điển giữa nhóm AI và nhóm App; minh chứng xuất sắc cho nguyên tắc "Không cần AI vẫn là kết luận tốt" (chọn Process/Rule thay vì nhồi AI) | Cần thống nhất nhóm tuân thủ viết docstrings/type-hints chuẩn trong code FastAPI |

---

### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

#### Problem Card #1 — Đánh giá chất lượng và phát hiện ảo giác (Eval & Hallucination QA) cho Chatbot/RAG

```text
Problem 1 câu:
Mỗi lần cập nhật prompt hoặc tri thức mới, sinh viên AI mất 2.5 tiếng đọc đối chiếu thủ công 50 câu benchmark để phát hiện ảo giác (hallucination) và câu trả lời sai lệch, dễ bị sót lỗi ở các văn bản dài.

Actor:
Sinh viên AI phát triển và kiểm định chất lượng hệ thống RAG / Chatbot.

Thời điểm / bối cảnh:
Cuối mỗi chu kỳ cập nhật dữ liệu hoặc khi chuẩn bị release phiên bản chatbot mới cho người dùng nội bộ.

Current workflow 3-7 bước:
1. Chạy pipeline RAG để sinh câu trả lời cho bộ 50 câu hỏi benchmark (10')
2. Đọc đối chiếu từng câu trả lời với các đoạn trích tài liệu gốc được truy xuất (Retrieved Chunks) để phát hiện thông tin bị bịa hoặc suy diễn sai (120')
3. Chấm điểm thủ công độ chính xác và độ liên quan của câu trả lời vào Google Sheets (15')
4. Tổng hợp tỷ lệ đạt chuẩn và ghi chú các ca lỗi nghiêm trọng gửi team lead (15')

Bottleneck:
Bước 2 — Đọc đối chiếu thủ công 50 câu văn bản dài với tài liệu gốc mất 120 phút, người kiểm tra bị quá tải thị giác và dễ bỏ sót các lỗi ảo giác tinh vi.

Impact:
Mất 2.5 tiếng/lần (5 tiếng/sprint). Sót lỗi ảo giác khiến chatbot cung cấp thông tin sai lệch cho người dùng nội bộ, làm mất độ tin cậy của toàn bộ sản phẩm.

Success metric:
Giảm thời gian đánh giá từ 150 phút xuống dưới 30 phút; tăng độ phủ phát hiện lỗi ảo giác lên >95% trên bộ benchmark; 100% các lần cập nhật đều được test trước khi release.

Non-AI alternative:
Dùng Keyword Matching / Regex hoặc tính điểm ROUGE/BLEU so với câu trả lời mẫu. Không hiệu quả vì chỉ so khớp mặt chữ thô sơ, không hiểu được sự thật ngữ nghĩa (Semantic Faithfulness) trong tài liệu.

AI hypothesis:
Sử dụng phương pháp LLM-as-a-Judge (áp dụng các tiêu chí chuẩn RAGAS: Faithfulness, Answer Relevance) để tự động chấm điểm sơ bộ toàn bộ 50 câu, tự động gắn cờ các câu có điểm nghi vấn; con người chỉ thẩm định lại các câu bị gắn cờ.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #1**:

```text
CURRENT STATE — 150 phút

[1 Chạy sinh câu trả lời: 10'] → [2 Đọc đối chiếu thủ công 50 câu: 120'] (Bottleneck) → [3 Chấm điểm vào sheet: 15'] → [4 Báo cáo team lead: 15']

FUTURE STATE — 30 phút

[1 Chạy LLM-as-a-Judge chấm sơ bộ 50 câu theo tiêu chí Faithfulness: 5'] → [2 Hệ thống lọc ra Top 10% câu có điểm nghi vấn: 2'] → [3 Human Review: chuyên gia chỉ thẩm định 5-7 câu bị gắn cờ: 18'] (Human boundary) → [4 Xuất báo cáo Eval tự động: 5']

Fallback: Nếu LLM judge hoạt động chập chờn hoặc không nhất quán, quay về quy trình chấm thủ công trên tập con rút gọn gồm 10 câu hỏi nghiệp vụ quan trọng nhất (vẫn kiểm soát được rủi ro chính trong 25 phút).
```

---

#### Problem Card #2 — Lọc và khử trùng lặp dữ liệu ảnh/video (Data De-duplication) trước khi gán nhãn

```text
Problem 1 câu:
Sinh viên phụ trách dữ liệu mất 3-4 tiếng/tuần lọc bỏ thủ công các khung hình trùng lặp từ 10,000 frames video camera giao thông tĩnh, làm phát sinh 30-40% chi phí và thời gian gán nhãn dư thừa.

Actor:
Sinh viên AI phụ trách Data Pipeline & Computer Vision.

Thời điểm / bối cảnh:
Mỗi đợt tiếp nhận video mới từ camera giám sát trước khi gửi dữ liệu cho đội ngũ gán nhãn (Annotators).

Current workflow 3-7 bước:
1. Chạy script cắt video 30 FPS thành tập hợp 10,000 ảnh rời (15')
2. Mở từng thư mục ảnh, cuộn chuột nhìn bằng mắt để tìm và xóa thủ công các ảnh xe đứng chờ đèn đỏ hoặc khung cảnh tĩnh giống hệt nhau (180')
3. Đếm lại số lượng ảnh còn lại và kiểm tra ngẫu nhiên xem có xóa nhầm ảnh quan trọng không (20')
4. Đóng gói dữ liệu sạch và gửi kèm hướng dẫn cho đội gán nhãn (15')

Bottleneck:
Bước 2 — Mở xem và xóa thủ công hàng nghìn ảnh tương đồng mất 180 phút, cực kỳ nhàm chán, mỏi mắt và vẫn bỏ sót nhiều ảnh trùng.

Impact:
Lãng phí 3-4 tiếng mỗi tuần cho sinh viên; đội gán nhãn phải làm việc thừa với các khung hình giống nhau, làm đội chi phí gán nhãn thêm 30-40% và kéo dài thời gian hoàn thành dataset thêm 2-3 ngày.

Success metric:
Giảm thời gian lọc dữ liệu từ 180 phút xuống dưới 20 phút; tự động loại bỏ >90% ảnh trùng lặp; tỷ lệ xóa nhầm các trường hợp biên (edge cases) dưới 1%.

Non-AI alternative:
So sánh độ chênh lệch điểm ảnh thô (Pixel Mean Squared Error hoặc SSIM). Nhược điểm: rất nhạy cảm với nhiễu hạt camera và sự thay đổi ánh sáng mặt trời, dẫn đến lọc sai hoặc bỏ sót nhiều.

AI hypothesis:
Sử dụng mô hình Vision Embedding nhẹ (như DINOv2 / MobileNet) để trích xuất đặc trưng hình ảnh, sau đó dùng thuật toán gom cụm (Clustering / Cosine Distance Threshold) để tự động giữ lại 1 ảnh đại diện cho mỗi cụm ảnh giống nhau.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #2**:

```text
CURRENT STATE — 230 phút

[1 Cắt video thành 10k frames: 15'] → [2 Lọc mắt & xóa ảnh trùng thủ công: 180'] (Bottleneck) → [3 Kiểm tra ngẫu nhiên: 20'] → [4 Đóng gói gửi annotators: 15']

FUTURE STATE — 35 phút

[1 Trích xuất vector embedding bằng mô hình thị giác nhẹ: 10'] → [2 Gom cụm & tự động loại bỏ ảnh có Cosine Similarity > 0.95: 5'] → [3 Human Review: kiểm tra nhanh 50 ảnh ở ngưỡng ranh giới (borderline): 15'] (Human boundary) → [4 Đóng gói dataset sạch: 5']

Fallback: Nếu mô hình embedding gặp lỗi môi trường phần cứng, chuyển sang chạy script so sánh sai khác histogram màu kết hợp hash ảnh (pHash) với ngưỡng an toàn để lọc tạm thời.
```

---

#### Problem Card #3 — Đồng bộ tài liệu API Spec giữa nhóm AI và nhóm Mobile/Frontend

```text
Problem 1 câu:
Mỗi lần cập nhật code backend mô hình, sinh viên AI mất 45 phút viết lại tài liệu schema trên Notion; nhóm Mobile liên tục nhắn tin hỏi lại và hệ thống bị vỡ trận khi tích hợp sát ngày demo.

Actor:
Sinh viên AI chịu trách nhiệm đóng gói backend (FastAPI) bàn giao cho thành viên phát triển Mobile/Web App.

Thời điểm / bối cảnh:
Mỗi sprint tích hợp khi mô hình AI có thêm tham số mới hoặc thay đổi cấu trúc dữ liệu đầu ra.

Current workflow 3-7 bước:
1. Chỉnh sửa code inference và cập nhật endpoint trong FastAPI (30')
2. Mở Notion để viết lại thủ công tài liệu mô tả input/output JSON schema và các mã lỗi (45')
3. Nhắn tin lên nhóm chat thông báo API đã đổi và giải thích cách gọi cho nhóm Mobile (15')
4. Nhóm Mobile gặp lỗi khi tích hợp, sinh viên AI phải ngồi debug chung qua Google Meet để đối chiếu từng trường dữ liệu (45')

Bottleneck:
Bước 2 & 4 — Viết tài liệu thủ công trên Notion tốn 45 phút và hay bị lệch pha so với code thực tế; dẫn đến mất thêm 45 phút họp giải thích và debug định dạng dữ liệu.

Impact:
Mất hơn 2 tiếng mỗi lần cập nhật API (xảy ra 2-3 lần/sprint); gây ức chế và mâu thuẫn nội bộ trong nhóm dự án, trễ hạn demo sản phẩm.

Success metric:
Giảm thời gian viết tài liệu và giải thích từ 90 phút xuống dưới 10 phút; loại bỏ 100% lỗi schema mismatch khi ghép code giữa AI và Mobile.

Non-AI alternative:
Áp dụng quy chuẩn Pydantic Models nghiêm ngặt trong FastAPI để hệ thống tự động sinh tài liệu Swagger / OpenAPI chuẩn mực (/docs) kèm nút "Try it out" thực tế. Không cần dùng đến AI!

AI hypothesis:
Dùng LLM để đọc code và sinh tài liệu. Tuy nhiên, phân tích kỹ cho thấy việc dùng OpenAPI chuẩn của framework là giải pháp tối ưu, chính xác 100% và không có rủi ro hallucination. Đây là trường hợp không cần dùng AI!

Quick gut:
[x] No AI / process fix
[ ] Rule
[ ] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #3**:

```text
CURRENT STATE — 135 phút

[1 Code endpoint: 30'] → [2 Viết doc Notion thủ công: 45'] (Bottleneck) → [3 Chat thông báo: 15'] → [4 Họp debug lỗi lệch schema: 45']

FUTURE STATE — 35 phút

[1 Định nghĩa Pydantic Schema chuẩn trong FastAPI: 30'] → [2 Framework tự động sinh Swagger UI / OpenAPI docs: 0'] → [3 Human Review: gửi link Swagger trực tiếp cho nhóm Mobile tự test: 5'] (Human boundary / Process fix)

Fallback: Nếu phía Mobile cần file spec dạng Postman Collection, chạy script một dòng lệnh xuất OpenAPI JSON sang Postman Collection trong 1 phút.
```

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card tôi muốn pitch nhất:**

```text
Problem Card #1 — Đánh giá chất lượng và phát hiện ảo giác (Eval & Hallucination QA) cho Chatbot/RAG.
```

**Vì sao (2-3 câu: workflow gì, số đo gì, impact gì):**

```text
Đây là bài toán chạm đúng "tử huyệt" kỹ thuật của làn sóng GenAI hiện nay: làm sao kiểm soát được ảo giác mô hình mà không kiệt sức vì đọc đối chiếu thủ công 50 câu benchmark. Giải pháp giúp cắt giảm thời gian kiểm thử từ 150 phút xuống còn 30 phút, đồng thời tăng độ phủ phát hiện lỗi lên trên 95%. Bài toán phân định ranh giới cực kỳ chuẩn xác: AI làm nhiệm vụ sàng lọc sơ bộ (Judge), còn con người nắm quyền thẩm phán tối cao ở các ca nghi vấn.
```

**Câu hỏi tôi muốn nhóm challenge (1-2 câu hỏi đúng chỗ yếu):**

```text
1. "Làm sao đảm bảo LLM-as-a-Judge không bị thiên kiến tự khen câu trả lời của mô hình cùng họ (Self-preference bias) khi chấm điểm?"
2. "Nếu câu hỏi trong bộ benchmark đòi hỏi suy luận logic phức tạp nhiều bước, liệu con số đánh giá từ AI có đáng tin cậy hơn con người đọc trực tiếp không?"
```

**AI phản biện Card (nếu có):**
- Điểm yếu AI chỉ ra: AI cảnh báo rằng nếu để LLM tự động quyết định release mô hình (Autonomous QA Agent) thì rủi ro sai sót lọt lưới là rất lớn vì LLM có thể bị đánh lừa bởi câu trả lời trôi chảy nhưng sai sự thật.
- Tôi sửa gì: Kiên quyết giữ mô hình **Workflow có Human-in-the-loop**, quy định rõ con người phải dành 18 phút thẩm định lại toàn bộ các câu bị gắn cờ cảnh báo trước khi cấp phép release.

### Self-check nộp phần 01
- [x] Có 5+ problems + top 3 Cards đủ field (đúng 5 problems cốt lõi + 3 Cards đầy đủ các trường)
- [x] Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [x] Đã chọn 1 card pitch + câu hỏi challenge
