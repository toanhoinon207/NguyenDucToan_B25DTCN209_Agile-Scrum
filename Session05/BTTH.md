# Phần A - Thiết kế vận hành Scrum

## Chọn độ dài Sprint

- Chọn Sprint 2 tuần, tổng cộng 4 Sprint (8 tuần), giúp đội Hoa thường xuyên nhận phản hồi từ Marketing, kế toán và người dùng, đồng thời có đủ thời gian phát triển và kiểm thử từng Increment.

## Bảng phân công 3 vai trò

| Vai trò | Trách nhiệm trong dự án |
|---|---|
| **Product Owner** | Xác định mục tiêu sản phẩm, quản lý và ưu tiên Product Backlog, làm rõ yêu cầu nghiệp vụ từ các bên liên quan. |
| **Scrum Master** | Đảm bảo đội hiểu và thực hành Scrum đúng cách, hỗ trợ loại bỏ trở ngại, điều phối quy trình xử lý thay đổi. |
| **Development Team** | Phân tích kỹ thuật, thiết kế, lập trình, kiểm thử và tạo Increment đáp ứng Definition of Done. |

## Sự kiện Scrum quan trọng

Sprint Review giúp thể hiện trụ cột Thanh tra (Inspection) vì đội Hoa trình diễn Increment cho các bên liên quan để kiểm tra kết quả thực tế. Từ phản hồi của Marketing, kế toán và người dùng, PO có thể điều chỉnh Product Backlog cho Sprint tiếp theo.

# Phần B - Product Backlog & Ưu tiên hoá bằng MoSCoW

- Tích điểm sau khi thanh toán thành công - **Must**
- Thu hồi điểm khi đơn hàng bị hủy hoặc hoàn - **Must**
- Quản lý thời hạn điểm và tự động trừ điểm hết hạn sau 12 tháng - **Must**
- Ghi nhận lịch sử giao dịch tích điểm, đổi điểm - **Must**
- Đổi điểm lấy ưu đãi theo tỷ lệ 100 điểm = 20.000đ - **Must**
- Xem số dư điểm và hạn sử dụng - **Should**
- Thông báo điểm sắp hết hạn - **Should**
- Hiển thị biểu đồ thống kê tích và đổi điểm - **Could**

#### Theo ràng buộc nguồn lực ở mục 3, Sprint đầu tiên chỉ thực hiện toàn bộ Must và tối đa 2 Should. Đội Hoa chọn 5 hạng mục Must và 1 hạng mục Should (Xem số dư điểm và hạn sử dụng)

# Phần C - Acceptance Criteria & Definition of Done

## 1. Chọn hạng mục - Tích điểm sau khi thanh toán thành công

### AC1 - Thanh toán thành công

- Given: Khách hàng có đơn hàng trị giá 100.000đ và đơn hàng chưa được tích điểm.
- When: Đơn hàng thanh toán thành công.
- Then: Hệ thống cộng 10 điểm vào tài khoản khách hàng.

### AC2 - Thanh toán thất bại

- Given: Khách hàng có đơn hàng trị giá 100.000đ nhưng thanh toán thất bại.
- When: Hệ thống nhận kết quả thanh toán thất bại.
- Then: Hệ thống không cộng điểm cho đơn hàng đó.

### AC3 - Không tích điểm trùng khi nhận thông báo thanh toán lặp

- Given: Đơn hàng trị giá 100.000đ đã thanh toán thành công và khách hàng đã được cộng 10 điểm.
- When: Hệ thống nhận lại thông báo thanh toán thành công của cùng đơn hàng.
- Then: Hệ thống không cộng thêm điểm lần thứ hai.

## 2. Definition of Done (DoD)

- Code được review và đáp ứng quy ước lập trình của dự án.
- Các kiểm thử đơn vị và kiểm thử tích hợp liên quan đều đạt yêu cầu.
- Không còn lỗi nghiêm trọng hoặc lỗi mức cao chưa được xử lý.
- Tài liệu API và hướng dẫn sử dụng liên quan được cập nhật.
- Increment được tích hợp vào môi trường kiểm thử và có thể trình diễn tại Sprint Review.

# Phần D - Xử lý tình huống thay đổi

## 1. Tiếp nhận yêu cầu mà không phá vỡ Sprint hiện tại

- Scrum Master ghi nhận và hỗ trợ Product Owner làm rõ lý do, phạm vi ảnh hưởng và mức độ ưu tiên
- PO cập nhật Product Backlog để đánh giá và lập kế hoạch thực hiện.
- Trong Sprint đang chạy, đội không tự ý thay đổi Sprint Goal hoặc đưa thêm công việc làm ảnh hưởng mục tiêu
- PO trao đổi với Development Team để thống nhất cách xử lý, và nếu thay đổi khiến Sprint Goal không còn phù hợp thì chỉ PO mới có thể hủy Sprint.

## 2. Ảnh hưởng đến Product Backlog, AC và DoD

- **Product Backlog:** Cập nhật từ 100 điểm = 20.000đ thành 100 điểm = 25.000đ, đồng thời đánh giá lại mức ưu tiên và các hạng mục liên quan.
- **Acceptance Criteria:** Bổ sung hoặc sửa AC của chức năng đổi điểm để kiểm tra tỷ lệ mới. Cần xác định rõ tỷ lệ mới áp dụng cho giao dịch từ thời điểm nào để tránh sai lệch với giao dịch trước đó.
- **Definition of Done:** Không cần thay đổi nếu DoD hiện tại vẫn đáp ứng yêu cầu. Tuy nhiên, đội phải kiểm thử lại chức năng đổi điểm, cập nhật tài liệu liên quan và đảm bảo các kiểm thử đạt trước khi coi hạng mục hoàn thành.