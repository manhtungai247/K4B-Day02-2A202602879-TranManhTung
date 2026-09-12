# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Trần Mạnh Tùng
- Mã học viên: 2A202602879
- Nhóm: Nhóm 5 anh em - Zone A (Nguyễn Mạnh Cường, Nguyễn Hồng Thái, Trần Mạnh Tùng, Đinh Hoàng Đức, Phan Đại Cương)
- Candidate problem nhóm chọn: C1 — Xác định yêu cầu hiện hành của bài tập từ nhiều nguồn (Thu hẹp từ problem #1; có bước đối chiếu hiệu lực rõ, đo được công tìm/kiểm tra, lỗi và mâu thuẫn bỏ sót)

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Quét và lập danh sách 5 bài toán kỹ thuật thực tế trong chuỗi AI Lab (Hallucination QA trong RAG, Khử trùng lặp ảnh data pipeline, Lệch schema API backend-ML, Debug log phân tán, Quản lý GPU compute). | Chọn lọc ra 3 Problem Cards độc lập, thực tế, hoàn toàn không bị trùng lặp với worked example về weekly report. |
| Pitch Problem Card | Trực tiếp pitch Card #1 (Đánh giá và phát hiện hallucination trong RAG pipeline - C7) trong 2 phút; lượng hóa thời gian gán nhãn thủ công 120 phút/tuần và rủi ro fail test khi release. | Nhóm đánh giá cao tính kỹ thuật và đưa C7 vào Top 3 Shortlist để chấm điểm ma trận phân loại. |
| Challenge bài của bạn khác | Đặt câu hỏi phản biện gắt gao cho C1 (Cường) và C10 (Đức): "Nếu chỉ là thông báo phân tán, tại sao giảng viên/labcoach không duy trì một bảng Google Sheet/Notion chuẩn cập nhật là xong mà phải tốn AI?". | Buộc nhóm phải xây dựng thêm nhánh No-AI Baseline (Process Fix) để làm thước đo đối chứng công bằng với AI. |
| Gom trùng / cluster | Đề xuất phân loại 15 candidates thành 4 cụm chuyên biệt: A (Quản lý thông tin & deadline đa kênh), B (Đọc hiểu & ôn tập), C (Phối hợp nhóm & API spec), D (Kỹ thuật AI & QA). | Giúp cả nhóm nhận diện sự hội tụ tự nhiên của 3 thành viên (Cường, Đức, Cương) vào Cụm A và giảm số lượng bài trùng lặp. |
| Chọn candidate problem | Cùng 4 thành viên chấm điểm ma trận 7 tiêu chí (35 điểm) cho Top 3 (C1, C4, C7). | Đồng thuận chọn C1 (33/35 điểm) vì giải quyết nỗi đau có thật của cả 5 bạn, khả thi để deep-dive và kiểm chứng trong 4 giờ lab. |
| Validation / research | Đảm nhận phân tích chuyên sâu tính năng và giới hạn kỹ thuật của 3 sản phẩm thị trường: Canvas LMS, Google Classroom và MyStudyLife. | Đưa ra bằng chứng cả 3 app chỉ quản lý dữ liệu có cấu trúc từ giảng viên, chưa app nào xử lý đối chiếu mâu thuẫn từ chat tự do. |
| Workflow nhóm | Thiết kế chi tiết Bước 4 (Đối chiếu phiên bản) và Bước 5 (Handoff hỏi giảng viên/labcoach); xác định điểm nghẽn (bottleneck) nằm ở khâu so khớp thẩm quyền. | Xác định ranh giới can thiệp AI: AI chỉ trích xuất thực thể và trích dẫn nguồn, tuyệt đối không được tự ý ghi đè deadline. |
| Problem Statement | Cùng nhóm xây dựng bản dự thảo PS v0 và bản tinh chỉnh PS v1; trực tiếp viết phần Boundary "Không làm" để chặn phạm vi rủi ro. | Đảm bảo sản phẩm thử nghiệm không vi phạm quyền riêng tư (không tự cào inbox cá nhân) và không tự hành hành động thay con người. |
| Rule / Workflow / Agent | Trực tiếp phản biện ý tưởng xây dựng "Autonomous Agent" tự động đọc tin nhắn và sửa Google Calendar; bảo vệ phương án Workflow + Rule. | Thuyết phục nhóm chọn mức độ "Workflow thử nghiệm", giúp giảm chi phí tính toán, tránh ảo giác và kiểm soát rủi ro an toàn. |
| Decision | Đề xuất nhóm đưa ra quyết định "Not Yet" thay vì vội vàng "Go"; thiết kế quy trình pilot trên 5 sinh viên với 2 assignment có độ khó tương đương. | Nhóm có một kế hoạch kiểm chứng bài bản với 3 chỉ số đo lường cụ thể và bộ tiêu chí exit/rollback rõ ràng trước khi code. |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Tôi là người thiết lập nhánh đối chứng quy trình không dùng AI (Process Fix dựa trên bảng chuẩn của giảng viên/labcoach) và kiên quyết kéo nhóm thoát khỏi cái bẫy "làm Agent cho ngầu", giữ kiến trúc ở mức Workflow trích xuất có người duyệt với ranh giới an toàn rõ ràng.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Gợi ý góc nhìn bóc tách bottleneck kỹ thuật trong các khâu chuẩn bị dữ liệu và kiểm thử AI. | Giúp liệt kê nhanh các công đoạn tốn thời gian trong một pipeline AI thông thường. | Đưa ra các ý tưởng chung chung, sách vở kiểu "khó học prompt", "viết code Python chậm", không phản ánh thực tế học tập. | Tự viết lại toàn bộ 5 bài toán dựa trên đúng trải nghiệm vướng mắc thực tế của bản thân khi làm bài tập thực chiến (RAG evaluation, trùng ảnh dataset, lệch API spec). |
| Problem Card | Hỗ trợ cấu trúc dàn ý kịch bản pitch 2 phút theo chuẩn Problem Card. | Sắp xếp mạch lập luận rõ ràng: Bối cảnh → Nỗi đau → Tần suất/Thời gian lãng phí → Hậu quả → Phương án đối chứng. | AI tự động vẽ ra giải pháp dùng mô hình siêu thông minh tự động sửa code mà không có phương án đối chứng thủ công. | Bổ sung phương án No-AI fix (dùng heuristic rule và gold dataset do chuyên gia gắn nhãn) để làm baseline so sánh bắt buộc. |
| Workflow | Tạo bản nháp sơ đồ các bước sinh viên xử lý bài tập từ lúc nhận thông báo đến lúc nộp bài. | Liệt kê đầy đủ các mắt xích tuần tự từ tiếp nhận thông tin đến tạo checklist. | Mặc định coi AI là "người giải quyết toàn năng", bỏ qua yếu tố thẩm quyền thông tin (ai có quyền sửa hạn nộp bài). | Bổ sung bước Human Boundary và Handoff: chỉ giảng viên/labcoach mới có thẩm quyền chốt mâu thuẫn; AI chỉ làm nhiệm vụ trích xuất và hiển thị nguồn. |
| Research | Tìm kiếm nhanh tài liệu mô tả tính năng của Canvas, Google Classroom, MyStudyLife. | Tổng hợp nhanh các link tài liệu chính thống và chức năng lịch/deadline của từng app. | Tự suy diễn chủ quan rằng "thị trường bỏ trống hoàn toàn, sản phẩm AI này làm ra chắc chắn sinh viên sẽ đổ xô mua". | Tự đọc tài liệu chính thức, bác bỏ kết luận viển vông; chỉ rõ khoảng cách kỹ thuật: các app hiện tại chỉ hỗ trợ dữ liệu có cấu trúc từ LMS, chưa xử lý văn bản tự do. |
| Problem Statement | Hỗ trợ gọt giũa câu từ theo cấu trúc chuẩn: Actor, Context, Pain, Metric, Root Cause. | Giúp câu văn cô đọng, văn phong kỹ thuật dứt khoát, mạch lạc. | Tự bịa ra các con số đo lường không tưởng như "giảm 99% lỗi sai", "tăng 80% điểm số sinh viên". | Viết lại hệ thống metric thực tế có thể đo lường trong phòng lab: thời gian thao tác T0, độ trễ chờ phản hồi W0, tỷ lệ phát hiện mâu thuẫn (TP/FP/FN). |
| Rule / Workflow / Agent | Phân tích ưu nhược điểm giữa Rule-based, Workflow có AI, và Autonomous Agent. | Phân định rạch ròi giữa logic tất định (deterministic) và mô hình tạo sinh xác suất (probabilistic). | Cổ vũ nhiệt tình việc xây dựng Multi-Agent vì "công nghệ thời thượng", phớt lờ nguy cơ ảo giác deadline và rò rỉ dữ liệu tài khoản. | Thuyết phục cả nhóm chọn mức Workflow; dùng Rule để so khớp metadata mã bài/thời gian, dùng AI ở khâu trích xuất thực thể kèm trích dẫn nguyên văn. |
| Decision | Gợi ý các tiêu chí thẩm định rủi ro trước khi ra quyết định đầu tư sản phẩm. | Đưa ra danh mục các câu hỏi checklist về tính khả thi của dữ liệu và chi phí bảo trì. | Luôn khuyến nghị chọn "Go" ngay lập tức vì thấy ý tưởng nghe rất triển vọng trên lý thuyết. | Giữ vững lập trường chọn "Not Yet"; lập kế hoạch pilot thực nghiệm trên 5 sinh viên thật với 2 bài tập để lấy dữ liệu kiểm chứng trước khi code. |

---

## 3. Reflection câu hỏi mở

Chọn 3-4 câu trong 6 câu dưới để viết thành đoạn 8-12 câu (không trả lời bullet 1 dòng):
- Nhóm có lúc nào bị solution-first, đòi làm Agent cho ngầu không?
- Tôi có thay đổi ý kiến sau khi bị challenge không, vì sao đổi?
- Tôi đóng góp gì thật sự vào artifact cuối, phần nào có dấu tay của tôi?
- Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

**Reflection:**

```text
Trong buổi thảo luận nhóm, khi Cường và Đức trình bày vấn đề thông báo bài tập bị phân tán, ban đầu cả nhóm đã rơi ngay vào cái bẫy "solution-first" khi hào hứng đề xuất dựng một Multi-Agent tự động đăng nhập LMS, Zalo, Discord để cào tin nhắn và tự lên lịch Google Calendar. Với vai trò phụ trách nghiên cứu giải pháp và baseline không dùng AI, tôi đã lập tức lên tiếng cảnh báo nguy cơ nghiêm trọng về quyền riêng tư và rủi ro ảo giác: nếu Agent cào nhầm tin nhắn đùa của sinh viên rồi tự ý đổi deadline khiến cả nhóm bị 0 điểm thì ai chịu trách nhiệm? Tôi đã đưa ra phản biện rằng một bảng Google Sheet hoặc Notion chuẩn do giảng viên và labcoach cập nhật (Process Fix) hoàn toàn có thể giải quyết được 80% vấn đề mà không tốn một đồng chi phí AI nào. Cuộc tranh luận gay gắt này đã giúp nhóm bình tâm lại và nhận ra điểm nghẽn thực sự không phải là thiếu một Agent tự hành, mà là sự mệt mỏi khi phải đọc lướt thủ công các đoạn chat dài để đối chiếu xem thông báo mới có hủy bỏ thông báo cũ hay không. Dù ban đầu tôi rất tâm huyết với bài toán đánh giá ảo giác RAG (C7) của mình, nhưng khi nghe các bạn chia sẻ nỗi ám ảnh có thật về việc nộp nhầm file hay lỡ hạn bài tập do trôi tin nhắn, tôi đã sẵn sàng đổi ý sang ủng hộ C1 vì tính đại diện và khả năng kiểm chứng cao hơn. Dấu tay rõ nhất của tôi trong báo cáo nhóm chính là việc kiên quyết hạ cấp giải pháp từ Agent xuống Workflow thử nghiệm, thiết lập ranh giới AI chỉ trích xuất kèm nguồn dẫn và con người giữ quyền quyết định cuối cùng. Nếu được làm lại từ đầu, tôi sẽ challenge nhóm quyết liệt hơn ngay từ bước phỏng vấn để yêu cầu người tham gia cung cấp các đoạn thông báo bài tập thực tế ngay tại chỗ, tránh việc báo cáo bị xếp ở trạng thái "Not Yet" chỉ vì thiếu tập dữ liệu thật có đáp án chuẩn.
```

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1)
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [x] [15đ] Nhóm có workflow trước/sau
- [x] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ
- [x] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [x] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI
