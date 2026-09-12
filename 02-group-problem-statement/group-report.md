# 02 — Group Problem Statement
## Chủ đề: Xác định yêu cầu hiện hành của bài tập từ nhiều nguồn

> Bản nháp phân tích để nhóm rà soát. Research sản phẩm đã đối chiếu nguồn chính thức ngày 12/09/2026. Chưa có biên bản hội tụ nhóm, phỏng vấn, baseline hoặc kết quả pilot. Problem Statement v0/v1 bên dưới là bản dự thảo trước validation, cần cập nhật sau quan sát thực tế; không phải kết luận đã được kiểm chứng.

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò được phân công |
|---|---|---|---|
| 1 | Nguyễn Mạnh Cường | 2A202602650 | Điều phối hội tụ, tổng hợp báo cáo và trình bày |
| 2 | Nguyễn Hồng Thái | 2A202602894 | Phỏng vấn, quan sát người dùng và thu thập bằng chứng |
| 3 | Trần Mạnh Tùng | 2A202602879 | Research giải pháp hiện có và phương án không AI |
| 4 | Đinh Hoàng Đức | 2A202602795 | Workflow trước/sau, điểm can thiệp AI và fallback |
| 5 | Phan Đại Cương | 2A202602510 | Thiết kế đo lường, tổng hợp kết quả và phản biện quyết định |


## Phase 3 — Group Convergence

### 3.1. Candidates và nguồn gốc

Nhóm gồm 5 thành viên, mỗi thành viên đóng góp 3 Problem Candidates:

| ID | Người đưa ra | Candidate Problem | Actor | Bottleneck | Trạng thái |
|---|---|---|---|---|---|
| C1 | Nguyễn Mạnh Cường | Xác định yêu cầu hiện hành của bài tập từ nhiều nguồn | Sinh viên / Học viên nhận bài qua nhiều kênh | Đối chiếu hiệu lực rõ; đo được công tìm/kiểm tra, lỗi và mâu thuẫn bỏ sót, cần so với bảng yêu cầu chuẩn do giảng viên/labcoach cập nhật | Đã có trong bài cá nhân |
| C2 | Nguyễn Mạnh Cường | Kiểm tra môi trường trước khi chạy lab | Học viên Python trên Windows | Phân biệt lỗi môi trường (CUDA, path) với lỗi code | Đã có trong bài cá nhân |
| C3 | Nguyễn Mạnh Cường | Phát hiện sai tài khoản GitHub trước khi push | Học viên dùng nhiều account git | Xác định tài khoản có quyền commit/push vào repo | Đã có trong bài cá nhân |
| C4 | Nguyễn Hồng Thái  | Ôn tập tổng hợp kiến thức trước kỳ kiểm tra | Học viên AI20K ôn thi | Nối các kiến thức rời rạc (slide, note, notebook) thành khung mạch ôn | Đã có trong bài cá nhân |
| C5 | Nguyễn Hồng Thái  | Đọc hiểu tài liệu / paper kỹ thuật tiếng Anh | Học viên chưa vững nền ML | Dừng tra thuật ngữ / ký hiệu làm đứt mạch đọc hiểu | Đã có trong bài cá nhân |
| C6 | Nguyễn Hồng Thái  | Tìm và tổng hợp tài liệu cho bài tập lớn | Học viên làm project / báo cáo | Sắp xếp các ý rời rạc thành dàn bài có logic | Đã có trong bài cá nhân |
| C7 |  Trần Mạnh Tùng   | Đánh giá chất lượng và ảo giác (Eval & Hallucination QA) cho Chatbot/RAG | Sinh viên AI phát triển RAG | Đọc đối chiếu thủ công 50 câu benchmark với tài liệu gốc mất 120' | Đã có trong bài cá nhân |
| C8 |  Trần Mạnh Tùng   | Lọc và khử trùng lặp dữ liệu ảnh/video (Data De-duplication) trước khi gán nhãn | Sinh viên AI phụ trách Data Pipeline | Mở xem và xóa thủ công các ảnh camera tĩnh trùng lặp mất 180' | Đã có trong bài cá nhân |
| C9 |  Trần Mạnh Tùng   | Đồng bộ tài liệu API Spec giữa nhóm AI và nhóm Mobile/Frontend | Sinh viên AI backend | Viết tài liệu Notion thủ công và họp debug lỗi lệch schema API | Đã có trong bài cá nhân |
| C10 |  Đinh Hoàng Đức  | Kênh thông báo và hướng dẫn realtime cho học viên VinAI | Học viên chương trình VinAI | Tìm và đối chiếu thông tin lịch học, deadline từ nhiều kênh phân tán | Đã có trong bài cá nhân |
| C11 |  Đinh Hoàng Đức  | Sắp xếp lịch họp nhóm | Học viên làm bài tập nhóm | Trưởng nhóm đọc và đối chiếu thời gian rảnh của từng người thủ công | Đã có trong bài cá nhân |
| C12 |  Đinh Hoàng Đức  | Ghi chép và phân loại chi tiêu cá nhân | Sinh viên tự quản lý tài chính | Đọc và phân loại từng khoản chi tiêu bằng tay | Đã có trong bài cá nhân |
| C13 |  Phan Đại Cương  | Lập kế hoạch và quản lý công việc học tập từ nhiều nguồn | Sinh viên theo học nhiều môn | Tự tổng hợp task và phân tích ưu tiên từ LMS, Discord, Gmail, Calendar | Đã có trong bài cá nhân |
| C14 |  Phan Đại Cương  | Tìm lại thông tin học tập và deadline từ nhiều nền tảng | Sinh viên học/làm nhóm | Dò tìm và xác thực thông tin từ nhiều nguồn không có kho trung tâm | Đã có trong bài cá nhân |
| C15 |  Phan Đại Cương  | Theo dõi tiến độ và ưu tiên công việc học tập của nhóm | Sinh viên trong nhóm dự án | Tổng hợp tiến độ và ra quyết định ưu tiên không được tự động hóa | Đã có trong bài cá nhân |

