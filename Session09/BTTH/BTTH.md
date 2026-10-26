# 5.1. Kiểm tra Increment

## Phân loại

| Mã | Bằng chứng | Trạng thái |
|---|---|---|
| SC-61 | 80/80 kiểm thử đạt; không còn lỗi cao | Done |
| SC-62 | 70/78 đạt; còn 8 ca lỗi dịch vụ đơn hàng | Chưa Done |
| SC-63 | 74/80 ca đúng; còn 1 lỗi nghiêm trọng cao | Chưa Done |
| SC-64 | 60/60 kiểm thử chính đạt; đang chờ kiểm tra che SĐT | Chưa Done |
| SC-65 | 42/42 đạt; kiểm tra quyền riêng tư đạt | Done |

**Cách trình bày phần chưa Done:** Nêu rõ mã PBI, số kiểm thử đạt/chưa đạt, lỗi còn tồn tại, điều kiện DoD chưa hoàn thành và bước tiếp theo. Không tính các PBI chưa đạt DoD là Done, PO xem xét lại chúng trong Product Backlog.

## Điểm sai Review cũ

| Điểm sai | Tác động |
|---|---|
| PO tuyên bố cả SC-61 đến SC-65 là Done dù một số PBI còn lỗi hoặc chưa kiểm tra quyền riêng tư. | Đánh giá sai mức độ hoàn thành, khiến phát hành sản phẩm chưa đạt chất lượng và an toàn. |
| Review biến thành buổi nghiệm thu và PO hứa thực hiện mọi Feedback. | Giảm trao đổi hai chiều, tạo cam kết sớm, khiến phạm vi Sprint sau khó kiểm soát và thiếu căn cứ ưu tiên. |

# 5.2. Thiết kế Sprint Review

## Lập Agenda

| Thời gian | Nội dung | Vai trò | Câu hỏi mở và trao đổi hai chiều |
|---|---|---|---|
| 0–5 phút | Giới thiệu mục tiêu Sprint và nội dung Review | SM, PO | Sprint Goal đã đáp ứng nhu cầu nào? Stakeholders mong muốn làm rõ điều gì? |
| 5–15 phút | Trình bày Increment và bằng chứng kiểm thử | Developers, PO, Stakeholders | Chức năng nào hoạt động tốt? Bằng chứng nào cho thấy chức năng đáp ứng yêu cầu? |
| 15–25 phút | Trình bày các hạng mục chưa Done và rủi ro | Developers, PO | Những lỗi hoặc điều kiện DoD nào còn chưa hoàn thành? Chúng ảnh hưởng đến người dùng ra sao? |
| 25–40 phút | Thu thập và thảo luận Feedback F-01 đến F-05 | Stakeholders, PO, Developers | Vấn đề thực tế là gì? Có dữ liệu hoặc ví dụ nào chứng minh? Kết quả mong muốn là gì? |
| 40–50 phút | Làm rõ nhu cầu và thảo luận thứ tự ưu tiên | PO, Stakeholders, Developers | Nhu cầu nào có giá trị cao nhất? Cần thêm dữ liệu gì trước khi quyết định? |
| 50–60 phút | Tổng kết và xác định bước tiếp theo | PO, SM, Developers, Stakeholders | Feedback nào cần cập nhật Product Backlog? Ai cần cung cấp thêm dữ liệu? |

## Tạo Feedback Log

