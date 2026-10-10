# 1. Lý do chọn Agile

- Waterfall chốt yêu cầu từ đầu và thường chỉ cho khách xem sản phẩm ở cuối dự án, khiến thay đổi dễ gây làm lại và tăng chi phí.
- Agile chia công việc thành các Sprint ngắn, tạo sản phẩm từng phần và nhận phản hồi thường xuyên để điều chỉnh kịp thời.
- **Kết luận:** GreenMart nên chọn Agile vì yêu cầu bán hàng đa kênh có thể thay đổi theo nhu cầu thực tế của khách hàng.

# 2. Nguyên tắc làm việc theo 4 giá trị Agile

| Thói quen hiện tại | Giá trị Agile | Cách làm mới |
|---|---|---|
| Chỉ trao đổi qua phần mềm | Cá nhân và sự tương tác hơn quy trình và công cụ | Trao đổi trực tiếp khi cần, tổ chức Daily Scrum hằng ngày. |
| Viết tài liệu chi tiết, chỉ demo cuối dự án | Phần mềm chạy được hơn tài liệu đầy đủ | Tạo Increment sau mỗi Sprint và trình diễn cho khách. |
| Chờ 2 tuần phê duyệt khi đổi yêu cầu | Hợp tác với khách hàng hơn đàm phán hợp đồng | Trao đổi thường xuyên, cập nhật và ưu tiên lại Product Backlog. |
| Cứng nhắc theo kế hoạch ban đầu | Phản hồi với thay đổi hơn bám theo kế hoạch | Điều chỉnh kế hoạch dựa trên phản hồi và tình hình thực tế. |

# 3. Khung Scrum

Chọn Sprint cố định 2 tuần. Trong 6 tuần đầu, đội thực hiện 3 Sprint.

- **Minh bạch:** Công khai Product Backlog, Sprint Backlog và tiêu chuẩn hoàn thành.
- **Thanh tra:** Kiểm tra tiến độ hằng ngày, đánh giá Increment cuối Sprint.
- **Thích nghi:** Điều chỉnh Product Backlog và cách làm việc dựa trên phản hồi.

- **Lý do chọn Scrum:** Scrum cho phép phát triển theo từng vòng lặp, kiểm tra thường xuyên và thích nghi với yêu cầu thay đổi tốt hơn cách làm Waterfall.

# 4. Phân vai Scrum Team

| Vai trò | Thành viên | Được quyết định | Không được quyết định |
|---|---|---|---|
| **Product Owner** | Long | Thứ tự ưu tiên Product Backlog, tối đa hóa giá trị sản phẩm | Không tự quyết định cách lập trình của đội |
| **Scrum Master** | Hoa | Cách hỗ trợ Scrum, thúc đẩy loại bỏ trở ngại | Không tự giao việc hoặc quyết định ưu tiên sản phẩm |
| **Development Team** | An, Bình, Chi, Dung | Cách thực hiện công việc và tạo Increment | Không tự thay đổi thứ tự ưu tiên Product Backlog |

# 5. Artifacts & lịch sự kiện

## Product Backlog

| STT | Hạng mục |
|:---:|---|
| **1** | Đăng nhập/đăng xuất |
| **2** | Tìm kiếm sản phẩm |
| **3** | Xem chi tiết sản phẩm |
| **4** | Giỏ hàng |
| **5** | Đặt hàng online |
| **6** | Thanh toán |
| **7** | Theo dõi đơn hàng |
| **8** | Quản lý tồn kho |

## Sprint Backlog - Sprint 1

- Mục tiêu: Xây dựng chức năng cơ bản giúp khách hàng tìm kiếm và xem sản phẩm.

**Công việc:**
- Đăng nhập/đăng xuất.
- Tìm kiếm sản phẩm.
- Xem chi tiết sản phẩm.
- Kiểm thử các chức năng trên.

## Increment cuối Sprint 1

- Một phiên bản chạy được, cho phép người dùng đăng nhập, tìm kiếm và xem chi tiết sản phẩm; các chức năng đáp ứng Definition of Done đã thống nhất.

## Lịch 5 sự kiện Scrum

| Sự kiện | Thời điểm | Mục đích |
|---|---|---|
| **Sprint** | Chu kỳ 2 tuần | Tạo Increment có giá trị |
| **Sprint Planning** | Ngày đầu Sprint | Xác định Sprint Goal và Sprint Backlog |
| **Daily Scrum** | Hằng ngày, 15 phút | Kiểm tra tiến độ, điều chỉnh kế hoạch |
| **Sprint Review** | Cuối Sprint | Trình diễn Increment, nhận phản hồi |
| **Sprint Retrospective** | Sau Review | Cải tiến cách làm việc |