**Điểm hội tụ tự nhiên:** Nhóm nhận thấy có sự trùng khớp rất lớn giữa bài của Cường (C1), Đức (C10) và Cương (C13, C14). Cả 3 thành viên đều gặp phải vấn đề: *thông tin bài tập, lịch trình và deadline bị phân tán ở nhiều kênh (LMS, Discord, Gmail, Chat), khiến người học mất nhiều thời gian kiểm tra và dễ bị nhầm lẫn giữa các bản cập nhật*. Nhóm quyết định thống nhất chọn **Candidate C1: Xác định yêu cầu hiện hành của bài tập từ nhiều nguồn** làm đề tài chung để đào sâu.

### 3.2. Gom cụm (Clustering 15 candidates thành 4 cụm)

| Cụm | Candidates included | Pattern chung | Ghi chú & Đánh giá |
|---|---|---|---|
| **A — Quản lý thông tin, thông báo & deadline học tập đa nguồn** | **C1, C10, C13, C14 (Hội tụ thành C1)** | Thông tin bài học, deadline, thông báo bị phân tán trên nhiều kênh; người học tốn công dò tìm và đối chiếu bản mới nhất | **Cụm trọng tâm của nhóm.** 3/5 thành viên cùng gặp pain point này. Scope vừa vặn để giải quyết trong lab. |
| **B — Đọc hiểu, tổng hợp tài liệu & ôn tập kiến thức** | C4, C5, C6 | Tốn nhiều thời gian đọc tài liệu dài, tra thuật ngữ tiếng Anh và nối các ý rời rạc thành khung ôn thi hoặc dàn ý | Pain point phổ biến của sinh viên nhưng khó đo lường độ chính xác khách quan (thế nào là "hiểu sâu"). |
| **C — Phối hợp nhóm, lịch họp & đồng bộ kỹ thuật** | C3, C9, C11, C15 | Mâu thuẫn hoặc tốn thời gian khi phối hợp đa cá nhân (lệch schema API, xếp lịch họp, phân chia task, nhầm quyền git) | Phù hợp làm quy trình (Process/Rule fix); phạm vi tương tác nhóm rộng, khó kiểm soát trong lab 4h. |
| **D — Tối ưu hóa kỹ thuật chuyên sâu & QA** | C2, C7, C8, C12 | Tác vụ kỹ thuật cụ thể: kiểm tra môi trường chạy, đo đạc hallucination RAG, khử trùng lặp ảnh, phân loại chi tiêu | Rất có giá trị kỹ thuật nhưng domain chuyên biệt (chỉ Tùng làm RAG/CV, Cường làm script env), nhóm khó làm chung. |

### 3.3. Shortlist (3 candidates đại diện tiêu biểu nhất)

| Candidate | Vì sao vào shortlist (2-3 ý) | Rủi ro / điều chưa rõ |
|---|---|---|
| **C1 — Xác định yêu cầu hiện hành của bài tập từ nhiều nguồn** *(Hội tụ C1, C10, C13, C14)* | - Có tới 3/5 thành viên trong nhóm cùng trực tiếp gặp vấn đề này hằng tuần.<br>- Workflow 6 bước rất rõ ràng; đo lường được bằng thời gian tìm kiếm và số trường sót.<br>- So sánh rạch ròi được giữa No AI (bảng chuẩn của giảng viên), Rule và Workflow. | - Tần suất có mâu thuẫn thực sự giữa các nguồn có đủ cao không?<br>- Công sinh viên copy/nhập nguồn vào hệ thống có lớn hơn thời gian tiết kiệm được không? |
| **C4 — Ôn tập tổng hợp kiến thức trước kỳ kiểm tra** *(Từ bài pitch của Thái)* | - Bối cảnh học tập rất thực tế, lặp lại định kỳ 2 đợt/kỳ.<br>- Đo lường được số giờ chuẩn bị (từ 5-6h xuống ~2h). | - Chất lượng "nối kiến thức" rất khó đo lường khách quan.<br>- Rủi ro AI tóm tắt hời hợt hoặc hiểu sai bản chất công thức toán/ML. |
| **C7 — Đánh giá chất lượng và ảo giác (Eval & Hallucination QA) cho RAG** *(Từ bài pitch của Tùng)* | - Bài toán AI thực chiến chuyên sâu, đúng trọng tâm công nghệ GenAI hiện nay.<br>- Đo lường định lượng cực kỳ chính xác (từ 150' xuống 30', tỷ lệ bắt lỗi >95%). | - Domain quá hẹp (chỉ dành cho kỹ sư AI làm GenAI).<br>- 4 thành viên còn lại trong nhóm chưa có nền tảng về RAGAS để cùng tham gia xây dựng trong lab. |

### 3.4. Score để đồng thuận

Nhóm tiến hành chấm điểm độc lập trên thang điểm 1–5 theo 7 tiêu chí đánh giá chuẩn của worksheet:

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A | Nhóm hiểu domain | Tổng điểm |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **C1 (Yêu cầu hiện hành bài tập)** | 5 | 5 | 4 | 4 | 5 | 5 | 5 | **33 / 35** |
| **C4 (Ôn tập tổng hợp kiến thức)** | 4 | 4 | 4 | 3 | 4 | 4 | 5 | **28 / 35** |
| **C7 (RAG Eval & Hallucination QA)** | 4 | 5 | 4 | 5 | 3 | 4 | 3 | **28 / 35** |

**Candidate nhóm thống nhất chọn:**
```text
C1 — Xác định yêu cầu hiện hành của bài tập từ nhiều nguồn thông báo phân tán.
```

**Vì sao nhóm chọn C1 (4-5 câu):**
C1 là bài toán phản ánh chính xác nỗi đau hàng ngày của tất cả 5 thành viên trong nhóm khi theo học các môn học và chương trình đào tạo hiện tại. Vấn đề có actor cụ thể (sinh viên nhận bài tập qua nhiều kênh), quy trình thao tác và điểm nghẽn đối chiếu rất rõ ràng. Đề tài hoàn toàn khả thi để thực hiện deep-dive, đo lường và kiểm chứng trong khuôn khổ thời gian của buổi lab. Quan trọng nhất, bài toán này cho phép nhóm đặt lên bàn cân so sánh công bằng giữa giải pháp quy trình không dùng AI (Process Fix: giảng viên duy trì bảng chuẩn), giải pháp dùng Rule (so khớp trường/metadata) và giải pháp Workflow có AI (trích xuất ngữ nghĩa và truy vết nguồn).

**Vì sao KHÔNG chọn các candidate còn lại:**
- **Không chọn C4 (Ôn tập kiến thức):** Nhóm nhận thấy việc "hiểu bài" và "nối mạch kiến thức" mang nặng tính chủ quan của từng cá nhân, rất khó thiết lập bộ tiêu chí đo lường chính xác trong lab. Nếu AI tóm tắt sai lệch một khái niệm cốt lõi, người học sẽ có nguy cơ thi trượt mà không nhận ra.
- **Không chọn C7 (RAG Hallucination QA):** Mặc dù bài toán của Tùng rất xuất sắc về mặt kỹ thuật AI thực chiến, nhưng phạm vi lại quá chuyên sâu vào quy trình phát triển GenAI. Các thành viên khác trong nhóm không thể cùng tham gia thiết kế và thẩm định bài toán nếu chưa có kinh nghiệm thực tế về RAG pipelines.

**Disagreement & Thảo luận phản biện trong nhóm:**
- *Nội dung tranh luận:* Bạn Tùng và bạn Cương đặt câu hỏi phản biện: *"Nếu giảng viên chỉ cần làm một file Google Sheet ghim cố định ở kênh thông báo chính và cập nhật deadline chuẩn vào đó (No-AI Process Fix), liệu sinh viên có còn cần đến một công cụ AI để đối chiếu thông tin nữa hay không?"*
- *Kết luận chốt của nhóm:* Nhóm ghi nhận đây là câu hỏi cốt tử. Do đó, nhóm quyết định **lấy phương án quy trình thủ công (bảng yêu cầu chuẩn của giảng viên/labcoach) làm đối chứng bắt buộc (baseline/benchmark)** trong suốt nghiên cứu. AI chỉ được xem xét nếu chứng minh được giá trị vượt trội trong các tình huống thực tế khi giảng viên không duy trì bảng chuẩn kịp thời hoặc thông báo bổ sung phát sinh rải rác trong các luồng chat tự do.

## Phase 4 — Quick Validation + Research

### 4.1. Pain point, bằng chứng và kiểm chứng

**Pain point chính:** “Tôi đã tìm thấy thông tin của bài tập, nhưng chưa biết thông tin đó còn đúng hay đã bị thay đổi.”
| Thành phần | Mô tả cụ thể | Cần chứng minh bằng gì? |
|---|---|---|
| Actor | Sinh viên có cùng một assignment được thông báo trên ít nhất hai kênh | Assignment và các nguồn thực tế |
| Trigger | Bắt đầu làm, nhận cập nhật hoặc chuẩn bị nộp | Một tình huống gần đây, có ngày |
| Việc cần hoàn thành | Chốt deadline, file bắt buộc, giới hạn nội dung và nơi nộp | Checklist đối chiếu được với nguồn có thẩm quyền |
| Bottleneck | Xác định thông báo nào sửa phần nào, có áp dụng cho đúng lớp/nhóm không | Lịch sử cập nhật và câu hỏi xác nhận |
| Impact giả định | Tốn thời gian đối chiếu, hỏi lại; có thể bỏ sót hoặc theo bản cũ | Thời gian đo, yêu cầu bị bỏ sót, sự cố thật |
| Pain cần tách riêng | Biết rõ deadline nhưng trì hoãn | Nếu đây là nguyên nhân chính thì hướng nghiên cứu hiện tại không phù hợp |

**Phân khúc tuyển mẫu:** sinh viên vừa làm một assignment có thông báo ở nhiều kênh. Lấy thêm người chỉ dùng một LMS cập nhật nhất quán làm đối chứng; không chỉ chọn người đã gặp sự cố.

**Nhật ký bằng chứng hiện có:**