| Mã | Nguồn | Bằng chứng | Điểm cần rõ | Hướng xử lý |
|---|---|---|---|---|
| F-01 | Stakeholder yêu cầu tự động hóa 90% | Có mục tiêu 90%, chưa có số liệu đo thực tế. | 90% tính trên tổng số hội thoại nào? Trong khoảng thời gian nào? | Xác định mẫu đo, cách tính tỷ lệ tự động hóa và thu thập dữ liệu trước khi đánh giá. |
| F-02 | Stakeholder đề nghị chuyển hội thoại cho nhân viên sớm hơn | Có phản hồi về việc chuyển giao, chưa có mốc thời gian cụ thể. | Chuyển giao trong trường hợp nào? “Sớm hơn” là bao lâu? Có đáp ứng mục tiêu nhận hội thoại trong 2 phút không? | Làm rõ điều kiện chuyển giao, thời điểm bắt đầu tính và thời hạn mong muốn; cập nhật tiêu chí chấp nhận nếu cần. |
| F-03 | Stakeholder phản ánh số điện thoại vẫn hiển thị | Có phản hồi về việc lộ số điện thoại; chưa xác định đầy đủ vị trí xuất hiện. | Số điện thoại hiển thị ở giao diện, lịch sử hội thoại, log hay nơi nào khác? | Kiểm tra các vị trí liên quan, ghi nhận bằng chứng và xác minh lại yêu cầu bảo vệ quyền riêng tư trước khi coi là đạt. |
| F-04 | Stakeholder phản ánh thiếu lịch sử hội thoại | Có phản hồi rằng lịch sử chưa đầy đủ, chưa có danh sách trường thông tin cụ thể. | Thiếu lịch sử ở kênh nào? Cần hiển thị những thông tin gì, chẳng hạn nội dung hội thoại hoặc trạng thái đơn hàng? | Thu thập ví dụ, xác định dữ liệu và các kênh cần hỗ trợ; PO đánh giá để cập nhật Product Backlog. |
| F-05 | Stakeholder phản ánh P95 ngoài ngưỡng | Chưa có giá trị P95 thực tế, ngưỡng mục tiêu hoặc điều kiện đo. | P95 đang đo chỉ số nào? Giá trị hiện tại và ngưỡng mục tiêu là bao nhiêu? Đo trong điều kiện nào? | Thu thập số liệu, xác định ngưỡng và môi trường đo rồi mới phân tích nguyên nhân, ưu tiên xử lý. |

# 5.3. Thiết kế Sprint Retrospective

| Thời gian | Giai đoạn | Hoạt động |
|---|---|---|
| 0–5 phút | Mở đầu | Scrum Master nhắc mục tiêu, thống nhất nguyên tắc an toàn, tôn trọng và không đổ lỗi. |
| 5–15 phút | Data | Xem dữ liệu: thay đổi quy tắc qua tin nhắn, staging có vào Day 4, Integration Test vào Day 8, điểm an toàn tâm lý 2,8/5. |
| 15–30 phút | Insight | Thảo luận nguyên nhân và tác động của các dữ liệu; phân biệt sự kiện với giả thuyết. |
| 30–40 phút | Action | Cả nhóm đề xuất, thảo luận và chọn tối đa 2 hành động cải tiến. |
| 40–50 phút | Follow-up | Thống nhất thời điểm kiểm tra, cách đo kết quả và cách xử lý nếu hành động không hiệu quả. |
| 50–60 phút | Kết thúc | Tóm tắt quyết định, kiểm tra mức độ đồng thuận và thu nhận phản hồi về buổi Retro. |

## Xử lý đổ lỗi

- Tập trung vào quy trình và dữ liệu, không quy kết lỗi cho cá nhân.
- Thay câu hỏi “Ai làm sai?” bằng “Điều gì trong quy trình khiến vấn đề xảy ra?”.
- Cho tất cả thành viên cơ hội phát biểu, SM điều phối để tránh một người quyết định thay cả nhóm.

## Rà Action cũ

| Mã | Hành động cải tiến | Nhóm theo dõi | Thời điểm | Bằng chứng |
|---|---|---|---|---|
| AI-01 | Ghi nhận mọi thay đổi quy tắc vào một nơi thống nhất; xác nhận nội dung thay đổi trước khi phát triển. | Developers phối hợp với PO | Bắt đầu Sprint 15; kiểm tra tại Daily Scrum và khi có thay đổi. | Các thay đổi có nội dung, thời điểm và xác nhận; không còn thay đổi chỉ được thông báo qua tin nhắn mà chưa cập nhật nơi thống nhất. |
| AI-02 | Chuẩn bị staging sớm và lập lịch Integration Test sớm hơn, tránh dồn kiểm thử vào cuối Sprint. | Developers phối hợp với SM | Lập kế hoạch đầu Sprint 15; kiểm tra tiến độ trong Sprint. | Có thời điểm staging sẵn sàng, lịch Integration Test và kết quả kiểm thử; nếu bị chậm, ghi nhận blocker và cách xử lý. |

