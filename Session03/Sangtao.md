# Phần 1 - Thiết kế

**Epic:** Hành trình đón khách xe ghép

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Feature 1:** Theo dõi hành trình

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- **UC1:** Là khách hàng, tôi muốn xem xe đang đón ai để biết tiến trình chuyến đi.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- **UC2:** Là khách hàng, tôi muốn xem thời gian dự kiến xe đến lượt mình để chủ động chờ đón.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Feature 2:** Hỗ trợ khi có sự cố

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- **UC1:** Là khách hàng, tôi muốn nhận thông báo khi lịch trình thay đổi để biết thời gian đón mới.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- **UC4:** Là khách hàng, tôi muốn xem hướng dẫn xử lý sự cố để biết cách liên hệ hỗ trợ.

# Phần 2 - Sắp xếp

| Ưu tiên | User Story | Lý do |
|:---:|---|---|
| **1** | UC2 – Xem thời gian dự kiến đến lượt | Giải quyết trực tiếp việc khách không biết khi nào đến lượt mình. |
| **2** | UC1 – Xem xe đang đón ai | Giúp khách hiểu tiến trình đón khách. |
| **3** | UC3 – Nhận thông báo thay đổi | Giúp khách cập nhật khi lịch trình thay đổi. |
| **4** | UC4 – Xem hướng dẫn xử lý sự cố | Hỗ trợ khách khi phát sinh vấn đề. |

- Story cần chi tiết nhất là UC2 vì phụ thuộc dữ liệu vị trí và lộ trình từ đối tác bản đồ; cần làm rõ cách tính thời gian dự kiến, tần suất cập nhật và cách xử lý khi thiếu dữ liệu.

# Phần 3 - Xử lý tình huống

## TH 1: Burndown Chart đi ngang 3 ngày
- **Ai xử lý:** Scrum Team, Scrum Master hỗ trợ loại bỏ trở ngại; Product Owner phối hợp với đối tác nếu cần.
- **Dấu hiệu nhận biết:** Đường thực tế đi ngang 3 ngày, lượng công việc còn lại không giảm.
- **Cách xử lý:** Xác nhận nguyên nhân do dữ liệu bản đồ chưa được bàn giao; liên hệ đối tác, tìm dữ liệu thay thế hoặc điều chỉnh phạm vi Sprint nếu phù hợp. Không tự động kéo dài Sprint; minh bạch tiến độ và cập nhật kế hoạch.
## TH 2: Đức muốn đưa cả Epic vào Sprint Backlog
- **Ai xử lý:** Product Owner và Developers trao đổi trong Sprint Planning; Scrum Master hướng dẫn đúng Scrum.
- **Cách xử lý:** Chọn các User Story ưu tiên cao, đủ rõ và có thể hoàn thành trong Sprint theo năng lực nhóm. Các Story còn lại tiếp tục nằm trong Product Backlog.