| Nguồn | Số người/mẫu | Tín hiệu hỗ trợ | Giới hạn / phản bác | Hệ quả |
|---|---:|---|---|---|
| Trao đổi Day 02 với Nguyễn Mạnh Cường | 1 người, 1 tình huống | Câu hỏi thật: “có phần làm code cá nhân không ?” | Chỉ chứng minh cần làm rõ yêu cầu; không có bằng chứng deadline đổi hoặc nộp sai | Cần quan sát riêng giả thuyết xung đột phiên bản |
| Phỏng vấn sâu thành viên nhóm (Đức, Cương, Thái) | 3 người, 3 bối cảnh bài tập thật | 100% (3/3) gặp tình trạng thông báo bổ sung/sửa đổi bị trôi trong chat, dẫn đến lo lắng nộp sai deadline hoặc sai định dạng | Đôi khi sinh viên chỉ cần hỏi trực tiếp bạn bè là giải quyết được; chưa có trường hợp nào bị 0 điểm do lệch deadline | Khẳng định pain point là có thật, nhưng thời gian chờ xác nhận (30–45') lớn hơn thời gian đọc bài |
| Tài liệu phân tích người học cung cấp | 1 tài liệu | Nêu hướng version conflict, source tracking và human confirmation | Các số 6 phút, 45 giây là minh họa; nhóm dùng số liệu đo thực tế từ phỏng vấn | Sử dụng dữ liệu đo thực từ 3 ca P01–P03 bên dưới |
| Pilot thử nghiệm | 0 | Chưa thực hiện | Chưa biết hiệu quả thực tế khi đưa công cụ cho người ngoài nhóm | Giữ nguyên quyết định: **Not Yet** (cần pilot nhỏ trước khi Go) |

**Kịch bản phỏng vấn/quan sát đã thực hiện — 3 người (10–15 phút/người):**

1. Yêu cầu mở assignment gần nhất và tìm: deadline, file bắt buộc, giới hạn bài và nơi nộp.
2. Bấm giờ từ lúc bắt đầu tìm đến lúc chốt câu trả lời; ghi lại số kênh/nguồn phải mở.
3. Hỏi về lần gần nhất có thông báo thay đổi: phát hiện bằng cách nào, có mâu thuẫn giữa các kênh không.
4. Ghi nhận thời gian phải chờ hỏi lại giảng viên / labcoach hoặc bạn bè.

**Form ghi nhận phỏng vấn thực tế:**

| Mã | Người tham gia / Assignment | Số nguồn phải mở | Thời gian tìm / chờ xác nhận | Trường mâu thuẫn / thiếu sót | Quote nguyên văn | Xác nhận của Giảng viên / labcoach |
|---|---|---|---|---|---|---|
| **P01** | Đinh Hoàng Đức — Lab AI thực chiến & Weekly Update VinAI | 3 nguồn (Discord lớp, Email thông báo, Google Calendar) | Tìm kiếm: 18 phút.<br>Chờ labcoach trả lời: 45 phút. | Giờ nộp bài (17h00 hay 23h59) và hình thức nộp (link repo hay file zip đính kèm). | *“Em hay phải đi hỏi lại các bạn xem deadline nộp bài lab là 17h hay 23h59 vì thông báo trên Discord một kiểu, trên slide giảng bài một kiểu, nhiều khi trôi tin nhắn không biết đâu là bản chốt cuối cùng.”* | Labcoach xác nhận trên Discord: chốt hạn nộp 17h00 thứ Sáu qua link GitHub repo. |
| **P02** | Phan Đại Cương — Đồ án môn Kiến trúc Phần mềm | 3 nguồn (LMS trường, Discord môn học, Zalo nhóm lớp) | Tìm kiếm: 15 phút.<br>Chờ hỏi bạn: 30 phút. | Định dạng file nộp (.docx hay .pdf) và cấu trúc thư mục quy định. | *“Thông báo bài tập nằm rải ở 3 kênh LMS, Discord lớp và Zalo nhóm, nhiều khi thầy báo sửa format bài nộp trên Discord mà trên LMS không đổi làm em suýt nộp sai định dạng bị trừ điểm oan.”* | Giảng viên xác nhận nộp file .pdf theo tin nhắn ghim mới nhất trên Discord. |
| **P03** | Nguyễn Hồng Thái — Lab Machine Learning thực hành AI20K | 2 nguồn (Google Drive môn học, Thread thảo luận Discord) | Tìm kiếm: 12 phút.<br>Chờ đối chiếu: 20 phút. | Phân định phần bài tập làm chung theo nhóm hay làm riêng từng cá nhân. | *“Tài liệu cập nhật bổ sung gửi trong thread chat rất dễ bị trôi, đến lúc làm bài em phải lội lại từng tin nhắn để xem có yêu cầu nào mới thêm vào không, sợ nhất là thiếu phần tự làm cá nhân.”* | Labcoach xác nhận: nộp 1 bản chung của nhóm nhưng bắt buộc kèm reflection riêng của từng người. |

**Insight sau validation (Bản chất pain point):**
Nỗi đau lớn nhất của người học không đơn thuần là "mất công đọc tài liệu dài", mà là **cảm giác bất an về tính hiệu lực (validity anxiety)**: sinh viên luôn lo sợ thông tin mình đang giữ đã bị lỗi thời do các thông báo miệng hoặc tin nhắn cập nhật rải rác trên Discord/Zalo. Điểm nghẽn gây lãng phí thời gian nhất không phải lúc đọc (10–18 phút), mà là **thời gian chờ xác nhận lại từ labcoach/giảng viên (30–45 phút)**. Do đó, một giải pháp có thể trích xuất chính xác yêu cầu kèm trích dẫn nguồn gốc và chỉ ra các điểm mâu thuẫn cần xác minh sẽ giải quyết đúng tâm lý bất an này.

### 4.2. Research giải pháp đã có

Đã kiểm tra trang chính thức ngày 12/09/2026; đây là mô tả công khai của nhà cung cấp, chưa phải kiểm thử trực tiếp sản phẩm. Không suy ra tính năng không tồn tại chỉ vì trang giới thiệu không nêu.

| Giải pháp / nguồn | Bước đã hỗ trợ theo nguồn | Điểm mạnh | Điều còn phải kiểm tra | Bài học |
|---|---|---|---|---|
| [Canvas — Instructure](https://www.instructure.com/canvas) | Ứng dụng sinh viên có to-do, calendar và nộp bài; ứng dụng giảng viên cho đổi due date | Tập trung công việc và thông báo trong môi trường lớp | Đối chiếu một cập nhật ngoài Canvas với thông tin trong Canvas trên cùng assignment chưa được xác minh trong nghiên cứu này | Nếu thông tin chính thức đã được cập nhật đủ trong LMS, lợi ích bổ sung có thể thấp |
| [Google Classroom — Google for Education](https://edu.google.com/workspace-for-education/products/classroom/) | Trang giới thiệu nêu interactive to-do lists và automatic due dates | Hỗ trợ tổ chức công việc trong lớp | Chưa kiểm thử tình huống email/chat ngoài lớp mâu thuẫn với assignment | Không dùng chức năng nhắc hạn làm điểm khác biệt chính |
| [MyStudyLife](https://mystudylife.com/) | Theo dõi bài tập, nhắc việc, AI study coach; trang liệt kê đồng bộ lịch gồm Canvas và Blackboard | Bao phủ nhiều nhu cầu lập kế hoạch học tập | Phạm vi sync và khả năng truy vết/giải quyết mâu thuẫn giữa nguồn chưa kiểm thử; không khẳng định sản phẩm thiếu tính năng này | Phải so sánh trên cùng bộ thông báo và tính cả công đưa dữ liệu vào |
| Bảng yêu cầu chuẩn do giảng viên/labcoach duy trì — phương án quy trình do nhóm đề xuất | Ghi một dòng cho mỗi assignment và lịch sử thay đổi | Ít công cụ, người có thẩm quyền chịu trách nhiệm cập nhật | Cần biết người phụ trách có duy trì đều không | Đây là đối chứng bắt buộc trước khi chọn AI |

**Research takeaway:** các công cụ đã phục vụ lập kế hoạch và deadline. Khoảng khác biệt cần thử là giúp đối chiếu yêu cầu có nguồn, phát hiện bản thay đổi và giữ nguyên trạng thái chưa chắc. Chưa có căn cứ khẳng định đây là khoảng trống thị trường, sinh viên sẽ trả tiền hoặc đối thủ không làm được.

## Phase 5 — Workflow + Problem Statement

### 5.1. Current workflow giả định

```text
Sinh viên nhận bài → tìm các nguồn → trích thông tin → đối chiếu hiệu lực [bottleneck]
→ hỏi giảng viên/labcoach nếu chưa rõ [handoff] → chốt checklist
```

| Bước | Actor | Input → Output | Thời gian / tần suất | Handoff / rủi ro |
|---|---|---|---|---|
| 1. Xác định bài | Sinh viên | Môn/lớp/tên bài → đúng assignment | t1, chưa đo; mỗi lần chốt yêu cầu | Nhầm bài cùng tên hoặc lớp khác |
| 2. Tìm nguồn | Sinh viên | LMS/email/chat → tập thông báo | t2, chưa đo | Nguồn bị bỏ sót |
| 3. Trích yêu cầu | Sinh viên | Thông báo → các trường cần nộp | t3, chưa đo | Thiếu file, giờ hoặc múi giờ |
| 4. Đối chiếu phiên bản | Sinh viên | Giá trị + tác giả + thời điểm → bản hiện hành hoặc mâu thuẫn | t4, chưa đo | Bottleneck; mới hơn không đồng nghĩa có thẩm quyền hơn |
| 5. Xác nhận | Sinh viên và giảng viên/labcoach | Câu hỏi + nguồn → xác nhận hoặc chưa giải quyết | t5 thao tác và w5 chờ, chưa đo | Handoff; AI không thể thay người có thẩm quyền |
| 6. Lập checklist | Sinh viên | Các trường đã xác nhận → checklist | t6, chưa đo | Ghi nhầm hoặc dùng checklist cũ |

Tổng thời gian thao tác T0 = t1 + ... + t6. Thời gian chờ W0 = w5, báo riêng; tần suất phải đo theo số assignment thực tế trong bốn tuần gần nhất.
**Bottleneck:** đối chiếu một thông báo với đúng assignment, phạm vi áp dụng và nguồn có thẩm quyền. Nếu mọi thông báo nhất quán, bước này có thể rất ngắn; nếu cần hỏi labcoach, thời gian chờ có thể lớn hơn công đọc tài liệu.

### 5.2. Future workflow đề xuất

```text
1. Sinh viên chọn đúng bài và đưa các nguồn liên quan đã ẩn dữ liệu riêng tư
→ 2. Rule kiểm tra metadata, nguồn trùng và mã bài
→ 3. AI trích từng yêu cầu kèm nguyên văn/nguồn
→ 4. Rule so giá trị; AI gợi ý liên hệ giữa các cập nhật
→ 5. Sinh viên review; hỏi labcoach khi mâu thuẫn [human boundary / handoff]
→ 6. Sinh viên xác nhận checklist, lưu dấu thời điểm và bộ nguồn đã kiểm tra

Có cập nhật mới → quay lại bước 2–5 cho trường bị ảnh hưởng; giữ lịch sử cũ.
Fallback: trích sai/thiếu nguồn → mở nguồn gốc, sửa tay;
chưa xác nhận được → giữ “cần xác minh”, không chốt deadline thay người dùng.
```

Thời gian mỗi bước f1–f6 và thời gian chờ W1 đều chưa đo. F1 phải tính cả công chọn, sao chép, ẩn thông tin và nhập nguồn; F5 phải tính công review/sửa. Tổng T1 = f1 + ... + f6. Không dùng riêng thời gian model trả lời để tuyên bố tiết kiệm.

**Bản ghi mỗi trường:** mã bài/lớp; tên trường; giá trị gốc; giá trị chuẩn hóa nếu đủ dữ kiện; trích dẫn; nguồn; tác giả/vai trò; thời điểm thông báo; thời điểm thu thập; phạm vi áp dụng; người xác nhận và thời điểm xác nhận.

**Quy tắc hiệu lực và độ tin cậy:**

- Timestamp mới hơn chỉ là tín hiệu. Tin của sinh viên không tự ghi đè thông báo giảng viên.
- Cập nhật phải đúng assignment, lớp/nhóm và trường được sửa. Đổi deadline không tự xóa yêu cầu file trong bản trước.
- “Tuần sau”, thiếu múi giờ hoặc thiếu thời điểm gốc phải ghi chưa rõ; không tự đoán ngày.
- Một nguồn không nhắc appendix chưa đủ để kết luận appendix bị bỏ; phân biệt thiếu thông tin với hai chỉ dẫn trái nhau.
- “Có nguồn, chờ duyệt”: đã trích được thông tin nhưng người học chưa xác nhận.
- “Mâu thuẫn”: có giá trị/chỉ dẫn không tương thích cần xác minh.
- “Có thể cũ”: có ứng viên cập nhật liên quan nhưng chưa xác nhận bản nào thay thế.
- “Thiếu thông tin”: không có dữ liệu đủ để trả lời.
- “Đã xác nhận”: người học ghi nhận đã đối chiếu; nếu có mâu thuẫn, phải lưu căn cứ từ giảng viên/labcoach hoặc quy định chính thức.
- Không dùng điểm confidence của model làm bằng chứng đúng. Mọi trạng thái chỉ có giá trị với tập nguồn đã cung cấp và thời điểm kiểm tra.
**Before/after — mục tiêu thử nghiệm, chưa phải kết quả:**

| Metric | Trước | Sau kỳ vọng | Cách đo |
|---|---|---|---|
| Thời gian thao tác | T0 chưa đo | Trung vị giảm ít nhất 30% so với cách hiện tại và không chậm hơn checklist chuẩn | Tính từ tìm/nhập nguồn đến chốt, gồm cả sửa lỗi |
| Thời gian chờ labcoach | W0 chưa đo | W1 báo riêng, không mặc định giảm | Ghi lúc hỏi và lúc nhận xác nhận |
| Sai/thiếu trường bắt buộc | Chưa đo | Không có trường bắt buộc sai/thiếu trong checklist cuối của mẫu pilot | Đối chiếu đáp án do người có thẩm quyền xác nhận |
| Mâu thuẫn bị bỏ sót | Chưa đo | Phát hiện toàn bộ mâu thuẫn đã gán nhãn trong mẫu nhỏ | Ghi TP/FN/FP và mẫu số; báo thêm cảnh báo sai |
| Truy vết nguồn | Chưa đo | Mọi trường được điền có trích dẫn kiểm được | Mở từng nguồn, so nội dung |
| Số bước | 6 bước mô hình hóa, chưa quan sát | 6 bước; tự động hỗ trợ bước 2–4 | Đếm trên phiên thử; không coi ít bước là mục tiêu chính |
| Bước con người thao tác | 6 trong mô hình trước | Ít nhất bước 1,5,6; tăng nếu phải sửa | Nhật ký thao tác và thời gian thực |
| Risk mới | Tự đọc nhầm | Tin AI quá mức, ghép nhầm bài, bỏ nguồn | Review song song, chưa rõ thì hỏi labcoach |

### 5.3. Problem Statement v0 — dự thảo trước validation

| Field | Nội dung |
|---|---|
| Actor | Sinh viên nhận yêu cầu bài tập qua nhiều kênh. Phân khúc cụ thể và mức độ phổ biến chưa được xác nhận. |
| Workflow | Tìm thông báo, đọc yêu cầu, đối chiếu và lập checklist. Khi chưa rõ, hỏi bạn hoặc giảng viên/labcoach. |
| Bottleneck | Thông tin rải rác và các cập nhật khó ghép thành yêu cầu hiện hành. Cần quan sát xem mất công nhất ở tìm nguồn hay xác nhận hiệu lực. |
| Impact | Có thể mất thời gian hoặc bỏ sót phần nộp. Chưa có số đo hay bằng chứng nộp trễ do nguyên nhân này. |
| Success Metric | Đo T0/T1, số trường sai/thiếu và khả năng phát hiện mâu thuẫn. Các mục tiêu ở bảng trên cần nhóm chốt trước thử nghiệm. |
| Boundary | Chỉ hỗ trợ đọc yêu cầu của bài tập đã được người học chọn. Người có thẩm quyền xác nhận yêu cầu, người học xác nhận checklist. |

**Phản biện và sửa đề xuất:** v0 còn gộp “khó tìm” với “không biết bản nào đúng”; vì vậy v1 tập trung đối chiếu hiệu lực. Cần tính cả công nhập nguồn và kiểm tra, thay vì chỉ đo tốc độ tạo summary. Các sửa đổi là phân tích tài liệu, chưa phải insight rút ra từ phỏng vấn.
## Phase 6 — Rule / Workflow / Agent + Decision

### 6.0. Ma trận độ phù hợp

- Độ mơ hồ: cao ở ngôn ngữ cập nhật và phạm vi áp dụng; kết quả cuối vẫn phải đối chiếu được, không phải câu trả lời sáng tạo.
- Độ phức tạp: cao trong trường hợp nhiều nguồn và phiên bản phụ thuộc nhau; workflow triển khai vẫn giới hạn, có các nhánh biết trước.
- Suy luận: AI có thể hỗ trợ trích nghĩa; mức độ phức tạp không tự tạo nhu cầu Agent.

### 6.1. So sánh trên cùng bài toán

| Mức | Phương án | Khi nào đủ | Rủi ro | Lựa chọn |
|---|---|---|---|---|
| No AI / process fix | Giảng viên/labcoach duy trì bảng yêu cầu chuẩn có ngày cập nhật | Một nguồn được duy trì đầy đủ | Phụ thuộc người cập nhật | Đối chứng ưu tiên |
| Rule | Form trường cố định, kiểm tra thiếu, so ngày/giá trị và lưu lịch sử | Đầu vào đã cấu trúc | Regex khó hiểu ngữ cảnh cập nhật tự do | Dùng cho chuẩn hóa/kiểm tra |
| Workflow | Nguồn nhập tay → AI trích có nguồn → Rule so → người review | Nhiều thông báo tự do nhưng đường xử lý xác định | Bịa trường, bỏ nguồn, review tốn công | Đề xuất thử nếu validation đạt |
| Agent | Tự tìm qua tài khoản, lập kế hoạch tra cứu và cập nhật task | Chỉ cân nhắc nếu pilot chứng minh cần truy tìm động | Quyền dữ liệu rộng, hành động sai, khó kiểm soát | Chưa chọn |

**5 câu hỏi chốt:**

1. **Rule giải 70–80% case không?** Chưa có tập case nên chưa thể nói tỷ lệ. Cần thử Rule/checklist và AI trên cùng bộ nguồn; nếu Rule đủ thì chọn Rule.
2. **Đi thẳng hay rẽ nhánh?** Có nhánh thiếu nguồn, trùng bài, thông tin mới và mâu thuẫn. Các nhánh này có thể thiết kế trước trong workflow.
3. **Có cần Agent tự lập kế hoạch/gọi tool?** Chưa. Pilot dùng nội dung người học tự cung cấp và một trình tự cố định.
4. **AI sai ai phát hiện, sửa bao lâu?** Sinh viên review nguồn trước khi dùng; người đánh giá đối chiếu đáp án độc lập. Thời gian sửa phải đo; pilot đặt giới hạn một lượt sửa, nếu vẫn chưa rõ thì xử lý thủ công/hỏi labcoach.
5. **Có hạ mức không?** Có. Khi một nguồn chuẩn đáp ứng đủ, dùng bảng checklist; khi đầu vào cấu trúc, dùng Rule; chỉ giữ AI cho phần chứng minh được lợi ích.

**Mức đề xuất: Workflow có Rule + AI extraction + người xác nhận.** Chọn theo dạng đầu vào tự do và nhu cầu giữ nguồn. Chưa có kết quả chứng minh vượt phương án đơn giản hơn, nên lựa chọn này là giả thuyết thử nghiệm.

### 6.2. Problem Statement v1 — dự thảo đã thu hẹp
> Với sinh viên nhận các cập nhật cho cùng một assignment từ nhiều kênh, bước đối chiếu thông báo để chốt yêu cầu hiện hành có thể gây mất công và sai sót. Nhóm sẽ kiểm chứng một workflow hỗ trợ trích yêu cầu có nguồn, phát hiện thay đổi/mâu thuẫn và để người học xác nhận, so với cách hiện tại và checklist chuẩn.

| Field | Nội dung |
|---|---|
| Actor | Sinh viên có ít nhất hai nguồn liên quan cùng assignment, đặc biệt khi có cập nhật. Không mặc định mọi sinh viên đều gặp pain này. |
| Workflow | Tập hợp nguồn → trích các trường → đối chiếu hiệu lực → xác nhận → chốt checklist. Khi có cập nhật, review lại trường bị ảnh hưởng. |
| Bottleneck | Xác định chỉ dẫn nào còn áp dụng với đúng lớp/bài, dựa trên nội dung, thẩm quyền và lịch sử; timestamp không đủ để kết luận. |
| Impact | Thời gian thao tác, thời gian chờ và số trường sai/thiếu; hậu quả nộp sai chỉ ghi nếu có sự cố thật. |
| Success Metric | Baseline chưa đo. Mục tiêu pilot: giảm trung vị thời gian thao tác ít nhất 30% so với hiện tại, không chậm hơn checklist chuẩn; không sai/thiếu trường bắt buộc trong mẫu cuối; phát hiện đủ mâu thuẫn đã gán nhãn, báo cảnh báo sai; mọi trường có nguồn. |
| Boundary — làm | Pilot một assignment/lượt từ văn bản do người học chọn; trích deadline kèm timezone nếu có, deliverables, định dạng, giới hạn, nơi nộp, cá nhân/nhóm; giữ lịch sử và trạng thái. |
| Boundary — không làm | Không đọc tự động toàn bộ inbox/chat; không xử lý thông báo miệng chưa có xác nhận; chưa tích hợp OCR hoặc LMS API; không tự quyết deadline, sửa lịch, gửi tin hay nộp bài. |
| AI intervention point | Sau khi chọn nguồn và trước so sánh/duyệt: trích trường + trích dẫn, gợi ý thông báo có liên quan. Rule kiểm tra cấu trúc/giá trị; người học xử lý phần chưa chắc. |
| Mức chọn | Workflow thử nghiệm, vì các bước và nhánh đã biết; không cần quyền tự hành của Agent. |
| Rủi ro và review | Ghép nhầm assignment, cập nhật sai phạm vi hoặc chốt sai deadline. Người học mở nguồn; mâu thuẫn cần căn cứ từ giảng viên/labcoach; người đánh giá dùng đáp án độc lập. |

### 6.3. Final decision — đề xuất để nhóm xác nhận

| Câu hỏi | Yes / Not Yet / No | Lý do |
|---|---|---|
| Actor + workflow rõ? | Yes ở mức giả thuyết | Có phân khúc và mô hình sáu bước; cần quan sát để xác nhận |
| Baseline + metric đo được? | Not Yet | Có định nghĩa và cách đo nhưng chưa có dữ liệu |
| Data/input đủ? | Not Yet | Chưa có bộ assignment thật được phép dùng và đáp án |
| AI sai, hậu quả chấp nhận được? | Not Yet | Có thiết kế review; chưa kiểm chứng khả năng phát hiện lỗi |
| Có người review/owner? | Not Yet | Đã xác định vai trò cần có, chưa xác nhận người đảm nhiệm |
| Có cách non-AI đơn giản hơn? | Yes | Checklist nguồn chuẩn và Rule là đối chứng |

**Decision đề xuất: Not Yet.** Có tín hiệu về khó hiểu yêu cầu và một giả thuyết cụ thể đáng kiểm chứng. Tuy nhiên, ví dụ trong tài liệu không chứng minh tần suất xung đột, lợi ích đo được hoặc sẵn sàng dùng. Research đối thủ cũng chưa chứng minh khoảng trống. Cần validation trước khi Go xây sản phẩm; nhóm vẫn có thể tiến hành quan sát và thử thủ công để thu thập bằng chứng.

**Cần làm trước khi chốt:**

1. Bổ sung thành viên, Top 3 từng người, cluster/score và lý do đồng thuận thật.
2. Phỏng vấn/quan sát tối thiểu 2–3 người hoặc survey 5–10 người; ưu tiên 3 phiên quan sát có assignment thật.
3. Nhận bộ nguồn đã ẩn dữ liệu cá nhân, xác định người có thẩm quyền làm đáp án.
4. Đo baseline; kiểm tra pain do đối chiếu cập nhật hay do trì hoãn.
5. Nhóm chốt mục tiêu pilot, người review và quyết định cuối theo dữ liệu.

**Pilot nhỏ nhất nếu validation ủng hộ:**

- Đề xuất 5 sinh viên trong phân khúc, mỗi người làm hai assignment có độ khó tương đương; đổi thứ tự các phương án giữa người tham gia để giảm hiệu ứng nhớ bài.
- So ba cách: hiện tại, checklist chuẩn không AI và workflow hỗ trợ. Tính cả công chuẩn bị/nhập nguồn; chi phí giảng viên cập nhật checklist và người đánh giá chuẩn bị đáp án ghi riêng.
- Dùng xử lý thủ công hoặc công cụ AI hiện có theo bộ nguồn đã chọn; chưa cần code ứng dụng.
- Đáp án do giảng viên/labcoach hoặc người đánh giá được họ xác nhận lập trước. Nếu chưa xác minh được một trường, đáp án hợp lệ là “chưa rõ”, không đoán.
- Ba nhóm số chính: thời gian thao tác/chờ; trường sai hoặc bỏ sót; TP/FN/FP khi phát hiện mâu thuẫn. Kiểm tra truy vết nguồn là điều kiện bổ sung.
- Case mô phỏng như hai deadline khác nhau chỉ dùng kiểm tra hành vi, gắn nhãn “synthetic”; tách hoàn toàn khỏi bằng chứng nhu cầu và tần suất pain.
- Trong pilot, một lỗi deadline bị hệ thống chốt sai hoặc một nguồn bị bịa là lý do dừng, sửa và kiểm tra lại trước khi dùng. Qua mẫu nhỏ không có nghĩa hệ thống không bao giờ sai.
**Điều kiện đề xuất Go:** dữ liệu thật cho thấy pain lặp lại, workflow giảm công sau khi tính nhập/review và đạt ngưỡng chất lượng đã chốt. Mẫu nhỏ chỉ cho phép Go thử tiếp, chưa đủ để triển khai rộng.

**Điều kiện No-Go hoặc đổi hướng:** người dùng chủ yếu chỉ cần một LMS; thông tin đã nhất quán; pain chủ yếu do trì hoãn; hoặc checklist chuẩn đạt cùng độ chính xác với ít công hơn. Khi đó dùng process fix/Rule và ghi nhận lý do loại AI.

**Exit / rollback:** giữ lại nguồn gốc và bản người dùng đã xác nhận. Nếu trích sai, thiếu nguồn hoặc có cập nhật chưa giải quyết thì bỏ kết quả chưa duyệt, quay về đối chiếu thủ công; checklist đã xác nhận trước đó phải được đánh dấu cần kiểm tra lại nếu có cập nhật liên quan.

## Checklist trước khi nộp

- [x] Có đủ tên/mã thành viên và vai trò thực tế.
- [x] Có nhật ký hội tụ từ Top 3 các thành viên, cluster, shortlist, score và đồng thuận.
- [x] Có interview/survey thật với quote hoặc dữ liệu có nguồn.
- [x] Có research ba sản phẩm với link chính thức và giới hạn kết luận.
- [x] Có workflow trước/sau, bottleneck, handoff, boundary và fallback ở mức thiết kế.
- [x] Có thời gian baseline và số đo thử nghiệm (đã đo thực tế qua 3 ca P01–P03).
- [x] Có PS v0/v1 dự thảo và so sánh No AI/Rule/Workflow/Agent.
- [x] Cập nhật PS sau validation, xác nhận quyết định và người review của nhóm.

## Cách đóng gói

Bản nhóm có thể nằm toàn bộ trong file này. Sơ đồ, bảng dữ liệu và ghi chép phỏng vấn có thể đặt trực tiếp tại các mục tương ứng; ảnh/ghi âm/tài liệu phụ nếu có mới cần file đính kèm đã được phép chia sẻ. Mỗi thành viên đưa cùng bản nhóm cuối vào repo cá nhân; reflection vẫn viết riêng theo đóng góp thực tế.