# 5.4. Chọn kỹ thuật Retro

## Tạo hai phương án

| Tiêu chí | Start – Stop – Continue | 4Ls |
|---|---|---|
| An toàn | Dễ tập trung vào hành vi cần dừng, có thể gây cảm giác bị phê bình. | Khuyến khích chia sẻ trải nghiệm và nhu cầu, phù hợp khi nhóm thiếu an toàn tâm lý. |
| Nguyên nhân | Tập trung vào việc cần bắt đầu, dừng và duy trì; nguyên nhân có thể chưa sâu. | Khai thác điều còn thiếu và bài học để tìm vấn đề, nhưng vẫn cần hỏi sâu để xác minh nguyên nhân. |
| Hành động | Dễ chuyển ý kiến thành hành động cụ thể. | Có thể tạo nhiều ý tưởng, cần bước tổng hợp và ưu tiên. |
| Thời lượng | Dễ triển khai và tổng hợp trong thời gian ngắn. | Cần thêm thời gian để chia sẻ và phân tích các góc nhìn. |
| Người ít nói | Có thể bị lấn át nếu thảo luận trực tiếp theo nhóm. | Có thể phát huy tốt hơn nếu cho viết ý kiến cá nhân trước khi chia sẻ. |

## Chọn bằng dữ liệu

### Chọn 4Ls

**Trade-off:** 4Ls hỗ trợ chia sẻ và khám phá vấn đề tốt hơn trong bối cảnh hiện tại, nhưng tốn thời gian tổng hợp và chưa tự động tạo ra hành động cụ thể. Vì vậy, cần dành riêng thời gian cuối buổi để thống nhất hành động, nhóm theo dõi và bằng chứng.

**Điều kiện đổi hoặc kết hợp:**
- Chuyển sang Start–Stop–Continue nếu mức độ an toàn tâm lý được cải thiện và nhóm cần cách tổng hợp hành động nhanh hơn.
- Kết hợp 4Ls với Start–Stop–Continue nếu vẫn cần không gian chia sẻ an toàn nhưng muốn chuyển các Insight thành hành động rõ ràng. Khi kết hợp, phải giữ giới hạn 60 phút và tối đa 2 Action Items.

# 5.5. Chu trình Inspect and Adapt

## Luồng Inspect and Adapt

## Truy vết

| Nội dung | Feedback F-03: Số điện thoại vẫn hiển thị | Action AI-02: Chuẩn bị staging và Integration Test sớm |
|---|---|---|
| Nguồn | Stakeholder phản ánh số điện thoại chưa được che. | Retrospective xác định staging vào Day 4 và Integration Test vào Day 8. |
| Bằng chứng | Phản hồi về việc lộ số điện thoại; cần xác minh vị trí xuất hiện và kết quả kiểm tra quyền riêng tư. | Lịch sử tiến độ Sprint 14 và lịch kiểm thử thực tế. |
| Quyền cập nhật | PO cập nhật và ưu tiên Product Backlog; Developers bổ sung thông tin kỹ thuật, tiêu chí kiểm thử. | Scrum Team thống nhất hành động cải tiến; Developers thực hiện, Scrum Master hỗ trợ theo dõi và gỡ trở ngại. |
| Thời điểm | Làm rõ tại Review, sau đó theo dõi hạng mục được ưu tiên trong các Sprint tiếp theo. | Lập kế hoạch đầu Sprint 15, kiểm tra trong Sprint và đánh giá cuối Sprint. |
| Tiêu chí đo | Xác định được các vị trí cần che số điện thoại; kiểm tra quyền riêng tư đạt trước khi xác nhận Done. | Có bằng chứng thời điểm staging sẵn sàng, lịch Integration Test và kết quả kiểm thử; nếu chậm phải ghi nhận blocker và cách xử lý. |